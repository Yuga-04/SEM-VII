# Virtualization of CPU, Memory and I/O Devices

> **Note:** The PDF has no section on this topic. It only says that VMs access the host's **CPU, memory (RAM) and storage**, that a **hypervisor** controls this access, and that each VM behaves like a real computer. Points marked **(general knowledge)** are added to complete the answer.

## 1. Introduction
Virtualization lets multiple VMs share one physical machine, each with its own OS and programs. The **hypervisor** sits between the hardware and the VMs and controls how they use the CPU, memory and I/O. Each VM sees what looks like a complete computer, though it is only a share of the physical one.

## 2. CPU Virtualization
- The hypervisor gives each VM one or more **virtual CPUs (vCPUs)** and schedules them on the physical cores. A VM that needs more power requests it from the hypervisor, which passes the request to the hardware.
- **(general knowledge)** Guest OSes expect full control of the CPU, so the hypervisor must trap and handle their privileged instructions. Three techniques do this:
  - **Full virtualization:** privileged instructions are trapped and emulated, and the guest OS is unmodified.
  - **Paravirtualization:** the guest OS is modified to call the hypervisor directly (hypercalls).
  - **Hardware-assisted virtualization:** CPU extensions such as Intel VT-x and AMD-V let the hardware handle the switching efficiently.
- vCPUs can be **overcommitted**, so more vCPUs than physical cores can exist and the hypervisor time-slices between them.

## 3. Memory Virtualization
- Each VM gets its own **virtual RAM**, carved out of the host's physical memory, and believes it owns that memory. Resources can be resized as needs change.
- **(general knowledge)** There are three address levels:
  - **Guest virtual address:** used by applications inside the VM.
  - **Guest physical address:** what the guest OS thinks is physical memory.
  - **Host physical address:** the real memory on the machine.
- The hypervisor maps guest physical to host physical memory, using **shadow page tables** or hardware support (Intel EPT, AMD NPT).
- Techniques for efficiency include **ballooning** (reclaiming unused guest memory), **page sharing** (identical pages stored once) and **swapping**.
- The hypervisor isolates each VM's memory, so one VM cannot read another's.

## 4. I/O Device Virtualization
- I/O devices such as disks, network cards and graphics adapters are shared among VMs. The PDF's **storage virtualization** and **network virtualization** are examples: pooled storage (Amazon S3) and virtual switches, routers, firewalls and VPNs.
- **(general knowledge)** There are three approaches:
  - **Emulation:** the hypervisor emulates a standard device in software. It is compatible but slow.
  - **Paravirtualized I/O (for example virtio):** the guest uses a special driver that talks efficiently to the hypervisor, giving better performance.
  - **Direct assignment / passthrough (for example SR-IOV):** a physical device or a slice of it is given directly to a VM, with near-native speed.
- The hypervisor multiplexes requests from all VMs onto the physical device and returns results to the correct VM.

## 5. Summary Table

| Resource | Virtual form | Main technique | Benefit |
|---|---|---|---|
| **CPU** | vCPU | Scheduling, trap-and-emulate, hardware assist | Many VMs share few cores |
| **Memory** | Virtual RAM | Address mapping, ballooning, page sharing | Efficient use and isolation |
| **I/O** | Virtual disk, NIC, switch | Emulation, paravirtual drivers, passthrough | Shared devices, flexible management |

## 6. Benefits (from the PDF)
- Better use of resources and lower cost of hardware, power and maintenance.
- Flexibility: VMs can be installed, moved and resized easily.
- Isolation, so a problem in one VM does not affect the others.
- Simple backup, recovery and scalability.

## 7. Conclusion
The hypervisor virtualizes the **CPU** through vCPUs and scheduling, **memory** through address mapping and isolation, and **I/O devices** through emulation, paravirtual drivers or passthrough. Together these let one physical server act as many independent computers.
