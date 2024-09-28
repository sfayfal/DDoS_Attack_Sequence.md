# DDoS_Attack_Sequence.md

 
```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker->>BotNet: Command to initiate attack
    BotNet->>WebServer: Send flood of requests
    WebServer-->>Firewall: Alert on unusual traffic
    Firewall->>WebServer: Analyze traffic patterns
    Firewall-->>BotNet: Block malicious IPs
    WebServer-->>Firewall: Report denial of service
    Firewall->>WebServer: Continue monitoring traffic

#### Sequence Diagram Description

1. **Attacker commands BotNet**: The attacker sends a command to the botnet, instructing it to start the DDoS attack on the targeted web server.

2. **BotNet sends flood of requests**: The compromised bots in the botnet begin sending a massive volume of requests to the web server, overwhelming its resources.

3. **WebServer alerts Firewall**: The web server detects an unusual spike in traffic and alerts the firewall to potential malicious activity.

4. **Firewall analyzes traffic patterns**: The firewall begins to analyze the incoming traffic patterns to identify and differentiate between legitimate users and attack traffic.

5. **Firewall blocks malicious IPs**: Based on its analysis, the firewall takes action to block the IP addresses identified as part of the attack.

6. **WebServer reports denial of service**: The web server communicates back to the firewall about the ongoing denial of service, confirming that legitimate users are being affected.

7. **Firewall continues monitoring traffic**: The firewall remains active, continuing to monitor the traffic to ensure that further attacks are mitigated and that legitimate traffic can pass through.
