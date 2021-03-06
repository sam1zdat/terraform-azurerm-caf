# Azure Automation

This submodule is part of Cloud Adoption Framework landing zones for Azure on Terraform.

You can instantiate this submodule directly using the following parameters:

```
module "caf_automation" {
  source  = "aztfmod/caf/azurerm//modules/automation"
  version = "4.21.2"
  # insert the 6 required variables here
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| azurecaf | n/a |
| azurerm | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| base\_tags | Base tags for the resource to be inherited from the resource group. | `map` | n/a | yes |
| diagnostics | n/a | `any` | n/a | yes |
| global\_settings | Global settings object (see module README.md) | `any` | n/a | yes |
| location | (Required) Specifies the supported Azure location where to create the resource. Changing this forces a new resource to be created. | `string` | n/a | yes |
| resource\_group\_name | (Required) The name of the resource group where to create the resource. | `string` | n/a | yes |
| settings | Configuration object for the Automation account. | `any` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| dsc\_primary\_access\_key | The Primary Access Key for the DSC Endpoint associated with this Automation Account. |
| dsc\_secondary\_access\_key | The Secondary Access Key for the DSC Endpoint associated with this Automation Account. |
| dsc\_server\_endpoint | The DSC Server Endpoint associated with this Automation Account. |
| id | The Automation Account ID. |
| name | The Automation Account name. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->