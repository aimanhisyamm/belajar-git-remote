# For generate private ssh key and public ssh key
ssh-keygen

# Copy ssh public key to github
cd ~/.ssh <br>
cat id_rsa.pub

# Test SSH to Github
ssh -T git@github.com

# Add remote repository
git add remote origin git@github.com:aimanhisyamm/belajar-git-remote.git <br>
git remote <br>
git remote get-url origin <br>
git remote rm origin

# Push code to remote repository
git push origin master <br>
git push origin master:development <br>
git push origin --all <br>
git push --delete origin development

# Clone from remote to local repository
git clone git@github.com:aimanhisyamm/belajar-git-remote.git <br>
git clone git@github.com:aimanhisyamm/belajar-git-remote.git belajar-git-remote-user2

# git branch remote
git branch -r # remote branch <br>
git branch -a # all branch local & remote <br>
git checkout -b feature/a origin/feature/a

# git fetch origin
git push origin feature/a <br>
git fetch origin feature/a <br>
git diff feature/a..origin/feature/a

# git pull
git pull origin feature/a <br>
git diff feature/a..origin/feature/a

# git tag
git tag 1.0.0-SNAPSHOT 421925a <br>
git tag --list <br>
git tag 1.0.0 9f63fbd <br>
git push origin 1.0.0-SNAPSHOT <br>
git push origin --tags <br>
<br>
git fetch origin 1.0.0-SNAPSHOT <br>
git fetch origin <br>
<br>
git tag --delete 1.0.0-SNAPSHOT
git push --delete origin 1.0.0-SNAPSHOT
