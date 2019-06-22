```mermaid
graph LR
2AG[2-arachidonylglycerol]
ARA[Arachidonic acid]
GLx[Glutamate]
ADORA2A


Ca[Calcium]

Ca --> NAPELD
Ca --> DAGLA
Ca --> DAGLB
ARA  --- 2AGBLK

subgraph 
 DAGLA
 DAGLA --> 2AGBLK
 DAGLB --> 2AGBLK
end 

THCOH[11-OH-THC]-->CNR1
THCOH-->THCOOHBLK
THCOHBLK(( ))
THCOOHBLK(( ))
CYP2C9---THCOHBLK
CYP2C9---THCOOHBLK
THCOOHBLK---THCOOH
THC-->THCOHBLK
THCOHBLK---THCOH

subgraph inactivated
THCOOH
end
NAPEBLK(( ))
NAPE --> NAPEBLK 
NAPEBLK--> AEA
NAPELD---NAPEBLK

subgraph CBD
CBD -->CNR2
CBD -->CNR1
CBD --> ADORA2A
end

ADORA2A --- AIP{Anti-Inflammantory pathways}

subgraph THC
    THC -->CNR1
end 
AEA --> CNR1
2AGBLK --> 2AG
2AGBLK(( ))
subgraph ECB
    2AG
    AEA
end

subgraph CNR1 - hyppocampus, cerrebellum, basal ganglia
 MAPK -.- MAPK1
   cAMPBLK(( ))
   ADCY1---cAMPBLK
   subgraph relevant
    MAPK1
    MAPK3
    MAPK8
    MAPK9
  end 
 CNR1-- "||||" ---GLx
 CNR1-- "||||" ---GABA
 CNR1-- "||||" ---ADCY1
 CNR1 --> MAPK
    subgraph 
         ATP1[ATP]-->cAMPBLK
        cAMPBLK---cAMP1[cAMP]
    end 
end

subgraph CNR2 - Leukocyte - bone tissue
 CNR2 --> ADCY7
    subgraph 
         ATP2[ATP]-->cAMP2[cAMP]
    end 
end

subgraph cAMP
    PKA-.-PRKAR1A
    cAMP1 --- PKA
    cAMP2 --- PKA
    subgraph relevant
         PRKAR1A
         PRKAR1B
         PRKAR2A
         PRKAR2B
         PRKACA
         PRKACB
         PRKACG 
    end 
end 

2AG --> CNR1
PE[Phosphatidylethanolamine]
PE-->NAPE

linkStyle default interpolate base
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzI0NTQ1MDQ2XX0=
-->