## Definition in ordinary category theory ##

+--{.query}

_[[Eric Forgy|Eric]] says_: I took the liberty of creating [[cone]] and placed this material there. Would it make sense to start this page with 

"A **limit** of $F$ is a [[representable|universal]] [[cone]] to $F$..."

?

***

Let $F: J \to C$ be a [[diagram]] in a category $C$. 
We have the following basic definitions: 

1. If $c$ is an object of $C$, a [[cone]] from $c$ to $F$ is a [[natural transformation]] 
$$\gamma: \Delta c \to F$$ 
where $\Delta c$ denotes the composite 
$$J \stackrel{!}{\to} 1 \stackrel{[c]}{\to} C.$$ 
Here $1$ is a [[terminal]] category (exactly one object and exactly one morphism, namely the identity), and $[c]$ denotes the unique morphism from $1$ with object-value $c$. 

In other words, a cone consists of morphisms 

$$\gamma_j: c \to F j,$$

one for each object $j$ of $J$, which are compatible with all the morphisms $F f: F j \to F k$ of the diagram, in the sense that $(F f)\gamma_j = \gamma_k$ for every morphism $f: j \to k$ of $J$. 

It's called a cone because one pictures $c$ as sitting at the vertex, and the diagram itself as forming the base of the cone. 

=--

1. A **limit** of $F$ is a [[representable|universal]] [[cone]] to $F$. In more detail, it is a cone $\theta$ from an object denoted $lim F$ to $F$, such that given any cone $\gamma: \Delta c \to F$, there exists a unique morphism $f: c \to lim F$ such that 
$$\gamma = (\Delta c \stackrel{\Delta f}{\to} \Delta lim F \stackrel{\theta}{\to} F$$ 
(Given $f: c \to d$, $\Delta f: \Delta c \to \Delta d$ is the evident natural transformation whose component at each object $j$ of $J$ is $f: c \to d$.) 

[To be continued...]