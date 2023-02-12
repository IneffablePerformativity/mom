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
