# build-nad

## Overview

The KPT function ```build-pod``` consumes pod spec from configMap(```pod-config```) and creates a Pod that uses NetworkAttachmentDefiniton created by KPT function ```build-nad``` .

## Usage
### Building from src
```
cd nad-pod-builder/src/pod-builder
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

