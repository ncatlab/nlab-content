## Idea

Maharam's theorem states a complete classification of isomorphism classes of the appropriate [[categories of measure theory|category of measurable spaces]].

In the case of [[σ-finite measure spaces]], the theorem classifies them up to an isomorphism, where an isomorphism is an equivalence class of measurable bijections $f$ with measurable inverse such that $f$ and $f^{-1}$ preserve measure 0 sets.

As explained in the article [[categories of measure theory]], for a truly general, unrestricted statement for non-[[σ-finite measure spaces]] there are additional subtleties to consider: equality almost everywhere must be refined to weak equality almost everywhere, and [[σ-finite measure spaces]] should be replaced by Marczewski-compact strictly localizible measure spaces.

In this unrestricted form, by the [[Gelfand-type duality for commutative von Neumann algebras]], Maharam's theorem also classifies isomorphism classes of [[localizable Boolean algebras]], [[abelian von Neumann algebras]], and [[hyperstonean spaces]] (or [[hyperstonean locales]]).  (In particular, the original formulation in the 1942 paper by Maharam uses measure algebras, i.e., Boolean algebras of measurable subsets modulo measure 0 subsets.)

## Statement

Every object in one of the above equivalent categories canonically decomposes as a [[coproduct]] (disjoint union)  of ergodic objects.  Here an object $X$ is ergodic if the only subobjects of $X$ invariant under all automorphisms of $X$ are $\emptyset$ and $X$ itself.

Furthermore, an ergodic object $X$ is (noncanically, using the [[axiom of choice]]) isomorphic to $\mathfrak{c}\times 2^\kappa$, where $\kappa$ is 0 or infinite, and $\mathfrak{c}$ is infinite if $\kappa$ is infinite.
Here the cardinal $\mathfrak{c}$ is known as the _cellularity_ of $X$ and $\kappa$ is its _Maharam type_.

In particular, if $\kappa=0$, we get a classification of isomorphism classes of atomic measure spaces: they are classified by the cardinality $\mathfrak{c}$ of their set of atoms.

Otherwise, $\kappa$ is infinite, and we get a classification of isomorphism classes of ergodic atomless (or diffuse) measure spaces: such spaces are isomorphic to $\mathfrak{c}\times 2^\kappa$, where $\mathfrak{c}$ and $\kappa$ are infinite cardinals.

Thus, a completely general object $X$ has the form
$$\coprod_\kappa \mathfrak{c}_\kappa\times 2^\kappa,$$
where $\kappa$ runs over 0 and all infinite cardinals, $\mathfrak{c}_\kappa$ is a cardinal that is infinite or 0 if $\kappa\ne0$, and $\mathfrak{c}_\kappa\ne0$ only for a set of $\kappa$.

## References

The original reference is

* [[Dorothy Maharam]], _On homogeneous measure a     lgebras_, Proc. Nat. Acad. Sci. U.S.A. 28 (1942) 108-111.  [doi](https://doi.org/10.1073/pnas.28.3.108).

A modern exposition can be found in Chapter 33 (Volume 3, Part I) of

* [[David H. Fremlin]], _[[Measure Theory]]_.

