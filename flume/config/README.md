# Creat configmap to mount configuration file

```
kubectl create configmap flume-config --from-file=[FILE_1] --from-file=[FILE_2]
```

### Use subPath like this to mount single file into existing directory:
```
volumeMounts:
  - name: "flume-config"
    mountPath: "/flume-config/<FILE_1>"
    subPath: "<FILE_1>"
  - name: "flume-config"
    mountPath: "/flume-config/<FILE_2>"
    subPath: "<FILE_2>"
restartPolicy: Always
volumes:
  - name: "flume-config"
    configMap:
      name: "flume-config"
```

For more details [Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
