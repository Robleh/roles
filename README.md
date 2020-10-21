Droplet
=========

Provision a DigitalOcean droplet

Requirements
------------

A DigitalOcean API token is needed. It can be set as an Ansible variable or one of the following environment variables: `DO_API_KEY`, `DO_API_TOKEN`, `DO_AUTH_TOKEN`

Role Variables
--------------

- `droplet_backups`: Enables automated backups
- `droplet_image`: The image slug from which to create the droplet
- `droplet_ipv6`: Whether or not to enable IPv6
- `droplet_monitoring`: Install the DigitalOcean agent for monitoring
- `droplet_private_networking`: Create private network interface
- `droplet_region`: Slug of the region in which to create the droplet
- `droplet_size`: Slug of the droplet size
- `droplet_state`: Droplet state
- `droplet_ssh_keys`: List of authorized SSH public key fingerprints
- `droplet_tags`: List of droplet tags
- `droplet_unique_name`: Whether or not droplet names can collide
- `droplet_user_data`: Droplet user data script
- `droplet_wait`: Whether or not to block until creation is confirmed
- `droplet_wait_timeout` 


Example Playbook
----------------

Create a digital ocean droplet.

    - hosts: localhost
      roles:
         - role: droplet
           droplet_oauth_token: 0398791xxx
           droplet_name: new-droplet-123
           droplet_image: ubuntu-20-04-x64
           droplet_region: nyc1
           droplet_ssh_keys:
             - xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx
           droplet_tags:
             - proxy
             - nginx

License
-------

BSD

Author Information
------------------

- [Robleh Esa](https://roblehesa.com)
- [Github](https://github.com/Robleh)
- [Twitter](https://twitter.com/roblehesa)
