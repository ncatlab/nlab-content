
#Contents#
* table of contents
{:toc}

## Idea

The [[moduli stack of formal groups]] $\mathcal{M}_{FG}$ admits a natural [[stratification]] whose open [[strata]] $\mathcal{M}^n_{FG}$ are labeled by a [[natural number]] called the _[[height of a formal group|height of formal groups]]_.

The [[deformation theory]] around these [[strata]] is _Lubin-Tate theory_. 

The universal Lubin-Tate deformation ring of a [[formal group]] of [[height of a formal group|height]] $n$ induces, via the [[Landweber exact functor theorem]] a [[complex oriented cohomology theory]], a localization of this is $n$th [[Morava E-theory]] $E(n)$.

## Lubin-Tate formal group

Let $k$ be a [[perfect field]] and fix a [[prime number]] $p$.

+-- {: .num_defn}
###### Definition

Write $W(k)$ for the [[ring of Witt vectors]] and 

$$
  R \coloneqq W(k)[ [ v_1, \cdots, v_{n-1} ] ]
$$

for the ring of [[formal power series]] over this ring, in $n-1$ [[variables]]; called the _Lubin-Tate ring_.

=--

There is a canonical [[morphism]]

$$
  p \;\colon\; R \longrightarrow k
$$

whose [[kernel]] is the [[maximal ideal]]

$$
  ker(p) \simeq (p,v_1, \cdots, v_{n-1})
  \,,
$$

This induces (...) for every [[formal group]] $f$ over $k$ a [[deformation]] $\overline{f}$ over $R$. This is the _[[Lubin-Tate formal group]]_.

## Lubin-Tate theorem

+-- {: .num_theorem}
###### Theorem

The [[Lubin-Tate formal group]] $\overline{f}$ is the [[universal property|universal]] deformation of $f$ in that for every [[infinitesimal object|infinitesimal thickening]] $A$ of $k$, $\overline{f}$ induces a [[bijection]]

$$
  Hom_{/k}(R,A) \stackrel{\simeq}{\longrightarrow} Def(A)
$$

between the $k$-[[associative algebra|algebra]]-[[homomorphisms]] from $R$ into $A$ and the [[deformations]] of $A$.

=--

(e.g. [Lurie 10, lect 21, theorem 5](#LurieLecture))

## Related concepts

* [[Lubin-Tate space]]

* [[Lubin-Tate formal group]]

* [[chromatic homotopy theory]]

* [[Morava E-theory]]

## References

* {#LurieLecture} [[Jacob Lurie]], Lecture 21 of: _[[Chromatic Homotopy Theory]]_, Lecture notes 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 21 _Lubin-Tate theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture21.pdf))
 
On the [[topological Hochschild homology]] of the Lubin-Tate ring spectrum via [[factorization homology]]:

* [[Geoffroy Horel]], *Higher Hochschild homology of the Lubin-Tate ring spectrum*, Algebr. Geom. Topol. **15** (2015) 3215-3252 &lbrack;[arXiv:1311.2805](https://arxiv.org/abs/1311.2805), [doi:10.2140/agt.2015.15.3215](https://doi.org/10.2140/agt.2015.15.3215)&rbrack;


[[!redirects Lubin-Tate spectrum]]

[[!redirects Lubin-Tate ring]]
[[!redirects Lubin-Tate rings]]

[[!redirects Lubin-Tate theorem]]
