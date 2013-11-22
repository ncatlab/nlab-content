
#Contents#
* table of contents
{:toc}

## Idea 

Unramified morphism of algebraic [[scheme]]s is a geometric generalization of a notion of an unramified [[field extension]]. The notion of ramification there, in turn is motivated by the branching phenomena in number fields, which in the [[Riemann surface]] picture involve branchings similar to the branching involved in Riemann surfaces over complex numbers. 

So "unramified" means "not branching". In the context of [[differential geometry]] unramified maps correspond to [[immersions]].

A weaker (infinitesimal) version is the notion of 
[[formally unramified morphism]]. 

### Historical remarks

The basic picture is one from the Riemann surfaces: the power $z\mapsto z^n$ has a branching point around $z=0$. Dedekind and Weber in 19th century considered more generally algebraic curves over more general fields, and proposed a generalization of a Riemann surface picture by considering valuations and in this analysis the phenomenon of branching occured again. 

## Definition

A [[morphism]] $f:X\to Y$ of [[scheme]]s is __unramified__ if it is locally of finite presentation, and if for every point $y\in Y$ the induced morphism 
$$
\mathcal{O}_{X,f(y)}/\mathfrak{m}_{f(y)}\to\mathcal{O}_{Y,y}/\mathfrak{m}_y
$$
of residue fields is a finite and separable extension of fields.

A morphism $f:X\to Y$ of schemes is __[[formally unramified]]__ if for every [[infinitesimal object|infinitesimal thickenning]]
$T\to T'$ of schemes over $Y$, the canonical morphism of sheaves of sets over $T$
$$
U\mapsto (Scheme/Y)(U,X)
$$
to
$$
U\mapsto (Scheme/Y)(U',X)
$$
is injective, where $U' = U$ as the open set, but as a scheme it is the open subscheme of the thickening $T'$. In this condition, it is sufficient to consider the
thickennings of  affine $Y$-schemes. Thus $f$ is formally unramified if for each morphism of $Y$-schemes $T\to X$ which has an extension to a morphism $T'\to X$ the extension is unique. 

## Properties and usage

The notion of unramified morphism is stable under base change and composition. 

[[etale morphism|Etale morphism]] is by (one of the equivalent definitions) a morphism of schemes which is [[flat morphism|flat]] and unramified.

Every [[open immersion of schemes]] is formally etale hence a fortiori formally unramified. A morphism which is locally of finite type is unramified iff the diagonal morphism $X\to X\times_Y X$ is an open immersion. 

Characterization: a morphism is formally unramified iff the module $\Omega_{Y/X}$ of relative [[Kahler differential]]s is zero.

## Literature

* Ogus, _Unramified morphisms_, [pdf](http://math.berkeley.edu/~ogus/Math%20_256A--08/unramif.pdf), notes from a course on algebraic geometry at Berkeley

* [[EGA]] IV


[[!redirects unramified morphisms]] 
[[!redirects unramified]]