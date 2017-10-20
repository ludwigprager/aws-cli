# Quick Start

## 1. Adding your credentials
In the root directory of this git repository type
~~~
docker run -ti --rm --name aws-cli \
	-v $(pwd)/aws/:/root/.aws/ \
	aws-cli:0.1 aws configure
~~~
Your credentials are stored in directory 'aws' for subsequent calls.

## 2. start the container
~~~
docker run -ti --rm --name aws-cli \
	-v $(pwd)/aws/:/root/.aws/ \
	aws-cli:0.1 /bin/bash
~~~

# Some more commands
~~~
docker build -t aws-cli:0.1 .

docker stop aws-cli; docker rm aws-cli

docker exec -ti aws-cli /bin/bash
docker run -ti --rm --name aws-cli aws-cli:0.1 /bin/bash
~~~
