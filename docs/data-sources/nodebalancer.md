---
page_title: "Linode: linode_nodebalancer"
description: |-
  Provides details about a NodeBalancer.
---

# Data Source: linode\_nodebalancer

Provides details about a Linode NodeBalancer.

## Example Usage

```terraform
data "linode_nodebalancer" "my-nodebalancer" {
    id = 123
}
```

## Argument Reference

The following arguments are supported:

* `id` - (Required) The NodeBalancer's ID.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `label` - The label of the Linode NodeBalancer

* `client_conn_throttle` - Throttle connections per second (0-20).

* `created` – When this Linode NodeBalancer was created

* `linode_id` - The ID of a Linode Instance where the NodeBalancer should be attached.

* `tags` - A list of tags applied to this object. Tags are for organizational purposes only.

* `hostname` - This NodeBalancer's hostname, ending with .ip.linodeusercontent.com

* `ipv4` - The Public IPv4 Address of this NodeBalancer

* `ipv6` - The Public IPv6 Address of this NodeBalancer

* `region` - The Region where this Linode NodeBalancer is located. NodeBalancers only support backends in the same Region.

* [`transfer`](#transfer) - The network transfer stats for the current month

* `updated` – When this Linode NodeBalancer was last updated

### transfer

The following attributes are available on transfer:

* `in` - The total transfer, in MB, used by this NodeBalancer for the current month

* `out` - The total inbound transfer, in MB, used for this NodeBalancer for the current month

* `total` - The total outbound transfer, in MB, used for this NodeBalancer for the current month
