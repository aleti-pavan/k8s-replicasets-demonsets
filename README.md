# k8s-replicasets-demonsets

ReplicaSet:
==========

Replica Set ensures how many replica of pod should be running. It can be considered as a replacement of replication controller.

DemonSet:
========

A DaemonSet ensures that all (or some) Nodes run a copy of a Pod. As nodes are added to the cluster, Pods are added to them. As nodes are removed from the cluster, those Pods are garbage collected. Deleting a DaemonSet will clean up the Pods it created.
