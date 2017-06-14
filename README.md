# docker-travis-demo [![Build Status](https://travis-ci.org/mtuduri/docker-travis-demo.svg?branch=master)](https://travis-ci.org/mtuduri/docker-travis-demo)

A simple demo showing Travis with Docker.

## Demo description
The idea of this demo is to show how we can use Docker in Travis.


First of all we need to include Docker as a service in order to be able to use it in Travis, thus:
```
		services:
			-docker
```

Then we can use docker as usual: 
```
script:
  - docker pull mtuduri/riga:1.0
  - docker run -d mtuduri/riga:1.0
  - docker ps
  - echo "Image built and running"
```
In this case an image is pulled from docker hub and creates a container using it. 
Finally shows the container running and a success message.


## Usage
- Fork or upload this code to your github
- Sign up in Travis ci using your github account https://travis-ci.org/
- Sync your account 
- Add this repository 
- Make any change in the repo
- commit your changes > git commit -a -m "test"
- update the repo > git push origin
- Travis will build branch updates by default and you will be able to see the build log at https://travis-ci.org/{yourGithubUserHere}/docker-travis-demo