```   
   69  mkdir 02-First-Stack-Deployment
   70  ls
   71  cd 02-First-Stack-Deployment/
   72  ls
   73  vim docker-compose.yaml
   74  docker images 
   75  vim docker-compose.yaml
   76  ls
   77  docker stack deploy -c docker-compose.yaml getstarted
   78  docker stack ls 
   79  docker stack inspect getstarted
   80  docker stack ls getstarted
   81* docker stack 
   82  docker stack ps  getstarted
   83  docker service ls 
   84  docker service inspect getstarted_web
   85  ls
   86  docker network ls 
   87  docker network inpect getstarted_webnet
   88  docker network inspect getstarted_webnet
   89  docker service ls 
   90  docker service inspect getstarted_web
   91  docker service ps  getstarted_web
   92  docker ps 
   93  ls
   94  cd ..
   95  ls
   96  mkdir 03-Vistual_App_Stack
   97  ls
   98  cd 03-Vistual_App_Stack/
   99  ls
  100  vim docker-compose.yaml
  101  docker stack deploy -c docker-compose.yaml visual_app
  102  docker stack ls 
  103  docker service ls 
  104  cat docker-compose.yaml 
  105  docker service ls 
  106  docker service scale getstarted_web=1
  107  docker service scale visual_app_web=1
  108  docker service ls 
  109  docker service scale getstarted_web=20
  110  docker service ls 
  111  docker stack ls 
  112  docker stack rm getstarted
  113  ls
  114  docker service ls 
  115  docker stack rm visual_app
  116  ls
  117  cd ..
  118  ls
  119  cd 02-First-Stack-Deployment/
  120  ls
  121  history > README.md
```


```
126  docker swarm --help
  127  docker swarm leave
  128  docker node ls
  129  docker swarm leave --force
  130  docker node ls
  131  ls
  132  docker network ls
```

