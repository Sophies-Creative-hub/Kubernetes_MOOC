1. `docker build -t sophiecreative/todo-app:1.0 .`

2. `docker push sophiecreative/todo-app:1.0`

3. `kubectl create deployment todo-app \
  --image=sophiecreative/todo-app:1.0`

```bash
NAME                READY   UP-TO-DATE   AVAILABLE   AGE
todo-app            1/1     1            1           12s
```

4. `kubectl get pods``

```bash
(base) butterfly:1.2 sophie$ kubectl get pods
NAME                                 READY   STATUS             RESTARTS   AGE
todo-app-7fc8bd44fd-j7kgn            1/1     Running            0          23s
```

5. `kubectl logs todo-app-7fc8bd44fd-j7kgn ``

```bash
> todo-app@1.0.0 start
> node index.js

Server started on Port: 3000
```