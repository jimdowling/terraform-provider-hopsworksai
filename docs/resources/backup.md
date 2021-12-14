---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "hopsworksai_backup Resource - terraform-provider-hopsworksai"
subcategory: ""
description: |-
  Use this resource to create a backup for your Hopsworks.ai clusters. The cluster has to be stopped to create a backup.
---

# hopsworksai_backup (Resource)

Use this resource to create a backup for your Hopsworks.ai clusters. The cluster has to be stopped to create a backup.

## Example Usage

```terraform
resource "hopsworksai_backup" "backup" {
  cluster_id  = "<CLUSTER_ID>"
  backup_name = "my-test-backup"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **backup_name** (String) The name to attach to this backup.
- **cluster_id** (String) The id of the cluster for which you want to create a backup.

### Optional

- **id** (String) The ID of this resource.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- **backup_id** (String) The backup id.
- **cloud_provider** (String) The backup cloud provider.
- **creation_date** (String) The creation date of the backup. The date is represented in RFC3339 format.
- **state** (String) The backup state.
- **state_message** (String) The backup state message.

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **create** (String)
- **delete** (String)
- **read** (String)

## Import

Import is supported using the following syntax:

```shell
terraform import hopsworksai_backup.my_backup <backup_id>
```