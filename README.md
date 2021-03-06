# Ansible Provision Server

Allows user to select their base url, element client url, the DigitalOcean droplet location or to connect their own On-Premises server.

# DigitalOcean Mode

Allows a user to select the location of their DigitalOcean server.

- base_url - what URL the Matrix service will be based around. For a base_url of 'example.org' a homeserver at 'matrix.example.org' will be created.
- base_domain_used - whether the base_url has an existing website at it, or if you want the base_url to be served by the digitalocean droplet.
- element_subdomain - the subdomain the element client will intially be hosted at.
- do_droplet_region_long - a long string to represent the location of the droplet that will be created. Available regions:
	- 'New York City (USA)'
	- 'San Francisco (USA)'
	- 'Amsterdam (NLD)'
	- 'Frankfurt (DEU)'
	- 'Singapore (SGP)'
	- 'London (GBR)'
	- 'Toronto (CAN)'
	- 'Balgalore (IND)'

# On-Premises Mode

Allows a user to connect their own hardware, at the moment it must be a Debian 10 server and it must have the SSH public key loaded into it.

- base_url
- base_domain_used
- element_subdomain
- server_ipv4 - the IPv4 address of the server to connect to AWX, at least one IP address must be defined.
- server_ipv6 - the IPv6 address of the server to connect to AWX, at least one IP address must be defined.
