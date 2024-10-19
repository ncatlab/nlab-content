## Idea

Maharam's theorem states a complete classification of isomorphism classes of the appropriate [[categories of measure theory|category of measurable spaces]].

In the case of [[σ-finite measure spaces]], the theorem classifies them up to an isomorphism, where an isomorphism is an equivalence class of measurable bijections $f$ with measurable inverse such that $f$ and $f^{-1}$ preserve measure 0 sets.

As explained in the article [[categories of measure theory]], for a truly general, unrestricted statement for non-[[σ-finite measure spaces]] there are additional subtleties to consider: equality almost everywhere must be refined to weak equality almost everywhere, and [[σ-finite measure spaces]] should be replaced by Marczewski-compact strictly localizible measure spaces.
For the sake of brevity, we refer to such objects simply as __measure spaces__ below.  (As explained in detail in the article [[categories of measure theory]], the actual choice of a measure is immaterial for the discussion below, and all what really matters is the [[σ-ideal]] of sets of measure 0.)

In this unrestricted form, by the [[Gelfand-type duality for commutative von Neumann algebras]], Maharam's theorem also classifies isomorphism classes of [[localizable Boolean algebras]] (equivalently: [[measurable locales]]), [[abelian von Neumann algebras]], and [[hyperstonean spaces]] (or [[hyperstonean locales]]).  (In particular, the original formulation in the 1942 paper by Maharam uses measure algebras, i.e., Boolean algebras of measurable subsets modulo measure 0 subsets.)

## Statement

Every measure space canonically decomposes as a [[coproduct]] (disjoint union)  of ergodic measure spaces.  Here a measure space $X$ is __ergodic__ if the only subobjects of $X$ (i.e., equivalence classes of measurable subsets modulo measure 0 subsets) invariant under all automorphisms of $X$ are $\emptyset$ and $X$ itself.

Furthermore, an ergodic measure space $X$ is (noncanically, using the [[axiom of choice]]) isomorphic to $\mathfrak{c}\times 2^\kappa$, where $\kappa$ is 0 or infinite, and $\mathfrak{c}$ is infinite if $\kappa$ is infinite.
Here the cardinal $\mathfrak{c}$ is known as the _cellularity_ of $X$ and $\kappa$ is its _Maharam type_.

In particular, if $\kappa=0$, we get a classification of isomorphism classes of atomic measure spaces: they are classified by the cardinality $\mathfrak{c}$ of their set of atoms.

Otherwise, $\kappa$ is infinite, and we get a classification of isomorphism classes of ergodic atomless (alias diffuse) measure spaces: such spaces are isomorphic to $\mathfrak{c}\times 2^\kappa$, where $\mathfrak{c}$ and $\kappa$ are infinite cardinals.

For $\kappa=\aleph_0$, we get $2^\kappa\cong\mathbf{R}$, the real line.
For $\kappa\gt\aleph_0$, we get non-[[σ-finite measure spaces]], which occur naturally in [[stochastic processes]].

Thus, a completely general object $X$ has the form
$$A\sqcup\coprod_\kappa \mathfrak{c}_\kappa\times 2^\kappa,$$
where $A$ is a discrete measure space, $\kappa$ runs over all infinite cardinals, $\mathfrak{c}_\kappa$ is an infinite cardinal or 0, and $\mathfrak{c}_\kappa\ne0$ only for a set of cardinals $\kappa$.

Such an object $X$ is a [[σ-finite measure space]] if and only if $A$ and $\mathfrak{c}_{\aleph_0}$ are countable and for every $\kappa\gt\aleph_0$ we have $\mathfrak{c}_\kappa=0$.

## Relative version

There is also a relative version of Maharam's theorem, which classifies morphisms in any of the equivalent categories considered above.

Observe that morphisms $2^\kappa\to2^\lambda$ exist if and only if $\kappa\ge\lambda$.
For example, there are no morphisms from the terminal space $2^0$ (i.e., a singleton) to the real line $\mathbf{R}\cong 2^{\aleph_0}$, since the image of such a point is a measure 0 subset, whose preimage therefore cannot have measure 0.  In the language of [[commutative von Neumann algebras]], this translates to saying that there are no normal \*-homomorphisms $L^\infty(\mathbf{R})\to\mathbf{C}$.

Observe also that we have a natural notion of locality for a measure space: a covering family is given by a family of measurable subsets whose [[essential supremum]] equals the entire space.  (This is more than just an analogy to open covers in [[topological spaces]]: when translated to the language of [[locales]], the two notions become identical.)
In fact, thanks to the very special nature of measure spaces, it suffices to consider only _disjoint_ covers, since every covering family as defined above can be refined by a disjoint family.  Maharam's theorem can be now formulated by saying that a 

With these two observations in mind, we can succinctly formulate the relative Maharam theorem as follows: every morphism $f\colon X\to Y$ locally in $X$ and $Y$ is isomorphic to a morphism of the form $2^\kappa\to2^\lambda$, where $\kappa\ge\lambda$ and the map is given by projecting to the first $\lambda$ coordinates.

## References

The original reference is

* [[Dorothy Maharam]], _On homogeneous measure a     lgebras_, Proc. Nat. Acad. Sci. U.S.A. 28 (1942) 108-111.  [doi](https://doi.org/10.1073/pnas.28.3.108).

A modern exposition can be found in Chapter 33 (Volume 3, Part I) of

* [[David H. Fremlin]], _[[Measure Theory]]_.

