首先，创建一个集群
`launch.sh`{{execute}}

然后，部署监控server
`kubectl apply -f metrics-server.yaml`{{execute}}

再部署kubernetes的dashboard
`kubectl apply -f dashboard.yaml`{{execute}}

检查一下集群以及组件是否正常运行
`kubectl cluster-info`{{execute}}

获取dashboard的token
`kubectl get secret -n kubernetes-dashboard $(kubectl get sa -n kubernetes-dashboard kubernetes-dashboard -o jsonpath='{.secrets[0].name}') -o jsonpath={.data.token} | base64 -d`{{execute}}

最后，通过下面链接可以访问dashboard(需要输入上面的token)
https://[[HOST_SUBDOMAIN]]-30443-[[KATACODA_HOST]].environments.katacoda.com
