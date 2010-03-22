# Idea

FOLDS (first-order logic with dependent sorts) is a form of ([[intuitionistic logic|intuitionistic]] or [[classical logic|classical]]) [[predicate logic|predicate]] [[logic]] with a weak form of [[equality]], in which [[category theory]] (and even [[higher category theory]]) can be formulated but it is impossible to say anything [[evil]].  It also induces general notions of [[equivalence]] for higher structures and for objects *in* higher structures, which reduce to familiar notions in most or all cases.

Formally speaking, FOLDS is "merely" a "first-order fragment" of [[dependent type theory]], but its special treatment of equality, its notions of equivalence, and its relationship to higher-categorical structures distinguish it from DTT in general.  These aspects have been developed primarily by [[Michael Makkai]].

# Signatures

FOLDS can be formulated using dependent types, terms, contexts, and judgments, as is typical in [[type theory]].  However, it is perhaps easier for a category theorist to understand when presented as the study of the [[presheaves]] which underlie higher-categorical structures.

Both [[algebraic definition of higher category|algebraic]] and [[geometric definition of higher category|geometric]] definitions of higher-categorical structures are generally specified by giving a presheaf on some small category $D$ (such as a category of [[geometric shapes for higher structures]]), which satisfies certain [[stuff, structure, property|properties]] or is equipped with certain [[stuff, structure, property|structure]].  The category $D$ in question is usually a [[Reedy category]], and as such comes equipped with a stratification of its objects by "degree," and a division of its morphisms into "coface maps," which raise degree, and "codegeneracy maps," which lower degree.  The perspective of FOLDS is that actually the codegeneracy maps should be regarded as part of the *structure* imposed (when present, they usually assign "identities"), while the coface maps are what really describe the "geometric shape" or "dependency structure."  Note that in some cases, such as [[opetopic sets]] and [[globular sets]], there are no degeneracies to start with.

This suggests that FOLDS should study presheaves on some [[direct category]], or equivalently (changing the variance) $Set$-valued diagrams on some [[inverse category]].  If $C$ is an inverse category and $x\in C$ an object, then $x$ represents one geometric shape appearing in the structures under consideration, while all of the morphisms *out* of $x$ indicate the lower-dimensional "faces" of such a shape, i.e. the "boundary" which it fills.  However, for an arbitrary inverse category, a given shape can still have infinitely many faces in its boundary; this is difficult to deal with in logic, so we impose the extra requirement that the category have **finite fan-out**: every object $x$ is the [[source]] of only finitely many arrows altogether.  A category with finite fan-out is an inverse category iff it is also both [[skeleton|skeletal]] and [[one-way category|one-way]] (every endomorphism is an identity); thus we study skeletal one-way categories with finite fan-out.  In FOLDS these are called **simple categories**.

A FOLDS signature, or vocabulary, should then consist of a simple category of *kinds*, together with information about [[function]] and [[relation]] symbols.  However, it turns out to be easier to include *only* relation symbols; the values of functions can then be recovered as the unique objects satisfying some relation, or more generally as unique-up-to-equivalence objects equipped with some higher structure (cf. [[anafunctor]], for instance).  One reason relation symbols are easier is that they can be represented simply as additional "shapes," whose boundary consists of those elements which they relate.  Such a shape should be *maximal*, in the sense that it is not the target of any nonidentity arrow.  Thus,

* A **FOLDS signature** or **vocabulary for dependent sorts (DSV)** consists of a simple category together with a distinguished set of maximal objects, called the **relation symbols**.  The objects that are not relation symbols are called **kinds**.

# Examples

...

# Equivalences

...

# References

*  First Order Logic with Dependent Sorts, with Applications to Category Theory, available from [Makkai\'s homepage](http://www.math.mcgill.ca/makkai/).
