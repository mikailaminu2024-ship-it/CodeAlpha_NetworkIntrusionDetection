# CodeAlpha_NetworkIntrusionDetection
Basic Network Detection System build with suricata for codealpha Cybersecurity Internship
# Network Intrusion Detection System 
Basic NIDS set up using suricata, developed as task 4 for the code alpha cybersecurity internship 
## What was done 
-Installed and configure suricata on kali linux 
-Initially tested in an isolated virtual box NAT network 
-switched to bridged networking to monitor real home network traffic 
-loaded the defaulted emerging threats ruleset (440=rules)
-wrote a custom detection rule to alert on ICMP traffic 
-verified live alert generation and logging via'fast.log'

## Custom rule
alert icmp any any -> any any (msg:"ICMP Ping Detected -custom Test";sid:1000001;rev:1;)

##Results
-successfully detected and logged ICMP traffic to/from a real netowrk IP(10.10.37.166)
-Suricata's default ruleset also originally detected a protocol anomaly ("Ethotype unkonwn")from background network traffic,without any manual trigger - demonstrating the IDS actively catching unusual patterns in real time
