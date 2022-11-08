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
    id1["Это текст (а вот это могло сломать рендеринг), но у нас есть экранирование"]  
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
## Под блок-схемы
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
## test  
```mermaid
flowchart TB
node8{какое-то условие}--> id1["чуть более длинный текст"] & id2["ну типа тут тоже длинно"]--> id3["типа получилось"]
```
