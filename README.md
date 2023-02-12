# mom
Let repository mom be supermodule and repository son be submodule, necessarily in a subfolder of mom.

Recipe; given mom and son both exist on github AND ARE NOT EMPTY!

cd ~/repo
rm -rf *
git clone git@github.com:IneffablePerformativity/mom.git
cd mom
git submodule add git@github.com:IneffablePerformativity/son.git son
git add .
git commit -m "Now have supermodule mom and submodule son."
git push


Having advance son past mom; I do find mom to be out of date, as follows:

ajs@AudreyLenovo:~/repo/mom$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   son (new commits)

no changes added to commit (use "git add" and/or "git commit -a")
ajs@AudreyLenovo:~/repo/mom$ git show
commit 7cfd9ad31b7eaaa6bcd2588177aef84b14ca7b3f (HEAD -> main, origin/main, origin/HEAD)
Author: IneffablePerformativity <74435573+IneffablePerformativity@users.noreply.github.com>
Date:   Sun Feb 12 16:58:50 2023 -0600

    Update README.md

    Recording first success.

diff --git a/README.md b/README.md
index f5cd512..b87cd65 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,13 @@
 # mom
 Let repository mom be supermodule and repository son be submodule, necessarily in a subfolder of mom.
+
+Recipe; given mom and son both exist on github AND ARE NOT EMPTY!
+
+cd ~/repo
+rm -rf *
+git clone git@github.com:IneffablePerformativity/mom.git
+cd mom
+git submodule add git@github.com:IneffablePerformativity/son.git son
+git add .
+git commit -m "Now have supermodule mom and submodule son."
+git push
ajs@AudreyLenovo:~/repo/mom$ git log
commit 7cfd9ad31b7eaaa6bcd2588177aef84b14ca7b3f (HEAD -> main, origin/main, origin/HEAD)
Author: IneffablePerformativity <74435573+IneffablePerformativity@users.noreply.github.com>
Date:   Sun Feb 12 16:58:50 2023 -0600

    Update README.md

    Recording first success.

commit 68579d0689bb8a6b35410b34033ee7b498880450
Author: IneffablePerformativity <IneffablePerformativity@gmail.com>
Date:   Sun Feb 12 09:43:39 2023 -0600

    Now have supermodule mom and submodule son.

commit d2dc86497f4081dbf835c4fd4d9e0cbc6654d147
Author: IneffablePerformativity <74435573+IneffablePerformativity@users.noreply.github.com>
Date:   Sun Feb 12 16:44:42 2023 -0600

    Initial commit
ajs@AudreyLenovo:~/repo/mom$ git diff
diff --git a/son b/son
index f3615b6..dea556e 160000
--- a/son
+++ b/son
@@ -1 +1 @@
-Subproject commit f3615b6b57d258ff60ccfbf23d5aca96d8effb6b
+Subproject commit dea556e1081534506f06a087d9afa893d2ff2856
ajs@AudreyLenovo:~/repo/mom$


