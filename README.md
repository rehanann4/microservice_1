<h4>Introduction:</h4>

this configuration is created for hypothetical demoization for microservices type but not a fully functional microservices suite.
This application is contructed for how to automate and virtulize platform and services.
There are large dependencies involve in this code and it is required and install prior to the execution.

<h5>Pre-requisites.</h5>

    1.  Linux (centos, Ubuntu), Darwin, or Windows platform server
    2.  Vagrant 2.0.2 or above (working install with Oracle virtual server)
    3.  python 3.6 or above 
    4.  python (requests, argparse)


<h4>Details:</h4>
For the demo purpose the application is distributed into two parts and it is a hypothetic represention of a Microservics and it is only meant for if the application running in distributed platform or a kubernetes POD's. in this senerio a user can request to any perticular service or both from the main server.

```sequence
Arch:

                                       |---------> service #1
                                       |
USER ----------> CURL--(POD)--Rproxy---|
                                       |
                                       |---------> service #2
```


Steps:
```
1.  git clone 'https://github.com/rehanann4/microservice_1.git'
2.  cd microservice_1
3.  vagrant init
4.  vagrant up
```
Tests:
```
./app.py -m HELLO
./app.py -w WORLD
./app.py -a ALL
```

```
Note:
High availabilty, monitoring and scalabity not included.
```