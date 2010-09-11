
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

* [[sheaf]]

* **2-sheaf** / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 


***


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _2-sheaf_ is the generalization of the notion of [[sheaf]] to the [[higher category theory]] of [[2-categories]]/[[bicategories]]. 

A special case is the notion of [[stack]]. See also [[derived stack]].

The 2-category of 2-sheaves forms a [[2-topos]].

## 2-sheaves

Let $C$ be a [[2-site]] having finite [[2-limit]]s (for convenience).  For a covering family $(f_i:U_i\to U)_i$ we have the comma objects
+--{: style="text-align:center"}
<svg xmlns="http://www.w3.org/2000/svg" width="10em" height="10em" viewBox="-30 -20 180 150">
 <desc>Comma Square</desc>
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="16" markdown="1">
  <foreignObject x="-10"  y="0" width="45" height="25">$(f_i/f_j)$</foreignObject>
  <foreignObject x="100"  y="0" width="20" height="20">$U_i$</foreignObject>
  <foreignObject x="0"  y="100" width="20" height="20">$U_j$</foreignObject>
  <foreignObject x="100"  y="100" width="20" height="20">$U$</foreignObject>
  <foreignObject x="110"  y="50" width="20" height="25">$f_i$</foreignObject>
  <foreignObject x="50"  y="110" width="20" height="25">$f_j$</foreignObject>
  <foreignObject x="-20"  y="50" width="20" height="30">$q_{i j}$</foreignObject>
  <foreignObject x="50"  y="-20" width="20" height="30">$p_{i j}$</foreignObject>
  <foreignObject x="60"  y="60" width="20" height="25">$\mu_{i j}$</foreignObject>
 </g>
 <g fill="none" stroke="#000" stroke-width="1.5" marker-end="url(#svg295arrowhead)">
   <line x1="40" y1="10" x2="90" y2="10"/>
   <line x1="30" y1="110" x2="90" y2="110"/>
   <line y1="30" x1="10" y2="90" x2="10"/>
   <line y1="30" x1="110" y2="90" x2="110"/>
   <line x1="65" y1="55" x2="55" y2="65"/>
 </g>
</svg>
=--

We also have the [[nlab:double comma object|double comma objects]] $(f_i/f_j/f_k) = (f_i/f_j)\times_{U_j} (f_j/f_k)$ with projections $r_{i j   k}:(f_i/f_j/f_k)\to (f_i/f_j)$, $s_{i j k}:(f_i/f_j/f_k)\to (f_j/f_k)$, and $t_{i j k}:(f_i/f_j/f_k)\to (f_i/f_k)$.

Now, a functor $X:C^{op} \to Cat$ is called a **2-presheaf**.  It is **1-separated** if

* For any covering family $(f_i:U_i\to U)_i$ and any $x,y\in X(U)$ and $a,b: x\to y$, if $X(f_i)(a) = X(f_i)(b)$ for all $i$, then $a=b$.

It is **2-separated** if it is 1-separated and

* For any covering family $(f_i:U_i\to U)_i$ and any $x,y\in X(U)$, given $b_i:X(f_i)(x) \to X(f_i)(y)$ such that $\mu_{i j}(y) \circ X(p_{i j})(b_i) = X(q_{i j})(b_i) \circ \mu_{i j}(x)$, there exists a (necessarily unique) $b:x\to y$ such that $b_i = X(f_i)(b)$.

It is a **2-sheaf** if it is 2-separated and

* For any covering family $(f_i:U_i\to U)_i$ and any $x_i\in X(U_i)$ together with morphisms $\zeta_{i j}:X(p_{i j})(x_i) \to X(q_{i j})(x_j)$ such that the following diagram commutes:
$$\array{X(r_{i j k})X(p_{i j})(x_i) &
  \overset{X(r_{i j k})(\zeta_{i j})}{\to} &
  X(r_{i j k})X(q_{i j})(x_j) & \overset{\cong}{\to} &
  X(s_{i j k})X(p_{j k})(x_j)\\
  ^\cong \downarrow && && \downarrow ^{X(s_{i j k})(\zeta_{j k})}\\
  X(t_{i j k}) X(p_{i k})(x_i) &
  \underset{X(t_{i j k})(\zeta_{i k})}{\to} &
  X(t_{i j k}) X(q_{i k})(x_k) & \underset{\cong}{\to} &
  X(s_{i j k}) X(q_{j k})(x_k)}$$
there exists an object $x\in X(U)$ and isomorphisms $X(f_i)(x)\cong x_i$ such that for all $i,j$ the following square
commutes:
$$\array{
  X(p_{i j})X(f_i)(X) & \overset{\cong}{\to}
  &     X(p_{i j})(x_i)\\
  ^{X(\mu_{i j})}\downarrow && \downarrow^{\zeta_{i j}}\\
  X(q_{i j})X(f_j)(x)  & \underset{\cong}{\to} &
  X(q_{i j})(x_j).}$$

A 2-sheaf, especially on a 1-site, is frequently called a **[[stack]]**. However, this has the unfortunate consequence that a 3-sheaf is then called a 2-stack, and so on with the numbering all offset by one. Also, it can be helpful to use a new term because of the notable differences between 2-sheaves on 2-sites and 2-sheaves on 1-sites. The main novelty is that $\mu_{i j}$ and $\zeta_{i j}$ _need not be invertible_.

Note, though, they must be invertible as soon as $C$ is (2,1)-site: $\mu_{i j}$ by definition and $\zeta_{i j}$ since an inverse is provided by $\iota_{i j}^*(\zeta_{i j})$, where $\iota_{i j}\mapsto (f_i/f_j) \to (f_j/f_i)$ is the symmetry equivalence.

If $C$ lacks finite limits, then in the definitions of "2-separated" and "2-sheaf" instead of the comma objects $(f_i/f_j)$, we need to use arbitrary objects $V$ equipped with maps $p:V\to U_i$, $q:V\to U_j$, and a 2-cell $f_i p \to f_j q$.  We leave the precise definition to the reader.

A 2-site is said to be **subcanonical** if for any $U\in C$, the representable functor $C(-,U)$ is a 2-sheaf.  When $C$ has finite limits, it is easy to verify that this is true precisely when every covering family is a (necessarily pullback-stable) quotient of its kernel [[2-polycongruence]].  In particular, the regular coverage on a regular 2-category is subcanonical, as is the coherent coverage on a coherent 2-category.

The 2-category $2Sh(C)$ of 2-sheaves on a small 2-site $C$ is, by definition, a [[Grothendieck 2-topos]].


## References

The above involves content transferred from 

* [[Michael Shulman]], _[[michaelshulamn:2-site]]_

Strict 2-sites were considered in

* [[Ross Street]], _Two-dimensional sheaf theory_ J. Pure Appl. Algebra 23 (1982), no. 3, 251-270.

Bicategorical 2-sites in

* [[Ross Street]], _Characterizations of bicategories of stacks_ , Lecture Notes in Math., 962, 


[[!redirects 2-sheaves]]