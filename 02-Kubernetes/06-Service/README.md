  ```
  348  git add . ; git commit -m "05-Deployments- v2 & v3"; git push 
  349  ls
  350  kubectl get pods 
  351  ls
  352  cd 02-Kubernetes/
  353  ls
  354  mkdir 06-Service
  355  ls
  356  cp -rf 05-Deployments/helloworld.yaml 06-Service/
  357  ls
  358  cd ..
  359  ls
  360  cat 02-Kubernetes/06-Service/helloworld.yaml 
  361  kubectl create -f 02-Kubernetes/06-Service/helloworld.yaml
  362  kubectl get deploy,rs,pod
  363  kubectl get svc 
  364  kubectl get deploy 
  365  kubectl expose deploy helloworld-deployment
  366  kubectl get svc 
  367  curl 10.104.109.109
  368  kubectl delete svc helloworld-deployment
  369  kubectl expose deploy helloworld-deployment --type=NodePort
  370  kubectl get svc 
  371  cat /etc/kubernetes/manifests/kube-apiserver.yaml 
  372  kubectl get svc 
  373  kubectl describe svc helloworld-deployment
  374  kubectl get pods --show-labels
  375  kubectl get pods -o wide
  376  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  377  kubectl get pods -o wide
  378  kubectl get pods --show-labels
  379  kubectl describe svc helloworld-deployment
  380  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  381  kubectl describe svc helloworld-deployment
  382  kubectl get pods --show-labels
  383  kubectl get pods -o wide
  384  ls
  385  cd 02-Kubernetes/
  386  ls
  387  cd 06-Service/
  388  ls
  389  kubectl  get svc 
  390  kubectl describe svc helloworld-deployment
  391  kubectl scale --replicas=1 deployment helloworld-deployment
  392  kubectl get pods 
  393  kubectl describe svc helloworld-deployment
  394  kubectl scale --replicas=5 deployment helloworld-deployment
  395  kubectl describe svc helloworld-deployment
  396  kubectl scale --replicas=10 deployment helloworld-deployment
  397  kubectl describe svc helloworld-deployment
  398  kubectl get pods 
  399  kubectl get pods -o wide 
  400  curl http://34.121.241.75:31914/
  401  curl k8s-worker-02
  402  curl k8s-worker-02:31914
  403  curl k8s-worker-01:31914
  404  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  405  curl k8s-worker-01:31914
  406  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web --record
  407  curl k8s-worker-01:31914
  408  ls
  409  kubectl get svc 
  410  ls
  411  cd ..
  412  ls
  413  cd 06-Service/
  414  ls
  415  history > README.md
```
