# zabbix-TemplateHyperVReplica

This is a template for Zabbix 6+ that enables monitoring of the replication status from Hyper-V hosts.

## How it works
This template utilizes the Zabbix agent's WMI.GETALL function, eliminating the need to directly add a user parameter to the hosts. The wmi.getall agent function is available on Zabbix agents v5.0+.

## What it does
The template incorporates low-level discovery to create items and triggers for all virtual machines on the host. After the low level discovery process runs you can disable any uneeded triggers.

## What is does not do
* This template has not been tested in scenarios where a virtual machine is replicated across multiple hosts (extended replication).
* It does not provide monitoring for Hyper-V performance or anything beyond vm status and replication status.
