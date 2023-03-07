---
title: "How to Check RAM in Linux Terminal"
datePublished: Tue Mar 07 2023 15:10:32 GMT+0000 (Coordinated Universal Time)
cuid: cleye1h47000e09mjfu3ucpaa
slug: how-to-check-ram-in-linux-terminal
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678201814213/cace5f57-c09e-49bd-945f-237e09e711e1.png
tags: linux

---

The "sudo dmidecode --type 17" command is a useful tool for users of Linux-based operating systems who want to know more about the physical memory, or RAM, installed on their system.

In essence, the command displays detailed information about the physical memory slots in your computer, including the type, speed, size, and manufacturer of the RAM modules. This information can be especially useful if you are planning to upgrade or replace your RAM, as it will allow you to make an informed decision about which type of RAM to purchase.

The "--type 17" flag specifies the type of data that dmidecode will display. In this case, type 17 refers to the memory device data, which includes information about the physical memory slots in your system.

To use the command, simply open a terminal window and type "sudo dmidecode --type 17". You will then see a detailed list of all the memory slots on your system, along with the relevant details about each slot.

For example, you might see something like:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678201759838/bfd0dc67-5935-4cf7-bd9b-d9659c5b63f1.png align="center")

In conclusion, the "sudo dmidecode --type 17" command is a valuable tool for Linux users who want to know more about the physical memory installed on their system. Whether you are planning to upgrade or replace your RAM, or simply curious about your system's hardware, this command can provide you with a wealth of useful information.