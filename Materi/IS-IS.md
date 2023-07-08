# IS-IS

## NET, IS-IS Network entity title

"Network Entity Title" (NET) refers to a unique identifier assigned to each IS-IS router in a network. It is used to distinguish between different routers and facilitate routing and communication within the network.

- Each IS-IS router is identified by a Network Entity Title  (NET). 
- NET is like the Router ID in other routing protocols
- Net is a type of Network Service Access Point (NSAP) address
 + NSAP address is defined in ISO/IEC 8348, is an identifying label for a Service Access Point (SAP) used in OSI Networking.

- NET is a type of Network Service Access point(NSAP) address, with NSAP Selector set 0.
- NET is hexadecimal. it has a variable length between 8 bytes and 20 bytes:
  ![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/532ea382-fa2a-47cb-b0cf-52d129b37602)

  To generate a Network Entity Title (NET) for a router in IS-IS, you can follow these steps:

Determine the System ID: Let's say the router's MAC address is "00:1A:2B:3C:4D:5E". You can take a portion of the MAC address, such as the last three bytes, to form the System ID. In this case, the System ID would be "3C4D5E".
![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/23e7e412-5610-4d84-8057-d5a10a2e9c6b)


Determine the Area ID: Suppose the network is divided into areas, and this router belongs to Area 42. The Area ID would be "42".
![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/5d29e741-d44c-41a7-b908-eacaf597eed7)


Determine the Domain ID: Let's assume the Autonomous System (AS) to which the router belongs is AS 65535. The Domain ID would be "65535".
![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/729560f1-25cb-4520-a264-697599dc82fd)

Combine the components: Finally, you combine the System ID, Area ID, and Domain ID to form the complete NET for the router. Using the example values, the NET for the router would be "3C4D5E.42.65535".

Remember that this is just an example, and the actual process and format of generating a NET may vary based on your specific IS-IS implementation and network configuration. It's always recommended to consult the documentation or configuration guides of your networking equipment or software for precise instructions on generating a NET for your router.

## What is NSAP?

NSAP stands for Network Service Access Point. It is a term used in networking to refer to an addressing scheme used by the OSI (Open Systems Interconnection) network model.

In particular, NSAP refers to the addressing structure defined by the Network Layer protocol of OSI, known as CLNP (Connectionless Network Protocol). NSAP addresses are used to uniquely identify network entities (routers or hosts) within an OSI network.

The NSAP address is a hierarchical structure consisting of several components, including:

Authority and Format Identifier (AFI): It identifies the format and authority responsible for the NSAP allocation. For example, AFI 47 represents the ISO/IEC standard.

Initial Domain Part (IDP): It specifies the administrative authority or organization responsible for the addressing within a particular domain.

Area Address: It identifies the routing domain or area within the administrative authority.

System Identifier: It represents the unique identifier of a specific network entity (router or host) within the area.

NSAP addresses are typically used in conjunction with the OSI routing protocols, such as IS-IS (Intermediate System to Intermediate System) and CLNP, to enable the routing and forwarding of packets within an OSI network. However, it's important to note that the OSI model and protocols are not widely used in modern networking, and TCP/IP-based protocols, such as IP addressing, are more prevalent in today's networks.

## NSAP Address Structure
![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/d12072fa-bcba-48b1-b178-9b5264ebc977)

# IS-IS Operations

## IS-IS Packets
IS-IS mempunyai 3 kategori paket,

- IS-IS Hello PDU (IIH) . Discovers, builds, and maintains IS-IS neighbors
- Link-State PDU (LSP) . Distributes routing information between IS-IS routers
- Sequence Number PDU (SNP) . Provides Mechanism to synchronize LSDBs between IS-IS routers
- ![image](https://github.com/Azzamkazamii/Networkizam/assets/69065703/3fb65bc2-3da6-427d-b8cc-117efd58af2d)




