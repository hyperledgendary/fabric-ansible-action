# :gear: `fabric-ansible-action` 
> Action to setup Hyperledger Fabric CLIs

## About

This action will run an Ansible Playbook using the ["Ansible Collection For Fabric"](https://github.com/IBM-Blockchain/ansible-collection)
It is based off the [v2.0.0-beta docker image](https://github.com/IBM-Blockchain/ansible-collection/pkgs/container/fabric-ansible).
## Usage

To run a playbook

```yaml
  - name: Create the Fabric Operations Console
    uses: hyperledgendary/fabric-ansible-action
    with:
      playbook: playbooks/operator_console_playbooks/02-console-install.yml
```

To run a playbook with an additional Ansible Arugments file

```yaml
  - name: Create the Fabric Operations Console
    uses: hyperledgendary/fabric-ansible-action
    with:
      playbook: playbooks/operator_console_playbooks/02-console-install.yml
      argsfile: _cfg/domain.yml
```

## Inputs
The actions supports the following inputs:

- `playbook`: Path to the playbook to run
- `argsfile`: path to an additional args file to supply to Ansible (standard Ansible yaml format)


## License
[APACAHE-2.0](LICENSE).
