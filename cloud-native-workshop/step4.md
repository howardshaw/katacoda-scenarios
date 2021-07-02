业务高负载，自动扩容
通过load geneator,模拟不断请求php-apache,使业务高负载
`kubectl apply -f load-generator.yaml`{{execute}}

观察HPA的变化
`kubectl get hpa php-apache -w`{{execute}}
