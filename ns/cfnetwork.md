[edit in github](https://github.com/christrees/cf.christrees.com/edit/main/ns/cfnetwork.md)  - or render -  [view in github](https://github.com/christrees/cf.christrees.com/blob/main/ns/cfnetwork.md)

``` mermaid
graph LR


subgraph cf Network
    Internet --> cfRouter
    style cfRouter fill:#000,stroke:#000,stroke-width:2px
    
    subgraph DMZ Subnet
        cfRouter --192.168.6.0/24--> DMZ-Switch
        style DMZ-Switch fill:#000,stroke:#000,stroke-width:2px
        DMZ-Switch --> DMZ-Device1
        style DMZ-Device1 fill:#000,stroke:#000,stroke-width:2px
    end

DMZ-Switch --192.168.6.180--> cattvwin10
SaaA-Switch --192.168.2.180--> cattvwin10
gh.lan-Switch --192.168.252.180--> cattvwin10

subgraph cf subnets
    DMZ-Switch --192.168.6.100--> saRouter
    DMZ-Switch --192.168.6.101--> ghRouter
    
    subgraph SaaA Subnet
        saRouter --192.168.2.0/24--> SaaA-Switch
        style SaaA-Switch fill:#000,stroke:#000,stroke-width:2px
        style SaaA-Device1 fill:#000,stroke:#000,stroke-width:2px
        style SaaA-Device2 fill:#000,stroke:#000,stroke-width:2px
        SaaA-Switch --> SaaA-Device1
        SaaA-Switch --> SaaA-Device2
        SaaA-Switch --> docker
        
        subgraph docker
            dockerSwitch --> SaaA-Device3
            dockerSwitch --> SaaA-Device4
            dockerSwitch --> SaaA-Device5
            dockerSwitch --> SaaA-Device6
            dockerSwitch --> SaaA-Device7
            dockerSwitch --> SaaA-Device8
        end
    end
    
    subgraph gh.lan Subnet
        ghRouter --192.168.252.0/23--> gh.lan-Switch
        style gh.lan-Switch fill:#000,stroke:#000,stroke-width:2px
        gh.lan-Switch --> gh.lan-Device1
        gh.lan-Switch --> gh.lan-Device2
        style gh.lan-Device1 fill:#000,stroke:#000,stroke-width:2px
        style gh.lan-Device2 fill:#000,stroke:#000,stroke-width:2px
    end
end

end
```
