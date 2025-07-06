![image](https://github.com/user-attachments/assets/98a3bd50-d7dd-46f6-8e76-ee10fe49959e)## Initial AD Attack Vectors
* Usually we place ourselves within the internal network leveraging a remote device (such as a laptop or a Raspberry Pi) with a VPN connection that phones home. We share the tunnel to run these attacks remotely while also being internal to client network.

### LLMNR Poisoning (Link Local Multicast Name Resolution)
* Used to identify hosts when DNS fails to do so in the network
* Used to be known as NBT-NS, but it has been upgraded to LLMNR. In older networks, you may still see NBT-NS.
* Key flaw is that services utilize a user's username and NTLMv2 hash when appropriately responded to (man-in-the-middle)
![image](https://github.com/user-attachments/assets/fb8de3c8-4268-42e0-8c57-d1743c5eb31a)
* If we as men in the middle can intercept the request asking where a resource exists, we can respond and ask for a victim's hash to "connect them" to the share. If hash is weak enough, we can crack it!
1. Run Responder: `sudo responder -I tun0 -dwP`
   * I is interface (VPN is tun0, network is eth0)
   * It's going to respond to traffic! Share folder is one example, requests fly across network if LLMNR is enabled. Best time to run it is morning and after lunch. 
2.  An event occurs...such as attempting to navigate to a non-existent network share


