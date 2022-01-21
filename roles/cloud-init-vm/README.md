Role Name
=========

Create a VM based on a cloud image

Requirements
------------

The following commands needs to be availabe:

- virt-install
- virsh
- qemu-img

Role Variables
--------------

| Variable   | Description                                               | Default                                                |
|------------|-----------------------------------------------------------|--------------------------------------------------------|
| vm_name    | Requiered: name of VM to create                           |                                                        |
| base_image | Path to base image                                        | `/home/martin/Downloads/debian-11-generic-amd64.qcow2` |
| target_dir | Directory where disk image and yaml files will be created | `/home/martin/tmp`                                     |
| disk_size  | Size of virtual disk to create                            | `10G`                                                  |
| dest_path  |                                                           | `{{ target_dir }}/{{ vm_name }}_disk.img`              |
| user_data  |                                                           | `{{ target_dir }}/{{ vm_name }}_user-data.yaml`        |
| meta_data  |                                                           | `{{ target_dir }}/{{ vm_name }}_meta-data.yaml`        |


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

	- name: Create 3 VMs
	  hosts: localhost
	  roles:
	    - role: cloud-init-vm
          vars:
            vm_name: vm_kafka-01
        - role: cloud-init-vm
          vars:
            vm_name: vm_kafka-02
        - role: cloud-init-vm
          vars:
            vm_name: vm_kafka-03


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
