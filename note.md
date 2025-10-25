# debug
- install uv env in ubuntu terminal, not vscode terminal!


# to get start
- source .venv/bin/activate
- jupyter notebook --port 8899 --ip 0.0.0.0 [in new terminal, not in vscode]


# submodule
at :~/eai/robot_world_models folder
git submodule add https://github.com/morning-star-7/openpi.git projects/openpi
git add .gitmodules projects/openpi
git commit -m "add openpi as submodule"
git push
# in the furure: add upstream


# upload branch (done)
git push --set-upstream origin hanchen_pi0



# generate a personal ssh Key
ssh-keygen -t ed25519 -C "hanchen.cui147@gmail.com"
Enter file in which to save the key (/home/abhagejji/.ssh/id_ed25519): /home/abhagejji/.ssh/id_ed25519_morningstar7
cat ~/.ssh/id_ed25519_morningstar7.pub | paste to your github

nano ~/.ssh/config
'''
# GitHub for morning-star-7
Host github-morningstar7
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_morningstar7
    IdentitiesOnly yes
'''
git remote set-url origin git@github-morningstar7:morning-star-7/openpi.git



# push to submodule
- go the submodule folder
- commit
- git push

# uddate the main project
- cd /robot_world_models
- git add projects/openpi
- git commit -m "update openpi submodule to latest commit"
- git push


# uv env -> conda env
- uv pip freeze > requirements.txt
- conda activate openpi
- pip install -r requirements.txt


