``` mermaid
        %%{init: {'securityLevel': 'loose', 'theme':'base'}}%%
        flowchart LR
               A[(fa:fa-hand-holding-water Uređaj zagrad  )] --> |0.6 l/s| B[\fa:fa-faucet VS Gaj /]
                A[(fa:fa-hand-holding-water Uređaj zagrad  )] --> |1.2 l/s| C{{fa:fa-building CS Sučica}}
              B --- |0.6l/s| D[/fa:fa-building naselje Gaj/]
            
              click A callback "Klikni me"
              click B "http://www.github.com" "Otvori u novom prozoru" _blank
        
              style B fill:cyan,stroke:#333,stroke-width:3px
```
