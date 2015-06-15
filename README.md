# kubectl-sub-command-search
kubectl sub-command search for searching kubernetes resurces definitions from registry.
<p/>
It is inspired by docker search and puppet search, we can use kubectl search command (a new command) to find available micro-services packages on a shared repository or simply from github.

# This project is still under development. 
(started in HACKATHON TAIWAN 6/13-6/14 2015) https://hackathon.tw/index.html
still on going, I need architect design for this project.

## The commands will look like these, as follow;
# Examples
```
$ kubectl search redis
NAME                             DESCRIPTION                                     STARS      OFFICIAL    TRUSTED
redis/redis                      Official redis kubernetes pods                  201        [OK]
foo/redis                        Redis pods example                              20                      [OK]
bar/redis-master                 Redis master only                               11                      [OK]
mingderwang/redis-master-slave   Redis master and slave replica controller       78                      [OK]

// then you can pull the source code either use git clone, or kubectl subcommand like pull as follow;

$ kubectl pull mingderwang/redis-master-slave
Cloning into 'redis-master-slave'...
remote: Counting objects: 4, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
Checking connectivity... done.

// so you can create these resources easily by just issue kubectl create command directly as follow;

$ kubectl create -f redis-master-slave/
```
# Community
This command will be helpful for people to learn, share, and use resources in kubernetes clusters.
<p/>
Welcome to contribute your idea and code, thanks in advance.


