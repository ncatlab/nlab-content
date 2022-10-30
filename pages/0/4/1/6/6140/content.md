An __operator topology__ is an abbreviation of a __topology on a space of (continuous linear) operators__ between [[topological vector space]]s over a fixed field $k$ of reals or complexes (possibly also p-adics, skewfield of quaternions etc.). In other words the hom-sets in the category of topological vector spaces as objects and continuous linear operators as morphisms are equipped with an operator topology.

There are many widely used topologies, some with standard names. Let $L(V,W) = Hom_{TVS}(V,W)$ be the set of continuous linear operators. 

* __weak operator topology__ on $L(V,W)$ is given by the basis of open neighborhoods of zero given by sets of the form $U(x,f) = \{A\in L(V,W) : |f(A(x)) \lt 1 \} $ where $x\in V$ and $f\in W^* = Hom_{TVS}(W,k)$. A sequence $(A_n)$ converges to $A$ is weak operator topology iff the sequence $(A_n(x))$ converges to $A(x)$ in the weak topology on $W$. We write $A_n\stackrel{w}\longrightarrow A$ or $w-lim A_n = A$. 

* __strong operator topology__: the basis of neighborhoods of zero are given by sets 
$N(x,U) = \{A\in L(V,W) \,|\, Av \in U\}$, where $v\in V$ and $U$ is a neighborhood of zero in $W$. For convergence of sequences, we write $A_n\stackrel{s}\longrightarrow A$ or $s-lim A_n= A$.

* __uniform operator topology__: here we assume that $V,W$ are normed spaces with norms $p_V$, $p_W$. Then $L(V,W)$ has a uniform operator topology induced by the norm given by the formula  

$$
p(A) = sup_{v\neq 0} \frac{p_W(Av)}{p_V (v)}
$$

* __ultraweak operator topology__ ...

### Links and literature

* A. A. Kirillov, A. D. Gvi&#353;iani, &#1058;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1080; &#1079;&#1072;&#1076;&#1072;&#1095;&#1080; &#1092;&#1091;&#1085;&#1082;&#1094;&#1080;&#1086;&#1085;&#1072;&#1083;&#1100;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; (theorems and exercises in functional analysis), Moskva, Nauka 1979, 1988

[[!redirects topology on a space of operators]]
[[!redirects strong operator topology]]
[[!redirects weak operator topology]]
[[!redirects uniform operator topology]]