
#Contents#
* table of contents
{:toc}

## Idea 

### General

The notion of _unramified morphism_ of algebraic [[schemes]] is a geometric generalization of the notion of an unramified [[field extension]]. The notion of ramification there is in turn motivated by branching phenomena in [[number fields]], which involve branchings similar to those occurring in [[Riemann surfaces]] over the [[complex numbers]]. 

So "unramified" means "not branching". In the context of [[differential geometry]] unramified maps correspond to [[immersions]].

A weaker (infinitesimal) version is the notion of _[[formally unramified morphism]]_. 

### Historical remarks

The basic picture is one from Riemann surfaces: the power $z\mapsto z^n$ has a branching point around $z=0$. Dedekind and Weber in 19th century considered more generally algebraic curves over more general fields, and proposed a generalization of a Riemann surface picture by considering valuations and in this analysis the phenomenon of branching occurred again. 

## Definition
 {#Definition}


+-- {: .num_defn}
###### Definition

A [[morphism]] $f \colon X\longrightarrow Y$ of [[schemes]] is __unramified__ if it is [[locally of finite presentation]], and if for every point $x\in X$ we have $\mathfrak{m}_{f(x)}\mathcal{O}_{X,x}=\mathfrak{m}_x$ and the induced morphism of [[residue fields]]
$$
\mathcal{O}_{Y,f(x)}/\mathfrak{m}_{f(x)}\to\mathcal{O}_{X,x}/\mathfrak{m}_{x}
$$
is a [[finite number|finite]] and [[separable field extension|separable]] [[extension of fields]].

=--

+-- {: .num_defn}
###### Definition

A morphism $f:X\to Y$ of schemes is __[[formally unramified]]__ if for every [[infinitesimal object|infinitesimal thickening]]
$T\to T'$ of schemes over $Y$, the canonical morphism of sheaves of sets over $T$
$$
U\mapsto (Sch_{/Y})(U,X)
$$
to
$$
U\mapsto (Sch_{/Y})(U',X)
$$
is injective, where $U' = U$ as the open set, but as a scheme it is the open subscheme of the thickening $T'$. 

=--

+-- {: .num_remark}
###### Remark


In this condition, it is sufficient to consider the
thickenings of  affine $Y$-schemes. Thus $f$ is formally unramified if for each morphism of $Y$-schemes $T\to X$ which has an extension to a morphism $T'\to X$ the extension is unique. 

=--

## Properties and usage

The notion of unramified morphism is stable under base change and composition. 

An [[etale morphism]] of schemes is, by one of the equivalent definitions, a morphism that is [[flat morphism|flat]] and unramified.

Every [[open immersion of schemes]] is formally etale hence a fortiori formally unramified. A morphism which is locally of finite type is unramified iff the diagonal morphism $X\to X\times_Y X$ is an open immersion. 

Characterization: a morphism is formally unramified iff the module $\Omega_{Y/X}$ of relative [[Kahler differential]]s is zero.

## Related concepts

* [[decidable object]]

* [[ramification of ideals]]

* [[formally unramified morphism]]

## Literature

* Ogus, _Unramified morphisms_, [pdf](http://math.berkeley.edu/~ogus/Math%20_256A--08/unramif.pdf), notes from a course on algebraic geometry at Berkeley

* [[EGA]] IV

* [[James Milne]], p. 20 of _[[Lectures on Étale Cohomology]]_


[[!redirects unramified morphisms]] 
[[!redirects unramified]]

[[!redirects unramified morphism of schemes]]
