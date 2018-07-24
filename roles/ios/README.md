# ios
This Ansible Network role provides a set of network functions that are designed
to work with Cisco IOS/IOS-XE network devices.  The functions included in this role
include gathering facts from ios devices, performing declarative configuration
tasks and handling various operational tasks on the device.  

## Requirements
* Ansible 2.5 or later
* Ansible Network Engine Role 2.5.3 or later

## Functions
This section provides a list of the availabe functions that are including
in this role.  Any of the provided functions can be implemented in Ansible
playbooks to perform automation activities on Cisco IOS/IOS-XE devices.

Please see the documentation link for each function for details on how to use
the function in an Ansible playbook.

* get_facts [[source]](https://github.com/privateip/ios/blob/devel/tasks/get_facts.yaml) [[docs]](https://github.com/privateip/eos/blob/devel/docs/get_facts.md)
* get_config [[source]](https://github.com/privateip/ios/blob/devel/tasks/get_config.yaml) [[docs]](https://github.com/privateip/eos/blob/devel/docs/get_config.md)
* load_config [[source]](https://github.com/privateip/ios/blob/devel/tasks/load_config.yaml) [[docs]](https://github.com/privateip/ios/blob/devel/docs/load_config.md)


## License
GPLv3

## Author Information
Peter Sprygada (privateip)
