``` mermaid
  Shema IZVORI
graph TD
    A[Izvor Ruda] -->|MM| C[(Vodovod Omiš)]
    B[Zahvat iz HE Kraljevac] -->|MM| C[(Vodovod Omiš)]
    D[Izvor Gojsalić, Jurjević] -->|MM| C 
    E[Zahvat HE Zakučac] -->|MM| C 
    

    style A stroke:#333,stroke-width:4px, stroke-dasharray: 5 5
    style B stroke:#333,stroke-width:4px, stroke-dasharray: 5 5
    style C fill:cyan,stroke:#333,stroke-width:4px, 
    style D stroke:#333,stroke-width:4px, 
    style E stroke:#333,stroke-width:4px, 

    click A callback "Klikni me"
              click B "http://www.edc.hr" "Otvori u novom prozoru" _blank

SHEMA SLIME
              flowchart TD
    
    subgraph Slime
    a0(MM 239 Slime)--> a1[fa:fa-building Slime Čokići]-->a2[\fa:fa-faucet HS Slime /]-->a3[fa:fa-building Slime Tadići]
    end
    subgraph Sodani
    b1[fa:fa-building Šodani]
    end
    subgraph Makarska
    c1[(Vodovod Makarska)]
    end
    Makarska -->Slime 
    Makarska -->|MM| Sodani

    Shema zagrad
    flowchart TD
               A[(fa:fa-hand-holding-water Uređaj zagrad  )] --> |0.6 l/s| P1[/fa:fa-pump CS Zagrad Gaj \] --> V1[\fa:fa-faucet VS Gaj /]
                A[(fa:fa-hand-holding-water Uređaj zagrad  )] --> |1.2 l/s| P2[/fa:fa-pump CS Zagrad Sučica \]--> V2[\fa:fa-faucet VS Sučica /]
            
            V2 -->|TH - AD Naklice| N1[fa:fa-building Naklice]
                subgraph Tugare_istok
                    P3[/fa:fa-pump HS Dočine \] --> N2[fa:fa-building Tugare istok]
                end
            
            V2 --> Tugare_istok

            V2 -->|TH - B6 Tugare zapad| N3[fa:fa-building Tugare zapad]
            
            

                subgraph Gata
                    G[fa:fa-building Gata]
                end
                subgraph Podcelje
                    PC[fa:fa-building Podcelje]
                end
                subgraph Cisla
                    CS[fa:fa-building Čišla]
                end
                subgraph Ostrvica_donja
                    OD[fa:fa-building Ostrvica donja]
                end
                subgraph Ostrvica_gornja
                    OG[fa:fa-building Ostrvica gornja]
                end
                subgraph Zvečanje
                    ZV[fa:fa-building Zvečanje]
                end
                subgraph Smolonje
                    SM[fa:fa-building Smolonje]
                end
                 
            V1 -->Gata
            V1 -->Podcelje
            V1 -->|TH-AD Naklice| P4[/fa:fa-pump HS Kuvačiči \]-->KU[fa:fa-building Kuvačići]
            V1 -->Cisla
            Cisla -->|MM 228, TH-BB|Ostrvica_donja
            Cisla -->PK[\fa:fa-faucet PK Čišla /]
            PK -->Ostrvica_gornja-->|TH-A9|Zvečanje-->|TH-A5|Smolonje
            
           

            A-->Spoj[ ]-->VS_Stomarica[\fa:fa-faucet VS Stomarica /]
            Spoj-->Otoci[Brač, Hvar, Šolta]
            VS_Stomarica -->Zakucac
                subgraph Zakucac
                   ZK[fa:fa-building Zakučac] 
                end
            VS_Stomarica --> PK_Priko[\fa:fa-faucet PK Priko /]
            VS_Stomarica --> Omis_zapad 
                subgraph Omis_zapad
                 OZ[fa:fa-building Omiš zapad] 
                end
            VS_Stomarica --> Duce 
                subgraph Duce
                 DU[fa:fa-building Duće] 
                end
            VS_Stomarica --> VS_Dugi_Rat[\fa:fa-faucet VS Dugi Rat /]
            PK_Priko --> VS_Dugi_Rat[\fa:fa-faucet VS Dugi Rat /]

            
                subgraph Dugi_rat_istok
                    DRI[fa:fa-building Dugi Rat istok] 
                end
                subgraph Dugi_rat_centar
                    DRC[fa:fa-building Dugi Rat centar] 
                end
                subgraph Dugi_rat_zapad
                    DRZ[fa:fa-building Dugi Rat zapad] 
                end
                subgraph Jesenice_istok
                    JI[fa:fa-building Jesenice istok] 
                end
                subgraph Jesenice_centar
                    JC[fa:fa-building Jesenice centar] 
                end
                subgraph Jesenice_zapad
                    JZ[fa:fa-building Jesenice zapad] 
                end
            VS_Dugi_Rat -->Dugi_rat_istok
            Dugi_rat_istok-->Dugi_rat_centar-->Dugi_rat_zapad-->Jesenice_istok-->Jesenice_centar-->Jesenice_zapad
            
            VS_Stomarica-->|MM 37 Punta 3, MM 237 Punta 1, MM226 Punta 2|Omis_Punta
                subgraph Omis_Punta
                    OP[fa:fa-building Omiš Punta] 
                end
            VS_Stomarica-->Omis_stari_grad
                subgraph Omis_stari_grad
                    OSG[fa:fa-building Omiš Stari grad] 
                end

            VS_Stomarica -->VS_Borak[\fa:fa-faucet VS Borak /]
            VS_Borak-->Omis_istok
            subgraph Omis_istok
            OI[fa:fa-building Omiš istok] 
            VS_Mlija[\fa:fa-faucet VS Mlija /]
                end
            VS_Borak-->VS_Pesici[\fa:fa-faucet VS/CS Pešići /]
            VS_Pesici-->VS_Cecuci[\fa:fa-faucet VS Čečuci /]






              click A callback "Klikni me"
              click 1 "http://www.github.com" "Otvori u novom prozoru" _blank
        
              style V1 fill:cyan,stroke:#333,stroke-width:3px
              style V2 fill:cyan,stroke:#333,stroke-width:3px
              style P1 fill:lightgreen,stroke:#333,stroke-width:3px
              style P2 fill:lightgreen,stroke:#333,stroke-width:3px
              style P3 fill:lightgreen,stroke:#333,stroke-width:3px
              style Tugare_istok fill:lightblue, stroke:blue, stroke-widt:3px
    

    
    
    
    
    
    
            
            
```
