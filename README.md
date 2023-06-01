#   TAP Sandbox

This repository contains configuration (YAML) to deploy the [gateway-reference-system](https://github.com/p-ssanders/gateway-reference-system) to Tanzu Application Platform.

##  Deployment

1.  `k apply -f namespace.yaml`
1.  `tanzu service class-claim create backend-postgres --class postgresql-unmanaged --parameter storageGB=1 -n sam`
1.  `tanzu apps workload apply -f backend/workload.yaml`
1.  `tanzu apps workload apply -f frontend/workload.yaml`
1.  `k apply -f gateway/`
