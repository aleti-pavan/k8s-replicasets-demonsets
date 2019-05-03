# k8s-replicasets-demonsets

ReplicaSet:
==========

Replica Set ensures how many replica of pod should be running. 

A ReplicaSet’s purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods.

It can be considered as a replacement of replication controller.


Lab
---

create replica set with manifest

$ kubectl apply -f rs-example1.yml 

replicaset.apps/frontend created


listing available replicasets on the k8s cluster

$ kubectl get rs

NAME       DESIRED   CURRENT   READY     AGE

frontend   3         3         0         12s



pods created by replicaset - 3 replicas = 3 pods

$ kubectl get po

NAME             READY     STATUS              RESTARTS   AGE

frontend-fhwrk   0/1       ContainerCreating   0          4s

frontend-m2vj9   0/1       ContainerCreating   0          4s

frontend-xqjkp   0/1       ContainerCreating   0          4s




DemonSet:
========

A DaemonSet ensures that all (or some) Nodes run a copy of a Pod. As nodes are added to the cluster, Pods are added to them. As nodes are removed from the cluster, those Pods are garbage collected. Deleting a DaemonSet will clean up the Pods it created.

