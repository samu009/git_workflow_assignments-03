"# git_workflow_assignments-03" 

CMD comandi
Microsoft Windows [Versione 10.0.28000.2525]
(c) Microsoft Corporation. Tutti i diritti riservati.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>echo "# git_workflow_assignments-03" >> README.md

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git init
Reinitialized existing Git repository in C:/Users/samuele.iudica/Desktop/git 03/git_workflow_assignments-03/.git/

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git commit -m "first commit"
On branch main

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git branch -M main

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git add README.md

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git commit -m "first commit"
[main (root-commit) b4e05cb] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git remote add origin https://github.com/samu009/git_workflow_assignments-03.git
error: remote origin already exists.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 258 bytes | 258.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/samu009/git_workflow_assignments-03.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git remote add origin https://github.com/ACCOUNT/calcolatore.git
error: remote origin already exists.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git checkout -b features/somma
Switched to a new branch 'features/somma'

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git branch
* features/somma
  main

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git add .

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git commit -m "added featusers somma and other operation"
[features/somma b807593] added featusers somma and other operation
 1 file changed, 94 insertions(+)
 create mode 100644 calcolatore.py

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git diff

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git push -u origin features/somma
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 24 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.08 KiB | 1.08 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'features/somma' on GitHub by visiting:
remote:      https://github.com/samu009/git_workflow_assignments-03/pull/new/features/somma
remote:
To https://github.com/samu009/git_workflow_assignments-03.git
 * [new branch]      features/somma -> features/somma
branch 'features/somma' set up to track 'origin/features/somma'.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git checkout -b fix/divisione
Switched to a new branch 'fix/divisione'

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git add .

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git commit -m "fixe4d division classe for issue#1"
[fix/divisione e52fb0c] fixe4d division classe for issue#1
 1 file changed, 2 insertions(+), 1 deletion(-)

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git push -u origino fix/divisione
fatal: 'origino' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git push -u origin fix/divisione
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 24 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 426 bytes | 426.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'fix/divisione' on GitHub by visiting:
remote:      https://github.com/samu009/git_workflow_assignments-03/pull/new/fix/divisione
remote:
To https://github.com/samu009/git_workflow_assignments-03.git
 * [new branch]      fix/divisione -> fix/divisione
branch 'fix/divisione' set up to track 'origin/fix/divisione'.

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git diff

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git show
commit e52fb0c6fadb3d8d645b051a626b6eabfbf3ba52 (HEAD -> fix/divisione, origin/fix/divisione)
Author: “samu009” <“samuele.iudica009@gmail.com”>
Date:   Thu Oct 8 12:33:32 2026 +0200

    fixe4d division classe for issue#1

diff --git a/calcolatore.py b/calcolatore.py
index 44d25b6..40047ef 100644
--- a/calcolatore.py
+++ b/calcolatore.py
@@ -30,7 +30,8 @@ class Divisione(Operazione):
         super().__init__("divisione", dividendo, divisore)

     def esegui(self):
-
+        if self.valori[1] == 0:
+            raise ValueError("Non si puo dividere per zero")
         return self.valori[0] / self.valori[1]



C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git show e52fb0c6fadb3d8d645b051a626b6eabfbf3ba52
commit e52fb0c6fadb3d8d645b051a626b6eabfbf3ba52 (HEAD -> fix/divisione, origin/fix/divisione)
Author: “samu009” <“samuele.iudica009@gmail.com”>
Date:   Thu Oct 8 12:33:32 2026 +0200

    fixe4d division classe for issue#1

diff --git a/calcolatore.py b/calcolatore.py
index 44d25b6..40047ef 100644
--- a/calcolatore.py
+++ b/calcolatore.py
@@ -30,7 +30,8 @@ class Divisione(Operazione):
         super().__init__("divisione", dividendo, divisore)

     def esegui(self):
-
+        if self.valori[1] == 0:
+            raise ValueError("Non si puo dividere per zero")
         return self.valori[0] / self.valori[1]



C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>git log --graph --oneline
* e52fb0c (HEAD -> fix/divisione, origin/fix/divisione) fixe4d division classe for issue#1
* b807593 (origin/features/somma, features/somma) added featusers somma and other operation
* b4e05cb (origin/main, main) first commit

C:\Users\samuele.iudica\Desktop\git 03\git_workflow_assignments-03>
