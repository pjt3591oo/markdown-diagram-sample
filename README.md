[mermaid 공식문서](https://mermaid-js.github.io/mermaid/#/)

* flow

```flow
st=>start: Start
e=>end
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes
or No?:>http://www.google.com
io=>inputoutput: catch something
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
```

* sequence

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

* dot

```dot
digraph G {
    main -> parse -> execute;
    main -> init;
    main -> cleanup;
    execute -> make_string;
    execute -> printf
    init -> make_string;
    main -> printf;
    execute -> compare;
}
```

* mermaid: flowchart

```mermaid
flowchart LR
  A[구매] --> B;
  B[유저, 파라미터, \n 어뷰징 검증] --> C;
  C{client가 안드로이드} -->|Yes| E;
  C -->|No| G;
  E[안드로이드 Proxy 처리] --> G;
  G[DB 저장] --> I;
  I[응답 반환];
```

* mermaid: flowchart

```mermaid
flowchart LR
  A[Service]
  B[(Database_1)]
  C[(Database_2)]
  A-->B
  A-->C
```

* mermaid: graph basic

```mermaid
graph TD
  A --> B;
  A --> node03(C)
  node04(A) --> node05((D))
```

```mermaid
graph LR
  A --> B;
  B --> id03{C}
  B -- from B to C -->
  D --- E
  E -- from E to F --- F
```

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

```mermaid
graph LR
A(입력)-->B[연산]
B-->C(출력)
```

* mermaid: graph

```mermaid
graph TD
A[Christmas] -->|Get money| B(Go shopping)
B --> C{Let me think}
C -->|One| D[Laptop]
C -->|Two| E[iPhone]
C -->|Three| F[fa:fa-car Car]
```

* mermaid: graph

```mermaid
graph LR
A[Hard edge] -->B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

* mermaid: sequence

```mermaid
%% Example of sequence diagram
  sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
    Bob->>Alice: Not so good :(
    else is well
    Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
    Bob->>Alice: Thanks for asking
    end
```


* mermaid: class diagram

```mermaid
classDiagram
  Animal <|-- Duck
  Animal <|-- Fish
  Animal <|-- Zebra
  Animal : +int age
  Animal : +String gender
  Animal: +isMammal()
  Animal: +mate()
  class Duck{
    +String beakColor
    +swim()
    +quack()
  }
  class Fish{
    -int sizeInFeet
    -canEat()
  }
  class Zebra{
    +bool is_wild
    +run()
  }
```


* mermaid: state diagram

```mermaid 
stateDiagram
  [*] --> Still
  Still --> [*]

  Still --> Moving
  Moving --> Still
  Moving --> Crash
  Crash --> [*]
```

* mermaid: pie chart

```mermaid
pie
  title Pie Chart
  "Dogs" : 386
  "Cats" : 85
  "Rats" : 150 
```

* mermaid: gantchart

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2022-02-10

section A section
Completed task            :done,    des1, 2022-02-06,2022-02-08
Active task               :active,  des2, 2022-02-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```
