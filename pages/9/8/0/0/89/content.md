
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the original sense, a _Morita equivalence_ between two [[rings]] is two [[bimodules]] between them that behave as [[inverses]] to each other under [[tensor product of modules]], up to isomorphism of bimodules. This is just the [[equivalence in a 2-category|2-categorical concept of equivalence]] for the two rings regarded as [[objects]] in the [[2-category]] of rings, with [[bimodules]] as [[1-morphisms]] and bimodule homomorphisms ([[intertwiners]]) as [[2-morphisms]] (see [here](bimodule#AsMorphismsInA2Category)).
By the [[Eilenberg-Watts theorem]] any such pair of bimodules equivalently induces a suitably "linear" [[equivalence of categories]] between the [[categories of modules]] over the given rings.
 
This is the original concept equivalence of rings due to [[Kiiti Morita]] (see [below](#ClassicalMoritaTheorem)).


Nowadays, the term is applied in different but closely related senses in a wide range of mathematical fields, and one speaks of _Morita equivalent_ [[categories]], [[algebraic theories]], [[geometric theories]] and so on.

Typically, such Morita situations involve three ingredients: a 'syntactic' ground level to which the respective concept of _Morita equivalence_ applies, a 'hypersyntactic' level that obtains from an 'idempotent' completion, and a second process of completion to a 'semantic' level where the equivalence relation for the syntactic ground level is defined by plain equivalence of category e.g. Morita equivalence for _small categories_ is defined as equivalence of their presheaf categories with [[Cauchy completion]] as intermediate hypersyntactic level.

So the broad intuition is that Morita equivalence is a _coarse grained semantic equivalence that obtains between syntactic gadgets_ - basically two [[theories]] that have up to equivalence the same category of [[models]]. The role of the intermediate hypersyntactic level in this analogy is that of an 'ideal syntax' (syntax classifier) that already reflects the relations at the semantic level. The categorical equivalence (via bimodules)  from the semantic level then shows up at the intermediate level as a ('Cauchy convergent'$\sim$ 'fgp-module') bidirectional _translation_ from one syntax into another.

## Classical Morita theorem
 {#ClassicalMoritaTheorem}

Given [[rings]] $R$ and $S$, the following properties are equivalent

1. The categories of left $S$-[[modules]] and left $R$-modules are [[equivalence of categories|equivalent]];

1. The categories of right $S$-modules and right $R$-modules
are equivalent;

1. There are [[bimodules]] ${}_R M_S$ and ${}_S N_R$ such that $\otimes_R M$ and $\otimes_S N$ form an [[adjoint equivalence]] between the category of right $S$- and the category of right $R$-modules;


1. The ring $R$ is isomorphic to the endomorphism ring of a finitely generated projective [[generator]] in the category of left (or right) $S$-modules;
1. The ring $S$ is isomorphic to the endomorphism ring of a finitely generated projective [[generator]] in the category of left (or right) $R$-modules.

An important weakening of the Morita equivalence is [[Morita context]] (in older literature sometimes called pre-equivalence).

## Definitions

### In algebra

Two rings are **Morita equivalent** if the equivalent statements in the Morita theorem above are true. A **Morita equivalence** is an [[equivalence in a 2-category]] in the [[bicategory]] $\mathrm{Rng}$ of [[rings]], [[bimodules]] as [[1-morphisms]] and bimodule homomorphisms ("[[intertwiners]]" as [[2-morphisms]]).

A theorem in ring theory says that the [[center]] of a ring is isomorphic to the center of its category of modules and that Morita equivalent rings have isomorphic centers. Especially, two _commutative_ rings are Morita equivalent precisely when they are isomorphic!

This shows that the property of _having center $Z$ up to isomorphism_ is stable within Morita equivalence classes. Properties of this kind are sufficiently important to deserve a special name:

A property $P$ of rings is called a **Morita invariant** iff whenever $P$ holds for a ring $R$, and $R$ and $S$ are Morita equivalent then $P$ also holds for $S$. Another classical example is the property of being [[simple ring|simple]]. (cf. Cohn 2003)

### In homotopy theory 

In any [[homotopy theory]] framework a **Morita equivalence** between objects $C$ and $D$ is  a span 
$$
  C \lt \stackrel{\simeq}{\leftarrow}
  \hat C
  \stackrel{\simeq}{\to} \gt
  D
$$
where both legs are acyclic fibrations.


In particular, if the ambient [[homotopical category]] is a [[category of fibrant objects]], then the _factorization lemma_ (see there) ensures that _every_ weak equivalence can be factored as a span of acyclic fibrations as above. 

Important fibrant objects are in particular [[infinity-groupoid]]s (for instance [[Kan complex]]es are fibrant in the standard [[model structure on simplicial sets]] and [[omega-groupoid]]s are fibrant with respect to the Brown-[[Golasinski]] [[folk model structure]]). And indeed, Morita equivalences play an important role in the theory of groupoids with extra structure:

### In Lie groupoid theory 

A **[[Morita morphism]] equivalence** of [[Lie groupoids]] is an [[anafunctor]] that is invertible, equivalently an invertible [[Hilsum-Skandalis morphism]]/[[bibundle]].

Lie groupoids up to Morita equivalence are equivalent to [[differentiable stack]]s. This relation between Lie groupoids and their stacks of torsors is analogous to the relation between algebras and their categories of modules, which is probably the reason for the choice of terminology.

### In tensor category theory 

A [[fusion category]] $\mathcal{C}$ is Morita equivalent to another fusion category $\mathcal{D}$ if there exist a $\mathcal{C}$-module category $\mathcal{M}$ such that $\mathcal{D}$ is equivalent to the [[reverse category]] of $\mathcal{C}$-module functors from $\mathcal{M}$ to itself, namely 
$$\mathcal{D}\simeq (\mathcal{C}_{\mathcal{M}}^{\vee})^{rev}:=\mathsf{Fun}_{\mathcal{C}}(\mathcal{M},\mathcal{M})^{rev}.$$
By the 'reverse category' of a monoidal category $\mathcal{C}$ we mean the monoidal category with reversed [[tensor product]] $x\otimes^{rev}y:=y \otimes x$. 

## Related Concepts

* [[derived Morita equivalence]]
* [[Morita context]]
* [[Eilenberg-Watts theorem]]
* [[generator]]
* [[bimodule]]
* [[projective module]]
* [[Picard group]]
* [[bicategory]]
* [[Cauchy completion]]


## References

The concept is named after [[Kiiti Morita]].

A beautiful classical exposition is in  

* [[Hyman Bass]], chapter II of _Algebraic K-theory_, Benjamin 1968.

The concept should be covered in any decent textbook on algebra and ring theory, e.g.:

* P. M. Cohn, _Further algebra and applications_ , Springer Heidelberg 2003. (sec. 4.4-4.5 pp.148ff)

* [[Ross Street]], _Quantum Groups - A Path to Current Algebra_ , Cambridge UP 2007. ([ps-draft](http://www-texdev.ics.mq.edu.au/Quantum/Quantum.ps))

For an early extension to domains other than ring theory see

* H. Lindner, _Morita equivalences of enriched categories_ , Cah. Top. G&#233;om. Diff. Cat **15** no.4 (1974) pp.377-397. ([pdf](http://archive.numdam.org/article/CTGDC_1974__15_4_377_0.pdf))

The generalizations to graded rings, Hopf algebras and corings are studied in references 

* A. Marcus, _Equivalences induced by graded bimodules_, Comm. Algebra 26 (1998) 713–731; _Homology of fully graded algebras, Morita and derived equivalences_, J. Pure Appl. Alg. __133__:1–2 (1998) 209-218 <a href="https://doi.org/10.1016/S0022-4049(97)00196-5">doi</a>
* S. Caenepeel, J.Vercruysse, Shuanhong Wang, _Morita theory for corings and cleft entwining structures_, J. Algebra __276__1 (2004) 210-235 [doi](https://doi.org/10.1016/j.jalgebra.2004.02.002)
* [[Stefaan Caenepeel]], Septimiu Crivei, Andrei Marcus, [[Mitsuhiro Takeuchi]], _Morita equivalences induced by bimodules over Hopf–Galois extensions_, J. Algebra __314__ (2007) 267–302 [pdf](https://core.ac.uk/download/pdf/81180359.pdf)
* Gabriella Böhm, Joost Vercruysse, _Morita theory for comodules over corings_,  3207-3247 (2009)  Commun. Alg. __37__:9 (2009) [doi](https://doi.org/10.1080/00927870902747993 )


The case of algebraic theories is covered in

* [[Francis Borceux|F. Borceux]], _Handbook of Categorical Algebra 2_ , CUP 1994. (sec. 3.12)

* [[Jiri Adamek|J. Adámek]], M. Sobral, L. Sousa, _Morita equivalence of many-sorted algebraic theories_ , JA **297** (2006) pp.361-371. ([preprint](https://estudogeral.sib.uc.pt/bitstream/10316/4616/1/filee8df8c9585d34e1a8d56fdaf0460d008.pdf))

For the use in O. Caramello's 'toposes as bridges'- approach that brings out the logical side of the concept:

* [[Olivia Caramello|O. Caramello]], _Topos-theoretic background_ , ms. 2014. ([pdf](http://www.oliviacaramello.com/Unification/ToposTheoreticPreliminariesOliviaCaramello.pdf))

Other references include

* [[Ralf Meyer]], _Morita equivalence in algebra and geometry_ . ([[MeyerMoritaEquivalence.pdf:file]])

* I. Dell'Ambrogio, [[Goncalo Tabuada]], _A Quillen model structure for classical Morita theory and a tensor categorification of the Brauer group_ , arXiv:1211.2309 (2012). ([pdf](http://arxiv.org/pdf/1211.2309v1))

* [[Hans Porst]], _Generalized Morita Theories: The power of categorical algebra_, ([pdf](http://www.math.uni-bremen.de/~porst/dvis/SAMSnoticesCorr.pdf))

* [[Francis Borceux]] and [[Enrico Vitale]], _On the notion of bimodel for functorial semantics_, Appl. Categ. Structures, __2__:283&#8211;295 (1994) [pdf](http://perso.uclouvain.be/enrico.vitale/BimodAPCS.pdf)

See also

* wikipedia, _[Morita equivalence](http://en.wikipedia.org/wiki/Morita_equivalence)_

[[!redirects Morita equivalences]]
[[!redirects Morita equivalent]]