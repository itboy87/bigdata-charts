# BigData Helm charts

Curated Big Data charts for Kubernetes.


hbase backup:

[https://blog.clairvoyantsoft.com/hbase-incremental-table-backup-and-disaster-recovery-using-aws-s3-storage-aa2bc1b40744](https://blog.clairvoyantsoft.com/hbase-incremental-table-backup-and-disaster-recovery-using-aws-s3-storage-aa2bc1b40744)


**Run hbase**

```bash
cd charts/hbase
helm dependency build
helm install hbase .
```

```
presumption

nm: namemanager, rm: resource manager, dn: datanode, nn: namenode 
hm: hbase-master, hrs: hbase-regionserver

nm --> rm
dn --> nn

hm --> nm
hrs -> hm

nn 71s
rm 30s
```

## Install chart from helm repository


[https://artifacthub.io/packages/helm/hdfs/hbase](https://artifacthub.io/packages/helm/hdfs/hbase)

You can add the helm repo to your Helm CLI:

```bash
helm repo add hdfs https://itboy87.github.io/bigdata-charts/
```

Then you have a collection of charts available to install. For example, to install hdfs:

```bash
helm install my-hbase hdfs/hbase
```


## Development

- clone repo
- adjust given chart
- bump chart version if required
- run tests
- create pull request with issue id, attach test results if possible