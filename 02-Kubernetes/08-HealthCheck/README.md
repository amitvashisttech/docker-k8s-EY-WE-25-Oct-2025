```
1250  cd 08-HealthCheck/
 1251  ls
 1252  vim 01-helloworld-deploy-hc.yaml
 1253  ls
 1254  kubectl apply -f 01-helloworld-deploy-hc.yaml
 1255  kubectl get po
 1256  kubectl delete -f ../07-Service/
 1257  kubectl get po
 1258  kubectl apply -f 01-helloworld-deploy-hc.yaml
 1259  kubectl get po
 1260  kubectl  describe  po  helloworld-deployment-548d9bfcd5-4xfr5
 1261  cat 01-helloworld-deploy-hc.yaml
 1262  ls
 1263  kubectl get deploy
 1264  kubectl get po
 1265  kubectl edit deploy helloworld-deployment
 1266  kubectl get po
 1267  kubectl  describe  po  helloworld-deployment-5b7dbffcf5-8m26s
 1268  kubectl get po
 1269  kubectl  describe  po  helloworld-deployment-5b7dbffcf5-8m26s
 1270  kubectl get po
 1271  vim 02-helloworld-deploy-hc-custom.yaml
 1272  kubectl apply -f 02-helloworld-deploy-hc-custom.yaml
 1273  kubectl get po
 1274  kubectl  describe  po  helloworld-2-deployment-b8dcfb87b-nn922
 1275  ls
 1276  kubectl get po
 1277  kubectl delete -f ../08-HealthCheck/
 1278  kubectl get po
 1279  vim 03-Prod-Prob-Exec.yaml
 1280  kubectl apply -f 03-Prod-Prob-Exec.yaml
 1281  kubectl get po
 1282  kubectl exec -it liveness-exec -- ls /tmp
 1283  kubectl get po
 1284  kubectl describe po liveness-exec
 1285  kubectl get po
 1286  kubectl exec -it liveness-exec -- ls /tmp
 1287  kubectl describe po liveness-exec
 1288  kubectl get po
 1289  ls
 1290  kubectl delete -f 03-Prod-Prob-Exec.yaml
 1291  vim 04-Readiness-and-Live-hc.yaml
 1292  kubectl apply -f 04-Readiness-and-Live-hc.yaml
 1293  kubectl get po
 1294  kubectl describe po helloworld-deployment-6564c6c678-2q7tr
 1295  ls
 1296  kubectl delete -f 04-Readiness-and-Live-hc.yaml
```
