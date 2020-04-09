KONG_ROUTE
=========

An Ansible role for managing kong routes.

## Notes
- Will fail if the specified service does not exist
- Routes cannot be uniquely identified at this stage, so there may be duplications.
- __paths__ should begin with a `/`

Requirements
------------

The Kong Admin URL needs to be enabled. This should ideally be exposed via a route on the Kong proxy URL. Kong does not recommend the Admin URL to be exposed directly.

Only JWT auth is supported for now. 

Example Playbook
----------------

The easiest way to use this role in your playbooks is by adding it as a submodule.
```bash
git submodule add https://github.com/rameezk/ansible-role-kong-route roles/kong_route
```

Usage:
```yaml

- hosts: servers
  vars:
    KONG_ADMIN_URL: "<<KONG_ADMIN_URL>>"
    KONG_JWT: "<<KONG_JWT>>"
  roles:
    - role: kong_route
      route:
        service_name: "testservice"
        paths: 
          - "/foo/bar"
```

License
-------

MIT

