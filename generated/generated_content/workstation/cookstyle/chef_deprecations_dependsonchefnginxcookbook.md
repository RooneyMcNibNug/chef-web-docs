+++
title = "DependsOnChefNginxCookbook"

+++

<!-- This content is automatically generated. See https://github.com/chef/chef-web-docs/blob/main/generated/README.md -->

The department is: `DependsOnChefNginxCookbook`

The full name of the cop is: `Chef/Deprecations/DependsOnChefNginxCookbook`

| Enabled by default | Supports autocorrection | Target Chef Version |
| --- | --- | --- |
| Enabled | Yes | All Versions |

do not depend on the deprecated `chef_nginx` cookbook that was replaced by the `nginx` cookbook. The legacy chef_nginx cookbook may not be compatible with newer Chef Infra Client releases.

## Examples


#### incorrect

```ruby
depends 'chef_nginx'
```

#### correct

```ruby
depends 'nginx'
```

## Configurable attributes

<table>
<tbody><tr>
<th>Name</th>
<th>Default value</th>
<th>Configurable values</th>
</tr>
<tr>
<td style="text-align:center">Version Added</td>
<td style="text-align:center">7.20.0</td>
<td style="text-align:center">String</td>
</tr>
<tr><td style="text-align:center">Include</td>
<td style="text-align:center"><ul>
<li><code>**/metadata.rb</code></li>
</ul>
</td>
<td style="text-align:center">Array</td>
</tr></tbody></table>
