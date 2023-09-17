
## Grafana Variables

Grafana 변수는 Dashboard에 귀속된다. 

name => namespace  
label => namespace  
query => label_values(kube_namespace_created, namespace)


Panel에서 사용하는 쪽에서 이런식으로 사용할 수 있다. 

> count(kube_replicaset_status_ready_replicas{namespace=~"$namespace"}) by (namespace)

> count(kube_deployment_status_condition{namespace=~"$namespace", status="true"}) by (namespace)

## Dashboard import (ID: 17900)

![img](https://github.com/hhk22/grafana/blob/master/images/import-dashboard.png)


## Grafana Alert

UI로 설정할 수 있기때문에 편하고, alertmanager보다 다양한 지원을 한다. 

![img](https://github.com/hhk22/grafana/blob/master/images/alert-grafana-settings.png)

![img](https://github.com/hhk22/grafana/blob/master/images/alert-grafana-policy.png)

![img](https://github.com/hhk22/grafana/blob/master/images/alert-grafana-rules.png)




