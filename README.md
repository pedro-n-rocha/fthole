# fthole


HW 

ixl0@pci0:1:0:0:	class=0x020000 card=0x00078086 chip=0x15728086 rev=0x02 hdr=0x00
    vendor     = 'Intel Corporation'
    device     = 'Ethernet Controller X710 for 10GbE SFP+'
    class      = network
    subclass   = ethernet

FreeBSD fw.polar 12.3-STABLE FreeBSD 12.3-STABLE RELENG_2_6_0-n226742-1285d6d205f pfSense  amd64


In FreeBSD, in /boot/loader.conf.local put:

hw.ixgbe.unsupported_sfp=1

https://forum.netgate.com/topic/140887/xg-7100-with-third-party-optics-best-place-and-way-to-configure-unsupported_sfp-options/2

https://docs.netgate.com/pfsense/en/latest/install/upgrade-before-2.2.html#intel-10gbit-s-ixgbe-ix-users-with-unsupported-sfp-modules

vi /boot/loader.conf.local
hw.ix.unsupported_sfp=1


ixl0: <Intel(R) Ethernet Controller X710 for 10GbE SFP+ - 2.3.1-k> mem 0x92000000-0x927fffff,0x92808000-0x9280ffff irq 16 at device 0.0 on pci1
ixl0: fw 6.0.48442 api 1.7 nvm 6.01 etid 800035cf oem 1.262.0
ixl0: PF-ID[0]: VFs 64, MSI-X 129, VF MSI-X 5, QPs 768, I2C
ixl0: Using 1024 TX descriptors and 1024 RX descriptors
ixl0: Using 2 RX queues 2 TX queues
ixl0: Using MSI-X interrupts with 3 vectors
ixl0: Ethernet address: 40:a6:b7:21:60:44
ixl0: Allocating 2 queues for PF LAN VSI; 2 queues active
ixl0: PCI Express Bus: Speed 8.0GT/s Width x8
ixl0: SR-IOV ready
ixl0: netmap queues/slots: TX 2/1024, RX 2/1024



