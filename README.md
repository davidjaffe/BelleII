# BelleII
Stuff for belle II

From KEKCC in main directory [THIS DID NOT WORK, SEE BELOW, NEED TO USE SSH TO GIT PUSH]
```
 git init  
 git pull https://github.com/davidjaffe/BelleII.git  
 git add .  
 git commit -m 'initial commit of results of SKW June 2019' 
 git remote add origin https://github.com/davidjaffe/BelleII.git 
 git pull origin master 
 ```
Following line did not work from KEKCC 
```
 git push origin master 
``` 
Instead I uploaded ssh key, then did the following
```
[djaffe@cw13 ~]$ git init
Reinitialized existing Git repository in /gpfs/home/belle2/djaffe/.git/
[djaffe@cw13 ~]$ git pull git@github.com:davidjaffe/BelleII.git
Warning: Permanently added 'github.com,52.192.72.89' (RSA) to the list of known hosts.
From github.com:davidjaffe/BelleII
 * branch            HEAD       -> FETCH_HEAD
Already up-to-date.
[djaffe@cw13 ~]$ git add .
[djaffe@cw13 ~]$ git commit -m 're-initialize with ssh'
  [master 5aeeab0] re-initialize with ssh

[djaffe@cw13 ~]$ git remote -v
 origin  https://github.com/davidjaffe/BelleII.git (fetch)
 origin  https://github.com/davidjaffe/BelleII.git (push)
[djaffe@cw13 ~]$ git remote set-url origin git@github.com:davidjaffe/BelleII.git
[djaffe@cw13 ~]$ git remote -v
origin  git@github.com:davidjaffe/BelleII.git (fetch)
origin  git@github.com:davidjaffe/BelleII.git (push)
[djaffe@cw13 ~]$ git pull origin master
Warning: Permanently added the RSA host key for IP address '52.69.186.44' to the list of known hosts.
From github.com:davidjaffe/BelleII
 * branch            master     -> FETCH_HEAD
Already up-to-date.
[djaffe@cw13 ~]$ git push origin master
Counting objects: 154, done.
Delta compression using up to 28 threads......
```
