# Patch Request / Cabling Request

This is a python script for network engineers to ease requesting cables (patches) in datacenters.

Network engineers use a *connectivity request* to request cables between devices. A connectivity request is a list of requests to create or remove patch cables between devices.

A *patch request* is an excel file that is sent to the cabling team. This team patches the requested cables between the devices. So, a patch request is in fact a connectivity request enhanced with information like datacenter room, rack, etc.

## Usage
The script uses two input files:
1. The connectivity request.
2. A file with device definitions/properties.

A connectivity request has this format:
> Create source-device source-port  -  destination-device destination-port  
> Remove source-device source-port  -  destination-device destination-port  

The *device definitions* are imported from a file in YAML format. This file contains a list of devices with its attributes. A device entry looks like this:
>       aDeviceName:
>           model: aModel
>           device_id: aNumber
>           room: aRoom
>           rack: aRack
>           location: aLocation
   
## Disclaimer
The script doesn't check missing files or syntax errors. It is for personal use only.