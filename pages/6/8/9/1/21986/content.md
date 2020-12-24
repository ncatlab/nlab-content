+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Integers object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

An **integers object** [[internalization|internal to]] a topos is an [[object]] that behaves in that topos like the set $\mathbb{Z}$ of [[integers]] does in [[Set]].

## Definition

### In a topos or cartesian closed category {#CCC}

An **integers object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbb{Z}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $z:1 \to \mathbb{Z}$ from the [[terminal object]] $1$;

  * a [[morphism]] $s : \mathbb{Z} \to \mathbb{Z}$ ([[successor]]),

  * a [[morphism]] $n : \mathbb{Z} \to \mathbb{Z}$ ([[negation]])

* such that the following diagram [[commutative diagram|commutes]]:
\begin{center}
  \begin{tikzcd}
    & \mathbb{Z} \ar[d, "n"] 
    & \mathbb{Z} \ar[l, "s"] \ar[d, "n"] \ar[rd, "id_\mathbb{Z}"] & \\
    1 \ar[ru, "z"] \ar[r, "z"] & \mathbb{Z} \ar[r, "s"] 
    & \mathbb{Z} \ar[r, "n"] & \mathbb{Z}
  \end{tikzcd}
\end{center}

* and that for every other [[commutative diagram]] of form 
\begin{center}
  \begin{tikzcd}
    & A \ar[d, "n_A"] & A \ar[l, "s_A"] \ar[d, "n_A"] \ar[rd, "id_A"] & \\
    1 \ar[ru, "z_A"] \ar[r, "z_A"] & A \ar[r, "s_A"] & A \ar[r, "n_A"] & A
  \end{tikzcd}
\end{center} 

* there is a unique morphism $u : \mathbb{Z} \to A$ such that the following diagram commutes
\begin{center}
  \begin{tikzcd}
    1 \ar[r, "z"] \ar[rd, "z_A"] & \mathbb{Z} \ar[r, "s"] \ar[d, "u"] &
    \mathbb{Z} \ar[r, "n"] \ar[d, "u"] & \mathbb{Z} \ar[d, "u"] \\
    & A \ar[r, "s_A"] & A \ar[r, "n_A"] & A
  \end{tikzcd}
\end{center} 

By the [[universal property]], the integers object is unique up to [[isomorphism]]. 

##Properties

###Inverse
The morphism $p : \mathbb{Z} \to \mathbb{Z}$  ([[predecessor]]), defined as $p = n \circ s \circ n$, is an [[inverse]] morphism of $s$, satisfying the [[commutative diagram]]: 
\begin{center}
  \begin{tikzcd}
    \mathbb{Z} \ar[r, "s"] \ar[d, "p"] \ar[rd, "id_\mathbb{Z}"] &
    \mathbb{Z} \ar[d, "p"]             \\
    \mathbb{Z} \ar[r, "s"] & \mathbb{Z}
  \end{tikzcd}
\end{center}

It follows that $s$ and $p$ are both isomorphisms of $\mathbb{Z}$. 

###Relation to ring objects
In a category with finite products, the initial [[ring object]], an object $\mathbb{Z}$ with global elements $0:1\rightarrow\mathbb{Z}$ and $1:1\rightarrow\mathbb{Z}$, a morphism $-:\mathbb{Z}\rightarrow\mathbb{Z}$, morphsims $+:\mathbb{Z}\times\mathbb{Z}\rightarrow\mathbb{Z}$ and $\times:\mathbb{Z}\times\mathbb{Z}\rightarrow\mathbb{Z}$, and suitable commutative diagrams expressing the ring axioms and [[initial object|initiality]], has the structure of an integers object given by $z = 0$, $s = x + 1$, and $n = -$. 

## Related concepts

* [[integers]]

* [[natural numbers object]]

* [[free group]]

* [[ring object]]


[[!redirects integers object]]
[[!redirects integers objects]]
[[!redirects integer object]]
[[!redirects integer objects]]