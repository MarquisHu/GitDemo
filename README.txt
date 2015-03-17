How to install and use Git, and how to use git clone project from github.
1. download and install git.
we can download from this location: http://code.google.com/p/msysgit/downloads/list

2. create a github account.
we can sign up in this page: https://github.com

3. create a ssh key in local use git bash command. we will find a new folder named .ssh generate in currect user folder.
$ ssh-keygen -t rsa -C "email address"

4. copy the whole content from id_rsa.pub that existed in .ssh folder and add it to your github account.
Account Setting -> SSH keys -> Add SSH key.

5. use below command to verify whether install successfully, and verify whether git can access github server.
$ ssh -T git@github.com
The authenticity of host 'github.com (ip)' can't be established. RSA key fingerprint is 888888888 Are you sure you want to continue connecting (yes/no)?
$ yes
Hi username! You've successfully authenticated, but GitHub does not provide shell access.

if you see above input and output message, then it replace we have successfully install Git in local. Congratulations!

6. provide an identity before we use git. and we can use below sample command to provide it.
$ git config --global user.name  'xxxx'
$ git config --global user.email  xxxx@163.com

7. use below command clone project from github.
$ git clone git@github.com:username/repositories.git
$ cd repositories folder
$ git init

8. Add a new file and commit.
manual create a new file such as README.txt in repositories. then execute below command.
$ git add README.txt
$ git commit -m 'first commit'

9. push local branch to remote branch that exited in github server
$ git remote add origin git@github.com:username/repositories.git
$ git push -u origin master

10. over.

How to create a branch?
$ git branch branchname.




