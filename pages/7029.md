

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An [[action]]

$$
  (-)\cdot(-) \;\colon\; G \times X \to X
$$

of a [[group]] $G$ on a [[set]] $X$ is called _free_ if for every $x \in X$,  the [[equation]] $g \cdot x = x$ [[implication|implies]] $g = e_G$ (the [[neutral element]]), hence if only the action of the [[neutral element]] has [[fixed points]].

Equivalently, an action is free if and only if for any [[pair]] of elements $x,y \in X$, there is _at most one_ group element $g \in G$ such that $g \cdot x = y$. 

In more abstract terms this says that the action is free if and only if its [[shear map]] 

$$
  \array{
    G \times X
    &
    \overset
      { (pr_2, \cdot) }
      {\longrightarrow}&
    X \times X
    \\
    (g, x) 
    &
    \mapsto
    & 
    \big( x, g \cdot x \big)
    \,.
  }
$$

is a [[monomorphism]]. In this form the definition makes sense for [[action objects]] [[internalization|internal]] to any ambient [[category]] (with [[finite products]]).



\begin{remark}
Beware the similarity to and difference of free actions with [[effective group action|effective action]]: a free action is effective, but an effective action need not be free.
\end{remark}

\begin{remark}
A free action that is also [[transitive action|transitive]] is called _[[regular action|regular]]_.
\end{remark}

## Examples

* Any group $G$ acts freely on itself by multiplication $\cdot : G \times G \to G$, which is called the (left) [[regular representation]] of $G$.

* An action of $\mathbb{Z}/2\mathbb{Z}$ on a set $X$ corresponds to an arbitrary [[involution]] $i : X \to X$, but the action is free just in case $i$ is a _[[fixed point]]-free_ involution.

* For any set $X$ equipped with a [[transitive action]] $* : G \times X \to X$, the group $Aut_G(X)$ of $G$-equivariant automorphisms of $X$ (i.e., [[bijections]] $\phi : X \to X$ commuting with the action of $G$) acts freely on $X$.  In particular, suppose $\phi \in Aut_G(X)$ is such that $\phi(x) = x$ for some $x\in X$, and let $y\in X$ be arbitrary.  By the assumption that $G$ acts transitively, there is a $g \in G$ such that $y = g*x$. But then $G$-equivariance implies that $\phi(y) = \phi(g*x) = g*\phi(x) = g*x = y$. Since this holds for all $y\in Y$, $\phi$ must be equal to the identity $\phi = id_X$, and therefore $Aut_G(X)$ acts freely on $X$.

* A [[combinatorial species]] $F : \mathbb{P} \to Set$ is said to be _flat_ if all of the actions $S_n \times F(n) \to F(n)$ are free (see [[Combinatorial species and tree-like structures]]). For example, the species of [[linear orders]] is flat.

## Related concepts

* [[fixed point]]

* [[homogeneous space]]

* [[torsor]]

* [[universal principal bundle]]

* [[transitive action]], [[effective action]], [[free action]], [[semi-free action]], [[regular action]],

* [[proper action]], [[properly discontinuous action]]


[[!redirects free actions]]