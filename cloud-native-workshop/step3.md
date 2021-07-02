创建HPA规则，当cpu利用率大于50%，副本数量在1-10之间弹性伸缩
`kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
`{{execute}}