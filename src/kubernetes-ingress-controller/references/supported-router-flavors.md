---
title: Supported Kong Router Flavors
---

## Supported Kong Router Flavors

{{site.base_gateway}} (open-source and enterprise edition) has included the new [expression based router][gateway-expression-router] in version 3.0 and later. 
The router of {{site.base_gateway}} could be configured to the following [modes][gateway-router-flavor]:

- `traditional`: uses the pre-3.0 router.
- `traditional_compatible`: uses the expression based router, but the rotuer configure interface remains the same as `traditional`.
- `expression`: uses expression based rputer, and expressions must be provided in router configure interface.

The compatabilities of router flavors between different {{site.kic_product_name}} version and {{site.base_gateway}} is shown in the following table.

| {{site.kic_product_name}}           | 2.7.x                           |
|:-----------------------------------:|:-------------------------------:|
| Kong 3.0.x  traditional             |  <i class="fa fa-check"></i>    |     
| Kong 3.0.x  traditional_compatible  |  <i class="fa fa-check"></i>(*) | 
| Kong 3.0.x  expression              |  <i class="fa fa-times"></i>    |

(*) Most use cases are supported. Regexed with a backslash (`\`) followed by a non-escaped character (for example `\j`) in matches of paths or headers
may not be accepted by Kong 3.0 configured to use `traditional_compatible` router.

[gateway-expression-router]:/gateway/latest/key-concepts/routes/expressions/
[gateway-router-flavor]:/gateway/latest/reference/configuration/#router_flavor

