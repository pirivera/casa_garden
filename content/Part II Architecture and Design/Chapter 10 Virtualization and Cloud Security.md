[Objective 2.2] Summarize virtualization and cloud computing concepts
##### Cloud Models
There are many different *cloud deployment models* 
Marketed under the concepts of Platform as a Service (PaaS), Software as a Service (Saas), and Infrastructure as a Service (IaaS)
A business analysis must be done to determine correct choice between cloud and on-premise computing.
###### Infrastructure as a Service (IaaS)
Used to describe cloud-based terms that are delivered as a virtual solution for computing
Rather than firms needing data centers, IaaS allow them to contract for utility computing
Specifically marketed on a pay-per-use basis, scalable directly with need
###### Platform as a Service (PaaS)
Used to describe the offering of a computing platform in the cloud
Multiple sets of platforms working together to provide services, can be delivered via the cloud as a platform.
PaaS focuses on security and scalability
###### Software as a Service (SaaS)
Used to offer software to end users from within the cloud
Rather than installing software on client machines, SaaS acts as software on demand
Couples advantages: Updates can be seamless, and integration between components can be enhanced.
###### Anything as a Service (XaaS)
The growth of cloud services, applications, storage, and processing the scale provided by cloud vendors has opened new offerings
The wrapping of SaaS and IaaS creates a new marketable item
###### Level of Control in the Hosting Models
One way to examine differences between the cloud models and on -premise computing is to look at who controls what aspect of the model.
###### Public
The term public cloud refers to a cloud service that is rendered over a system for public use.
There is little operational difference between public and private cloud architectures, but the security ramifications will be significantly less in a public cloud.
###### Community
A *community cloud* is one where several organizations with a common interest share a cloud environment for the specific purpose of the shared endeavor.
###### Private
Private clouds are essentially reserved resources used only by your organization
More expensive, but should carry less exposure and should enable better security, processing, and handling of data
###### Hybrid
A *hybrid cloud* is one where elements of private. public, community are combined
These different communities are not joined but rather are used together
##### Cloud Service Providers
One important thing to remember: If something isn't in the contract, it won't be done.
Otherwise you won't receive that functionality.
##### Manages Service Provider (MSP)/ Managed Security Service Provider (MSSP)
The scope of the engagement, what is in the contract details is what is being provided, and nothing else.
The downside is flexibility, as there is no room for change without renegotiating the contract for services.
##### On-Premises vs. Off-Premises
On premise advantage us that the organization has total control of the system and high connectivity to it.
Disadvantage is that it requires local resources and is not easy to scale
Off-premise or hosted services refer to having the services hosted somewhere else
Using third party provides you a set cost based on the amount of services you use
##### Fog Computing
Fog computing is using someone else's computer
Fog computing moves some of the work into the local space to manage latency issues
Fog computing is an architecture where devices mediate processing between local hardware and remote servers
It regulates which information is sent to the cloud and which is processed locally
It can be viewed as an intelligent gateway, that handle immediate needs while managing the clouds more efficient data storage and processing.
Not a replacement to cloud.
##### Edge Computing
*Edge computing* refers to computing performed at the edge of a network
The true growth in edge computing has occurred with IoT
`Edge computing brings processing power to the edge of the network, which optimizes web application and IoT devices`
##### Thin Client
A lightweight computer with limited resources, whose primary purpose is to communicate with another machine
A device that connects to power and acts as an input/output device where resources can be shared
##### Containers
Container holds the portions of an OS that it it needs separate from the kernel
Therefore, multiple containers can share an OS, yet have separate memory, CPU, and storage threads guaranteeing that they will not interact with other containers.
This allows multiple instances of an application or different apps to share a host OS with virtually no overhead.
Think of containers as the evolution of the VM concept to the application space.
`Containers are a form of OS virtualization. They are a packaged up combination of code and dependencies that help apps run quickly in different computing environments`
##### Microservices/API
An application programming interface is a means for specifying how one interacts with a piece of software.
Microservices is a different architectural style. Microservices divide a system into a series of small modules that can be coupled together to produce a complete system.
Each of the modules is designed to be lightweight, with simple interfaces and structurally complete.
Allows for more rapid development and maintenance of code.
##### Infrastructure as Code
Is the use of code to manage and provision computer systems.
There are significant scalability and flexibility advantages.
Instead of managing physical hardware configuration this can be done programmatically
###### Software-Defined Networking
SDN is a network architecture where the control plane and the data plane are separated.
This allows for networking hardware to be under programmatic control, even while processing data.
A key element of SDN is network function virtualization (NFV)
NFV virtualizes network services, such as routers, firewalls and load balancers, as opposed to specific hardware.
Together SDN and NFV create a functional network under IaaC
###### Software-Defined Visibility
Helps see data flow
Rather than next gen firewall being placed strategically in line with data flow physically, it is done via code through the SDN fabric.
This allows flexibility in design and the ability to reconfigure on the fly
##### Serverless Architecture
Is a way to develop and run applications and services without owning and managing an infrastructure. Servers are still used, but they are owned and managed "off-premise"
##### Services Integration
Is the connection of infrastructure and software elements to provide specific services to a business entity.
Through predesigned scripts, the cloud provider can manage services integration in a much more scalable fashion that individual businesses.
##### Resource Policies
Management of resources such as processing power, security requirements, is done via resource policies.
Through resource policies you can define what, where, or how resources are provisioned.
##### Transit Gateways
Transit gateway is a network connection that is used to interconnect virtual private clouds (VPCs) and on premise networks.
Organization can define and control communication between resources on the cloud providers network and their own infrastructure.
##### Virtualization
`A hypervisor is the interface between a virtual machine and the host machine hardware. Hypervisor compromise the layer that enables virtualization`
Separation of hardware and software, this increases security
###### Type 1
Type 1 hypervisors run directly on the system hardware.
Referred to as native, bare-metal, or embedded hypervisors
Designed for speed and efficiency. 
Thee come with management tool sets to facilitate VM management.
###### Type II
Type II hypervisors run on top of a host OS
Admins can buy VM software and install it on a server they already had running
Type II software such as Oracles VirtualBox and VMWare Player
Typically running in a desktop or small server
###### Virtual Machine Sprawl Avoidance
Sprawl is the uncontrolled spreading and disorganization caused by a lack of organizational structure when many similar elements require management.
Can be avoided through policy, through naming conventions and proper storage architecture.
###### VM Escape Protection
Where malware or an attacker escaped from one VM to the underlying OS
Large scale VM environments have specific modules designed to detect escape and provide VM escape protection to other modules

cbcdbabdbb