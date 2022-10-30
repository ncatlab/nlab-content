
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For Lie algebras

Given a [[Lie algebra]] $L$ internal to some [[symmetric monoidal category|symmetric monoidal]] $k$-linear category $C = (C,\otimes, \mathbf{1},\tau)$, an __enveloping monoid__ (or __enveloping algebra__) of $L$ in $C$ is any morphism $f: L\to Lie(A)$ of Lie algebras in $C$ where $A$ is a monoid (= algebra) in $C$, and $Lie(A)$ is the underlying object of $A$ equipped with the Lie bracket $[,]_{Lie(A)}=\mu-\mu\circ\tau_{A,A}$. In further we will just write $A$ for $Lie(A)$. A morphism of enveloping algebras $\phi : (f:L\to A)\to (f':L\to A')$ is a morphism $g: A\to A'$ of monoids completing a commutative triangle of morphisms in $C$, i.e. $g\circ f = f'$. With an obvious composition of morphisms, the enveloping algebras of $L$ form a category. A __universal enveloping algebra__ of $L$ in $C$ is any universal [[initial object]] $i_L:L\to U(L)$ in the category of enveloping algebras of $L$; it is of course unique up to an isomorphism if it exists. If it exists for all Lie algebras in $C$, then the rule $L\mapsto U(L)$ can be extended to a functor $U$ which is the left adjoint to the functor $Lie:A\mapsto Lie(A)$ defined above and the morphism $i_L:L\to U(L)$ is the unit of the adjunction. 

### For $L_\infty$-algebras

In the more general context of [[higher algebra]] there is a notion of universal enveloping [[E-n algebra]] of an [[L-infinity algebra]] for all $n \in \mathbb{N}$ which generalizes the notion of universal associative algebra envelope of a Lie algebra. See at _[[universal enveloping E-n algebra]]_.

## Existence

The existence of the universal enveloping algebra is easy in many concrete symmetric monoidal categories, e.g. the symmetric monoidal category of bounded chain complexes (giving the universal enveloping [[differential graded algebra|dg-algebra]] of a [[differential graded Lie algebra|dg-Lie algebra]]), but not true in general. 

First of all if $C$ admits countable coproducts, form the tensor algebra $TL=\coprod_{n=0}^\infty L^{\otimes n}$ on the object $L$; this is a monoid in $C$.
In most standard cases, one can also form the smallest 2-sided ideal (i.e. $A$-subbimodule) $I$ in monoid $A$ among those ideals whose inclusion into $A$ is factorizing the map $([,]-m_{TL}+m_{TL}\circ\tau)\circ \otimes :L\otimes L\to TL$; if the coequalizers exist in $C$ then we can form the quotient object $TL/I$ and there is an induced monoid structure in it. Under mild conditions on $C$, the natural morphism $i_L:L\to TL/I$ is an universal enveloping monoid of $L$ in $C$. If $C$ is an abelian tensor category and some flatness conditions on the tensor product are satisfied, then the enveloping monoid $i_L:L\to TL/I$ is a monic morphism in $C$ and $U(L\coprod L)\cong U(L)\otimes U(L)$.

## Properties

### Isomorphism problem

The _isomorphism problem_ for enveloping algebras is about the fact that the universal enveloping monoids of two Lie algebras of $C$ are isomorphic as associative [[monoids]] in $C$, but this does not imply that the Lie algebras are isomorphic. This is even not true in general for the Lie $k$-algebras (in classical sense), even if $k$ is a [[field]] of characteristics zero. It is known however in that case that the dimension of the finite-dimensional Lie $k$-algebra $L$ can be read off from its universal enveloping $k$-algebra as its Gel'fand-Kirillov dimension $GK(U(L))$. 

### Poisson algebra structure on $U(\mathfrak{g})$

The universal enveloping algebra $U(\mathfrak{g})$ of a [[Lie algebra]] is naturally a (non-commutative) [[Poisson algebra]] with the restriction of the Poisson bracket to generators being the original [[Lie bracket]]

### Hopf algebra structure on $U(\mathfrak{g})$

Suppose the universal enveloping algebras of Lie algebras exist in a $k$-linear symmetric monoidal category $C$ and the functorial choice $L\mapsto U(L)$ realizing the above construction with tensor products is fixed. For example, this is true in the category of $k$-[[modules]] where $k$ is a [[commutative ring]]. Then the projection $L\to 0$ (where $0$ is the trivial Lie algebra) induces the counit $\epsilon:U(L)\to U(0)=\mathbf{1}$. The coproduct $\Delta:U(L)\to U(L\times L)\cong U(L)\otimes U(L)$ is induced by the [[diagonal]] map $L\to L\times L$ whereas the antipode $S=U(-id):U(L)\to U(L)$. One checks that these morphisms make $U(L)$ into a [[Hopf algebra]] in $C$. (e.g [Milnor-Moore 65, section 5](#MilnorMoore65)) The _[[Milnor-Moore theorem]]_ states conditions under which the converse holds (hence under which a primitively generated Hopf algebra is a universal enveloping algebra of a Lie algebra).

If the category is simply the vector spaces over a field $k$, then for $l\in L$, after we identify $L$ with its image in $U(L)$, $\Delta(l) = l\otimes 1 + 1\otimes l$, i.e. the elements in $L$ are the [[primitive element]]s in $U(L)$. 

### PBW theorem

The [[Poincaré–Birkhoff–Witt theorem]] states that the 
[[associated graded]] algebra of an enveloping algebra $U(g)$ in [[characteristics zero]] is canonically isomorphic to a [[symmetric algebra]] $Sym(g)$, and $U(g)$ is isomorphic to $S(g)$ as a coalgebra, via the projection map $U(g)\to Gr U(g)$. 

### Relation to formal deformation quantization

See at _[[deformation quantization]]_ the section _[Relation to universal enveloping algebras](deformation+quantization#RelationToUniversalEnvelopingAlgebras)_.

## Examples

### Universal enveloping of a tangent Lie algebra

The universal enveloping algebra of the [[tangent Lie algebra]] of a 
finite-dimensional Lie group $G$ over real or complex numbers is canonically isomorphic to the algebra of the left invariant 
[[differential operators]] on $G$.

## Related concepts

* [[Hausdorff series]], [[Poincaré–Birkhoff–Witt theorem]], [[coexponential map]], [[Duflo isomorphism]] 

* An [[oidification]] is the [[universal enveloping algebroid]].

* [[universal enveloping E-n algebra]]

## References


* [[N. Bourbaki]], _Lie groups and Lie algebras_

* [[Jacques Dixmier]]; 1974; _[[Algèbres enveloppantes]]_, Cahiers Scientifique. English translation: 1996; _Enveloping Algebras_, Graduate Studies in Mathematics 11, American Mathematical Society.

* {#MilnorMoore65} [[John Milnor]], [[John Moore]], _On the structure of Hopf algebras_, Annals of Math. __81__ (1965), 211-264. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/milnor-moore-ann-math-1965.pdf))


* wikipedia: [universal enveloping algebra](http://en.wikipedia.org/wiki/Universal_enveloping_algebra), [PBW theorem](http://en.wikipedia.org/wiki/Poincar%C3%A9%E2%80%93Birkhoff%E2%80%93Witt_theorem)

* F. A. Berezin, _Some remarks about the associated envelope of a Lie algebra_, Func. Analysis and Its Appl. 1967, 1:2, 91&#8211;102; Rus. original in Fun. Anal. Pril. 1:2 (1967) 1&#8211;14 [Rus. pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2813&volume=1&year=1967&issue=2&fpage=1&what=fullt&option_lang=eng) [MR219671](http://www.ams.org/mathscinet-getitem?mr=219671)

* MathOverflow question [What is the universal enveloping algebra](http://mathoverflow.net/questions/25020/what-is-the-universal-enveloping-algebra) which is looking for a rather general construction in a class of symmetric monoidal [[pseudoabelian category|pseudoabelian categories]].

[[!redirects universal enveloping algebras]]