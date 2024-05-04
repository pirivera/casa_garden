[Objective 2.5] Given a scenario, implements cybersecurity resilience
##### Redundancy
*Redundancy* is the use of multiple, independent elements to perform a critical function, so that if one element fails, there is another that can take over the work.
Having spare for critical functions can greatly facilitate maintaining business continuity in the event of hardware failures.
##### Geographic Dispersal
An important element to factor into the cost of the backup strategy is the expense of storing the backups.
Keep copies of backups in separate locations. The most recent copy can be stored locally.
There are also advancements in online backup services.
###### Disk
Disks are primary storage mechanism in a system, whether physical hard drives or solid state memory.
###### Redundant Array of Inexpensive Disk (RAID) Levels
Takes data on a single disk and spreads it out among several others.
If any data is lost it can be recovered from other disks where the data resides also.
- <mark style="background: #FFB86CA6;">RAID 0 (striped)</mark> spreads data that would be kept in one disk across several disks. Decreases time it takes to retrieve data, but does not improve reliability because the loss of any single drive will result in the loss of all data. No redundancy.
- <mark style="background: #FF5582A6;">RAID 1 (mirrored) </mark>copies the data from one disk onto two or more disks. If one is lost the data is not lost since it also copied onto other disks. Improves reliability and retrieval speed, but expensive.
- <mark style="background: #FFB8EBA6;">RAID 2 (bit level error correcting code)</mark> not typically used, as it stripes data across the drives at the bit level opposed to block level. Designed to be able to recover the loss of any single disk through the use of error correcting techniques.
- <mark style="background: #D2B3FFA6;">RAID 3 (byte striped with error check) </mark>spreads data across multiple disks at byte level with one disk dedicated to parity bits. Not commonly used.
- <mark style="background: #ADCCFFA6;">RAID 4 (dedicated parity drive)</mark> stipes data across several disks but in larger stripes than RAID 3. Does not improve retrieval speeds.
- <mark style="background: #BBFABBA6;"> RAID 5 (block striped with error checks)</mark> stipes the data at block level and spreads the parity data across the drives. Provides reliability and speed. Requires min. three drives.
`RAID 0 and 1 require 2 drive minimum. RAID 3 and 5 require minimum 3 drives. RAID 10 (1 + 0) requires 4 drives minimum`
###### Multipath
Between the storage systems and the server/computer is an I/O interface.
This I/O converts the information from the computer to a form that works for the specific storage system.
There are different interfaces for storage systems (RAID, SCSI,SATA, and Fiber)
Multipath is a storage element connected by multiple adapters, which provides redundancy for the adapters.
##### Network
Two major elements to consider are load balancers and network interface cards (NIC) teaming to remove traffic failures in networks
###### Load Balancers
Moves loads across a set of resources in an effort to not overload individual servers.
Designed to distribute the processing load over to two or more systems.
Used to help improve resource utilization and throughput and also the advantage of increasing the fault tolerance of the overall system.
Best for stateless systems.
###### NIC Teaming
Connecting servers that have multiple network cards.
The OS combines the NICs into a virtual NIC from the OS perspective
If one has heavy traffic the other NICs carry the load
Allows redundancy and increased bandwidth
##### Power
Equipment such as UPS, generators, and managed power distribution all support having the proper if electricity available to the networking equipment at all times.
###### UPS
Are power supply systems that can function using a temporary battery backup in the event of power failure. Designed to keep equipment running while backup power is connected or enough time to gracefully shutdown
###### Generator
Backup generators are used to provide power when normal sources of electricity are lost.
Circuits energized by the backup generator are separate circuits that provide power to desired components.
It is not easy or cost efficient to resize the backup power. Long term use, resupply of fuel needs to be managed.
Typically used during natural disasters
###### Dual Supply
A dual supply is a system where two independent power supply units are used. Made to be hot swappable, the bad supply can be replaced without powering down the unit.
###### Managed PDUs
Designed to handle the electrical power for server racks
Objective is to efficiently convert the power and manage the heat from the conversion while producing a power flow that is conditioned from spikes and over/under voltage.
PDUs offer extensive monitoring capability
##### Replication
Simple form of redundancy, having another copy of something should something happen to the original.
Dual power supplies replicate the power.
Common replication include storage area networks and virtual machine technologies.
###### Storage Area Network (SAN)
Is a dedicated network that connect compute elements to storage elements,
This network can be optimized for the types of data storage needed.
SAN resolves point of failure by making the data storage independent of any individual computer and can even interface to multiple redundant storage systems to allow redundancy on the side of data storage as well.
###### VM
VM technologies can enable replication of processing units that be manipulated between different computers.
Provides administrators ease of adding storage.
##### Backup Types
Key element in business continuity/disaster recovery (BC/DR) is the availability of backups
Four main forms of backups: full, incremental, differential, and snapshot
###### Full
In a full backup, all files and software are copied onto the storage media
In a full backup, the archive bit is cleared
`A full backup copies all data and clears/resets the archive bit.Takes time but a full restore with one tape`
###### Incremental
Incremental backs up only files that have changed since the last full or incremental backup occurred, requiring less files to be backed up
Incremental relies on the occasional full backup
After that you backup files that have changes since the last backup
Advantage is that it requires less storage and time to accomplish.
Disadvantage is restoration is more involved.
Incremental will clear the archive bit.
`You need the last full backup and every incremental tape since the last backup`
###### Snapshot
Copy of a virtual machine at a specific point in time
Created by copying the files that store the virtual machine
Advantage is the ease of backing up and restoring
Easy as a click
###### Differential
Only the files that have changed since the last backup was completed are backed up
A full backup needs to be accomplished periodically
Restoration involves: a full backup needs to be loaded, and then the last differential backup performed can be applied
Takes less time than a full backup, depending on how long the differential has been
Archive bit is not cleared
###### Tape
Tape drives are an older form of storage mechanism, characterized by their read/write access
Disk allows to directly access specific elements, tape is stored in one long structure requiring to physically move tape if you want access halfway through storage
For bulk storage of backups tape is still a alternative in terms of cost and operation.
###### Disk
Term *disk* refers to either a physical hard drive with spinning platters or a SSD,
Many systems can perform a full, incremental, snapshot, or differential backup of a disk.
###### Copy
Copying is the simplest form of backup for a file or set of files.
For larger scaled backups, previous options is more efficient for backing up and restoring
Advantages of having users make copies of critical documents is the ability to do a quick restore in the event of an overwrite error.
###### Network Attached Storage (NAS)
Is the use of a network connection to attach external storage to a machine
NAS is a simple extension of data storage to an external system, and typically these devices do not transfer data fast enough for regular operations.
However, they work well as an external site for data backup and recover solutions on smaller single machine scale.
###### Storage Area Network (SAN)
A SAN is a dedicated network that connects compute elements to storage elements.
Multiple different servers across the enterprise can connect via a SAN to a backup array, enabling efficient and effective backups in a flexible manner.

`NAS is a single storage devuce that serves files over the network to a machine. SAN is a network of multiple devices designed to manage large and complex sets of data in real time speed`
###### Cloud
Advantage is offsite, and can have multiple redundant copies, and available via the web.
Disadvantage is its managed by legal agreement to a backup vendor.
###### Image
An image based backup is a specific structure of the backup file to match that of the system being backed up.
This takes more time and space, but guaranteed not to miss anything including deleted data and free space.
Image backups can provide extra layers of assurance when certain types of failures leave a system unusable (malware attack)
###### Online vs. Offline
Online backups are stores in a location accessible via the internet
Offline are stored on an offline system that is not accessible via the internet
Online have the advantage of providing geographic separation of the backups from the original system.
###### Offsite Storage
Stored in a location separate from the system being backed up
Having offsite alleviates the risk of losing the backups to the same problem.
###### Distance Considerations
Distance associated with offsite backup is a logistics issue. If you need a system there can be a delay if stored hours away.
Also far away to not be affected by natural disaster even for clouds hosted in this area.
##### Nonpersistence
Nonpersistence refers to a system that are not permanent and can change
Needs to be managed and systems that have this characteristic typically have mechanisms built in to manage this diversity.
###### Revert to Known State
Data backups can bring back data elements of a system, but brining back the configuration of a system, including patches and drivers is more complicated.
Many OSs have the ability to roll back: both servers and desktops
###### Last Known-Good Configuration
On boot failure, Microsoft Windows gives an option to revert to last-known good configuration
Windows Recovery system
###### Live Boot Media
Boot to live boot media using USB or DVD source that contains a complete image of the OS
##### High Availability
Refers to the ability to maintain the availability of data and processing despite a disrupting event
More than data redundancy, need both data and services to be available
###### Scalability
Is a design element that enables a system to accommodate larger workloads by adding resources either making the hardware stronger (scaling up) or adding additional nodes (scaling out)
###### Restoration Order
Developing a restoration plan, along with the order what needs restoration first and so on is important because this will drive certain operations when backing up in the first place.
