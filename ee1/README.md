# ee1

A demo EE definition file

## What's included

### Ansible collections

No additional collections. This EE uses only what the base image provides.



## Details

- **Tags:** `execution-environment`

- **Image registry:** `3.95.136.152/abcd/abcd:1.0.0`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login 3.95.136.152
podman pull 3.95.136.152/abcd/abcd:1.0.0
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `3.95.136.152/abcd/abcd:1.0.0`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel8:2.18`
- **Definition file:** `ee1.yml`
- **Template file:** `ee1-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
