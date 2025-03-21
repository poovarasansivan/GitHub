# Topic - Git Hooks to perform automated checks 
 
- There will be multiple sample files available inside the .git/hooks. we will Create out own hooks.

# Types of Hooks

# Client Side Hooks

1. pre-commit
2. prepare-commit-msg
3. commit-msg
4. post-commit
5. pre-rebase
6. post-checkout
7. post-merge

# Server-side
1. pre-recive
2. update
3. post-recive

# Task Performed Using pre-commit and run a linter 

# pre-commit
- This will hook will work before commit is made.
- It is used to inspect the snapshot that is about to be committed, to see if it passes the pre-commit hook.
- If the pre-commit hook returns a non-zero status(1), the commit is aborted.
- This hook is used to check the code before committing the code.
- I have used a pre-commit hooks to check any file contains Empty file and a file with sensitive information is trying to commit.

# Steps Performed

- Created a pre-commit hook inside the .git/hook pre-commit

```  
    prints the message of Running a pre-commit check
    echo " Running pre-commit checks..."

    Get the list of staged files
    STAGED_FILES=$(git diff --cached --name-only --diff-filter=ACM)

    Check for empty files
    for FILE in $STAGED_FILES; do
    if [ ! -s "$FILE" ]; then
        echo " Error: Empty file detected - $FILE"
        exit 1
    fi
    done

    Define secret key patterns
    SECRET_PATTERNS="(API_KEY|SECRET|PASSWORD|TOKEN|AWS_ACCESS_KEY_ID|AWS_SECRET_ACCESS_KEY|PRIVATE_KEY|ENCRYPTION_KEY)=[A-Za-z0-9+/=]{20,}"

    # Check for secret keys in staged changes
    if git diff --cached | grep -E "$SECRET_PATTERNS"; then
    echo " Error: Potential secret key detected! Remove it before committing."
    exit 1
    fi
    
    
    # Run ESLint on staged .js files

    if git diff --cached --name-only | grep -E "\.js$"; then
        echo "Running ESLint..."
        npx eslint . --fix
        if [ $? -ne 0 ]; then
            echo " Linting failed! Fix issues before committing."
            exit 1
        fi
    fi
```

- Created a Empty.txt file 

- Then staged it and tried to commit. 

```
   Output:
    Running pre-commit checks...
    git commit "-m committing empty file"
    Error: Empty file detected Empty.txt
```

- Added a some line of content and committed the Empty.txt file.

- Created .env file with secret_keys and Tried to stage and commit it.
```
    Output:
    Running pre-commit checks...
    Error: Potential secret key detected! Remove it before committing.
```

- Created a .gitignore file and added .env file inside it to avoid commit Error.

- Then staged the changes and committed it.
```
    Output: 
    Running pre-commit checks...
    [main <commit-hash>] .gitignore added
```

- Created a sample .js file with syntax issues and tried to commit after stagging it.

```
    Output

    git commit -m "Test Eslint"
    Running pre-commit checks...
    Task-8/sample.js
    Running ESLint...

    D:\Internship Training\Git-Hub\Task-8\sample.js
    1:12  error  Parsing error: Unterminated string constant

    1 problem (1 error, 0 warnings) 

    Linting failed! Fix issues before committing.
```

# How Git Hooks Improves the Code Quality in Collaborative Projects.

- git hooks helps to enforce coding standards and prevent bad code from being committed to a repository. They automates checks and reducing errors and improves code quality.

# Benifits of Git Hooks

- Automates Code Quality Checks.
- Prevents Bad Code being committed.
- Ensures consistency accross the team members.
- Saves Time & Effort.
- Enhances Security.