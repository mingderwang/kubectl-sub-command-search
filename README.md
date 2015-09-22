# kubectl-sub-command-search

The prototype is gonna use "kube" command instead.

kubectl sub-command search for searching kubernetes resurces definitions from registry.
<p/>
It is inspired by docker search and puppet search, we can use kube search command (a new command) to find available kubernetes resource files on a shared repository.

# This project is still under development

(started in HACKATHON TAIWAN 6/13-6/14 2015) https://hackathon.tw/index.html
still on going, I need architect design for this project.
(will implement on Docker Hack Day 9/16-9/21 2015) https://blog.docker.com/2015/07/announcing-docker-global-hack-day-3/

# Implementation

coding on 9/21/2015 for both cli and backend database microserver.
source code can be cloned from https://github.com/mingderwang/kube

or 

```
go get github.com/mingderwang/kube
```

## The commands will look like these, as follow;

Remark: Current version v1.0.0 only support a sinlte file for push and get.

# Examples
```
$ kube search redis
NAME                          DESCRIPTION                                                    STARS
mingderwang.redis             ming no slash for tag                                          3
redis.master                  jak  for tag                                                   5

// then you can get the source code either use git clone, or kube subcommand like get as follow;

$ kube get mingderwang.redis
get tag:  mingderwang.redis
NOTICE: You will get the resource files, you can use kubectl command after that.
The file is download.

$ ls
my-redis-rc.yaml

// so you can create these resources easily by just issue kubectl create command directly as follow;

$ kubectl create -f my-redis-rc.yaml

// you also can vote a repo use "kube like" command

$ kube like mingderwang.redis
I like tag:  mingderwang.redis

$ kube search redis
NAME                          DESCRIPTION                                                    STARS
mingderwang.redis             ming no slash for tag                                          4
redis.master                  jak  for tag                                                   5
```
# Community
This command will be helpful for people to learn, share, and use resources in kubernetes clusters.
<p/>
Welcome to contribute your idea and code, thanks in advance.


