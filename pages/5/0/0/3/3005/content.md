
#Contents#
* automatic table of contents goes here
{:toc}


## Statement

__Beck's monadicity theorem__ (or _tripleability theorem_) states that a [[functor]] $U : D \rightarrow C$ is [[monadic]] (tripleable) if and only if

1. $U$ has a [[left adjoint]], and
1. $U$ [[created limit|creates]] [[coequalizers]] of $U$-split pairs.

Here a [[parallel pair]] $f,g : a \rightarrow b$ in $D$ is **$U$-split** if the pair $U f, U g$ has a [[split coequalizer]] in $C$.  Specifically, this means that there is a diagram in $C$: 

$$U a \;\underoverset{U f}{U g}{\rightrightarrows}\; U b \;\overset{h}{\rightarrow}\; c$$

where $h$ has a [[section]] $s$ and $U f$ has a section $t$ such that $U g \cdot t = s \cdot h$.  This implies that the arrow $h$ is necessarily a coequalizer of $U f$ and $U g$.  To say that $U$ *creates coequalizers of $U$-split pairs* is to say that for any such $U$-split pair, there exists a coequalizer $e$ of $f,g$ in $D$ which is preserved by $U$, and moreover any fork in $D$ whose image in $C$ is a split coequalizer must itself be a coequalizer (not necessarily split).

An equivalent, and sometimes easier, way to state thess conditions is to say that

1. $U$ has a left adjoint,
1. $U$ reflects [[isomorphisms]] (i.e. it is [[conservative functor|conservative]]), and
1. $C$ has, and $U$ preserves, coequalizers of $U$-split pairs.

This is because a conservative functor [[reflected limit|reflects]] any limits or colimits which exist in its domain and it [[preserved limit|preserves]], while monadic functors are always conservative.


### The crude monadicity theorem

The __crude monadicity theorem__ gives a *sufficient*, but not necessary, condition for a functor to be monadic.  It states that a functor $U : D \rightarrow C$ is [[monadic]] if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $D$ has and $U$ preserves coequalizers of reflexive pairs

where a parallel pair $f,g : a \rightarrow b$ is __reflexive__ if $f$ and $g$ have a common [[section]].  This sufficient, but not necessary, condition is sometimes easier to verify in practice.  In contrast to the crude monadicity theorem, the necessary and sufficient condition above is sometimes called the __precise monadicity theorem__.


## In $(\infty,1)$-categories

There is a version of the monadicity theorem for [[(∞,1)-monad]]s in [section 3.4](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=107) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))


## Applications

The monadicity theorem plays a central role in [[monadic descent]].



[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck Monadicity Theorem]]
[[!redirects Barr-Beck theorem]]
[[!redirects monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck monadicity theorem]]
[[!redirects tripleability theorem]]
[[!redirects Beck's tripleability theorem]]
[[!redirects Beck's tripleability theorem]]
[[!redirects Beck tripleability theorem]]
[[!redirects Beck's theorem]]
[[!redirects Beck's theorem]]
[[!redirects Beck theorem]]
[[!redirects crude monadicity theorem]]
[[!redirects crude tripleability theorem]]
