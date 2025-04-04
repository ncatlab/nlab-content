+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Categories of simplices
* table of contents
{: toc}

## Idea

For $X$ a [[simplicial set]] its _category of simplices_ is the [[category]] whose [[objects]] are the [[simplices]] _in_ $X$ and whose [[morphisms]] are maps between these, as simplices in $X$.

In particular the [[subcategory]] on the non-degenerate simplices has a useful interpretation: it is the [[poset]] of subsimplex inclusions whose [[nerve]] is the [[barycentric subdivision]] of $X$, at least if every non-degenerate simplex in $X$ comes from a monomorphism $\Delta^n \to X$, as for a [[simplicial complex]].


## Definition

Let $X \in $ [[sSet]] be a [[simplicial set]].

+-- {: .num_defn}
###### Definition

The **category of simplices** of $X$ is equivalently (in increasing order of explicitness)

* the [[category of elements]] of the [[presheaf]] $X_\bullet : \Delta^{op} \to Set$;

* the [[comma category]] $(\Delta\downarrow X)$, where $\Delta$ denotes the [[Yoneda embedding]] $[n] \mapsto \Delta^n$.

* the [[category]] whose [[objects]] are [[homomorphisms]] of simplicial sets $c : \Delta^n \to X$ from a standard simplicial [[simplex]] $\Delta^n$ to $X$, and whose morphisms $c \to c'$ are morphisms $f : \Delta^n \to \Delta^{n'}$ in the [[simplex category]] $\Delta$ such that the [[diagram]]

  $$
    \array{ 
      \Delta^n 
        &&
        \stackrel{f}{\longrightarrow}
        && 
      \Delta^{n'}
      \\
      & {}_{c}\searrow && \swarrow_{c'}  
      \\
      && X
    }
  $$
 
  [[commuting diagram|commutes]].

=--

+-- {: .num_defn #BarycentricSubdivision}
###### Definition
  

An $n$-[[simplex]] $x\in X_n$ is said to be *non-degenerate* if it is not in the image of any degeneracy map.  

Write 

$$
  (\Delta\downarrow X)_{nondeg}\hookrightarrow (\Delta\downarrow X)
$$ 

for the (full) subcategory on the non-degenerate simplices.
Notice that a morphism of $\Delta\downarrow X$ with source
a non-degenerate simplex of $X$ is necessary a [[monomorphism]].

This is called the **category of non-degenerate simplices**.

=--

+-- {: .num_remark}
###### Remark

If every non-degenerate simplex in $X$ comes from a [[monomorphism]] $\Delta^n \to X$, then the [[nerve]] $N((\Delta \downarrow X)_{nondeg})$ is also called the **[[barycentric subdivision]]** of $X$.

=--

See at _[barycentric subdivision -- Relation to the category of simplices](subdivision#RelationToCategoryOfSimplices)_.


## Properties

### General

+-- {: .num_prop}
###### Proposition

If $X$ has the property that every face of every non-degenerate simplex is again non-degenerate, then the inclusion of the category of non-degenerate simplices $(\Delta \downarrow X)_{nondeg} \hookrightarrow (\Delta \downarrow X)$ has a [[left adjoint]] and is hence a [[reflective subcategory]].

=--

+-- {: .num_prop}
###### Proposition

The category of simplices is a [[Reedy category]].

=--

### Colimits

Write $(\Delta \downarrow X) \to sSet$ for the canonical functor
that sends $(\Delta^n \to X)$ to $\Delta^n$.

+-- {: .num_prop #ColimitOverSimplicesOfXIsX}
###### Proposition

The [[colimit]] over the [[functor]] $(\Delta \downarrow X) \to sSet$ is $X$ itself

$$
  X \simeq \underset{\to}{\lim}((\Delta \downarrow X) \to sSet)
$$

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]].

=--

In the textbook literature this appears for instance as ([Hovey, lemma 3.1.3](#Hovey)).

+-- {: .num_cor}
###### Corollary

A colimit-preserving [[functor]] $F\colon sSet \to C$ is uniquely determined by its action on the standard simplices:
$$ F(X) \cong colim_{(\Delta\downarrow X)} F(\Delta^\bullet). $$

=--

+-- {: .num_example}
###### Example

Important colimit-preserving functors out of [[sSet]] include

* [[geometric realization]] of simplicial sets
* [[subdivision]] of simplicial sets
* the [[left adjoint]] to the [[nerve]] functor $N:Cat \to SSet$
* the category of simplices itself, as a functor $SSet \to Cat$; see [category of elements -- colimit preserving](category+of+elements#ColimitPreserving).

=--

### The nerve and subdivision

Let $N\colon$ [[Cat]] $\to$ [[sSet]] denote the simplicial [[nerve]] functor on [[categories]].

+-- {: .num_theorem}
###### Theorem

The functor $sSet \to sSet$ that assigns [[barycentric subdivision]], def. \ref{BarycentricSubdivision},

$$
  X\mapsto N(\Delta\downarrow X)
$$ 

preserves [[colimits]].

=--
+-- {: .proof}
###### Proof

An $n$-[[simplex]] of $N(\Delta\downarrow X)$ is determined by a string of $n+1$ composable morphisms
$$ \Delta^{k_n} \to \dots\to \Delta^{k_0} $$
along with a map $\Delta^{k_0} \to X$, i.e. an element of $X_{k_0}$
Thus, each the functor $X\mapsto N(\Delta\downarrow X)_n$ from $SSet \to Set$ is a coproduct of a family of "evaluation" functors.
Since evaluation preserve colimits, coproducts commute with colimits, and colimits in $SSet$ are levelwise, the statement follows.

=--

Therefore, the simplicial set $N(\Delta\downarrow X)$ itself can be computed as a colimit over the category $(\Delta\downarrow X)$ of the simplicial sets $N(\Delta\downarrow \Delta^n)$.




## References

The terminology "category of simplices" is attributed by [Hovey 1999](#Hovey99) to:

* [[William G. Dwyer]], [[Philip S. Hirschhorn]], [[Daniel M. Kan]], Section 5.9 of: *[[Model Categories and More General Abstract Homotopy Theory]]* (1997) &lbrack;[pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/dhk.pdf), [[DwyerHirschhornKan-ModelCategories.pdf:file]]&rbrack;

Textbook account:

* {#Hovey99} [[Mark Hovey]], Section 3.1 (specifically [p. 75](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf#page=85)) in: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;


[[homotopy final functor|Homotopy finality]] of the non-degenerate simplices:

* {#Lurie} [[Jacob Lurie]], Prop. 4.2.3.14 ([p. 254](https://www.math.ias.edu/~lurie/papers/HTT.pdf#page=272)) of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;


More on [[barycentric subdivision]]:

* [[J. F. Jardine]], Section 2 of: *Simplicial approximation*, Theory and Applications of Categories, **12** 2 (2004) 34-72 &lbrack;[tac:12-02](http://www.tac.mta.ca/tac/volumes/12/2/12-02abs.html)&rbrack;


[[!redirects category of simplices]]
[[!redirects category of simplicies]]
[[!redirects categories of simplices]]

[[!redirects category of nondegenerate simplices]]
[[!redirects categories of nondegenerate simplices]]
[[!redirects category of non-degenerate simplices]]
[[!redirects categories of non-degenerate simplices]]
