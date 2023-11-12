# for generate private ssh key and public ssh key
ssh-keygen

# copy ssh public key to github
cd ~/.ssh
cat id_rsa.pub

# Test SSH to Github
ssh -T git@github.com

# add remote repository
git add remote origin git@github.com:aimanhisyamm/belajar-git-remote.git
git remote
git remote get-url origin
git remote rm origin

# push code to remote repository
git push origin master
git push origin master:development
git push origin --all
git push --delete origin development

# clone from remote to local repository
git clone git@github.com:aimanhisyamm/belajar-git-remote.git
git clone git@github.com:aimanhisyamm/belajar-git-remote.git belajar-git-remote-user2

# git branch remote
git branch -r # remote branch
git branch -a # all branch local & remote
git checkout -b feature/a origin/feature/a

# git fetch origin
git push origin feature/a
git fetch origin feature/a
git diff feature/a..origin/feature/a

# git pull
git pull origin feature/a
git diff feature/a..origin/feature/a

# git tag
git tag 1.0.0-SNAPSHOT 421925a
git tag --list
git tag 1.0.0 9f63fbd
git push origin 1.0.0-SNAPSHOT
git push origin --tags

git fetch origin 1.0.0-SNAPSHOT
git fetch origin

git tag --delete 1.0.0-SNAPSHOT
git push --delete origin 1.0.0-SNAPSHOT
