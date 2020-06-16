# etcd-backup-example
sample cronjob for backing up an openshift cluster

## Purpose
The goal of the repo is to provide an example for a creating a backup of etcd using an OpenShift cronjob, in a fully declarative fashion.

## Bootstrapping

Run this apply command to instantiate the manifests. You can run this command again to update any changes you make to the configurations.
```
oc apply -Rf . --prune -l config.example.com/name=etcd-backup
```

## Clean Up
```
oc delete -Rf . -l config.example.com/name=etcd-backup
```

## Support
This is a workin in progress and not a supported solution.
