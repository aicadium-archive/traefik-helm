# Traefik Helm Chart

Helm Chart for Deploying Traefik on Kubernetes based off the
[official Helm Chart](https://github.com/helm/charts/tree/master/stable/traefik).

[Traefik](https://traefik.io/) is a modern HTTP reverse proxy and load balancer made to deploy
microservices with ease.

## Prerequisites

- Kubernetes 1.6+
- One of the [supported Key-value Store](https://docs.traefik.io/user-guide/kv-config/)
- You are deploying the chart to a cluster with a cloud provider capable of provisioning an
    external load balancer (e.g. AWS or GKE)
- You control DNS for the domain(s) you intend to route through Traefik

### Key-value Store (KV Store)

A [KV Store](https://docs.traefik.io/user-guide/kv-config/) is needed for
[HA](https://docs.traefik.io/user-guide/cluster/). We recommend that you use
[Consul](https://www.consul.io/).

You can deploy a Consul cluster onto Kubernetes using HashiCorp's
[Helm Chart](https://www.consul.io/docs/platform/k8s/helm.html). You can also elect to use our
[Terraform module](https://github.com/basisai/terraform-modules-gcp/tree/master/modules/consul)
to run this.
