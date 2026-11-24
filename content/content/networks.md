# Computer Networks

**Topic leader:** Aya Baroudi
**Team:** Aero AI
**Module:** Hardware, Networks & Behaviorist AI
**Level:** Beginner
**Status:** Final version (Stage 3)

## Learning Outcomes

After this section, learners should be able to:

- Explain what a computer network is and why networks are useful.
- Distinguish LAN, WAN and WLAN, and explain why Wi-Fi is not the same as the Internet.
- State the job of a router, a switch, a modem and a wireless access point.
- Explain what an IP address, a packet, a protocol and DNS are, and describe how a website loads.
- Tell bandwidth from latency, and use `ping`, `nslookup` and `tracert`/`traceroute` to observe latency, DNS and hops.

**Prerequisite:** none. Learners only need to have used a computer or phone to open a website. Mission 1 (Hardware) is helpful but not required.

## 1. Introduction to Computer Networks

A **computer network** is a group of two or more devices connected together to communicate and share information.

Examples of network devices include:

- Computers
- Smartphones
- Printers
- Servers

Devices can connect using:

- **Wired connections** (Ethernet cables)
- **Wireless connections** (Wi-Fi)

### Why Are Networks Important?

- **Communication:** sending messages and emails.
- **Resource sharing:** sharing printers and files.
- **Information sharing:** accessing websites and online information.
- **Collaboration:** working together on shared documents.

## 2. Important Networking Vocabulary

| Word | Simple explanation |
|---|---|
| Network | Connected devices that exchange information. |
| Node | A device connected to a network. |
| Data | Information sent between devices. |
| Packet | A small piece of data sent through a network. |
| IP address | A numerical address used to identify a device on an IP network. |
| Protocol | Rules that devices follow to communicate. |
| Bandwidth | The maximum amount of data a connection can carry per second. |
| Latency | The time needed for data to travel between two points. |
| Hop | One router that packets pass through on the way to their destination. |

## 3. Types of Computer Networks

There are three common types of networks:

| Type | Full name | Explanation | Example |
|---|---|---|---|
| LAN | Local Area Network | Connects devices in a small area. | University laboratory |
| WAN | Wide Area Network | Connects networks over large geographical areas. | A company linking offices in different cities (the Internet is the largest example) |
| WLAN | Wireless Local Area Network | A local network that uses wireless connections. | Home Wi-Fi |

**Remember:** Wi-Fi and the Internet are different. Wi-Fi connects devices wirelessly to a local network, while the Internet connects networks around the world. You can be connected to Wi-Fi even when Internet access is unavailable.

## 4. Common Network Devices

| Device | Function |
|---|---|
| Router | Connects different networks and forwards data between them. |
| Switch | Connects devices within the same local network. |
| Modem | Connects a network to an Internet service provider's access technology. |
| Wireless access point | Allows wireless devices to connect to a local network. |

### Example

In a university computer laboratory:

- A **switch** connects computers and printers.
- A **router** connects the university network to the Internet.
- A **wireless access point** provides Wi-Fi for students.

## 5. IP Addresses and Network Protocols

An **IP address** helps identify where data should be delivered on an IP network.

Example: `192.168.1.10`

A **protocol** is a set of rules that allows devices to communicate.

Common protocols:

- **IP:** provides addressing and helps deliver packets.
- **TCP:** provides reliable and ordered data delivery.
- **UDP:** sends data without TCP's built-in delivery guarantees.
- **DNS:** translates domain names into IP addresses.
- **HTTP/HTTPS:** used for communication between web browsers and web servers. HTTPS adds encryption through TLS.

## 6. Worked Example: How Does a Website Load?

Imagine Aya opens a website using her laptop and home Wi-Fi.

1. **Step 1:** The laptop connects to the local network through Wi-Fi, using the wireless access point (in many homes this is built into the router).
2. **Step 2:** DNS helps find the IP address of the website.
3. **Step 3:** The laptop prepares a request to the website.
4. **Step 4:** The router forwards the data towards the Internet.
5. **Step 5:** Routers forward the packets towards the website's server.
6. **Step 6:** The server sends a response to the laptop.
7. **Step 7:** The browser displays the website.

**Explanation:** The access point provides wireless connectivity, the router forwards traffic between networks, DNS helps find the server, and the server provides the requested information.

## 7. Network Diagram

```text
                 INTERNET
                     |
                   MODEM
                     |
                  ROUTER ~~~~ Wi-Fi ~~~~ LAPTOP, PHONE
                     |
                  SWITCH
                  /     \
             DESKTOP   PRINTER
```

Lines (`|`, `/`, `\`) are cables. `~~~~` is a wireless connection.

The diagram shows how devices connect to a home network. The router connects the local network to the Internet. The switch connects wired devices, while Wi-Fi connects wireless devices. A labelled picture of the same network is in `Figure2_Home_Network.png` (see Section 12).

## 8. Practical Activities

Activities 4, 5 and 6 are numbered the same way in the Study Guide, the slides and the Test Bank. For each one, try your own answer before reading the solution.

### Activity 4: Find the Network Mistake

**Goal:** tell a switch from a router, and reason about local communication.
**Preparation:** none. No software is needed.

**Scenario:** A student wants to print a document from a laptop.

- The laptop is connected to the university Wi-Fi.
- The printer is connected to the same local network through a switch.

The student says:

> "My laptop cannot print, so the router must be broken. A switch is only used to connect the university to the Internet."

**Questions**

1. Trace a possible path between the laptop and printer.
2. Identify the mistake in the student's explanation.
3. Predict which connections or devices should be checked first.

**Reflection:** why is it useful to know the difference between a switch and a router?

**Hint:** does printing need to leave the local network, or stay inside it?

#### Answers and Explanations

**Answer 1.** Laptop → Wireless access point → Local network / Switch → Printer.

**Explanation:** The access point connects the wireless laptop to the local network, and the switch forwards local traffic to the printer.

**Answer 2.** The student is wrong because a switch connects devices inside a local network. It is not only used to connect a university to the Internet.

**Explanation:** A router connects different networks, while a switch mainly connects devices within the same LAN.

**Answer 3.** Check:

- Whether the laptop is connected to the correct Wi-Fi network.
- Whether the printer is powered on.
- Whether the printer's Ethernet cable is connected correctly.
- Whether both devices are configured to communicate on the same network.

**Explanation:** If both devices are on the same local network, printing may work without an Internet connection. Therefore, the router is not automatically the cause.

### Activity 5: Bandwidth or Latency?

**Goal:** tell data capacity apart from delay.
**Preparation:** use the two connections below.

Connection A carries 100 Mbps and data takes 200 ms to arrive. Connection B carries 10 Mbps and data takes 20 ms to arrive.

1. Which connection has the higher bandwidth?
2. Which connection has the lower latency?
3. Which connection might feel more responsive for a small interactive request, and which can carry more data per second?

**Reflection:** why is "faster Internet" not a precise technical description?

**Hint:** bandwidth = how much per second; latency = how long the wait is.

#### Answers and Explanations

1. Connection A (100 Mbps is more data per second).
2. Connection B (20 ms is a shorter delay).
3. Connection B may feel quicker for small interactive requests because of its lower latency, while Connection A can carry more data per second. Real performance also depends on other factors.

### Activity 6: Network Detective: Ping, Trace, Lookup

**Goal:** observe latency, routing and DNS on a real network, with no account and no installation.

**Three tools you will use**

| Tool | What it shows |
|---|---|
| `ping` | The round-trip time to a site in milliseconds (ms). This is a measure of **latency**, not bandwidth. |
| `nslookup` | The IP address that DNS returns for a domain name. |
| `tracert` (Windows) or `traceroute` (Mac/Linux) | The list of routers (hops) your packets pass through on the way to the site. |

**Preparation:** open Command Prompt (Windows) or Terminal (Mac/Linux). Choose two websites that load for you: one you expect to be hosted fairly near you and one you expect to be far away. Below, `site1` and `site2` stand for your two choices.

**Task**

1. Run `ping site1` and `ping site2` (type the full domain name). Record the average time in ms. On Mac/Linux, stop with Ctrl+C.
2. Predict which site will have the higher latency, and why.
3. Run `nslookup site1` and note the IP address returned.
4. Run `tracert site1` (Windows) or `traceroute site1` (Mac/Linux) and count the hops.

**Observation:** record your results in a table:

| Site | Average ping (ms) | IP address | Number of hops |
|---|---|---|---|
| site1 | | | |
| site2 | | | |

Take a screenshot of one result.

**Reflection**

- Which step shows DNS at work?
- Does `ping` measure bandwidth or latency?
- Which devices from Section 4 might appear as hops?

**Hint:** DNS = names to addresses; ping = round-trip delay; trace = the list of routers along the way.

**Fallback (if your network blocks these commands):** use the illustrative output below and answer the Reflection questions from it. Real values will differ.

```text
> ping site1.example
Reply from 203.0.113.10: bytes=32 time=18ms TTL=56
Reply from 203.0.113.10: bytes=32 time=21ms TTL=56
Reply from 203.0.113.10: bytes=32 time=19ms TTL=56

> nslookup site1.example
Name:     site1.example
Address:  203.0.113.10

> tracert site1.example
 1    <1 ms   192.168.1.1    (home/lab router)
 2     9 ms   10.20.0.1      (internet provider)
 3    14 ms   198.51.100.5   (another router)
 4    18 ms   203.0.113.10   (destination)
```

This output is an example only. The addresses are reserved for documentation, so they are not real websites.

#### Answers and Explanations

- `nslookup` shows DNS translating a name into an IP address.
- `ping` reports round-trip time, which is latency. It does not measure bandwidth (compare Activity 5).
- Farther sites often, but not always, have higher latency, because routing and network load also matter.
- Each hop in a trace is a router forwarding your packets.
- Some networks block `ping` or `traceroute` replies, so you may see "Request timed out" or `* * *`. That does not mean the site is broken.
- Large sites may return different IP addresses on different runs.

## 9. Optional Investigation: Cisco Packet Tracer

This part is **optional** and is not needed for the rest of the module. Cisco Packet Tracer is a network simulation tool for designing, configuring and observing virtual networks. It is a simulation, not a replacement for all behavior of real hardware.

1. Create a small topology with two PCs and one switch. Connect each PC to the switch with the appropriate Ethernet cable.
2. Give the PCs addresses in the same example network: `192.168.1.10/24` and `192.168.1.11/24`.
3. Open the command prompt on one PC and `ping` the other. Record whether the ping succeeds.
4. Change the second PC to a different subnet, such as `192.168.2.11/24`, and predict what will happen without a router.
5. Restore the original address and compare the results. Explain what the test shows about local addressing and connectivity.

**Access and fallback:** Packet Tracer needs installation and a Cisco Networking Academy account to download (the free course "Getting Started with Cisco Packet Tracer" is listed in Section 14). If you cannot use it, draw the topology on paper and explain the expected result.

**Expected result:** two correctly addressed PCs in the same subnet can communicate through a switch. Changing one to a different subnet generally requires a router or another Layer 3 device before they can communicate.

## 10. Check Yourself

1. Which device mainly connects devices within one LAN: a router or a switch?
2. Does being connected to Wi-Fi always mean the Internet is working?
3. What does DNS do?
4. Connection A is 100 Mbps / 200 ms and Connection B is 10 Mbps / 20 ms. Which has the lower latency?
5. In Activity 6, what does one extra hop in a traceroute represent?

**Answers:**

1. A switch. A router mainly forwards traffic between different networks.
2. No. Wi-Fi may connect you to the local network even when the Internet service is unavailable.
3. It helps translate a domain name into an IP address.
4. Connection B, because 20 ms is a shorter delay than 200 ms.
5. One more router that your packets pass through on the way to the destination.

## 11. Quick Review

- LAN covers a small geographical area.
- WAN covers a large geographical area.
- WLAN uses wireless connections.
- Wi-Fi is not the same as the Internet.
- A wireless access point gives Wi-Fi access, a switch connects local devices, and a router connects networks.
- IP addresses help deliver data. Protocols define communication rules. DNS turns names into IP addresses.
- Bandwidth is capacity per second. Latency is delay.
- `ping` measures latency, `nslookup` shows DNS at work, and `traceroute`/`tracert` lists the hops.

## 12. Supporting Files

| File | Use |
|---|---|
| `Networks_Activity.pdf` | Printable worksheet for Activities 4 to 6, including an offline fallback. |
| `Network_Cards.pdf` | Cut-out cards (devices, steps and packets) to act out how a website loads. |
| `Figure2_Home_Network.png` | Labelled picture of the home/lab network from Section 7. |

See the project README for where these files are stored.

## 13. How This Topic Connects to the Other Missions

A laptop needs the hardware from Mission 1 to send a request, and the network from this mission to carry it to a server. See `connections.md` for the full connected scenario with Mission 3.

## 14. References

- Kurose, J. F., & Ross, K. W. (2017). *Computer Networking: A Top-Down Approach* (7th ed.). Pearson. Chapter 1.
- Cisco Networking Academy. (n.d.). *Networking Basics.* https://www.netacad.com/courses/networking-basics
- Cisco Networking Academy. (n.d.). *Getting Started with Cisco Packet Tracer.* https://www.netacad.com/courses/getting-started-cisco-packet-tracer/1000
- Internet Engineering Task Force (IETF). (1981). *RFC 791: Internet Protocol.* https://www.rfc-editor.org/rfc/rfc791
- Internet Engineering Task Force (IETF). (1981). *RFC 793: Transmission Control Protocol.* https://www.rfc-editor.org/rfc/rfc793
- Internet Engineering Task Force (IETF). (1980). *RFC 768: User Datagram Protocol.* https://www.rfc-editor.org/rfc/rfc768
- Internet Engineering Task Force (IETF). (1987). *RFC 1034: Domain Names, Concepts and Facilities.* https://www.rfc-editor.org/rfc/rfc1034

The RFCs are the official technical standards, so they are for further reading, not beginner material.
