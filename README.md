# Cloud9 python version Issue

# python list
ec2-user:/usr/local/lib $ ls
python2.7  python3.6
ec2-user:/usr/local/lib $ ls python*
python2.7:
site-packages

python3.6:
site-packages

# ec2-user:/usr/local/lib $ ls -l /usr/bin/python*
lrwxrwxrwx 1 root root   24 Jun 14 09:25 /usr/bin/python -> /etc/alternatives/python
lrwxrwxrwx 1 root root   17 Jun 14 09:25 /usr/bin/python2 -> /usr/bin/python27
-rwxr-xr-x 1 root root 5120 May  2 18:32 /usr/bin/python27
-rwxr-xr-x 1 root root 5120 May  2 18:32 /usr/bin/python2.7
-rwxr-xr-x 1 root root 1846 May  2 18:31 /usr/bin/python2.7-config
lrwxrwxrwx 1 root root   25 Jun 14 09:25 /usr/bin/python3 -> /etc/alternatives/python3
-rwxr-xr-x 3 root root 6872 Apr 26 00:16 /usr/bin/python36
-rwxr-xr-x 3 root root 6872 Apr 26 00:16 /usr/bin/python3.6
lrwxrwxrwx 1 root root   17 Jun 14 09:25 /usr/bin/python3.6-config -> python3.6m-config
-rwxr-xr-x 3 root root 6872 Apr 26 00:16 /usr/bin/python3.6m
-rwxr-xr-x 1 root root  173 Apr 26 00:16 /usr/bin/python3.6m-config
-rwxr-xr-x 1 root root 3373 Apr 25 23:57 /usr/bin/python3.6m-x86_64-config
lrwxrwxrwx 1 root root   32 Jun 14 09:25 /usr/bin/python3-config -> /etc/alternatives/python3-config
lrwxrwxrwx 1 root root   31 Jun 14 09:25 /usr/bin/python-config -> /etc/alternatives/python-config

# ec2-user:/usr/local/lib $ ls -l /etc/alternatives/python*
lrwxrwxrwx 1 root root 18 Jun 14 09:25 /etc/alternatives/python -> /usr/bin/python2.7
lrwxrwxrwx 1 root root 34 Jun 14 09:25 /etc/alternatives/python.1.gz -> /usr/share/man/man1/python2.7.1.gz
lrwxrwxrwx 1 root root 18 Jun 14 09:25 /etc/alternatives/python3 -> /usr/bin/python3.6
lrwxrwxrwx 1 root root 34 Jun 14 09:25 /etc/alternatives/python3.1.gz -> /usr/share/man/man1/python3.6.1.gz
lrwxrwxrwx 1 root root 25 Jun 14 09:25 /etc/alternatives/python3-config -> /usr/bin/python3.6-config
lrwxrwxrwx 1 root root 25 Jun 14 09:25 /etc/alternatives/python-config -> /usr/bin/python2.7-config

# remove /etc/alternatives/python
ec2-user:/usr/local/lib $ sudo rm /etc/alternatives/python

# insert /etc/alternatives/python
ec2-user:/usr/local/lib $ sudo ln -s /usr/bin/python3.6 /etc/alternatives/python

# review but not changed
ec2-user:/usr/local/lib $ python --version
Python 2.7.14
ec2-user:/usr/local/lib $ /usr/bin/python --version
Python 3.6.5

# alias issue
ec2-user:/usr/local/lib $ alias python
alias python='python27'

# edit bashrc follow
ec2-user:/usr/local/lib $ vi ~/.bashrc
# User specific aliases and functions 
# alias python = python27

# unalias
ec2-user:/usr/local/lib $ unalias python

# Confirm version
ec2-user:/usr/local/lib $ python --version
Python 3.6.5
