# patch-request
Request for cabling in Datacenters

A Connectivity Request is used by network engineers to create or remove connections between devices.
It is a list of requests to create or remove (patch) cables between devices.

A connectivity request has this format:
* Create source-device source-port  -  destination-device destination-port
* Remove source-device source-port  -  destination-device destination-port

A Patch Request is an excel file that is sent to the cabling team.
This team patches the cables between the devices.
A patch request is a connectivity request enhanced with information like datacenter room, rack, etc.
