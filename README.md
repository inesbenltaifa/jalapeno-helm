<h1 align="center">Jalapeno Helm Chart</h1>
<p align="center">
	<img src="https://raw.githubusercontent.com/cisco-open/jalapeno/main/docs/diagrams/jalapeno_architecture.png">
</p>

<p align="center">
This repository contains the helm chart to deploy Jalapeno on a Kubernetes cluster.
The official repository for Jalapeno can be found <a href="https://github.com/cisco-open/jalapeno">here</a>.
</p>

---

## Requirements
In order to use the Helm chart as is, a Kubernetes load balancer is needed.

## Installation
1. Create namespace "jalapeno" on cluster
2. Create namespace "monitoring" on cluster
3. Install using files locally ``helm install jalapeno ./jalapeno-helm -n jalapeno``

## Changes to ArangoDB
If the arangoDB gets changed the ArangoDB Chart has to be rebuild and copied into the charts folder of the Jalapeno Chart.

- build ArangoDB Chart: ``helm package .``

## Known Bugs
- arangodb works only with image tag ``3.6.12``
- influxdb has to be set to version ``1.7``