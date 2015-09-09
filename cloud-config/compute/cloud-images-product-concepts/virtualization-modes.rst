.. _virtualization-modes:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Virtualization modes: PV and PVHVM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can choose between two virtualization modes to be used by the
hypervisor that runs your cloud server:

* Paravirtualized (PV), in which the guest operating system is aware of
  the virtual environment

* Hardware virtualized with paravirtualized drivers (PVHVM), in which
  the guest operating system includes paravirtualized drivers and works
  with hardware virtualization

In general, PVHVM offers better performance than PV, especially for disk
and network I/O, but is not well supported in Linux operating systems
with a kernel version earlier than 2.6.36. The availability of PV and
PVHVM images in the Rackspace cloud is determined by the effectiveness
of each virtualization mode for that particular operating system.

If both PV and PVHVM options are available for the operating system that
you choose to use, consider the following factors when choosing between
them:

Performance
'''''''''''
* Network and disk I/O are faster with PVHVM images because QEMU
  emulation is bypassed.

* PVHVM requires more memory overhead than PV. If your
  application is memory intensive, or if it is optimized for PV Memory
  Management Units, PV might be a better choice.

* If you are striving for performance optimization, test both options
  to determine which one performs better for your application.

File system
'''''''''''
* Ext3 is used for all PV Linux images.

* Ext4 is used for all Arch, Fedora, Gentoo, and Ubuntu PVHVM images.

Boot loader
'''''''''''
* PV images boot via pygrub.

* PVHVM images boot via the boot loader in the master boot record of
  the operating system.

Disk configuration
''''''''''''''''''
* Automatic disk configuration can be used with PV images but fails
  with PVHVM images. The error message looks as follows: ``ERROR:
  Requested image $UUID has automatic disk resize disabled. (HTTP 400)``
