```
    1  docker ps -a 
    2  docker volume ls 
    3  docker volume create my-vol
    4  docker volume ls 
    5  docker volume inspect my-vol
    6  cd "/var/lib/docker/volumes/my-vol/_data"
    7  ls
    8  cd ..
    9  ls
   10  cd ..
   11  ls
   12  cd ..
   13  ls
   14  cd 
   15  ls
   16  docker run -itd --name test-vol-1 -v my-vol:/app ubuntu:16.04
   17  docker ps 
   18  docker inspect test-vol-1 
   19  ls
   20  docker ps 
   21  docker run -itd --name test-vol-2 -v my-vol:/app centos:8
   22  docker ps 
   23  docker inspect test-vol-2
   24  docker ps 
   25  docker attach test-vol-1
   26  docker attach test-vol-2
   27  ls
   28  cd /var/lib/docker/volumes/my-vol/_data/
   29  ls
   30  cat hello.txt 
   31  date >> hello.txt 
   32  hostname >> hello.txt 
   33  cat hello.txt 
   34  cd 
   35  ls
   36  docker run -itd --name test-vol-3 -v my-vol:/app:ro centos:8
   37  docker attach test-vol-3
   38  docker ps 
   39  docker volume ls 
   40  docker run -itd --name data-cont -v /var/www/html/amit -v /var/log/amit -v /etc/amitvashist:ro busybox 
   41  docker run -itd --name data-cont -v /var/www/html/amit -v /var/log/amit -v /etc/amitvashist busybox 
   42  docker ps 
   43  docker inspect data-cont
   44  ls
   45  docker ps 
   46  docker run -itd --name data-cont-test-1 --volume-from data-cont ubuntu:16.04
   47  docker run -itd --name data-cont-test-1 --volumes-from data-cont ubuntu:16.04
   48  docker run -itd --name data-cont-test-2 --volumes-from data-cont ubuntu:16.04
   49  docker volume ls 
   50  docker volume inspect 4d064441325da81950ad55789d038e775a13ebe4aa2f4e356b62cde8a9e52e40
   51  ls
   52  docker ps 
   53  docker attach data-cont-test-2
   54  ls
   55  docker volume ls 
   56  cd docker-kubernetes-ericsson-22-Nov-2021/
   57  ls
   58  pwd
   59  ls
   60  cd 
   61  ld
   62  ls
   63  docker run -itd --name source-vol-test-1 -v /root/docker-kubernetes-ericsson-22-Nov-2021:/app ubuntu:16.04
   64  docker run -itd --name source-vol-test-2 -v /root/docker-kubernetes-ericsson-22-Nov-2021:/app:ro ubuntu:16.04
   65  docker volume ls 
   66  docker inspect source-vol-test-2
   67  ls
   68  docker ps 
   69  docker attach source-vol-test-1
   70  docker ps 
   71  docker kill $(docker ps -qa ) 
   72  docker rm $(docker ps -qa ) 
   73  docker ps 
   74  docker ps -a
   75  ls
   76  docker volume ls 
   77  docker run -itd --name source-vol-test-2 -v my-vol:/app ubuntu:16.04
   78  docker exec -it source-vol-test-2 cat /app/hello.txt
   79  docker kill $(docker ps -qa ) 
   80  docker rm $(docker ps -qa ) 
   81  docker volumes ls 
   82  docker volume ls 
   83  docker volume ls -q
   84  docker volume rm $(docker volume ls -q) 
   85  docker volume ls 
   86  ls
   87  cd docker-kubernetes-ericsson-22-Nov-2021/
   88  ls
   89  cd 01-Docker/
   90  ls
   91  mkdir 03-Docker-Volumes
   92  history > 03-Docker-Volumes/README.md
```
