#Definition#

A **von Neumann algebra** is a unital $*$-subalgebra of the algebra of bounded operators on a complex [[Hilbert space]], which is closed in weak operator topology. Clearly, they are automatically closed in norm topology, hence they form a (particularly nice) class of $C^*$-[[C*-algebra|algebras]]. 

#Relevance#

The [[Gelfand-Naimark theorem|Gel'fand–Naimark theorem]] states that there is a contravariant [[equivalence of categories|equivalence]] between the category of commutative von Neumann algebras and the category of localizable [[measurable space|measurable spaces]]; that is, the [[opposite category]] of one is equivalent to the other. General von Neumann algebras are seen then as a 'noncommutative' measurable spaces in a sense analogous to [[noncommutative geometry]].

The importance of von Neumann algebras for ([[higher category theory|higher]]) [[category theory]] and topology lays in the evidence that von Neumann algebras are deeply connected with the low dimensional [[quantum field theory]] (2d CFT, TQFT in low dimensions, inclusions of factors, quantum groups and knot theory; elliptic [[cohomology]]: works of Wenzl, Vaughan Jones, Anthony Wasserman, Kerler, Kawahigashi, Ocneanu, Szlachanyi etc.). 

The highlights of their structure theory include the results on classification of factors (A. Connes, 1970s) and theory of inclusions of subfactors (V. Jones). (Hilbert) bimodules over von Neumann algebras have a remarkable tensor product due Connes ([[Connes fusion]]). Following Segal's manifesto

* Graeme Segal, _Elliptic cohomology (after Landweber-Stong, Ochanine, Witten, and others)_. S&#233;minaire Bourbaki, Vol. 1987/88.  Ast&#233;risque  No. 161-162  (1988), Exp. No. 695, 4, 187--201 (1989).

and its update

* G. Segal, _What is an elliptic object?_  Elliptic cohomology,  306--317, London Math. Soc. Lecture Note Ser., 342, Cambridge Univ. Press, Cambridge, 2007. 

on hypothetical connections between CFT and elliptic cohomology, Stolz and Teichner have made a case for a role von Neumann algebras seem to play in a partial realization of that program:

* S. Stolz and P. Teichner, _What is an elliptic object?_ ([pdf](http://math.berkeley.edu/~teichner/Papers/Oxford.pdf))

See also the [Wikipedia entry](http://en.wikipedia.org/wiki/Von_Neumann_algebra) entry for more on von Neumann algebras and a list of references and links.

#Topics of interest for the understanding of AQFT
This paragraph will collect some facts of interest for the aspects of [[AQFT]] in the nLab.

In this paragraph $\mathcal{M}$ will always be a von Neumann algebra acting on a Hilbert space $\mathcal{H}$ with commutant $\mathcal{M}'$.

##Vectors

* Definition: A vector $x \in \mathcal{H}$ is **cyclic** if $\mathcal{M}x$ is dense in $\mathcal{H}$.

* Definition: A vector $x \in \mathcal{H}$ is **separating** if $M(x) = 0$ implies $M = 0$ for all $M \in \mathcal{M}$.

* Theorem: The notions of cyclic and separating are dual with respect to the commutant, that is a vector is cyclic for $\mathcal{M}$ iff it is separating for $\mathcal{M}'$.

##projections in von Neumann algebras
One crucial feature of von Neumann algebras is that they contain 
"every projection one could wish": there are three points that make this statement precise:

* the linear combinations of projections are norm dense in a von Neumann algebra

* Gleason's theorem

* Murray-von Neumann classification of factors 

### projections are norm dense
First let us note that every element $A$ of a von Neumann algebra can trivially be written as a sum of two selfadjoint elements:
$$
A = \frac{1}{2} (A + A^*) + \frac{1}{2} (A - A^*)
$$

Then, by the [[spectral theorem]] every selfadjoint element A is represented by it's spectral measure E via
$$
A = \integral_{-\|A\|}^{\|A\|} \lambda E(d\lambda)
$$
The integral converges in norm to A and all spectral projections are elements of the von Neumann algebra. It immediatly follows that the set of finite sums of multiples of projections are norm dense in every von Neumann algebra. 

### Gleason's theorem

* Wikipedia on [Gleason's theorem] (http://en.wikipedia.org/wiki/Gleason%27s_theorem)

### Murray-von Neumann classification of factors 
To be done...

#Remarks#

* Von Neumann algebras may also be defined abstractly as (abstract) $C^*$-algebras with a predual.

* Von Neumann algebras are also sometimes called $W^*$-algebras; they should not be confused with $W$-algebras in (logarithmic) conformal field theory.

* Combining the previous two remarks, some authors use '$W^*$-algebra' for the abstract concept and 'von Neumann algebra' for the concrete concept.  Equivalently, then, a von Neumann algebra is a $W^*$-algebra equipped with a free action on a Hilbert space (and it\'s a theorem that any $W^*$-algebra may be so equipped).

+-- {: .query}
[[Tim van Beek]]: I'm confused by the remarks, to my knowledge, the situation is this: $W^*$-algebra is the abstract concept, von Neumann algebra is the concrete concept, meaning that the definition of a von Neumann algebra needs a Hilbert space $\mathcal{H}$, so that it can be defined as a e.g. weakly closed subalgebra of $\mathcal{L}(\mathcal{H})$, the algebra of all bounded linear operators on $\mathcal{H}$. Without the Hilbert space you can't say what the weak topology should be.

According to

* Schaefer, Helmut H.; Wolff, M.P.: Topological vector spaces. 2nd ed., Springer 1999 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0983.46002&format=complete))

the situation is then this:

Definition:
A $W^*$-algebra is a $C^*$-algebra whose underlying normed space is a dual Banach space.

Theorem:
Every $W^*$-algebra is $W^*$-isomorphic to a von Neumann algebra ("on a suitable Hilbert space" is added in corollary 3 in paragraph 7.1, which is redundant however) and vice versa.

Any objections to change the remarks accordingly? 
=--

[[!redirects W*-algebra]]
[[!redirects W-star-algebra]]