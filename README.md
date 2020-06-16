# etcd-backup-example
sample cronjob for backing up an openshift cluster

## Purpose
The goal of the repo is to provide an example for a creating a backup of etcd using an OpenShift cronjob, in a fully declarative fashion.

## Warning
This implementation is very very specific to the OpenShift minor version, and has only been tested on OCP 4.3.10. You should double check all scripts in the 2-manifests/configmap.yaml that they match the scripts on the master of your cluster. For more info on backing up etcd, refer to https://docs.openshift.com/container-platform/4.3/backup_and_restore/backing-up-etcd.html

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
