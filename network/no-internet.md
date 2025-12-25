# Usuario sin acceso a Internet

## Symptoms
One or more users report that they are unable to browse the Internet.
Devices are powered on and appear to be correctly connected to the network, either via Wi-Fi or Ethernet.

## Possible Causes
- Local connectivity issue: unplugged cables, disabled Wi-Fi, faulty network hardware.
- Incorrect IP configuration: invalid IP address, IP conflict, wrong subnet mask, or no DHCP response.
- DNS failure: the system cannot resolve domain names into IP addresses.
- Router or gateway issue: the router does not respond to outbound Internet requests.

## Diagnosis - OSI Model Based
Layer 1 (Physical) - Physical media failure, damaged cable, disabled network adapter, or weak/no Wi-Fi signal.
Layer 3 (Network) - Addressing issue: the device has an APIPA address (169.254.x.x) or an IP conflict caused by static configuration.
Layer 3 (Network) - Gateway failure: the device has a valid IP address, but the default gateway (router) is unreachable or misconfigured.
Layer 7 (Application) - DNS resolution failure: network connectivity is available, but domain names cannot be resolved.

## Solution
1. Verify the physical layer: check cable connections, Wi-Fi status, and network interface state.
2. Validate IP configuration: ensure the device has a valid IP address, subnet mask, and gateway.
3. Test local connectivity, ping the default gateway, ping the router ip, if the ping fails, the issue is within the local network or the router.
4. Test external connectivity, ping the public IP, if the ping succedes but browing fails, the issue is likely DNS-related.
5. Perfom a DNS test, run nslookup on a domain name, if no IP is returned, the configured DNS server may be down or incorrect.

## Prevention
- Use a basic connectivity checklist and verify whether other devices on the same network are affected.
- Document the correct network configuration and record the solution for future similar incidents.
- Educate users on basic troubleshooting steps and ensure router firmware and network drivers are kept up to date.
