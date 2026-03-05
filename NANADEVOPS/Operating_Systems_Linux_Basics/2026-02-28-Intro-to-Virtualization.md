<h1> Intro to Virtualization </h1>

```console 
Virtualization: no separate hardware is needed which is done by a 'Hypervisor'
Hypervisor: technology that allows hosting multiple virtual computers on a physical 
computer on top of the operating system that you already have installed. 

Popular Hypervisor: VirtualBox from Oracle- works on all operating system 
    -VirtualBox takes hardware resources from Host OS
    -Creates virtual CPU, virtual RAM, virtual storage for each virtual machine
    -You can only give resources you actually have
    -Virtual machines are completely isolated- doesn't have the host machine 
```

<h3> Type 1 vs Type 2 Hypervisor </h3>

```console 
Type 2 Hypervisor: Creating virtual machines on top of an existing operating system 
    -Host Operating system which is already installed on the hardware on the machine
    -Hypervisor: ex: VirtuaBox 
    -then install guest operating systems 
**Guest OS borrows hardware resources from the Host OS
**These type of hypervisors are typically used for peronal computers


Type 1 Hypervisor: works the same way as Type 1 Hypervisor, however, the Hypervisor is 
                   installed directly on the hardware
                   -also called 'Bare Metal' Hypervisors 
                   -The Hypervisor controlls the hardware resources instead of talking to the Host OS
Ex: VMware ESXi, Microsoft's Hyper-V
Type 1 Hypervisor are mostly utilized by big companies or big cloud platform 
```
