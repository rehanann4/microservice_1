<h4>Introduction:</h4>

following app is created for hypothetical demoization for microservices type but not a fully functional microservices suite.
This application is contructed for how to automate and virtulize platform and services.
There are large dependencies involve in this code and it is required and install prior to the execution.

<h5>Pre-requisites.</h5>
-   Linux (centos, Ubuntu), Darwin, or Windows platform server
-   Vagrant 2.0.2 or above (working install with Oracle virtual server)
-   python 3.6 or above 
-   python (requests, argparse)


Details:
Hypotheically purpose application is distributed into two parts, user can request to any perticular service or both.

```sequence
Arch:

                                  |---------> service #1
                                  |
USER ----------> CURL----Rproxy---|
                                  |
                                  |---------> service #2
```


Steps:
```
Clone the repo 
git clone 'https://github.com/rehanann4/microservice_1.git'
cd microservice_1
vagrant init
vagrant up
```
Tests:
```
./app.py -m HELLO
./app.py -w WORLD
./app.py -a ALL
```

```
Note:
High availabilty and scalabity not included.
```