# nad-pod-builder

This is KPT package to generate NetworkAttachmentDefinitions and Pod from configMaps.

## Description

The KPT function ```build-nad``` consumes cni configurations from configMap(```nad-config```) and generates the NetworkAttachmentDefintion.

The KPT function ```build-pod``` consumes pod spec from configMap(```pod-config```) and creates a Pod that uses NetworkAttachmentDefiniton created by KPT function ```build-nad``` .

## Detailed readme
Build from src: 

Deploy from KPT packages: 