
poova@POOVARASAN MINGW64 /d/Internship Training/Git-Hub (main)
$ git add Task-10

poova@POOVARASAN MINGW64 /d/Internship Training/Git-Hub (main)
$ git add Task-10

poova@POOVARASAN MINGW64 /d/Internship Training/Git-Hub (main)
$ git commit -m "Main branch commit"
[main 643cf5a] Main branch commit
 1 file changed, 1 insertion(+)
 create mode 100644 Task-10/Index.txt


$ git checkout -b new-feature
Switched to a new branch 'new-feature'

poova@POOVARASAN MINGW64 /d/Internship Training/Git-Hub (new-feature)
$ git push origin new-feature
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 340 bytes | 340.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'new-feature' on GitHub by visiting:
remote:      https://github.com/poovarasansivan/GitHub/pull/new/new-feature
remote:
To https://github.com/poovarasansivan/GitHub.git
 * [new branch]      new-feature -> new-feature

$ git checkout -b bugfix-branch
Switched to a new branch 'bugfix-branch'

poova@POOVARASAN MINGW64 /d/Internship Training/Git-Hub (bugfix-branch)
$ git push origin bugfix-branch
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'bugfix-branch' on GitHub by visiting:
remote:      https://github.com/poovarasansivan/GitHub/pull/new/bugfix-branch
remote:
To https://github.com/poovarasansivan/GitHub.git
 * [new branch]      bugfix-branch -> bugfix-branch


$ git checkout -b release-branch
Switched to a new branch 'release-branch'

$ git push -u origin release-branch
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'release-branch' on GitHub by visiting:
remote:      https://github.com/poovarasansivan/GitHub/pull/new/release-branch
remote:
To https://github.com/poovarasansivan/GitHub.git
 * [new branch]      release-branch -> release-branch
branch 'release-branch' set up to track 'origin/release-branch'.