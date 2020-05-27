# Routing for K8s logs
## TL;DR;
* Application/Audit Logs are important for everybody! (not just Dev and Ops)
* Different use cases can arise from proper handling of the application/audit logs (realtime alerting, live tailing during 
incident investigation/development clusters, offline analysis and long-term storage in your datalake, easy correlation 
between system metrics and logs from your services)
* As the Kubernetes workloads are increasing proper routing of the logs can enable a faster feedback loop in our system

##Description
The purpose of this sample project is to explore the options available for handling the application/audit logs within
(but not limited to) a kubernetes cluster. An example use case could be: 

1) We need the application logs of service A/B to be available for correlation along with system metrics in a single 
Grafana dashboard
2) We need the application logs of service A/B to be available in our Elasticsearch cluster for specific amount of time
3) We need the audit/application logs to be available for analysis and reporting by our BI services and long 
term storage in our datalake for compliance
4) We need to have distinct routing policy for different services depending on the requirements

##Architecture
![alt text](https://github.com/carvanitis/k8s-log-fluent-cluster/blob/master/pictures/sample-architecture.png?raw=true)


