+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The underlying higher [[directed graph]] of an [[(n,r)-category|$(n, r)$-category]]. 

## Definition 

### Directed (n,r)-pseudographs

For finite $r$, directed $(n,r)$-pseudographs are defined inductively as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, a **directed $(n,0)$-pseudograph** is an [[∞-groupoid]] that is [[n-truncated]]: an [[n-groupoid]]. 

For $0 \leq r \lt \infty$, a **directed $(n+1,r+1)$-pseudograph** is an (n+1)-groupoid $G$ such that for every object $A$ and $B$,  called a **vertex**, in $G$, there is a directed $(n,r)$-pseudograph of **edges** $Edge(A, B)$ between $A$ and $B$. 

where $\infty + 1 = \infty$
=--

For the case $r = \infty$, directed $(n, \infty)$-pseudographs are [[coinductive definition|defined coinductively]] as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, a **directed $(n,\infty)$-pseudograph** is an [[n-groupoid]] $G$ such that for every object $A$ and $B$, called a **vertex**, in $G$, there is a directed $(n,\infty)$-pseudograph of **edges** $Edge(A, B)$ between $A$ and $B$. 
=--

### Directed (n,r)-multigraphs

For finite $r$, directed $(n,r)$-multigraphs are defined inductively as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, a **directed $(n,0)$-multigraph** is an [[∞-groupoid]] that is [[n-truncated]]: an [[n-groupoid]]. 

For $0 \leq r \lt \infty$, a **directed $(n+1,r+1)$-multigraph** is an (n+1)-groupoid $G$ such that for every object $A$ and $B$,  called a **vertex**, in $G$, there is a directed $(n,r)$-multigraph of **edges** $Edge(A, B)$ between $A$ and $B$ such that given any vertex $A$, $Edge(A, A)$ is equivalent to the empty $\infty$-groupoid. 

where $\infty + 1 = \infty$
=--

For the case $r = \infty$, directed $(n, \infty)$-multigraphs are [[coinductive definition|defined coinductively]] as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, a **directed $(n,\infty)$-multigraph** is an [[n-groupoid]] $G$ such that for every object $A$ and $B$, called a **vertex**, in $G$, there is a directed $(n,\infty)$-multigraph of **edges** $Edge(A, B)$ between $A$ and $B$ such that given any vertex $A$, $Edge(A, A)$ is equivalent to the empty $\infty$-groupoid.
=--

### Note on terminology

Some authors use "directed (n,r)-graph" to mean what we refer here as a "directed (n,r)-pseudograph". 

## The periodic table 

### Directed $(n,r)$-pseudographs

There is a [[periodic table]] of directed $(n,r)$-pseudographs:
<table><tr><th markdown="1">$r$&#8595;\$n$&#8594;</th><th markdown="1">$-2$</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">...</th><th markdown="1">$\infty$</th></tr>
<tr><th markdown="1">$0$</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[groupoid]]</td><td>[[2-groupoid]]</td><td>...</td><td>[[infinity groupoid]]</td></tr>
<tr><th markdown="1">$1$</th><td>"</td><td>"</td><td>[[directed loop graph]]</td><td>[[directed pseudograph]]</td><td>directed (2,1)-pseudograph</td><td>...</td><td>directed (infinity,1)-pseudograph</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>"</td><td>"</td><td>directed loop 2-graph</td><td>directed (2,2)-pseudograph</td><td>...</td><td>directed (infinity,2)-pseudograph</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>directed loop 3-graph</td><td>...</td><td>directed (infinity,3)-pseudograph</td></tr>
<tr><th markdown="1">&#8942;</th><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8945;</td><td>&#8942;</td></tr>
<tr><th markdown="1">$\infty$</th><td>trivial</td><td>truth value</td><td>directed loop graph</td><td>directed loop 2-graph</td><td>directed loop 3-graph</td><td>...</td><td>directed loop infinity-graph</td></tr>
</table>

### Directed $(n,r)$-multigraphs

There is a [[periodic table]] of directed $(n,r)$-multigraphs:
<table><tr><th markdown="1">$r$&#8595;\$n$&#8594;</th><th markdown="1">$-2$</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">...</th><th markdown="1">$\infty$</th></tr>
<tr><th markdown="1">$0$</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[groupoid]]</td><td>[[2-groupoid]]</td><td>...</td><td>[[infinity groupoid]]</td></tr>
<tr><th markdown="1">$1$</th><td>"</td><td>"</td><td>[[directed graph]]</td><td>[[directed multigraph]]</td><td>directed (2,1)-multigraph</td><td>...</td><td>directed (infinity,1)-multigraph</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>"</td><td>"</td><td>directed 2-graph</td><td>directed 2-multigraph</td><td>...</td><td>directed (infinity,2)-multigraph</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>directed 3-graph</td><td>...</td><td>directed (infinity,3)-multigraph</td></tr>
<tr><th markdown="1">&#8942;</th><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8942;</td><td>&#8945;</td><td>&#8942;</td></tr>
<tr><th markdown="1">$\infty$</th><td>trivial</td><td>truth value</td><td>directed graph</td><td>directed 2-graph</td><td>directed 3-graph</td><td>...</td><td>directed infinity-graph</td></tr>
</table>

## See also 

* [[directed pseudograph]]

* [[pseudograph]]

* [[n-graph]]

* [[(n,r)-category]]

* [[coinduction]]

[[!redirects directed (n,r)-graphs]]
[[!redirects directed (n,r)-multigraph]]
[[!redirects directed (n,r)-multigraphs]]
[[!redirects directed (n,r)-pseudograph]]
[[!redirects directed (n,r)-pseudographs]]