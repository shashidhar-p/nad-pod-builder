# build-nad

## Overview

The KPT function ```build-nad``` consumes cni configurations from configMap(```nad-config```) and generates the NetworkAttachmentDefintion.

## Usage
### Building from src
```
cd nad-pod-builder/src/nad-builder
```

```
export FUNCTION_NAME=<Name of your function>
```

```
export FN_CONTAINER_REGISTRY=<Your GCR or docker hub>
```

```
export TAG=<Your KRM function tag>
```

```
docker build . -t ${FN_CONTAINER_REGISTRY}/${FUNCTION_NAME}:${TAG}
```

### Function eval
```
kpt fn eval ./testdata/test1/resources.yaml --image ${FN_CONTAINER_REGISTRY}/${FUNCTION_NAME}:${TAG}
```

