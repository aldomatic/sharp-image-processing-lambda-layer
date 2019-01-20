
## Sharp Image Processing Lambda Layer

This is a serverless project that creates a AWS lambda layer for [Sharp]('https://github.com/lovell/sharp').


#### Structure
```sh
# Layer code node module(s) reside in.
/sharp-layer/nodejs/[node modules]
```
Shap package needs to be built in an environemnt that resembles AWS lambda. We will use a [docker image]('https://github.com/lambci/docker-lambda') for this. The command is below.

```sh
# Navigate to /sharp-layer/nodejs/ and then run the command below
docker run -v "$PWD":/var/task lambci/lambda:build-nodejs8.10 npm install sharp
```
