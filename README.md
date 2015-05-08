testes utilizando vagrant e docker - Paulo Henrique Lerbach Rodrigues
==============

Envelopei 

###Utilização do Docker:

#####Contruir a imagem Docker:
```h
$ sudo docker build -t=vertxdev .
```

#####Obter aplicação de exemplo:
```h
$ sudo docker run -t --rm -v /src/vertx/:/usr/local/src vertxdev git clone https://github.com/vert-x/vertx-examples.git
```

#####Rodar a aplicação de exemplo apenas no docker:
```h
$ sudo docker run -d -v /src/vertx/:/usr/local/src -p 8080:8080 vertxdev vertx run vertx-examples/src/raw/java/httphelloworld/HelloWorldServer.java
```

#####Verificar o log do docker:
```h
$ sudo docker logs
```

###Utilização do Docker com o Vagrant:

#####Obter aplicação de exemplo:
```h
$ vagrant docker-run vertxdev -- git clone https://github.com/vert-x/vertx-examples.git
```

#####Rodar a aplicação de exemplo:
```h
$ vagrant up
```

#####Verificar o log do docker:
```h
$ vagrant docker-logs
```

###Teste:
Navegue até: *http://localhost:8080/*: http://localhost:8080/

###Referência: 
*http://blog.zenika.com/index.php?post/2014/10/07/Setting-up-a-development-environment-using-Docker-and-Vagrant*: http://blog.zenika.com/index.php?post/2014/10/07/Setting-up-a-development-environment-using-Docker-and-Vagrant








