
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $R$ a [[ring]] and $N$ an $R$-[[module]] which is finitely [[generators and relations|generated]] over $R$ on $n$ generators, the _syzygies_ are the _[[generators and relations|relations]]_ between these generators. 

Higher order syzygies are relations between these relations, and so forth.

Similar definitions apply in non-additive contexts. In the theory of [[group presentation]]s, 2-dimensional [[homotopical syzygies]] are specific cellular representatives for [[identities among relations]] of a presentation of a group.

## Definition

Let $R$ be a [[ring]], $N$ an $R$-[[module]] generated on $n$ generators. Write

$$
  R^n \to N
$$

for the canonical projection from the [[free module]] over $R$ on $n$ generators to $N$, which takes these generators to their image in $N$. 

The **module of syzygies** is the [[kernel]] of this morphism. This being a [[submodule]] of a [[free module]] it is itself free under suitable conditions on $R$, and hence the resulting [[exact sequence]] looks like

$$
  R^{n_1} \to R^{n} \to N
$$

relations/syzygies $\to$ generators $\to$ elements

Continuing in this way yields, under suitable assumptions on $R$, a [[projective resolution]] (actually a [[free resolution]]) of $N$ by syzygies and higher order syzygies.

$$
  \cdots \to R^{n_3} \to R^{n_2} \to R^{n_1} \to R^{n} \to N
  \,.
$$

## Properties

### Hilbert's syzygy theorem

For $k$ a [[field]] and $R = k[x_1, \cdots, x_n]$ the [[polynomial ring]] over $k$ in $n$ [[variables]], every finitely-generated $R$-module has a [[free resolution]] of length at most $n$.


## Related concepts

* [[projective resolution]]

* [[Koszul complex]]


Non-linear variants of the idea of syzygy are

* [[homotopical syzygy]]

* [[computad]]

and

* [[homological syzygy]].

The idea of a homotopical  $n$-syzygy is discussed at 

* [[higher dimensional szyzgy]]

## References

An exposition is in 

* Roger Wiegand, _What is... a syzygy?_ ([pdf](http://www.ams.org/notices/200604/what-is.pdf))

Lecture note discussion in a general context of [[projective resolutions]] in [[homological algebra]] includes

* E. L. Lady, _A course in homological algebra -- Syzygies, Projective dimension, regular sequences and depth_ (1997) ([pdf](http://www.math.hawaii.edu/~lee/homolog/proj-dim.pdf))

and section 4.5 of 

* [[Pierre Schapira]], _Categories and homological algebra_, lecture notes (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 {#Schapira}

Discussion in the context of the [[Koszul complex]] is in 

* Yasuhiro Shimoda, _On the syzygy part of Koszul homology on certain ideals_, J. Math. Kyoto Univ. (1984) ([EUCLID](http://projecteuclid.org/euclid.kjm/1250521386))

A useful source that discusses the use of syzygies in algebraic geometry, 


* [[D.Eisenbud]], _The Geometry of Syzygies_, Graduate Texts in Mathematics, vol. 229, Springer, 2005. 


[[!redirects syzygies]]

[[!redirects Hilbert's syzygy theorem]]












