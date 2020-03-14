---
title: Lab Status 2018-8-27
date: 2018-08-27 22:52:42
tags: SELAB
---

- Jump Server is ready, using the old 6th server in the rack.
- Vcenter windows is not ready as the server can not be booted with USB or DVD
- Add a new ```ESXi-3```, using the old 3th server in the rack.
- Add new ```vSwitch-10G``` in all esxi for vms, create new ```Common_vm_network``` port-group and associate it to the new ```vSwitch-10G```. (the vswitch name in the ```esxi3``` is ```vSwitch-1G```)
- Remove the default vm port-group which using the ```vswitch0```.
- Thus make sure the mgtm and vm are split. 
