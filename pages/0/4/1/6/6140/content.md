
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


\tableofcontents

## Idea

By an *operator topology* one means a [[topology]] (the [[structure]] of a [[topological space]]) on the [[set]] of [[continuous map|continuous]] [[linear operators]] between [[topological vector spaces]].

In other words, given a [[sequence]] of [[linear operators]] $(T_n)_{n \in \mathbb{N}}$, an operator topology determines whether this [[convergence of a sequence|converges]] to a given limit operator $T \;\colon\; V \longrightarrow W$.

There are three key examples:

1. the *strong operator topology* requires that for each [[vector]] $v \in V$ the sequence of [[image]] vectors $T_n(v)$ converges to $T(v)$ in $W$,

1. the *weak operator topology* requires less: namely that for every $v \in V$ and every [[linear functional]] $\omega$ on $W$, the sequence of numbers $\omega\big(T_n(v)\big)$ converges to $\omega\big(T(v)\big)$,

1. the *[[norm topology]]* requires more (assuming now that $V$ and $W$ are equipped with [[normed vector space|norms]] $\vert-\vert$), namely that the [[supremum]] over all unit norm vectors, $\vert v \vert = 1$, of the [[norm]] $\vert T_n(v) - T(v)\vert$ converges to zero.


## Definition

Let 

* $k$ denote the [[ground field]], assumed [[normed field|normed]],

* $V$, $W$ be [[topological vector space]],

* $L(V,W) = Hom_{TVS}(V,W)$ denote the set of [[continuous maps|continuous]] [[linear operators]] between them.


\begin{definition}
The *weak operator topology* on $L(V,W)$ is given by the [[neighbourhood base|basis of open neighborhoods]] of [[zero]] given by [[subsets]] of the form 

$$
  U(v,f) 
    \;=\; 
  \Big\{
     T\in L(V,W)  
      \,\Big\vert\, 
    \omega\big(T(v)\big) \vert \lt 1 
  \Big\}
  \mathrlap{\,,} 
$$ 

where $v\in V$ and $\omega \in W^* = Hom_{TVS}(W,k)$. 

\end{definition}

\begin{definition}
The *strong operator topology* on $L(V,W)$ is given by the [[neighbourhood base|basis of open neighborhoods]] of [[zero]] is given by subsets of the form
$$
  N(v,U) 
   \;=\; 
  \Big\{
    T \in L(V,W) 
      \,\Big|\, 
    T(v) \in U 
  \Big\}
  \,,
$$

where $v\in V$ and $U$ is a [[neighborhood]] of zero in $W$. 
\end{definition}

\begin{definition}
Assuming that $V,W$ are [[normed vector spaces]] with [[norms]] $p_V$, $p_W$ then the *uniform operator topology* or *norm topology* on $L(V,W)$ is induced by the norm given by the formula  

$$
  p(T) 
    \;=\; 
  sup_{v\neq 0} \frac{p_W(T v)}{p_V (v)}
  \mathrlap{\,.}
$$

\end{definition}


## Examples

### The unitary group

The reason that in the definition of a [[unitary representation]], the strong operator topology on [[U(ℋ)|$\mathcal{U}(\mathcal{H})$]] is used and not the [[norm topology]], is that only few [[group homomorphisms]] turn out to be [[continuous map|continuous]] in the norm topology.

For instance, let

* $G$ be a [[compact Lie group]],

* $L^2(G)$ denote the [[Hilbert space]] of [[square integrable function|square integrable]] [[measurable functions]] with respect to its [[Haar measure]],

then the (right) [[regular representation]] of $G$ on $L^2(G)$, defined as

$$
  \begin{array}{ccc}
    G &\longrightarrow& \mathcal{U}\big(L^2(G)\big)
    \\
    g 
      &\mapsto&
    \big( 
       U(-) \mapsto U( - \cdot g) 
    \big)
    \mathrlap{\,,}
  \end{array}
$$

is generally not continuous in the [[norm topology]], but is always continuous in the strong operator topology. 

(The exception is of course when $G$ is [[discrete group|discrete]], hence [[finite group|finite]].)


## Related entries

* [[norm topology]]

* [[U(ℋ)]]

## References

* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988

See also: 

* Wikipedia: *[Operator topologies](https://en.wikipedia.org/wiki/Operator_topologies)*

[[!redirects operator topologies]]

[[!redirects topology on a space of operators]]
[[!redirects topologies on a space of operators]]

[[!redirects strong operator topology]]
[[!redirects weak operator topology]]
[[!redirects uniform operator topology]]

