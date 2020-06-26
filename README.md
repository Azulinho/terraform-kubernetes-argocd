# Terraform Argo CD Module

This modules makes it easy to set up a fresh installation of Argo CD in your Kubernetes cluster.

## Compatibility

This module is meant for use with Terraform >= 0.12.20 If you haven't [upgraded](https://www.terraform.io/upgrade-guides/0-12.html).

## Dependencies
This module use the [k8s Terraform provider](https://github.com/banzaicloud/terraform-provider-k8s) from Banzai Cloud to manages Kubernetes manifests
. See the [documentation](https://github.com/banzaicloud/terraform-provider-k8s#installation) to see how to install it.

## Usage
You can go to the examples folder, however the usage of the module could be like this in your own `main.tf` file:

```hcl
module "argo_cd" {
  source = "terraform-argo-cd/"

  namespace       = "argocd"
  argo_cd_version = "1.5.5"
}
```