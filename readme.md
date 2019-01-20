
## Sharp Image Processing Lambda Layer

This is a serverless project that creates a AWS lambda layer for [Sharp](https://github.com/lovell/sharp).


### Layer Structure

Layer code

```sh.
/sharp-layer/nodejs/[node modules]
```

### Building the package

Shap package needs to be built in an environemnt that resembles AWS lambda. We will use a [docker image](https://github.com/lambci/docker-lambda) for this. The command is below.

```sh
# Navigate to /sharp-layer/nodejs/ and then run the command below
docker run -v "$PWD":/var/task lambci/lambda:build-nodejs8.10 npm install sharp
```
Once the docker command runs you will have a **node_modules** directory in **/sharp-layer/nodejs/**. 
This is what will get packaged up and become a lambda layer.


