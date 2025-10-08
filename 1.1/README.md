

## Deployment and Monitoring


### 1. Kubernetes Deployment


```bash
kubectl create deployment hashgenerator --image=sophiecreative/loutput:2.0
```


```bash
kubectl get deployments
```



```
NAME            READY   UP-TO-DATE   AVAILABLE   AGE
hashgenerator   0/1     1            0           7s
```


```bash
kubectl get pods
```


```
NAME                             READY   STATUS    RESTARTS   AGE
hashgenerator-5767cc8bf4-khvn9   1/1     Running   0          11s
```

### 2. Viewing Logs


```bash
kubectl logs hashgenerator-5767cc8bf4-khvn9
```


```
> app1@1.0.0 start
> node index.js

📅 10/08/2025 ⏰ 08:11:54 | Hash: 411e7edf-f8f1-4e9c-bb8b-d641dd194e54
📅 10/08/2025 ⏰ 08:11:59 | Hash: d9fe203c-de3a-42c0-a24a-780e3027e691
📅 10/08/2025 ⏰ 08:12:04 | Hash: fe844cf3-534d-4a36-aacf-7712bc387742
```