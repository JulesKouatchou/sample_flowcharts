# Sample Flowcharts with  `mermaid`

#### Example

```mermaid
%%{ init: {'flowchart': { 'curve': 'stepAfter' } } }%%

flowchart LR
    O[ ]:::empty
    A(A):::c1
    B(B):::c1
    C(C):::c1
    AB([A->B]):::c2
    AC([A->C]):::c2

    classDef c1 width:60px,fill:#f16,font-size:15px  
    classDef c2 fill:#f96    
    classDef empty width:0px,height:0px
    
    A --- O
    O --> AB 
    O --> AC
    AB --> B
    AC --> C
```

#### Example

```mermaid
flowchart LR
    A("A::run"):::c1
    B("B: T=T+delta"):::c1
    AB([A->B]):::c2
    BA([B->A]):::c2
    
    classDef c1 width:100px,fill:#f16,font-size:15px 
    classDef c2 fill:#f96

    A ~~~ AB
    AB ~~~ B
    B ~~~ BA
```

#### Example

```mermaid
%%{ init: {'flowchart': { 'curve': 'stepAfter' } } }%%

flowchart TB
    %% This is a test
    P[Parent]:::c1
    O[ ]:::empty
    A(A):::c1
    B(B):::c1
    C(C):::c1
    AB([A->B]):::c2
    AC(["A->C"]):::c2
    BA(["B->A"]):::c2
    BC(["B->C"]):::c2
    CA(["C->A"]):::c2 
    CB(["C->B"]):::c2
    
    classDef c1 width:60px,fill:#f16,font-size:15px,font-weight:bold
    classDef c2 fill:#f96
    classDef empty width:0px,height:0px

    P --- O
    O --> A
    O --> B 
    O --> C
    A --> AB
    A --> AC
    B --> BA
    B --> BC
    C --> CA
    C --> CB
```
