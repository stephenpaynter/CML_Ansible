## Automating Cisco Modelling Labs with Ansible

Cisco Modeling Labs is an on-premise network simulation tool that runs on workstations and servers. With Cisco Modeling Labs, you can quickly and easily simulate Cisco and non-Cisco networks, using real Cisco images. This gives you highly reliable models for designing, testing, and troubleshooting. Compared to building out real-world labs, Cisco Modeling Labs returns results faster, more easily, and for a fraction of the cost.


### Generate Inventory

CML personal allows the user to create and model a lab environment containing 20 nodes. I want to be able to stand these devices up quickly from an IP range covering only the 20 addresses needed for management. An inventory files should be created with the devices assigned to the correct ansible groups and variables assigned.

The playbook allows the creation of devices from the specified pool of addresses, if 20 devices is exceeded the excess devices are ignored and the user warned. The play allows the user to feed in device names to be allocated addressing. A jinja2 template renders the inventory file.
