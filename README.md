# Patch Request / Cabling Request

This is a python script to request cabling in datacenters.

A Patch Request is an excel file that is sent to the cabling team. This team patches the requested cables between the devices. 

A Connectivity Request is used by network engineers to create or remove connections between devices. It is a list of requests to create or remove (patch) cables between devices.

The patch request is a connectivity request enhanced with information like datacenter room, rack, etc.


## Usage
The script needs two inputs:
1. The connectivity 
2. A file with device definitions.

A connectivity request has this format:
> Create source-device source-port  -  destination-device destination-port  
> Remove source-device source-port  -  destination-device destination-port  

The Device Definitions are imported from a file in YAML format. This file contains a list of devices with its attributes. A device entry looks like this:
>       aDeviceName:
>           model: aModel
>           device_id: aNumber
>           room: aRoom
>           rack: aRack
>           location: aLocation
   

## Disclaimer
The script doesn't check missing files or syntax errors. It is for personal use only.