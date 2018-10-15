# Firewalls

## Firewall Explanations

* firewalls are an **access control** for a network
* like a "secretary," filters requests
* Types:
    * Packet Filter
    * Stateful PAcket Filter
    * Application Proxy
    * **these are for different layers**

## Packet
* On Network Layer
* TCP/IP
* checks header
* filters based on specific data points
* Fastest Firewall
* No concept of state: no memory of state (i.e. an ongoing communication)
* cannot see TCP, attack vulnerable
* blind to application data, which most likely has malware
* ACL would be trivial (only needs to check source/destination port)

## TCP ACK Scan
* scan for open ports, aka **port scanning**
* Send ACK, without SYN, check all ports until gets back a port that works
* knowing an open port lets you do further attacks

## Stateful Packet Filter
* remembers TCP/IP connections
* prevents TCP ACK scan

## Application Proxy
* proxy, acts on your behalf
* **important** can see everything, complete view
* can filter bad data at application layer, aka Viruses
* disadvantage: 
    * speed, needs to analyze *everything*, regenerates all header values

## Firewalk
* Scans ports that are open
* TTL: Time To Leave
* If system sends "time exceeded," found an open port
* app. proxy will deny this by destroying old TTL