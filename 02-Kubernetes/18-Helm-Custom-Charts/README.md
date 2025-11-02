``` 
 1629  cd 20-Helm-Custom-Charts/
 1631  mkdir v1
 1633  cd v1/
 1635  helm  create mywebapp
 1637  apt-get install tree -y
 1639  tree .
 1641  cd mywebapp/
 1643  vim Chart.yaml
 1645  cat templates/service.yaml
 1647  tree templates/
 1649  vim values.yaml
 1651  cd ..
 1653  helm list
 1654  helm install my-webapp-a mywebapp --dry-run
 1655  helm install my-webapp-a mywebapp
 1656  helm list
 1657  kubectl get deploy
 1658  kubectl get pd
 1659  kubectl get po
 1660  kubectl get svc
 1661  kubectl get sa
```

```
1672  cd 20-Helm-Custom-Charts/
 1673  ls
 1674  cp -rf v1 v2
 1675  ls
 1676  cd v2/
 1677  ls
 1678  cd mywebapp/
 1679  ls
 1680  vim Chart.yaml
 1681  ls
 1682  vim values.yaml
 1683  ls
 1684  cd ..
 1685  ls
 1686  helm upgarde my-webapp-a mywebapp --dry-run
 1687  helm upgrade my-webapp-a mywebapp --dry-run
 1688  helm upgrade my-webapp-a mywebapp
 1689  helm  list
 1690  helm  history my-webapp-a
 1691  kubectl get po
 1692  kubectl get svc
 1693  ls
 1694  kubectl get po
 1695  kubectl describe po my-webapp-a-mywebapp-8648bdd764-rbgcf
 1696  ls
 1697  cd ..
 1698  ls
 1699  cp -rf v2 v3
 1700  ls
 1701  vim v3/mywebapp/Chart.yaml
 1702  vim v3/mywebapp/values.yaml
 1703  ls
 1704  cd v3/
 1705  ls
 1706  helm upgrade my-webapp-a mywebapp
 1707  helm  list
 1708  kubectl get po
 1709  kubectl describe po my-webapp-a-mywebapp-6b9f48b95f-2f9w5
 1710  kubectl get po
 1711  ls
 1712  kubectl get svc
 1713  curl 172.23.0.3:30803
 1714  kubectl get svc
 1715  kubectl describe svc my-webapp-a-mywebapp
 1716  ls
 1717  cd ..
 1718  ls
 1738  helm upgrade my-webapp-a mywebapp
 1739  kubectl get po
 1740  kubectl get svc
 1741  kubectl describe svc my-webapp-a-mywebapp
 1742  curl 172.23.0.3:30803
 1743  curl 172.23.0.3:30803/info
 1744  ls
 1745  cd .
 1746  cd
 1747  ls
 1748  helm  list
 1749  helm  history my-webapp-a
 1750  helm rollback my-webapp-a
 1751  helm  history my-webapp-a
 1752  curl 172.23.0.3:30803/info
 1753  kubectl describe svc my-webapp-a-mywebapp
 1754  kubectl get svc
 1755  helm rollback my-webapp-a
 1756  helm  history my-webapp-a
 1757  curl 172.23.0.3:30803/info
 1758  kubectl describe svc my-webapp-a-mywebapp
 1759  helm  history my-webapp-a 1
 1760  helm rollback my-webapp-a 1
 1761  helm  history my-webapp-a
```
