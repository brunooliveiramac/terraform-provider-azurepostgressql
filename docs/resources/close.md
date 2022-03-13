---
page_title: "firewalldbs_close Resource - terraform-provider-firewalldbs"
subcategory: ""
description: |-
  
---

# Resource `firewalldbs_close` 

The firealldbs_close resource allow you to remove the agent ip from the server firewall.
Remember, it should always be created with depends_on with firewalldbs_open resource.
## Example Usage

```terraform
resource "firewalldbs_close" "default" {
  server_name         = "brunoxy-ix4-north-eu-sandbox"
  resource_group_name = "bees-eu-sbx-brunoxy"
  agent_ip            = "192.168.1.1"

  depends_on = [
    firewalldbs_open.default
  ]
}
```


<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **resource_group_name** (String)
- **server_name** (String)
- **agent_ip** (String)


### Optional

- **id** (String) The ID of this resource.

