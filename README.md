# nad-pod-builder

KPT package to generate NetworkAttachmentDefinitions and Pod from configMaps.

## Description

The KPT function ```build-nad``` consumes cni configurations from configMap(```nad-config```) and generates the NetworkAttachmentDefintion and the ```build-pod``` function consumes pod spec from configMap(```pod-config```) and creates a Pod that uses NetworkAttachmentDefiniton created by KPT function ```build-nad``` .

## Detailed readme
- Build from src
    - [build-nad](https://github.com/shashidhar-p/nad-pod-builder/blob/main/src/nad-builder/README.md)
    - [build-pod](https://github.com/shashidhar-p/nad-pod-builder/blob/main/src/pod-builder/README.md)

- Deploy from KPT packages: [KPT](https://github.com/shashidhar-p/nad-pod-builder/blob/main/packages/README.md)