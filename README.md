# Bank-Network-System-
Computer Networks Semester Project
Bank Network System - Enterprise Infrastructure Design
This repository contains the complete Cisco Packet Tracer architectural design for a comprehensive bank network system. The project demonstrates advanced networking concepts including VLAN segmentation, Inter-VLAN routing, and high-availability redundancy.

🏗️ Network Architecture
The network is built using a Hierarchical Model distributed across four floors and a dedicated banking zone to ensure efficient traffic management.

📍 Floor Distribution & VLAN Segmentation
The network is segmented into 13 distinct zones to ensure security and reduce broadcast domains:

Floor/Zone | Department / VLAN | IP Subnet (VLSM)
First Floor | Management (10), Research (20), HR (30) | 192.168.10.x/26
Second Floor | Marketing (40), Accounting (50), Finance (60) | 192.168.11.x/26
Third Floor | Logistics (70), Customer Care (80), Guest (90) | 192.168.11.x & 12.x/26
Fourth Floor | Administration (100), ICT (110), Server Room (120) | 192.168.12.x/26
Banking Zone | ATM Network | Dedicated Segment

🏧 ATM Integration
A dedicated ATM Network Segment is connected directly to the core infrastructure to simulate a realistic banking environment.
Hardware: Utilizes a Cisco 2960-24TT switch to interface with the ATM terminal.
Connectivity: Integrated into the "Floor 2" routing hub (Cisco 2911) for centralized transaction monitoring.
Security: The ATM is placed on a dedicated path to isolate sensitive financial traffic from general office data.

🛠️ Core Technologies Used
Inter-VLAN Routing: Configured on Layer 3 Switches (3650 series) to allow communication between departments.
Redundancy: Dual Core/Distribution switches per wing are implemented to prevent Single Points of Failure (SPOF).
Wireless Connectivity: Lightweight Access Points (APs) are integrated into every department for mobile device support.
Infrastructure Services: A dedicated Server Farm hosts HTTPS, Email, and DHCP services.
Point-to-Point Links: High-speed serial and fiber connections utilize /30 subnets (e.g., 10.10.10.24/30) for the backbone.

🚀 Key Features
Scalability: The use of /26 subnetting allows for up to 62 hosts per department, providing room for institutional growth.
Secure Isolation: Financial data (Finance/Accounting/ATM) is logically separated from the Guest Area (VLAN 90) using strict VLAN tagging.
Full Connectivity: Comprehensive routing tables allow seamless communication across all four floors while maintaining security policies.

💻 How to Run
Software: Download and install Cisco Packet Tracer (v8.0 or higher recommended).
Open: Launch the .pkt file included in this repository.
Simulate: Wait for STP convergence (green link lights) and use the "Simple PDU" tool to test connectivity between the ATM and the Server Room.

