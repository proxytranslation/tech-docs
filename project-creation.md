# Project generation
## Basic project creation

While the Proxy Application is capable of processing almost any format of domains, it will automatically process the URL given to use the TLD and any subdomains specified. Additional path structures will be stripped from the initial URL, and must be added back as pages (either by adding via URL or by using the discovery function).

At project creation, the Proxy Application will attempt to determine the canonical hostname. If successful, this host is used automatically as the project's root. Any path component specified in the domain field will be added as an "Unvisited" page.
If the initial `HEAD` request fails (socket timeout or more than five redirections), the Proxy Application will consider the domain invalid, and the project will not be created. This behavior can be overridden at creation-time by opening the Advanced Options and unselecting the "Check for redirections" checkbox - if done, the Proxy Application will create the `Project` entity without any initial pages, which must be added by hand using the Add pages function.

## Advanced project options

Certain attributes of the `Project` entity can be pre-loaded at creation:
- Exclusion prefixes
- Prefix masks
- Custom SRX file (can be uploaded only at creation time!)
