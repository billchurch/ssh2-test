# Malformed packets in wireshark dissector when using SSH2 as a client
mscdex/ssh2 v0.8.9
node v14.17.0
client (node host) macOS 10.15.7 (19H1030) OpenSSH_8.1p1, LibreSSL 2.7.3
server (Ubuntu 14.04.5 LTS x86_64) OpenSSH_6.6.1p1 Ubuntu-2ubuntu2.10, OpenSSL 1.0.1f 
wireshark Version 3.0.2 (v3.0.2-0-g621ed351d5c9) 

When using ssh2 as a client, wireshark reports malformed packets after key exchange complete in the first encrypted data packet. In the example `malformed_packets.pcapng` line 19 shows the example.

And example of the same session using the macOS client (OpenSSH_8.1p1, LibreSSL 2.7.3) and executing the same command does NOT result in these malformed packets (again line 19 in `normal_packets.pcapng`)

In both cases, the wireshark element is running on the macOS client/node server and the Ubuntu server is running on a seperate VM host outside of this environment.
