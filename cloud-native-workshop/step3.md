创建HPA规则
`kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
`{{execute}}