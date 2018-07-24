# Get facts from device
The `get_facts` function can be used to collect facts from an Cisco IOS/IOS-XE
devices.  This function is only supported over `network_cli` connection
type and requires the `ansible_network_os` value set to `ios`.

## How to get facts from the device
To collect facts from the device, simply include this function in the playbook
using either the `roles` directive or the `tasks` directive.  If no other
options are provided, then all of the available facts will be collected for the
device.

Below is an example of how to use the `roles` directive to collect all facts
from the IOS/IOS-XE device.

```
- hosts: cisco_ios

  roles:
    - name privateip.ios
      function: get_facts
```

The above playbook will return the facts for the host under the `cisco_ios`
top level key.  

### Filter the subset of facts returned
By default all available facts will be returned by the `get_facts` function.
If you only want to return a subset of the facts, you can specify the `subset`
variable and set one or more sub keys to return.  

For instance, the below will return only `interfaces` and `system` facts.

```
- hosts: cisco_ios

  roles:
    - name privateip.ios
      function: get_facts
      subset: 
        - interfaces
        - system
```

### Implement using tasks
The `get_facts` function can also be implemented using the `tasks` directive
instead of the `roles` directive.  By using the `tasks` directive, you can
control when the fact collection is run. 

Below is an example of how to use the `get_facts` function with `tasks`.

```
- hosts: cisco_ios

  tasks:
    - name: collect facts from cisco ios devices
      import_role:
        name: privateip.ios
        tasks_from: get_facts
      vars:
        subset:
          - system
          - interfaces
```

## Arguments

### subset 

Defines the subset of facts to collection when the `get_facts` function is
called.  This value must be a list value and contain only the sub keys for the
facts you wish to return.

The default value is `all`

#### Current supported values for subset are
- system
- interfaces

## Notes
None


