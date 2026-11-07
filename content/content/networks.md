# Computer Networks: Study Guide

**Topic leader:** Aya Baroudi
**Team:** Aero AI
**Module:** Hardware, Networks & Behaviorist AI
**Level:** Beginner
**Status:** Peer-reviewed (V2.0)

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

## 3. Types of Computer Networks

There are three common types of networks:

| Type | Full name | Explanation | Example |
|---|---|---|---|
| LAN | Local Area Network | Connects devices in a small area. | University laboratory |
| WAN | Wide Area Network | Connects networks over large geographical areas. | A company linking offices in different cities (the Internet is the largest example) |
| WLAN | Wireless Local Area Network | A local network that uses wireless connections. | Home Wi-Fi |

**Remember:** Wi-Fi and the Internet are different. Wi-Fi connects devices wirelessly to a local network, while the Internet connects networks around the world.

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
- **HTTP/HTTPS:** used for communication between web browsers and web servers.

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

The diagram shows how devices connect to a home network. The router connects the local network to the Internet. The switch connects wired devices, while Wi-Fi connects wireless devices.

## 8. Practical Activity: Find the Mistake!

### Scenario

A student wants to print a document from a laptop.

- The laptop is connected to the university Wi-Fi.
- The printer is connected to the same local network through a switch.

The student says:

> "My laptop cannot print, so the router must be broken. A switch is only used to connect the university to the Internet."

### Questions

1. Trace a possible path between the laptop and printer.
2. Identify the mistake in the student's explanation.
3. Predict which connections or devices should be checked first.

Try answering before reading the solution!

## 9. Answers and Explanations

### Answer 1

Laptop → Wireless access point → Local network / Switch → Printer.

**Explanation:** The access point connects the wireless laptop to the local network, and the switch forwards local traffic to the printer.

### Answer 2

The student is wrong because a switch connects devices inside a local network. It is not only used to connect a university to the Internet.

**Explanation:** A router connects different networks, while a switch mainly connects devices within the same LAN.

### Answer 3

Check:

- Whether the laptop is connected to the correct Wi-Fi network.
- Whether the printer is powered on.
- Whether the printer's Ethernet cable is connected correctly.
- Whether both devices are configured to communicate on the same network.

**Explanation:** If both devices are on the same local network, printing may work without an Internet connection. Therefore, the router is not automatically the cause.

## 10. Check Yourself: Bandwidth and Latency

Connection A carries 100 Mbps and data takes 200 ms to arrive. Connection B carries 10 Mbps and data takes 20 ms to arrive.

1. Which connection has the higher bandwidth?
2. Which connection has the lower latency?

**Answer:** 1. Connection A (100 Mbps is more data per second). 2. Connection B (20 ms is a shorter delay).

## 11. Quick Review

- LAN covers a small geographical area.
- WAN covers a large geographical area.
- WLAN uses wireless connections.
- Routers connect different networks.
- Switches connect devices within a local network.
- IP addresses help deliver data.
- Protocols define communication rules.

## 12. References

- Kurose, J. F., & Ross, K. W. (2017). *Computer Networking: A Top-Down Approach* (7th ed.). Pearson. Chapter 1.
- Cisco Networking Academy. (n.d.). *Networking Basics.* https://www.netacad.com/courses/networking-basics
- Internet Engineering Task Force (IETF). (1981). *RFC 791: Internet Protocol.* https://www.rfc-editor.org/rfc/rfc791
- Internet Engineering Task Force (IETF). (1981). *RFC 793: Transmission Control Protocol.* https://www.rfc-editor.org/rfc/rfc793
- Internet Engineering Task Force (IETF). (1980). *RFC 768: User Datagram Protocol.* https://www.rfc-editor.org/rfc/rfc768
- Internet Engineering Task Force (IETF). (1987). *RFC 1034: Domain Names, Concepts and Facilities.* https://www.rfc-editor.org/rfc/rfc1034

The RFCs are the official technical standards, so they are for further reading, not beginner material.
