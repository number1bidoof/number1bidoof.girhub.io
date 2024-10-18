``` mermaid
sequenceDiagram
    actor Attacker
    participant Botnet
    actor targetServer

    Attacker->>Botnet: Command to attack
    botnet->>targetServer: Send request 1
    botnet->>targetServer: Send request 2
    botnet->>targetServer: Send request 3
    botnet->>targetServer: Send request 4
    targetServer-->>Botnet: Response (ignored)
    targetserver->>targetServer: Overload with requests
    targetServer-->>Attacker: Unable to respond (denied services)
    
 ```
 This sequence diagram is a demonstration of a typical DDOS attack, where the attacker lauches an attack by using a Botnet, then the botnet sends in several acess request, the overwhemed target is now overfilled with requests and denies services to the users due to sheer amount of requests made by the botnet