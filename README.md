# Landmark Technology - www.mylandmarktech.com
# TEL: +1 437 215 2483  - TEL: +1 437 215 2483
# Kubernetes Metrics Server 

Metrics-server aggregates resource consumption data like CPU and memory usage for Kubernetes nodes, pods and containers. These metrics are collected from the API exposed by the Kubelet on each node.

The metrics server is commonly used by other Kubernetes add ons, such as the Horizontal Pod Autoscaler or the Kubernetes Dashboard. 

It is not deployed by default.

## Deployment
In order to deploy metrics-server in your kubernetes master machine , google the latest metric server deployment yaml file. We found the command below with the latest yaml file already. '

So run the command below on the cosole 

kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
 

## Usage

```console
# Display node metrics
$ kubectl top nodes

# Display pod metrics
$ kubectl top pods
```

## User guide

You can find the user guide in
[the official Kubernetes documentation](https://kubernetes.io/docs/tasks/debug-application-cluster/resource-metrics-pipeline/).

## Design

The detailed design of the project can be found in the following docs:

- [Metrics API](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/instrumentation/resource-metrics-api.md)
- [Metrics Server](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/instrumentation/metrics-server.md)

- [Metrics Server Git Hub](https://github.com/kubernetes-sigs/metrics-server.git)

For the broader view of monitoring in Kubernetes take a look into
[Monitoring architecture](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/instrumentation/monitoring_architecture.md)
