[![GCP Python 3.7](https://github.com/martingus/github-actions-demo/actions/workflows/gcp.yml/badge.svg)](https://github.com/martingus/github-actions-demo/actions/workflows/gcp.yml)

[![Azure Python 3.6](https://github.com/martingus/github-actions-demo/actions/workflows/main.yml/badge.svg)](https://github.com/martingus/github-actions-demo/actions/workflows/main.yml)![image](https://user-images.githubusercontent.com/16271912/152659730-164de0cc-6e2d-4b71-80ee-c3b26620b81e.png)


# github-actions-demo
This is a fork of a repo made by instructor Noah Gift (Coursera cloud foundation course) for building out Github Actions and Tricks.  

I used it and tested it on GCP and Azure. 

Main steps (for each cloud platform):
Open CloudShell
Create a new project/folder and CD into that
Setup ssh keys
   ssh-keygen -t rsa, the enter and enter
   do a cat on the public key and copy text
   In Github, go to settings/SSH PGP keys and add new SSH key. Give suitable name and paste the key
In Github repo, Click Code (green button), select SSH and copy the string
Back in cloud shell: git clone <paste string>
Setup a virtual environment, eg virtualenv VENV, and then source VENV/bin/activate
Next, do a make install, or make all, and then test-run the hello.py

I then went on to open hello.py in an editor and made minor changes to it, then saved.
  
Push to git:
  git status (shows 1 file changed)
  git add * (adds one file)
  git commit -m 'minor tweak'  (makes a local commit, that one file, with this comment)
  git push
  
Then quickly back to Github and chose Actions. There you can see that the 4 actions setup to be triggered by all Push events are running.
  As long as the change to hello.py was OK, all actions will run OK.
   
That's it.
