STEPS FOR PERFECT BITBUCKET / GITHUB WORKFLOW

1. Create Repo on bitbucket or git
2. Create Local repo then run the following:
   - git init
   - git clone <repo name>
   - place your files in here, main file for this process will be deploy.php
     - deploy.php file content: <?php `git pull`; ?>
   - upload command: git add .
   - commit command: git commit -m "type comment here"
   - push command: git push
3. Connecting Server with Github
   1. ssh username@domain.com
   2. check for exisiting ssh key by typing
      cd ~/.ssh
   3. if (ssh -> exists) ? go to step 5 : go to step 4;
   4. Generate SSH key
      - ssh-keygen -t rsa
        - set passphrase too none
   5. Copy id_rsa.pub 
      - cd ~/.ssh && cat id_rsa.pub (use mouse to copy the key)
4. Go to bitbuck.com or github.com / enter your setting, find SSH Key. Enter revelant title and paste key in key textbox. 
5. Go to your repo and copy SSH clone URL. 
6. Go back to SSH connect server, cd into your proper folder and run git clone <pasteSshURL>
 
DONE!

Now, just do normal commits to your github / bitbucket and the changes will appear on your server in a few seconds.



