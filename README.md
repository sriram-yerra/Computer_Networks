### Week-by-Week Learning Plan for Computer Networks

This 24-week plan is designed for your 2 years of industry experience, assuming 5-10 hours/week. It follows the 3-phase structure: **Phase 1 (Weeks 1-4: Fundamentals)**, **Phase 2 (Weeks 5-12: Intermediate Protocols)**, and **Phase 3 (Weeks 13-24: Advanced Applications)**. Each week includes:
- **Focus**: Key topics and goals.
- **Resources**: Targeted readings/videos/labs.
- **Hands-On**: Practical coding or lab tasks (Python-focused for industry standards like RFCs).
- **Time Breakdown**: Suggested allocation (e.g., 3h reading, 4h coding).
- **Check-In**: Quick milestone to track progress.

Set up your environment in Week 1: Install Python, Wireshark, Scapy (`pip install scapy`), Mininet (via Ubuntu VM), and Git for version control. Use a notebook for notes and code repos.

#### Phase 1: Refresh and Core Fundamentals (Weeks 1-4)
Focus on OSI/TCP/IP basics with quick code to solidify packet flow understanding.

| Week | Focus | Resources | Hands-On | Time Breakdown | Check-In |
|------|-------|-----------|----------|----------------|----------|
| **1** | OSI/TCP/IP models; Physical layer (Ethernet basics). Goal: Map layers to real traffic. | - Book: Kurose/Ross Ch. 1 (1h).<br>- Video: NetworkChuck "OSI Model" (20min).<br>- Cisco NetAcad: Intro module (free signup). | - Install tools; capture Ethernet frames in Wireshark (analyze MAC addresses per RFC 894).<br>- Code: Simple Python script to print network interfaces (`socket.getifaddrs()`). | 2h setup/resources, 3h lab/coding. | Wireshark capture of 10+ packets; understand layer encapsulation. |
| **2** | Data Link layer: MAC, VLANs, switches. Goal: Differentiate hub vs. switch behavior. | - Book: Kurose/Ross Ch. 2 (1h).<br>- Coursera Google course: Week 1 quizzes (30min).<br>- GeeksforGeeks: VLAN article. | - Lab: Set up 2 VMs in VirtualBox; ping between them and trace ARP (RFC 826).<br>- Code: ARP spoofing detector sketch with Scapy (sniff ARP packets). | 3h resources, 3h lab, 1h coding. | Diagram a simple LAN; run ARP trace successfully. |
| **3** | Network layer: IP addressing, subnetting, ICMP. Goal: Master CIDR calculations. | - Book: Kurose/Ross Ch. 4 (1h).<br>- Video: NetworkChuck "Subnetting" (30min).<br>- Cisco NetAcad: IP addressing lab. | - Lab: Wireshark ICMP echo (ping) analysis.<br>- Code: IP subnet calculator (use `ipaddress` module; validate per RFC 791). | 2h resources, 4h coding/lab. | Calculate 5 subnets; code handles /24 to /30 masks accurately. |
| **4** | Review Phase 1; intro to sockets. Goal: Send first network message. | - Review notes; Coursera Week 2 (quizzes).<br>- Tanenbaum Ch. 2 summary (30min). | - Code: Basic TCP echo client-server (socket library; localhost test per RFC 793).<br>- Integrate: Add IP validation from Week 3 code. | 2h review, 4h coding, 1h testing. | **Phase Milestone**: Running echo app; analyze its packets in Wireshark. Git commit project. |

#### Phase 2: Intermediate Protocols and Implementation (Weeks 5-12)
Build transport/routing skills with protocol coding; simulate small networks.

| Week | Focus | Resources | Hands-On | Time Breakdown | Check-In |
|------|-------|-----------|----------|----------------|----------|
| **5** | Transport layer: TCP basics, 3-way handshake. Goal: Grasp reliability. | - Book: Kurose/Ross Ch. 3 (1h).<br>- IBM Coursera: Transport module (labs).<br>- Video: NetworkChuck "TCP Handshake". | - Lab: Wireshark TCP capture (trace SYN-ACK).<br>- Code: Extend echo app to handle TCP connections with timeouts (RFC 1122). | 3h resources/lab, 3h coding. | Dissect a full TCP session; code reconnects on failure. |
| **6** | UDP and congestion control. Goal: Compare TCP/UDP trade-offs. | - Book: Kurose/Ross Ch. 3 cont. (1h).<br>- GeeksforGeeks: UDP article.<br>- Cisco CCNA: Transport labs. | - Lab: UDP flood test in Mininet (observe drops).<br>- Code: UDP client-server for unreliable messaging (add basic checksum per RFC 768). | 2h resources, 4h lab/coding. | UDP app sends 100 packets; measure loss rate. |
| **7** | Routing basics: Static routes, OSPF intro. Goal: Understand path selection. | - Book: Tanenbaum Ch. 5 (1h).<br>- Coursera Google: Routing week.<br>- Video: CBT Nuggets OSPF basics (free trial). | - Lab: GNS3 simple router setup (static routes).<br>- Code: Networkx graph for route visualization (simulate OSPF paths per RFC 2328). | 3h resources/lab, 3h coding. | Visualize 3-node network; trace a route. |
| **8** | Advanced IP: NAT, IPv6. Goal: Handle address translation. | - Book: Kurose/Ross Ch. 4 cont. (1h).<br>- Cisco NetAcad: NAT lab.<br>- GeeksforGeeks: IPv6. | - Lab: Mininet NAT simulation.<br>- Code: IPv6 address validator/converter (extend Week 3 script; RFC 8200). | 2h resources, 4h lab/coding. | Convert 5 IPv4 to IPv6; simulate NAT forwarding. |
| **9** | Application layer: DNS, HTTP. Goal: Query real services. | - Book: Kurose/Ross Ch. 2 (app section).<br>- IBM Coursera: App protocols.<br>- Video: NetworkChuck DNS. | - Lab: Wireshark DNS query capture.<br>- Code: Simple DNS resolver with socket (query A records per RFC 1035). | 3h resources/lab, 3h coding. | Resolve 3 domains; parse responses. |
| **10** | SMTP and basic security (ACLs). Goal: Secure simple apps. | - Book: Tanenbaum Ch. 6 (1h).<br>- Coursera: Security intro.<br>- GeeksforGeeks: SMTP. | - Lab: Test email flow in Wireshark.<br>- Code: HTTP client with basic auth (socket; add ACL-like filtering). | 2h resources, 4h coding/lab. | Send HTTP GET with auth; block unauthorized IPs. |
| **11** | Packet analysis deep dive. Goal: Detect protocol issues. | - Review Phase 2; Cisco CCNA routing module.<br>- Video: Wireshark tutorials. | - Code: Scapy packet sniffer (craft/sniff TCP/IP; detect anomalies like odd TTL). | 2h review, 5h coding. | Sniff 50 packets; flag 2+ issues. |
| **12** | Review Phase 2; mini-project. Goal: Integrate protocols. | - Notes review; CompTIA Network+ practice quiz (free online). | - Code: Full chat app (TCP + DNS lookup for peer discovery).<br>- **Phase Milestone**: Test in Mininet; document on GitHub. | 2h review, 4h coding, 1h testing. | App connects 2+ nodes; handles DNS resolution. |

#### Phase 3: Advanced Topics and Industry Applications (Weeks 13-24)
Apply to cloud/automation; build portfolio projects.

| Week | Focus | Resources | Hands-On | Time Breakdown | Check-In |
|------|-------|-----------|----------|----------------|----------|
| **13** | SDN basics, firewalls. Goal: Centralize control. | - Book: "Computer Networking Bible" Ch. on SDN (1h).<br>- AWS free tier: VPC intro.<br>- Video: NetworkChuck SDN. | - Lab: Mininet SDN flow rules.<br>- Code: Basic firewall script (Scapy; drop packets by rules). | 3h resources/lab, 3h coding. | Block 5 packet types; visualize flows. |
| **14** | VPNs and IPsec. Goal: Secure tunnels. | - Coursera: Network Security module.<br>- GeeksforGeeks: IPsec.<br>- Cisco CCNA security labs. | - Lab: OpenVPN setup on VMs.<br>- Code: Simple IPsec-like encryptor (cryptography lib; RFC 4301 basics). | 2h resources, 4h lab/coding. | Encrypt/decrypt sample tunnel traffic. |
| **15** | IDS/IPS intro. Goal: Detect threats. | - Book: Tanenbaum security section.<br>- IBM Coursera: IDS labs.<br>- Video: Snort basics. | - Code: Scapy-based IDS (detect SYN scans; add ML with scikit-learn for patterns). | 3h resources, 4h coding. | Detect simulated scan; alert on 80% accuracy. |
| **16** | Cloud networking: AWS VPCs. Goal: Scale to cloud. | - AWS Certified Networking course (free labs).<br>- Video: AWS VPC tutorial. | - Lab: Create VPC, subnets in AWS free tier.<br>- Code: Boto3 script to automate VPC setup (query resources). | 2h resources, 4h lab/coding. | Deploy VPC with 2 subnets; script provisions it. |
| **17** | IoT protocols: MQTT. Goal: Edge networking. | - Coursera: IoT networking.<br>- GeeksforGeeks: MQTT.<br>- Book: Bible Ch. on emerging tech. | - Lab: Mosquitto broker setup.<br>- Code: MQTT publisher/subscriber (paho-mqtt lib; secure with TLS). | 3h resources/lab, 3h coding. | Publish/subscribe 10 messages securely. |
| **18** | Network automation: Ansible/Netmiko. Goal: Script configs. | - Cisco DevNet: Automation intro.<br>- Video: NetworkChuck Ansible. | - Lab: GNS3 with virtual routers.<br>- Code: Netmiko script for Cisco-like config (backup/restore per industry standards). | 2h resources, 4h lab/coding. | Automate config on 2 devices. |
| **19** | Advanced routing: BGP. Goal: Internet-scale. | - Book: Kurose/Ross Ch. 5.<br>- CCNA BGP module. | - Lab: GNS3 BGP peering.<br>- Code: Networkx BGP path simulator (advertise routes). | 3h resources/lab, 3h coding. | Simulate AS paths for 3 peers. |
| **20** | 5G basics and troubleshooting. Goal: Modern infra. | - GeeksforGeeks: 5G overview.<br>- Video: 5G networking crash course. | - Code: Troubleshooter script (parse Wireshark exports for latency issues). | 2h resources, 4h coding. | Analyze sample trace; identify 3 faults. |
| **21** | Project: VPN + IDS integration. Goal: End-to-end security. | - Review security notes; Reddit r/networking threads. | - Code: Combine Weeks 14-15: VPN tunnel with inline IDS detection. | 1h review, 6h coding/testing. | Secure chat app over VPN; detect breaches. |
| **22** | Project: Automation tool. Goal: Industry-ready script. | - Packet Pushers resources.<br>- AWS labs. | - Code: Netmiko + Boto3 for hybrid cloud-network config (e.g., auto-VPC peering). | 7h coding/lab. | Deploy to AWS; config 3 elements. |
| **23** | Portfolio and cert prep. Goal: Job-ready validation. | - CCNA practice exams (Boson free).<br>- Update GitHub with all projects. | - Refine 2-3 codes; add READMEs with RFC references.<br>- Mock interview: Explain a project. | 3h prep, 3h portfolio, 1h review. | 80% on practice quiz; 5+ repo commits. |
| **24** | Review full plan; next steps. Goal: Sustain learning. | - Full notes scan; LinkedIn networking.<br>- Explore FRR open-source contrib. | - **Final Milestone**: Deploy 1 project to cloud; share on LinkedIn.<br>- Plan: Schedule CCNA exam; join local meetup. | 2h review, 3h deployment, 2h networking. | Portfolio live; 1 cert booked or community post. |

#### Overall Guidance
- **Adaptation**: If a week feels light, add extra coding (e.g., from GitHub's networking-projects repo). Skip reviews if ahead.
- **Tracking**: End each week with a 15-min reflection: What worked? Git commit weekly.
- **Challenges**: For hardware limits, stick to Mininet/AWS. If coding stalls, debug with Stack Overflow.
- **Outcomes**: By Week 24, you'll have 5+ coded projects implementing standards (e.g., TCP/IP, OSPF), a GitHub portfolio, and CCNA readiness—boosting your industry edge.

This granular plan keeps momentum high. Share progress or tweaks for customization!
