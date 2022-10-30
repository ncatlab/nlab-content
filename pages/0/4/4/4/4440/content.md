
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

The notion of _2-sheaf_ is the generalization of the notion of [[sheaf]] to the [[higher category theory]] of [[2-categories]]/[[bicategories]]. 
A 2-category of 2-sheaves forms a [[2-topos]].

+-- {: .num_remark }
###### Remark on terminology

A _2-sheaf_ is a higher sheaf of [[categories]]. More restrictive than this is a higher sheaf with values in [[groupoids]], which would be a _[[(2,1)-sheaf]]_. Both these notions are often referred to as **[[stack]]**, or sometimes "stack of groupoids" and "stack of categories" for definiteness. But moreover, traditionally a [[stack]] (in either flavor) is considered only over a [[1-site]], whereas it makes sense to consider [[(2,1)-sheaves]] more generally over [[(2,1)-sites]] and 2-sheaves over [[2-sites]].

Therefore, saying "2-sheaf" serves to indicate the full generality of the notion of higher sheaves in [[2-category theory]], as opposed to various special cases of this general notion which have traditionally been considered.

=--

## Definition

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

## Properties

### Characterization of over $(n,r)$-sites

If the underlying [[2-site]] happens to be an [[(n,r)-site]] for $n$ and/or $r$ lower than 2, there may be other equivalent ways to think of 2-sheaves.

A [[2-topos]] with a [[2-site]] of definition that happens to be just a 1-site or [[(2,1)-site]] is _1-localic_ or _(2,1)-localic_.

#### Over a 1-site

Over a 1-site, the [[Grothendieck construction]] says that [[2-functors]] on the site are equivalent to [[fibered categories]] over the site. Hence in this case the theory of 2-sheaves can be entirely formulated in terms of fibered categories. See _[References -- In terms of fibered categories](#InTermsOfFiberedCategories)_.

Also, over a 1-site a 2-sheaf is essentially a _[[indexed category]]_. Therefore stacks over 1-sites can also be discussed in this language, see notably the work ([Bunge-Pare](#BungePare)).

In particular, if the 1-site $C$ is a [[topos]], then every topos _over_ $C$ as its [[base topos]] (a $C$-topos) induces an [[indexed category]]. 

+-- {: .num_prop }
###### Proposition

If $C$ is a topos and $E$ is a $C$-topos, then (the [[indexed category]] corresponding to) $E$ is a 2-sheaf on $C$ with respect to the [[canonical topology]].

=--

This appears as ([Bunge-Pare, corollary 2.6](#BungePare)).
 
Moreover, over a [[1-site]] the [[2-topos]] of 2-sheaves ought to be equivalent to the (suitably defined) [[2-category]] of [[internal categories]] in the underlying [[1-topos]]. See _[References -- In terms of internal categories](#ReferencesInTermsOfInternalCategories)_.

#### Over a $(2,1)$-site -- As internal categories

Over a [[(2,1)-site]] the [[2-topos]] of 2-sheaves ought to be equivalent to the [[2-category]] of [[internal (infinity,1)-categories]] in the corresponding [[(2,1)-topos]].

This is discussed at _[2-Topos -- In terms of internal categories](2-topos#InTermsOfInternalCategories)_.



## Examples

### Codomain fibrations / sheaves of modules

A classical class of examples for 2-sheaves are [[codomain fibrations]]
over suitable sites, or rather their [[tangent categories]]. As discussed there, this includes the case of sheaves of categories of [[modules]] over sites of [[algebra over an algebraic theory|algebras]].

+-- {: .num_prop }
###### Proposition

For $C$ an [[exact category]] with [[finite limits]], the [[codomain fibration]] $Cod : C^I \to C$ or equivalently (under the [[Grothendieck construction]]), the self-[[indexed category|indexing]] of $C$ is a 2-sheaf with respect to the [[canonical topology]].

=--

This is for instance ([Bunge-Pare, corollary 2.4](#BungePare)).

## Related concepts

* [[presheaf]] /  [[sheaf]] / [[cosheaf]]

* **2-sheaf** / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 

* [[(∞,2)-sheaf]]

* [[(∞,n)-sheaf]]

* [[descent]]


## References

Historically, the original definition of _[[stack]]_ 
included the case of category-valued functors, hence of 2-sheaves, in:

* [[Jean Giraud]], _Cohomologie non ab&#233;lienne, Grundlehren 179, Springer Verlag (1971) ([doi:10.1007/978-3-662-62103-5](https://www.springer.com/gp/book/9783540053071))

* [[Jean Giraud]], _Classifying topos_, in: [[William Lawvere]] (ed.) _Toposes, Algebraic Geometry and Logic_, Lecture Notes in Mathematics, vol 274. Springer (1972) ([doi:10.1007/BFb0073964](https://doi.org/10.1007/BFb0073964))

### In terms of categories internal to sheaf toposes
 {#ReferencesInTermsOfInternalCategories}

Category-valued stacks as [[internal categories]] in the underlying [[sheaf topos]] have been considered in

* [[Marta Bunge]], [[Robert Pare]], _Stacks and equivalence of indexed categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no.4 (1979) ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_4_373_0))
 {#BungePare}

* [[Marta Bunge]], _Stack completions and Morita equivalence for categories in a topos_, Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle xx-4, (1979)
401-436, ([MR558106](http://www.ams.org/mathscinet-getitem?mr=558106), [numdam](http://www.numdam.org/item?id=CTGDC_1979__20_4_401_0))
 {#Bunge}

and in section 3 of

* [[André Joyal]], [[Myles Tierney]], _Strong stacks and classifying spaces_, Category theory ([[Como]], 1990), 213&#8212;236, Lecture Notes in Math. 1488, Springer (1991) ([pdf](http://www.pps.jussieu.fr/~mellies/semantics-operads-categories/joyal-tierney-strong-stacks.pdf)) 
 {#JoyalTierney}

### In terms of fibered categories
 {#InTermsOfFiberedCategories}

A discussion of stacks over [[1-sites]] in terms of their [[Grothendieck construction|associated]] [[fibered categories]] is in 

* [[Angelo Vistoli]], _Notes on Grothendieck topologies, fibered categories and descent theory_ ([pdf](http://homepage.sns.it/vistoli/descent.pdf))

### 2-Sites

The above text involves content transferred from 

* [[Michael Shulman]], _[[michaelshulman:2-site]]_

2-sites were earlier considered in

* [[Ross Street]], _[[StreetCBS]]_

[[!redirects 2-sheaves]]