``` mermaid
graph LR

subgraph cf Network
    Internet --> cfRouter
    style cfRouter fill:#fff,stroke:#000,stroke-width:2px
    
    subgraph DMZ Subnet
        cfRouter --192.168.6.0/24--> DMZ-Switch
        style DMZ-Switch fill:#fff,stroke:#000,stroke-width:2px
        DMZ-Switch --> DMZ-Device1
        style DMZ-Device1 fill:#fff,stroke:#000,stroke-width:2px
    end

subgraph cf subnets
    DMZ-Switch --192.168.6.100--> saRouter
    DMZ-Switch --192.168.6.101--> ghRouter
    
    subgraph SaaA Subnet
        saRouter --192.168.2.0/24--> SaaA-Switch
        style SaaA-Switch fill:#fff,stroke:#000,stroke-width:2px
        SaaA-Switch --> SaaA-Device1
        SaaA-Switch --> SaaA-Device2
        style SaaA-Device1 fill:#fff,stroke:#000,stroke-width:2px
        style SaaA-Device2 fill:#fff,stroke:#000,stroke-width:2px
    end
    
    subgraph gh.lan Subnet
        ghRouter --192.168.252.0/23--> gh.lan-Switch
        style gh.lan-Switch fill:#fff,stroke:#000,stroke-width:2px
        gh.lan-Switch --> gh.lan-Device1
        gh.lan-Switch --> gh.lan-Device2
        style gh.lan-Device1 fill:#fff,stroke:#000,stroke-width:2px
        style gh.lan-Device2 fill:#fff,stroke:#000,stroke-width:2px
    end
end

end
```
