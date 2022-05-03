* Ubuntu as router
  * virtualBox setup
  * Add two NAT Network: NATNetwork1 (10.0.2.0/24) and NATNetwork2 (10.0.3.0/24)
  * Create VM.
    * node1: 10.0.2.4 NIC on NATNetwork1
    * node2: 10.0.3.4 NIC on NATNetwork2
    * node3: 10.0.3.5 NIC on NATNetwork2,  10.0.2.5 NIC on NATNetwork1
    * Goal is, on node 2 start udp server 'nc -u -l 5333'; Then on node 1, 'nc -u 10.0.3.4 533' can send udp request to node2.
  * configure route node3, following https://askubuntu.com/questions/1050816/ubuntu-18-04-as-a-router can complete it.
  * then on node 1, 'ip add route add 10.0.3.0/23 via 10.0.2.5'
  * Similarly, you have to config node2, you can then access (TCP/UDP) to node 1 from node 2. 
