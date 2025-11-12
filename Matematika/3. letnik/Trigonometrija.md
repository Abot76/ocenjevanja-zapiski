# OSNOVNI POJMI O KOTNIH FUNKCIJAH

```latex
\begin{tikzpicture}
\coordinate [label=left:{$B$}] (B) at (0,0);
\coordinate [label=right:{$C$}] (C) at (4,0);
\coordinate [label=above:{$A$}] (A) at (0,3);

\draw (A) -- node[left] {$c$} (B) -- node[below] {$a$} (C) -- node[above right] {$b$} (A);

\draw (0,0) rectangle (0.3,0.3);
\end{tikzpicture}
```

```mermaid
graph TD
    A[A] -->|c| B[B]
    B -->|a| C[C]
    C -->|b| A
```


```mermaid
flowchart TD
    A[A] -- c --> B[B]
    B -- a --> C[C]
    C -- b --> A
    
    linkStyle 0 stroke:#000, stroke-width:2px
    linkStyle 1 stroke:#000, stroke-width:2px  
    linkStyle 2 stroke:#000, stroke-width:2px
```

