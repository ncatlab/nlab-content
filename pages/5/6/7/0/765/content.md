
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Connected filtered spaces
* table of contents
{: toc}

## Definition

A [[filtered space]] $X_*$ is called a **connected filtered space** if it satisfies:  

1. $(\phi)_0$: The function $\pi_0X_0  \to \pi_0X_r$ induced by   inclusion is surjective for all $r \gt 0$; and, 

2. for all $i \geq 1$, $(\phi_i): \pi_i(X_r,X_i,v)=0$  for all $r \gt i$  and $ v \in  X_0$.


Another equivalent form is:

1. $(\phi_0')$: The function $\pi_0X_s  \to \pi_0X_r$ induced by   inclusion is surjective for all $0=s \lt r$ and bijective for all $1 \leq s \leq   r$; and,

2. for all $i \geq 1$, $(\phi_i'): \, \pi_j(X_r,X_i,v)=0$  for all  $v \in X_0$ and all $ j,r$ such that $ 1 \leq j \leq i \lt r$.


## Examples

Examples of connected filtered spaces are:

1. The skeletal filtration of a CW-complex. 

2. The word length filtration of the James construction for a space with base point such that $\{x\} \to X$ is a closed cofibration. 

3. The filtration $(B C)_*$ of the classifying space of a crossed complex, filtered using skeleta of $C$. 

This condition occurs in the [[higher homotopy van Kampen theorem]] for [[crossed complex]]es.


[[!redirects connected filtered space]]
[[!redirects connected filtered spaces]]
