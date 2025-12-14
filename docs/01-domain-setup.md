# Domain Setup

## Objective
Create the Domain and promote server to DC

## Steps Performed
1. Assigned server with a static IP address and pointed its DNS to the loopback address
2. Installed Active Directory Domain Services
3. Created a new Forest with domain name lab.local and configured server as a Domain Controller
4. Renamed server to DC01

## Validation

- IP and DNS Configuration

![image](/screenshots/Server_IP_DNS_setup.png)

---

- Active Directory Domain Services successfully installed

![](/screenshots/Installed_Active_Directory_Domain_Services.png)

---

- Server successfully configured as the DC for lab.local domain and server name changed to DC01

