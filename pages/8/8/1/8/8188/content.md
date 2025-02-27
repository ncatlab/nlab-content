
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Sequence spaces
* table of contents
{: toc}

## Sequence spaces

A classical _sequence space_ is a [[vector space]] of [[sequences]] of [[real numbers]], equipped with a [[p-norm]] that makes it a [[normed vector space]]. More generally one may consider spaces of functions on any set. 

Specific sequence spaces are usually known through their symbolic names, such as '$c_0$' and '$l^p$', that appear below.  The term 'sequence space' is useful as a general name without symbols in it.

The sequences spaces are basic examples of [[topological vector spaces]].  They all have a discrete flavour that (maybe) makes them easy to understand, but they are not actually [[discrete spaces]].

The generalization of sequences space to spaces of functions on more general [[measure spaces]] are the _[[Lebesgue spaces]]_.




## Definitions

Fix a [[set]] $N$; typically, $N$ is the set $\mathbb{N}$ of [[natural numbers]], but this is not necessary for the basic concepts.  Sometimes one uses the set $\mathbb{Z}$ of [[integers]] (which is the [[underlying set]] of an [[abelian group]], useful for some purposes), which of course is [[bijective]] with $\mathbb{N}$.  For the simplest examples, let $N$ be a [[finite set]].

Also fix a [[topological vector space]] $K$; typically, $K$ is either the space $\mathbb{C}$ of [[complex numbers]] or the space $\mathbb{R}$ of [[real numbers]].  We will assume below that $K$ is at least a [[Banach space]]; but since much of the point of the sequence spaces is to be simple examples of Banach spaces, you probably want something familiar as $K$.

We will think of a [[function]] from $N$ to $K$ as a __$K$-valued $N$-sequence__, or simply a __sequence__.  The various sequence spaces will be [[subsets]] of the [[function set]] $K^N$ of all sequences.  In general, if '$X$' is the symbol for a sequence space, then we may specify $N$ and $K$ by writing '$X(N,K)$' (or a variation thereon), but often this is suppressed.


+-- {: .num_defn}
###### Definition

$l^1$ is the space of __absolutely summable sequences__:
$$ \sum_k {|a_k|} \lt \infty .$$
We equip $l^1$ with the __$l^1$-norm__
$$ {\|a\|_1} \coloneqq \sum_k {|a_k|} .$$
=--

This is a [[Banach space]].


+-- {: .num_defn}
###### Definition

$l^2$ is the space of __absolutely square-summable sequences__ (or, over a [[real field]], simply _square-summable sequences_):
$$ \sum_k {|a_k|^2} \lt \infty .$$
We equip $l^2$ with the __$l^2$-norm__
$$ {\|a\|_2} \coloneqq \sqrt{\sum_k {|a_k|^2}} .$$
=--

This is also a Banach space; in fact, it\'s a [[Hilbert space]] (assuming that $K$ is).  Furthermore, *every* Hilbert space (over $K$ a [[field]]) arises in this way, up to [[isometric isomorphism]], using an [[orthonormal basis]] for $N$.


More generally, for $0 \lt p \lt \infty$:

+-- {: .num_defn}
###### Definition

$l^p$ is the space of __absolutely $p$th-power--summable sequences__:
$$ \sum_k {|a_k|^p} \lt \infty .$$
We equip $l^p$ with the __$l^p$-norm__
$$ {\|a\|_p} \coloneqq \sqrt[p]{\sum_k {|a_k|^p}} .$$
=--

This is at least an $F$-[[F-space|space]], which is a Banach space iff $p \geq 1$.  (For $p \lt 1$, the 'norm' is not really a norm in the sense of a [[normed vector space]].)


+-- {: .num_defn}
###### Definition

$l^\infty$ is the space of __absolutely bounded sequences__:
$$ \sup_k {|a_k|} \lt \infty .$$
We equip $l^\infty$ with the __supremum norm__:
$$ {\|a\|_\infty} \coloneqq \sup_k {|a_k|} .$$
=--

This is also a Banach space.


+-- {: .num_defn}
###### Definition

$c_c$ (or $c_{00}$) is the space of __almost-zero sequences__:
$$ \ess\forall k,\; a_k = 0 ,$$
where '$\ess\forall$' means 'for all but finitely many' ($\tilde{K}$-[[K-finite|finite]] in [[constructive mathematics]]).
We equip $c_c$ with the topology of [[compact convergence]] (here, convergence on finite subsets).
=--

This is a [[locally convex space]] and not a Banach space.


+-- {: .num_defn}
###### Definition

$c_0$ is the space of __zero-limit sequences__:
$$ \forall \epsilon,\; \ess\forall k,\; {|a_k|} \lt \epsilon ,$$
where as usual $\epsilon$ is a [[positive number]] and again '$\ess\forall$' means 'for all but finitely many'.
We equip $c_0$ with the [[supremum norm]].
=--

This is also a locally convex space, in fact a [[Banach space]].


+-- {: .num_defn}
###### Definition

$c_\infty$ is the space of __convergent sequences__:
$$ \exists L,\; \forall \epsilon,\; \ess\forall k,\; {|a_k - L|} \lt \epsilon ,$$
where $L$ is an element of $K$ and the other notation is as in $c_0$ above.
We also equip $c_\infty$ with the supremum norm.
=--

This is also a [[Banach space]].  $c_\infty$ is also written simply '$c$', but this can be confusing; see the [Generalisations](#Generalisations) below.

There is some argument to be made that an element of $c_\infty$ should be a sequence with the [[extra structure]] of a specific limit $L$, rather than a sequence with the [[extra property]] that some limit exists.  This makes no difference if $N$ is [[infinite set|infinite]]; but if $N$ is finite then the version of $c_\infty$ with extra structure is the $l^\infty$-[[l-infinity-direct sum|direct sum]] of the [[ground field]] and the version of $c_\infty$ with extra property.


+-- {: .num_defn}
###### Definition

$c_b$ is the space of __absolutely bounded sequences__:
$$ \sup_k {|a_k|} \lt \infty .$$
We equip $c_b$ with the supremum norm too.
=--

This is yet another [[Banach space]].  Indeed, $c_b = l^\infty$, two different ways of thinking about the same thing.  (But they generalise differently.)


+-- {: .num_defn}
###### Definition

Finally, $K^N$ is the space of all sequences.  We equip $K^N$ with the [[product topology]], also called the topology of [[pointwise convergence]].
=--

This should probably be denoted '$c$', in line with the [generalisation](#Generalisations) below; but that symbol is often used for $c_\infty$, so it would be confusing.


## Properties

These properties all use the version of $c_\infty$ with extra property.

For $0 \lt p \lt q \lt \infty$, we have $c_c \subseteq l^p \subseteq l^q \subseteq c_0$, with each space [[dense subspace|dense]] in the next (using the topology of the next).  This continues: $c_0 \subseteq c_\infty \subseteq c_b = l^\infty$, but now each space, far from being dense, is a [[closed subspace]] of the next (with the [[induced topology]]).  Finally, $l^\infty = c_b \subseteq K^N$

When $N$ is [[finite set|finite]], these spaces are all the same, being just the [[cartesian spaces]] $K^N$; when $N$ is [[infinite set|infinite]], the inclusions above are all proper (at least if $K$ is nontrivial).

The various [[direct sums of Banach spaces]] follow the sequence spaces $l^p$ for $1 \leq p \leq \infty$.

The [[Riesz representation theorems]] give many nice results for the [[dual vector space|dual spaces]] of the sequence spaces:

*  the dual of $c_0$ is $l^1$,
*  the dual of $l^p$ is $l^q$ for $p + q = p q$ and $1 \lt p , q \lt \infty$,
*  the dual of $l^1$ is $l^\infty$,
*  the dual of $l^\infty$ is $l^1$ in [[dream mathematics]], but something much larger in [[classical mathematics]].


## Generalisations
   {#Generalisations}

The sequence spaces $l^p$ generalise to the [[Lebesgue spaces]] $L^p$ on arbitrary [[measure spaces]].  In fact, $l^p(N)$ is simply $L^p(N,\mu)$, where $\mu$ is [[counting measure]].

The sequence spaces $c_c$, $c_0$, $c_\infty$, $c_b$, and $K^N$ generalise to the spaces $C_c$, $C_0$, $C_\infty$, $C_b$, and $C$ of [[continuous maps]] on a [[local compactum]].  In fact, $c_*(N)$ is simply $C_*(N,\tau)$, where $\tau$ is the [[discrete topology]].  (Note that one never uses the symbol '$C$' for '$C_\infty$' with capital letters.)

A common setting for both of these generalisations is a (locally compact Hausdorff) [[topological group]].  While $l^\infty$ and $c_b$ are the same, $L^\infty$ and $C_b$ are the same *only* if the group is discrete.  (Otherwise $C_b \subset L^\infty$ properly.)


## In constructive mathematics

The spaces $c_c$, $c_0$, and $c_\infty$ work just fine in [[constructive mathematics]] (as does $K^N$, since it has no interesting structure anyway).  For $l^p$, we need $N$ to have [[decidable equality]] to define $\|a\|_p$; even so, $\|a\|_p$ (even when bounded) is only a [[lower real number]], so we usually require it be [[located real number|located]] to have an element of $l^p$.  With these caveats, $l^p$ works just fine for $0 \lt p \lt \infty$.  For $c_b = l^\infty$, we cannot get a [[Banach space]] with [[located real number|located]] [[norms]], as is usually required for constructive [[functional analysis]] ... well, unless we require $N$ to be [[finite set|finite]] (in the strictest sense), which leaves out the motivating example.  Nevertheless, we can still treat $l^\infty$ as a *semicontinuous* Banach space, that is one where the norms may be any bounded [[lower reals]]; for that matter, we can also consider semicontinuous versions of $l^p$.  (Another way to treat $l^\infty$ may be formally, as the [[dual vector space|dual]] of $l^1$; I don\'t know how well this works.)

## See also 

* [[sequence]]

* [[sequence algebra]]

## References

At least for the term 'sequence space', try [Wikipedia](https://en.wikipedia.org/wiki/Sequence_space) and _[[HAF]]_.


[[!redirects sequence space]]
[[!redirects sequence spaces]]

[[!redirects l1-space]]
[[!redirects l1-spaces]]
[[!redirects l-1-space]]
[[!redirects l-1-spaces]]
[[!redirects l^1-space]]
[[!redirects l^1-spaces]]
[[!redirects l_1-space]]
[[!redirects l_1-spaces]]
[[!redirects l1 space]]
[[!redirects l1 spaces]]
[[!redirects l-1 space]]
[[!redirects l-1 spaces]]
[[!redirects l^1 space]]
[[!redirects l^1 spaces]]
[[!redirects l_1 space]]
[[!redirects l_1 spaces]]

[[!redirects lp-space]]
[[!redirects lp-spaces]]
[[!redirects l-p-space]]
[[!redirects l-p-spaces]]
[[!redirects l^p-space]]
[[!redirects l^p-spaces]]
[[!redirects l_p-space]]
[[!redirects l_p-spaces]]
[[!redirects lp space]]
[[!redirects lp spaces]]
[[!redirects l-p space]]
[[!redirects l-p spaces]]
[[!redirects l^p space]]
[[!redirects l^p spaces]]
[[!redirects l_p space]]
[[!redirects l_p spaces]]

[[!redirects linfty-space]]
[[!redirects linfty-spaces]]
[[!redirects l-infty-space]]
[[!redirects l-infty-spaces]]
[[!redirects l^infty-space]]
[[!redirects l^infty-spaces]]
[[!redirects l_infty-space]]
[[!redirects l_infty-spaces]]
[[!redirects linfty space]]
[[!redirects linfty spaces]]
[[!redirects l-infty space]]
[[!redirects l-infty spaces]]
[[!redirects l^infty space]]
[[!redirects l^infty spaces]]
[[!redirects l_infty space]]
[[!redirects l_infty spaces]]
[[!redirects linfin-space]]
[[!redirects linfin-spaces]]
[[!redirects l-infin-space]]
[[!redirects l-infin-spaces]]
[[!redirects l^infin-space]]
[[!redirects l^infin-spaces]]
[[!redirects l_infin-space]]
[[!redirects l_infin-spaces]]
[[!redirects linfin space]]
[[!redirects linfin spaces]]
[[!redirects l-infin space]]
[[!redirects l-infin spaces]]
[[!redirects l^infin space]]
[[!redirects l^infin spaces]]
[[!redirects l_infin space]]
[[!redirects l_infin spaces]]
[[!redirects linfinity-space]]
[[!redirects linfinity-spaces]]
[[!redirects l-infinity-space]]
[[!redirects l-infinity-spaces]]
[[!redirects l^infinity-space]]
[[!redirects l^infinity-spaces]]
[[!redirects l_infinity-space]]
[[!redirects l_infinity-spaces]]
[[!redirects linfinity space]]
[[!redirects linfinity spaces]]
[[!redirects l-infinity space]]
[[!redirects l-infinity spaces]]
[[!redirects l^infinity space]]
[[!redirects l^infinity spaces]]
[[!redirects l_infinity space]]
[[!redirects l_infinity spaces]]
[[!redirects l∞-space]]
[[!redirects l∞-spaces]]
[[!redirects l-∞-space]]
[[!redirects l-∞-spaces]]
[[!redirects l^∞-space]]
[[!redirects l^∞-spaces]]
[[!redirects l_∞-space]]
[[!redirects l_∞-spaces]]

[[!redirects cc-space]]
[[!redirects cc-spaces]]
[[!redirects c-c-space]]
[[!redirects c-c-spaces]]
[[!redirects c_c-space]]
[[!redirects c_c-spaces]]
[[!redirects cc space]]
[[!redirects cc spaces]]
[[!redirects c-c space]]
[[!redirects c-c spaces]]
[[!redirects c_c space]]
[[!redirects c_c spaces]]
[[!redirects c00-space]]
[[!redirects c00-spaces]]
[[!redirects c-00-space]]
[[!redirects c-00-spaces]]
[[!redirects c_00-space]]
[[!redirects c_00-spaces]]
[[!redirects c00 space]]
[[!redirects c00 spaces]]
[[!redirects c-00 space]]
[[!redirects c-00 spaces]]
[[!redirects c_00 space]]
[[!redirects c_00 spaces]]

[[!redirects c0-space]]
[[!redirects c0-spaces]]
[[!redirects c-0-space]]
[[!redirects c-0-spaces]]
[[!redirects c_0-space]]
[[!redirects c_0-spaces]]
[[!redirects c0 space]]
[[!redirects c0 spaces]]
[[!redirects c-0 space]]
[[!redirects c-0 spaces]]
[[!redirects c_0 space]]
[[!redirects c_0 spaces]]

[[!redirects cinfinity-space]]
[[!redirects cinfinity-spaces]]
[[!redirects c-infinity-space]]
[[!redirects c-infinity-spaces]]
[[!redirects c_infinity-space]]
[[!redirects c_infinity-spaces]]
[[!redirects cinfinity space]]
[[!redirects cinfinity spaces]]
[[!redirects c-infinity space]]
[[!redirects c-infinity spaces]]
[[!redirects c_infinity space]]
[[!redirects c_infinity spaces]]
[[!redirects cinfin-space]]
[[!redirects cinfin-spaces]]
[[!redirects c-infin-space]]
[[!redirects c-infin-spaces]]
[[!redirects c_infin-space]]
[[!redirects c_infin-spaces]]
[[!redirects cinfin space]]
[[!redirects cinfin spaces]]
[[!redirects c-infin space]]
[[!redirects c-infin spaces]]
[[!redirects c_infin space]]
[[!redirects c_infin spaces]]
[[!redirects cinfty-space]]
[[!redirects cinfty-spaces]]
[[!redirects c-infty-space]]
[[!redirects c-infty-spaces]]
[[!redirects c_infty-space]]
[[!redirects c_infty-spaces]]
[[!redirects cinfty space]]
[[!redirects cinfty spaces]]
[[!redirects c-infty space]]
[[!redirects c-infty spaces]]
[[!redirects c_infty space]]
[[!redirects c_infty spaces]]
[[!redirects c∞-space]]
[[!redirects c∞-spaces]]
[[!redirects c-∞-space]]
[[!redirects c-∞-spaces]]
[[!redirects c_∞-space]]
[[!redirects c_∞-spaces]]

[[!redirects cb-space]]
[[!redirects cb-spaces]]
[[!redirects c-b-space]]
[[!redirects c-b-spaces]]
[[!redirects c_b-space]]
[[!redirects c_b-spaces]]
[[!redirects cb space]]
[[!redirects cb spaces]]
[[!redirects c-b space]]
[[!redirects c-b spaces]]
[[!redirects c_b space]]
[[!redirects c_b spaces]]

[[!redirects c-space]]
[[!redirects c-spaces]]
[[!redirects c space]]
[[!redirects c spaces]]
