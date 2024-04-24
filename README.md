## Install with Docker

```sh
## steps to build the image and push into docker hub
docker build  -t netflix-clone .
docker run  -d -p 80:80 netflix-clone
docker login
docker tag netflix-clone ameer65/test-practice:test-image
docker push ameer65/test-practice:test-image
## steps to configure aws by installing aws cli and push the image into ECR
aws configure
aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/z6b8a8c7
docker push public.ecr.aws/z6b8a8c7/test-practice/netflix:latest
```
