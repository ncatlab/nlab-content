
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The **singular cohomology** (also **Betti cohomology**) of a [[topological space]] $X$ is the [[cohomology]] in [[∞Grpd]] of its [[fundamental ∞-groupoid]] $\Pi(X)$:

for $\mathcal{B}^n \mathbb{Z} \in \infty Grpd$ the [[Eilenberg-MacLane object]] with the group $\mathbb{Z}$ in degree $n$, the degree $n$-singular cohomology of $X$ is

$$
  H^n(X,\mathbb{Z}) := \pi_0 \infty Grpd(\Pi(X), \mathcal{B}^n \mathbb{Z})
  \,.
$$


With $\infty Grpd$ [[presentable (∞,1)-category|presented]] by the category [[sSet]] of [[simplicial set]]s, the fundamental $\infty$-groupoid $\Pi(X)$ is modeled by the [[Kan complex]] 

$$
  \Pi(X) = Sing X = Hom_{Top}(\Delta^\bullet_{Top}, X)
  \,,
$$

the [[singular simplicial complex]] of $X$. 

The object $\mathcal{B}^n \mathbb{Z}$ is usefully modeled by the simplicial set 

$$
  \mathcal{B}^n \mathbb{Z} = U (\Xi \mathbb{Z}[n])
$$

which is 

* the underlying simplicial set under the [[forgetful functor]] 

  $$
    (F \dashv U)
    sAb \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
    sSet
  $$

  from abelian [[simplicial group]]s to [[simplicial sets]];

* of the abelian [[simplicial group]] $\Xi \mathbb{Z}[n]$ which is the image under the [[Dold-Kan correspondence]]

  $$
    sAb \stackrel{\overset{\Xi}{\leftarrow}}{\underset{}{\to}}
    Ch^+
  $$

* of the [[chain complex]]

  $$
    \mathbb{Z}[n] =
    (\cdots \to \mathbb{Z} \to 0 \to 0 \to \cdots \to 0)
  $$

  concentrated in degree $n$.

So in this model we have

$$
  H^n(X,\mathbb{Z}) = \pi_0 sSet(Sing X, U(\Xi \mathbb{Z}[n]))
  \,.
$$

A [[cocycle]] in this cohomology theory is a [[cochain on a simplicial set]], on the singular complex $Sing X$.

Using the [[adjunction]] $(F \dashv U)$ this is [[isomorphism|isomorphic]] to

$$
  \cdots \simeq \pi_0 sAb( Ch_n(X), \Xi \mathbb{Z}[n] )
  \,,
$$

where 

$$
  F(Sing X) = \mathbb{Z}[Sing X]
$$

is the [[free functor|free]] abelian simplicial group on the simplicial set $Sing X$: this is the simplicial abelian group of **singular chains** of $X$. Its elements are formal sums of continuous maps $\Delta^n_{Top} \to X$. In this form

$$
  \cdots \simeq \pi_0 sAb( \mathbb{Z}[Sing X], \Xi \mathbb{Z}[n] )
  \,.
$$

Using next the [[Dold-Kan correspondence|Dold-Kan adjunction]] this is

$$
  \cdots \simeq H_0 Ch( Ch_\bullet(X), \mathbb{Z}[n] )
  \,,
$$

where

$$
  Ch_\bullet(X) := N^\bullet(\mathbb{Z}(Sing X))
$$

is the [[Moore complex]] of normalized chains of $\mathbb{Z}[Sing X]$: this is the complex of **singular chains**, formal sums over $\mathbb{Z}$ of simplices in $X$.


This way singular cohomology is the abelian dual of [[singular homology]].

...



## Related concepts

* [[cochain on a simplicial set]]

* [[cup product]]

* [[de Rham theorem]]

## Comparison to sheaf cohomology

If the topological space $X$ is semi-locally contractible
(meaning: any open subset $U\subset X$ has an open cover $W$ by open subsets $W_i\subset U$ that are contractible in&#160;$U$),
then the [[sheaf cohomology]] of&#160;$X$ is isomorphic
to the singular cohomology of&#160;$X$ for any abelian
group of coefficients.

This was proved in ([Sella 16](#Sella16)).

## Discussion

A previous version of this entry led to the following discussion, which later led to extensive discussion by email. Partly as a result of this and similar discussions, there is now more information on how Kan complexes _are_ $\infty$-groupoids at 

* [[Kan complex]]

* [[∞-groupoid]].


## References


Original references on [[chain homology]]/[[cochain cohomology]] and [[singular homology]]/[[singular cohomology]]:

* [[Andrei Kolmogoroff]], _Über die Dualität im Aufbau der kombinatorischen Topologie_, Recueil Mathématique 1(43) (1936), 97–102.  ([mathnet](http://mi.mathnet.ru/msb5361))

* [[Andrei Kolmogoroff]], _Homologiering des Komplexes und des lokal-bicompakten Raumes_, Recueil Mathématique 1(43) (1936), 701–705.  [mathnet](http://mi.mathnet.ru/msb5475).

* [[J. W. Alexander]], _On the chains of a complex and their duals_, Proc. Nat. Acad. Sei. USA, 21(1935), 509–511 ([doi:10.1073/pnas.21.8.50](https://doi.org/10.1073/pnas.21.8.509))

* [[J. W. Alexander]], _On the ring of a compact metric space_, Proc. Nat. Acad. Sci. USA, 21(1935), 511–512 ([doi:10.1073/pnas.21.8.511](https://doi.org/10.1073/pnas.21.8.511))

* [[J. W. Alexander]], _On the connectivity ring of an abstract space_, Ann. of Math., 37 (1936), 698–708 ([doi:10.2307/1968484](https://doi.org/10.2307/1968484), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/alexcon.pdf))

The term “[[cohomology]]” was introduced in this context in

* {#Whitney37} [[Hassler Whitney]], _On matrices of integers and combinatorial topology_.  Duke Mathematical Journal 3:1 (1937), 35–45 ([doi:10.1215/S0012-7094-37-00304-1](https://projecteuclid.org/journals/duke-mathematical-journal/volume-3/issue-1/On-matrices-of-integers-and-combinatorial-topology/10.1215/S0012-7094-37-00304-1.short))

Singular cohomology was introduced by Eilenberg in

* [[Samuel Eilenberg]], _Singular homology theory_, Annals of Mathematics 45:3 (1944).  [doi](https://doi.org/10.2307/1969185)


Relation to [[sheaf cohomology]]:

* {#Sella16} [[Yehonatan Sella]], _Comparison of sheaf cohomology and singular cohomology_ ([arXiv:1602.06674](http://arxiv.org/abs/1602.06674))

[[!redirects Betti cohomology]]

[[!redirects singular chain]]
[[!redirects singular chains]]
[[!redirects singular chain complex]]
[[!redirects singular chain complexes]]
[[!redirects singular cochain]]
[[!redirects singular cochains]]
[[!redirects singular cochain complex]]
[[!redirects singular cochain complexes]]
