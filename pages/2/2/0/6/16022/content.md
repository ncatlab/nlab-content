
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[topology|point set topology]], every subspace $X$ of a space $A$ has a unique largest subspace in which $X$ is [[dense subspace|dense]], namely simply the closure $\overline{X}$. Using maps, this amounts to say that $X\hookrightarrow A$ factors as $X\hookrightarrow\overline{X}$ followed by $\overline{X}\hookrightarrow A$.

The **(dense,closed)-factorization** generalizes this idea from topology to [[topos theory]]. It can be viewed as a way to associate to every [[subtopos]] $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ a closure $\overline{Sh_{j}(\mathcal{E})}$.

## Statement

A [[geometric embedding]] of [[elementary toposes]]

$$
  Sh_j(\mathcal{E}) \hookrightarrow \mathcal{E}
$$


factors as

$$
  Sh_j(\mathcal{E}) 
    \hookrightarrow
  Sh_{c(ext(j))}(\mathcal{E})
    \hookrightarrow
  \mathcal{E}
$$

where $ext(j)$ (the "exterior" of $j$) denotes the $j$-closure of $\emptyset \rightarrowtail 1$ and 

$$
  \bar j \coloneqq c(ext(j))
$$ 

the [[closed subtopos|closed topology]] that corresponds to the [[subterminal object]] $ext(j)$.

Here the first inclusion exhibits a [[dense subtopos]] and the second a [[closed subtopos]].

## Remark

$Sh_{c(ext(j))}(\mathcal{E})$ can be viewed as the 'best approximation' of $Sh_j(\mathcal{E})$ by a closed subtopos and therefore might be called the _closure_ $Cl(Sh_j(\mathcal{E}))$ of $Sh_j(\mathcal{E})$.[^sga4] 

[^sga4]: ([SGA4](#SGA4), p.461) uses the term '_l'adh&#233;rence_' for it.

Its complement, the [[open subtopos]] $Ext(Sh_j(\mathcal{E}))$ corresponding to the [[subterminal object]] $ext(j)$ deserves in turn to be called the _exterior_ of $Sh_j(\mathcal{E})$.

## The (dominant,closed)-factorization

The (dense,closed)-factorization is a special case for inclusions of a slightly more general factorization which attaches to a general [[geometric morphism]] the closure of its image.

Recall that an inclusion is [[dense subtopos|dense]] precisely if it is a [[dominant geometric morphism]], hence the following is pertinent for the (dense,closed)-factorization as well.

+-- {: .num_prop #dense-closed}
###### Proposition
Let $i:Sh_{c(U)}(\mathcal{E})\hookrightarrow\mathcal{E}$ be dominant and a [[closed subtopos|closed inclusion]] at the same time. Then $i$ is an isomorphism.
=--

**Proof**: Recall that $X\in\mathcal{E}$ are in the [[closed subtopos]] precisely when they satisfy $X\times U\cong U$ with $U$ the [[subterminal object]] associated to $i$. But $i$ is dominant, or what comes to the same for inclusions: dense, hence $\emptyset$ is in $Sh_{c(U)}(\mathcal{E})$ and therefore $\emptyset\times U\cong U$ . From this follows $U\cong\emptyset$, which in turn implies that all $X\in\mathcal{E}$ are in $Sh_{c(U)}(\mathcal{E})$ . $\qed$

+-- {: .num_prop #dominant-closed}
###### Proposition
Let $f:\mathcal{F}\to\mathcal{E}$ be a geometric morphism. Then $f$ factors as a [[dominant geometric morphism]] $d$ followed by a [[closed subtopos|closed inclusion]] $c$.
=--

**Proof**: Let $i\circ d_1$ be the [[(geometric surjection, embedding) factorization system|surjection-inclusion factorization]] of $f$. Since $d_1$ is surjective, it is dominant (cf. [this proposition](dominant+geometric+morphism#dominant_surjection)). Then we use the (dense,closed)-factorization to factor $i$ into $c\circ d_2$. Since both $d_i$ are dominant, so is $d:=d_2\circ d_1$ and $c\circ d$ yields the demanded factorization of $f$. $\qed$

## Related entries

* [[dense subtopos]]
* [[dominant geometric morphism]]
* [[(geometric surjection, embedding) factorization system]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV 9.3.4-9.4., pp.456ff)

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.I_ , Oxford UP 2002. (around Lemma A 4.5.19, p. 219)

* {#Caramello09} [[Olivia Caramello]], _Lattices of theories_ , [arXiv:0905.0299](http://arxiv.org/abs/0905.0299) (2009). (section 8)
