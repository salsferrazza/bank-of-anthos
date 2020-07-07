# BoA Monolith Testing


## Without Istio

Created a GCP project.

Created a GKE cluster.

Ran make monolith on my project.

https://pantheon.corp.google.com/storage/browser/boa-monolith/monolith?project=boa-monolith

Deployed BoA release/ *without* the 3 java backends.



## With Istio (Same VPC)

https://istio.io/latest/docs/examples/virtual-machines/single-network/

Start with a fresh cluster.

Install Istio 1.6 on cluster.  Inject into default namespace.

Deploy BoA into default namespace *without* the 3 java backends.

Add Istio VirtualService and Gateway for the BoA frontend.

Install Istio remote on GCE (proxy inbound ledgermonolith traffic through Envoy)

Test frontend (Traffic to monolith via Envoy)

Open Kiali

Enable mTLS
