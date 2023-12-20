
> This entry is about the concept in [[category theory]]. For the [[core of a ring]] see there.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{C}$ any [[category]] or, more generally, [[(n,r)-category]], its *core* is the maximal [[groupoid]] inside it, generally the maximal sub-[[(n,0)-category]], hence the maximal [[infinity-groupoid|$\infty$-groupoid]] inside it.

Since a [[functor]] out of a groupoid $\mathcal{G}$, and generally an [[(infinity,n)-functor|(n,r)-functor]] out of an [[infinity-groupoid|$\infty$-groupoid]], necessarily takes values in [[isomorphisms]] or generally in [[equivalences]], hence in the core of its [[codomain]], 

$$
  Cat_{n,r}
  \big(
    \mathcal{G}
    ,\,
    \mathcal{C}
  \big)
  \;\;
  \simeq
  \;\;
  Grpd_{n}
  \big(
    \mathcal{G}
    ,\,
    core(\mathcal{C})
  \big)
  \,,
$$

the core construction is the [[right adjoint]] to the [[full subcategory|full inclusion]] of [[groupoids]] among [[categories]] (generally: [[(n,0)-categories]] among [[(n,r)-categories]]):

$$
  Grpd_n
  \underoverset
    {\underset{core}{\longleftarrow}}
    {\overset{F}{\hookrightarrow}}
    {\bot}
  Cat_{n,r}
  \,.
$$

(Incidentally, the [[forgetful functor]] $F$ from $Grp$ to $Cat$ also has a [[left adjoint]], called the *[[free groupoid]]*-construction.)


## Definition

+-- {: .num_defn #CoreOfCategories}
###### Definition

For $C \in $ [[Cat]] a [[category]], its **core** $core(C) \in$ [[Grpd]]  
is the [[groupoid]] which is the maximal [[subcategory|sub]]-[[groupoid]] of $C$: the [[subcategory]] consisting of all objects of $C$ but with [[morphisms]] only the [[isomorphisms]] of $C$.

This construction extends to a 1-[[functor]]

$$
  Core \colon Cat \to Grpd
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

We usually think of a groupoid as a special kind of category, but we can also think of a category as a groupoid equipped with additional morphisms.  (This is possible because [[Grpd]] is a [[reflective subcategory]] of [[Cat]].)  One level [[decategorification|decategorified]], we usually think in the opposite way: a [[poset]] is a [[set]] equipped with a [[partial order]], but we can also think of a set as a special kind of poset (specifically, a [[symmetric relation|symmetric]] one).

=--

## Examples

\begin{example}
Given a [[preorder|preordered set]], regarded as a category, taking its core is the same as partitioning the set into [[equivalence classes]] of the preorder.
\end{example}

\begin{example}
The core of [[FinSet]] is known as the *[[permutation groupoid]]* or *[[symmetric groupoid]]* or similar.

A *[[combinatorial species]]* is a [[functor]] from the [[symmetric groupoid]] to [[Set]].
\end{example}


## Properties

### Universal property

+-- {: .num_prop }
###### Proposition

The core-functor of def. \ref{CoreOfCategories} is [[right adjoint]] to the [[full subcategory]]-inclusion $U \colon Grpd \to Cat$ of groupoids into categories. 

$$
  Grpd
  \underoverset
    {\underset{core}{\longleftarrow}}
    {\hookrightarrow}
    {\bot}
  Cat
  \,.
$$

=--

+-- {: .proof}
###### Proof

Given a [[category]] $C$ and a [[groupoid]] $A$, a [[functor]]

$$
 A \to C
$$

(hence a functor out of the underlying category $U(A)$ of $A$)
has to send [[isomorphisms]] to isomorphisms, hence has to send every [[morphism]] of $A$ to an [[isomorphism]] in $C$. This means that it factors through the core-inclusion

$$
  A \to Core(C) \to C
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The [[left adjoint]] to $U \colon Grpd \to Cat$ is the [[localization]] functor that universally inverts every morphism in $C$. On [[nerves]] this is [[Kan fibrant replacement]].

=--



## Variations and generalizations

### $\dagger$-Categories

The __core__ of a [[dagger category]] consists of its [[unitary morphism|unitary]] isomorphisms only.  This is why, for example, it makes sense to think of [[Hilb]] either as a category whose morphisms are linear maps bounded by $1$ or as a dagger category whose morphisms are all linear maps; either way, the core is the same (invertible linear maps of norm exactly $1$).


### Higher categories

The __core__ of an $n$-[[n-category|category]] is the $n$-[[n-groupoid|groupoid]] consisting only of [[equivalence]]s at each level; the __core__ of an $\infty$-[[infinity-category|category]] is similarly an $\infty$-[[infinity-groupoid|groupoid]]: the core of a [[quasicategory]] is the maximal [[Kan complex]] inside it.

For more on this see also at _[[category object in an (infinity,1)-category]]_.

## Related concepts

* [[free groupoid]], [[free category]]

* [[core in a 2-category]]

* [[decategorification]]


## References

* [[Pierre Gabriel]], [[Michel Zisman]], §1.5.4 of: *[[Calculus of fractions and homotopy theory]]*, Ergebnisse der Mathematik und ihrer Grenzgebiete **35**, Springer (1967) &lbrack;[doi:10.1007/978-3-642-85844-4](https://link.springer.com/book/10.1007/978-3-642-85844-4), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf)&rbrack;


Discussion in the generality of [[(infinity,n)-categories|$(\infty,n)$-categories]]:

* {#Lurie09} [[Jacob Lurie]], Around Prop. 1.1.14 in: _[[(∞,2)-Categories and the Goodwillie Calculus]]_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 

[[!redirects core groupoids]]

[[!redirects core]]
[[!redirects cores]]

[[!redirects underlying groupoid]]
[[!redirects underlying groupoids]]

[[!redirects maximal subgroupoid]]
[[!redirects maximal subgroupoids]]
[[!redirects maximal sub-groupoid]]
[[!redirects maximal sub-groupoids]]

[[!redirects groupoid core]]
[[!redirects groupoid cores]]

