# Creat configmap to mount configuration file

```
kubectl create configmap flume-config --from-file=[FILE_1] --from-file=[FILE_2]
```

### Use subPath like this to mount single file into existing directory:
```
volumeMounts:
  - name: "config-volume"
    mountPath: "/etc/conf/<FILE_1>"
    subPath: "<FILE_1>"
  - name: "config-volume"
    mountPath: "/etc/conf/<FILE_2>"
    subPath: "<FILE_2>"
restartPolicy: Always
volumes:
  - name: "config-volume"
    configMap:
      name: "flume-config"
```

For more details [Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)

### For Persistence channel
> For now flume is configured using memory channel. We have to use file channel for crash recovery.

For more details [File Channel](https://flume.apache.org/FlumeUserGuide.html#file-channel)
