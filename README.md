# ovirt-guest agent


Installationand confuguration of the ovirt guest agent.

# Requirements

For Redat based OS **epel** is required, but I do not put in in depencency.

# Role Variables
--------------

## ovirt_guest_agent_device

**ovirt_guest_agent_device** file in the **/dev//virtio-ports/**. Defualt value is `ovirt-guest-agent.0`.
For older relases of the **oVrt** should be changed into `com.redhat.rhevm.vdsm`.


# Dependencies
------------

NONE

# Example Playbook


    - hosts: servers
      roles:
      - role: hudecof.ovirt-guest-agent
        when: "ansible_virtualization_type == 'kvm'and ansible_virtualization_role == 'guest'"

# License

BSD

# Author Information

Peter Hudec
CNC, a.s.