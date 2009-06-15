A computad is a formal device (due to [[Ross Street]]) for describing "generators" of $n$-categories, much as directed graphs describe generators of 1-categories. Originally the $n$-categories under consideration were strict, but more recently the concept of $n$-computad has been expanded to take into account weak $n$-categories (in an algebraic, not geometric sense). 

## Definitions ##

First we work in Street's original strict setting. 

An **n-computad** is defined recursively as follows: 

1. A 0-computad is a set; 

1. The data of an $n$-computad consists of an $(n-1)$-computad $\mathcal{C}$, a set $C_n$, and source and target maps 
$$s, t: C_n \overset{\to}{\to} F_{n-1}(\mathcal{C})_{n-1}$$ 
where $F_{n-1}: (n-1)Comp \to (n-1)Cat$ is the "free $(n-1)$-category on an $(n-1)$-computad", and $D_j$ denotes the set of $j$-cells in a higher-dimensional category $D$. 

1. The data must satisfy globularity conditions: for all $c \in C_n$, the $(n-1)$-cells $s(c)$ and $t(c)$ must share the same source and the same target (as elements in $F_{n-1}(\mathcal{C})_{n-2}$). 

To complete the induction, we need to define $F_n$. Roughly speaking, in dimensions $j \lt n$, the structure agrees with that of $F_{n-1}(\mathcal{C})$. In dimension $n$, the $n$-cells are formal pasting diagrams built from the elements of $C_n$ by formal whiskerings and formal compositions across $(n-1)$-cells in $F_{n-1}(\mathcal{C})$. 

(Much detail to be filled in...) 
