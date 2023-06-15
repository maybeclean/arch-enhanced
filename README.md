# Arch Enhanced (Mainly for VMs)

This is a modified version of the latest Arch Kernel as of 6/14/23 (6.3.8) which has patches in place to bypass vmexit detections by modifying RDTSC and with enableable PCIE ACS Overrides to bypass cases of unwanted IOMMU Grouping.
* ACS Overrides are technically unsafe and expose the memory of devices on the real IOMMU group to the guest, casual VM gamers are probably not a target for this type of attack but just something to know.
* * You only need to enable ACS Overrides as a boot parameter if the devices you want to passthrough are in an undesirable group. EG: GPU grouped with CPU PCIE Devices. 

![Example Screenshot](https://i.imgur.com/WF34AYd.png)