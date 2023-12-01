# KPT Package for nad-pod-builder

## Overview

The KPT function ```build-nad``` consumes cni configurations from configMap(```nad-config```) and generates the NetworkAttachmentDefintion.

The KPT function ```build-pod``` consumes pod spec from configMap(```pod-config```) and creates a Pod that uses NetworkAttachmentDefiniton created by KPT function ```build-nad``` .

## Usage
### Building from KPT packages
- Pull the package

    ```
    kpt pkg get https://github.com/shashidhar-p/nad-pod-builder.git/packages@v1 nad-pod-builder
    ```

- Run the kpt functions

    ```
    cd nad-pod-builder
    ```

    ```
    kpt fn render
    ```
 
- Apply the resources

    ```
    kpt live apply
    ```
 
- Check if POD and NAD is created.
    ```
    kubectl get network-attachment-definitions
    ```

    ```
    kubectl get pod
    ```

  


