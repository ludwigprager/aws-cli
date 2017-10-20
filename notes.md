# Some more commands
~~~
docker build -t aws-cli:0.1 .

docker stop aws-cli; docker rm aws-cli

docker exec -ti aws-cli /bin/bash
docker run -ti --rm --name aws-cli aws-cli:0.1 /bin/bash
~~~
