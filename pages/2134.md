
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Schur's lemma is one of the fundamental facts of [[representation theory]]. It concerns basic properties of the [[hom-sets]] between [[irreducible representations|irreducible]] [[linear representations]] of [[groups]]. 

The lemma consists of two parts that depend on different assumptions (a distinction often not highlighted in the literature): 

1. The first statement applies over _every_ [[ground field]]: 

   It says that there are no non-[[zero morphism|zero]] [[homomorphisms]] between distinct (i.e. non-[[isomorphism|isomorphic]]) [[irreducible representations]] 

1. The second statement applies only in the special case that the [[ground field]] is an [[algebraically closed field]] (such as the [[complex numbers]]) and that the [[representations]] are [[finite dimensional vector space|finite-dimensional]]: 

   It says that, in this case, moreover the only non-trivial [[endomorphisms]] of an [[irreducible representation]] are multiples of the [[identity morphism]].



## Statement

Let $G$ be a [[group]]. In the following:

* "representation" means _[[linear representation]] of $G$_, linear over some [[ground field]]. 

* "finite dimensional representation" means that the underlying [[vector space]] is a [[finite-dimensional vector space]].

An

* _[[irreducible representation]]_ is one whose only $G$-[[invariant]] [[subspaces]] are the trivial degenerate cases: the [[zero object|zero]]-subspace and the full space itself.

+-- {: .num_prop}
###### Proposition
**(Schur's lemma)**

1. A [[homomorphism]] $\phi \;\colon\; V\to W$ between [[irreducible representations]], is either the [[zero morphism]] or an [[isomorphism]]. 

   It follows that the [[endomorphism ring]] of an [[irreducible representation]] is a [[division ring]].

2. In the case that the [[ground field]] is an [[algebraically closed field]]; [[endomorphisms]] $\phi \;\colon\; V \to V$ of a [[finite-dimensional vector space|finite dimensional]] [[irreducible representations]] $V$ are a multiple $c \cdot id$ of the [[identity morphism|identity operator]]. 

   In other words, nontrivial automorphisms of irreducible representations, _a priori_ possible by (1), are ruled out over algebraically closed fields.  

=--

## Proof

As it goes with very fundamental lemmas, the [[proof]] of Schur's lemma follows by elementary inspection.

For the first statement:

It is immediate to see that both the [[kernel]] as well as [[image]] of a [[homomorphism]] 

$$
  V \overset{f}{\longrightarrow} W
$$

of any $G$-[[representations]] are $G$-[[invariant]] [[subspaces]]. But by the very definition of [[irreducible representation|irreducibility]], the only such subspaces of $V$ and $W$ are the degenerate ones: their zero subspaces and the full spaces themselves.

Now if the [[kernel]] is all of $V$ or the [[image]] is [[zero object|zero]], then $f$ is the [[zero morphism]]. The only case left is that the [[kernel]] is [[zero object|zero]] _and_ the [[image]] is all of $W$, but this means that $f$ is [[injective map|injective]] and [[surjective map|surjective]] and is hence an [[isomorphism]].

For the second statement:

Now we use that over an [[algebraically closed field]] $k$ of every [[linear map|linear]] [[endomorphism]] of a [[finite dimensional vector space]] has an [[eigenvalue]] $c \in k$ (which is, ultimately, due to the [[fundamental theorem of algebra]] for [[algebraically closed fields]]). Now, with $f$ also the linear combination

$$
  (f - c \cdot \mathrm{id}) \;\colon\; V \longrightarrow V
$$

is a [[homomorphism]] of $G$-[[representations]]. But then, by the first part, this must be an [[isomorphism]] or [[zero morphism|zero]]. But it is not an [[isomorphism]], by construction, since now the [[eigenvectors]] with [[eigenvalue]] $c$ are in the [[kernel]]. Therefore, all of the linear combination must be [[zero morphism|zero]]

$$
  f - c \cdot id = 0
$$

and hence

$$
  f = c \cdot id
$$

is a multiple of the identity.

## Interpretation in categorical algebra
 {#InterpretationInCategoricalAlgebra}

The statement of _Schur's lemma_ is particularly suggestive in the language of [[categorical algebra]].

Here it says that [[irreducible representations]] form a [[categorification|categorified]] _[[orthogonal basis]]_ for the [[2-Hilbert space]] of [[finite-dimensional vector space|finite-dimensional]] [[representations]], and even an _[[orthonormal basis]]_ if the [[ground field]] is [[algebraically closed field|algebraically closed]].

After [[decategorification]] this becomes equivalently the statement that the [[isomorphism classes]] of [[irreducible representations]] form an _[[orthogonal basis]]_ for the [[representation ring]], and even an _[[orthonormal basis]]_ if the [[ground field]] is [[algebraically closed field|algebraically closed]].

For more on this perspective see also at _[[Gram-Schmidt process]]_ the section _[Categorified Gram-Schmidt  process](Gram-Schmidt+process#CategorifiedGramSchmidtProcess)_.

$\,$

We now explain this perspective of in more detail:

$\,$

Notice that the [[hom-sets]] in a [[category of representations]] $G Rep$ are canonically [[vector spaces]]: given any two [[homomorphisms]] $f,g \;\colon\; V \to W$ of $G$-[[representations]], also the (value-wise) [[linear combination]] $c_1 f + c_2 g \;\colon\; V \to W$ is a $G$-homomorphism. ($G Rep$ is canonically [[enriched category|enriched]] over [[Vect]].)

Now it makes sense to regard this [[vector space]]-valued [[hom-functor]] on $G Rep$ as analogous

$$
  hom_G(-,-) \;\colon\; G Rep^{op} \times G Rep \longrightarrow Vect
$$

as a [[categorification|categorified]] [[inner product]] (see at _[[2-Hilbert space]]_ for more on this). 

This is a useful perspective even after [[decategorification]]:

For $V, W \in G Rep^{fin}$ two [[finite-dimensional vector space|finite-dimensional]] [[representations]], write  

$$
  \langle V,W\rangle
  \;\coloneqq\;
  dim\big( hom_G(-,-) \big)
  \;\in\;
  \mathbb{N}
$$

for the [[dimension]] of the vector space of homomorphism between them (e.g. [tom Dieck 09, p. 29](#tomDieck09)). 

This construction only depends on the [[isomorphism classes]] of $V$ and $W$, and hence descends to a [[function]]

$$  \langle -,-\rangle 
  \;\colon\; 
  G Rep^{fin}_{/\sim} \times G Rep^{fin}_{/\sim}
  \longrightarrow
  \mathbb{N}
$$

on [[sets]] of [[isomorphism classes]]. In fact, under [[direct sum]] and [[tensor product of representations]], $G Rep^{fin}_{/\sim}$ is a [[rig]], and this pairing is [[linear map|linear]] with respect to the underlying [[commutative monoid|additive monoid]] structure:

$$
  \left\langle
    V_1 \oplus V_2
    \,,\,
    W
  \right\rangle
  \;=\;
  \left\langle
    V_1 
    \,,\,
    W
  \right\rangle
  +
  \left\langle
    V_2
    \,,\,
    W
  \right\rangle
$$

and

$$
  \left\langle
    V
    \,,\,
    W_1 \oplus W_w
  \right\rangle
  \;=\;
  \left\langle
    V
    \,,\,
    W_1
  \right\rangle
  +
  \left\langle
    V
    \,,\,
    W_2
  \right\rangle
$$

(This is, ultimately, due to the [[universal property]] of [[direct sum]] as a [[biproduct]].)

To further strengthen the emerging picture, we may consider the [[group completion]] of the [[commutative monoid]] $G Rep^{fin}_{/\sim}$ by passing to its [[Grothendieck group]], in fact its [[Grothendieck ring]] if we remember also the [[tensor product of representations]]. This [[commutative ring]] is called the [[representation ring]]

$$
  R(G) \;\coloneqq\; K\left(  G Rep^{fin}_{/\sim} \right)
$$

of $G$. By the evident $\mathbb{Z}$-linear extension, the above pairing gives an actual symmetric $\mathbb{Z}$-[[bilinear map|bilinear]] [[inner product]] on $R(G)$:

\[
  \label{DecategorifiedInnterProduct}
  \langle
   -,- 
  \rangle
  \;\colon\;
  R(G) \times R(G)
  \longrightarrow 
  \mathbb{Z}
\]

Now  the underlying [[abelian group]] of $R(G)$ is a [[free abelian group]] whose canonical [[generators and relations|generators]] are nothing but the [[isomorphism classes]] $V_i$ of the [[finite-dimensional vector space|finite-dimensional]] [[irreducible representations]]:

$$
  R(G) \;\simeq_{\mathbb{Z}}\;  \mathbb{Z}\big[ \{V_i\}_i \big]
  \,.
$$

In summary, in the language of [[linear algebra]], the [[irreducible representations]] $[V_i]$ constitute a canonical _[[linear basis]]_ of the [[representation ring]].

In terms of this language, **Schur's lemma** becomes the following statement:

The canonical [[linear basis]] of the [[representation ring]] given by the [[irreducible representations]] is

1. generally: an _[[orthogonal basis|ortho-gonal basis]]_;

1. even an _[[orthonormal basis|ortho-normal basis]]_ if the [[ground field]] is [[algebraically closed field|algebraically closed field]]

with respect to the canonical [[decategorification|decategorified]] [[inner product]] from (eq:DecategorifiedInnterProduct).




## Generalizations and variants
 {#GeneralizationsAndVariants}

### For simple modules
  
Part (1) is essentially [[category theory|category-theoretic]] and can be generalized in many ways, for example, by replacing the [[group]] $G$ by some $k$-[[associative algebra|algebra]] and taking the representations compatible with the action of $k$. 


### For simple objects in an abelian category

More generally, given an [[abelian category]], part (1) of  Schur's lemma applies to the [[simple objects]] (see [there](simple+object#SchurLemma)) and the  [[endomorphism ring]] of a [[simple object]] is a [[division ring]]. 

For (2), if the [[endomorphism rings]] of all objects in an [[abelian category]] are [[finite-dimensional vector space|finite-dimensional]] over an [[algebraically closed field]] $k$ (as is the case for group representations), then the endomorphism ring of a simple object is $k$ itself.

### For Bridgeland stable objects

The statement of Schur's lemma applies also to objects which are stable with respect to a [[Bridgeland stability condition]], see [there](Bridgeland+stability+condition#SchurLemma)


## References

Named after *[[Issai Schur]]*.

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], (1.1.2) in _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))


See also 

* Wikipedia, _[Schur's lemma](https://en.wikipedia.org/wiki/Schur%27s_lemma)_

[[!redirects Schur's lemmas]]

[[!redirects Schur lemma]]
[[!redirects Schur lemmas]]

