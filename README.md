## Quick Start

# 1. Adding your credentials
You only need your **Access Key ID** and **Secret Access Key**.
If you didn't check out the git repository type
~~~
mkdir -p aws/
~~~
To add your credentials type
~~~
docker run -ti --rm --name aws-cli \
	-v $(pwd)/aws/:/root/.aws/ \
	aws-cli:0.1 \
	aws configure
~~~
Your credentials are now stored in directory 'aws' for subsequent calls.

# 2. test: list your running containers
~~~
docker run -ti --rm --name aws-cli \
	-v $(pwd)/aws/:/root/.aws/ \
	aws-cli:0.1 \
	aws ec2 describe-instances
~~~
