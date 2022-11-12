 # mermaid  
 ## Формы:
  
 ```mermaid
flowchart TB
  node1[Форма 1]  
  node2(Форма 2)
  node3([Форма 3])
  node4[[Форма 4]]
  node5[(Форма 5)]
  node6((Форма 6))
  node7>Форма 7]
  node8{Форма 8}
  node9{{Форма 9}}
  node10[/Форма 10/]
  node11[\Форма 11\]
  node12[/Форма 12\]
  node13[\Форма 13/]
```
## Размещение текста:  

```mermaid
flowchart LR
    id1["Это текст, он в кавычках, чтобы ничего не сломалось (★‿★) "]  
```
## Ориентация:  
```    
    TB - top to bottom
    TD - top-down/ same as top to bottom
    BT - bottom to top
    RL - right to left
    LR - left to right
```

## Узлы:  

```mermaid
flowchart TB
    А --> B
    C --- D
    E -.-> F
    G ==> H
    I --o J
    K --x L
```
## Текст на стрелочке:  

```mermaid
flowchart TD
    A-- Text ---B
    C---|Text|D 
    E-->|text|F 
    G-- text -->H 
    I-. text .-> J 
    K == text ==> L
```
## Cоединения:  
```mermaid
flowchart LR
   A -- text --> B -- text2 --> C
```
## Cоединения 2:  
```mermaid
flowchart LR
   a --> b & c--> d
```
## Cоединения 3:  
```mermaid
flowchart TB
    A & B--> C & D
```
## Cоединения 3(альтернативная запись):  
```mermaid
flowchart TB
    A --> C
    A --> D
    B --> C
    B --> D
```
## Подблок-схемы:
```mermaid
flowchart TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
```
## Подблок-схемы 2:  
```mermaid
flowchart TB
    c1-->a2
    subgraph ide1 [one]
    a1-->a2
    end
```
## Подблок-схемы 3:  
```mermaid
flowchart TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
    one --> two
    three --> two
    two --> c2
```
## Условие  
```mermaid  
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```
## Условие + цвета   
Используем цвета HTML  
P.S. подходит как имя цвета так и шестнадцатеричное представление цвета в RGB
```mermaid
flowchart TB
    style b color:SpringGreen,stroke:MediumSpringGreen,stroke-width:4px
    style i1 fill:#483D8B,stroke:#4B0082,stroke-width:4px
    style i2 fill:#BA55D3,stroke:DarkMagenta,stroke-width:4px,color:#FFFFFF
    style i3 fill:#008080,stroke:#00CED1,stroke-width:4px,stroke-dasharray: 12 5
    style f  fill:#FA8072,stroke:#DC143C,stroke-width:4px,color:#DC143C,stroke-dasharray: 12 5
    b{бирюзовое условие}
    a(["обычное начало"])-->b
    b--> |yes|i1["текст в фиолетовом"]--> i3["текст в голубом + пунктир"]
    b--> |no|i2["текст в розовом"]--> i3
    i3-->f(["прикольный конец"])
```  
    fill — заливка;

    stroke — цвет границы;

    stroke-width — толщина границы;

    color — цвет текста;

    stroke-dasharray — пунктирная граница.

