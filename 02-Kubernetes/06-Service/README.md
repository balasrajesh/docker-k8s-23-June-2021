```
  233  cd 06-Service/

  234  ls
  235  kubectl get deploy,svc 
  236  kubectl delete deploy helloworld-2-deployment
  237  kubectl delete svc helloworld-2-deployment
  238  ls
  239  cat helloworld.yaml 
  240  ls
  241  kubectl apply -f helloworld.yaml 
  242  kubectl get deploy 
  243  kubectl get svc 
  244  kubectl expose deploy helloworld-deployment 
  245  kubectl get svc 
  246  cat /root/.kube/config 
  247  ls
  248  kubectl get svc 
  249  kubectl edit svc helloworld-deployment
  250  kubectl get svc 
  251  ls
  252  kubectl delete -f helloworld.yaml 
  253  kubectl delete svc helloworld-deployment
  254  ls
  255  cat helloworld.yaml 
  256  cat helloworld-svc.yaml 
  257  kubectl apply -f helloworld.yaml 
  258  kubectl apply -f helloworld-svc.yaml 
  259  kubectl get pods 
  260  kubectl get svc 
  261  ls
  262  vim app-svc.yaml 
  263  ls
  264  kubectl  apply -f app-svc.yaml 
  265  kubectl get pods,svc 
  266  kubectl get pods 
  267  kubectl describe pod my-webapp
  268  kubectl get pods 
  269  kubectl exec -it my-webapp -- bash  
  270  kubectl get pods 
  271  ls
  272  cp -rf app-svc.yaml app-svc-deployment.yaml 
  273  ls
  274  cat helloworld.yaml >> app-svc-deployment.yaml 
  275  ls
  276  vim app-svc-deployment.yaml 
  277  ls
  278  kubectl apply -f app-svc-deployment.yaml --dry-run 
  279  kubectl apply -f app-svc-deployment.yaml 
  280  kubectl get svc,pods 
  281  ls
  282  history 
  283  history  > README.md 
```
