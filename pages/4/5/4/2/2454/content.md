
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
 {#ForLieAlgebras}

Given a [[Lie algebra object]] $L$ [[internalization|internal]] to some [[symmetric monoidal category|symmetric monoidal]] $k$-[[linear category]] $C = (C,\otimes, \mathbf{1},\tau)$, an __enveloping monoid__ (or __enveloping algebra__) of $L$ in $C$ is any morphism $f \colon L\to Lie(A)$ of Lie algebras in $C$ where $A$ is a monoid (= algebra) in $C$, and $Lie(A)$ is the underlying object of $A$ equipped with the [[Lie bracket]] $[,]_{Lie(A)}=\mu-\mu\circ\tau_{A,A}$. 

A morphism of enveloping algebras 
$$
  \phi 
    \;\colon\; 
  \big(A, f \colon L\to Lie(A)\big) 
  \longrightarrow 
  \big(A, f' \colon L\to A'\big)
$$ 
is a morphism $g \colon A\to A'$ of [[monoid objects]] completing a commutative triangle of morphisms in $C$, i.e. $g\circ f = f'$. With an obvious composition of morphisms, the enveloping algebras of $L$ form a [[category]]. 

A __universal enveloping algebra__ of $L$ in $C$ is any universal [[initial object]] $i_L \colon L\to U(L)$ in the category of enveloping algebras of $L$, which implies that it is unique up to an isomorphism if it exists. 

If it exists for all Lie algebras in $C$, then the rule $L\mapsto U(L)$ can be extended to a [[functor]] $U$ which is the [[left adjoint]] to the [[forgetful functor]] $Lie \colon A\mapsto Lie(A)$ defined above and the morphism $i_L:L\to U(L)$ is the [[unit of an adjunction|unit of the adjunction]]. 

\begin{remark}\label{ForSuperLieAlgebras}
**(for [[super Lie algebras]] as eg. in [[algebraic topology]])**
\linebreak
  The [[internalization|internal]] generality of the above definitions is used notably in [[algebraic topology]] where the relevant Lie algebras arise from [[Whitehead brackets]] which are [[super Lie algebras]] (see [there](super+Lie+algebra#AsLieAlgebrasInternalToSuperVectorSpaces)), i.e. [[Lie algebra objects]] [[internalization|internal]] to [[super vector spaces]] (cf. eg. [Milnor & Moore 1965, §5](#MilnorMoore65); [May & Ponto 2012, Def. 22.1.3](#MayPonto12)).
\end{remark}

### For $L_\infty$-algebras

In the more general context of [[higher algebra]] there is a notion of universal enveloping [[E-n algebra]] of an [[L-infinity algebra]] for all $n \in \mathbb{N}$ which generalizes the notion of universal associative algebra envelope of a Lie algebra. See at _[[universal enveloping E-n algebra]]_.

## Existence

The existence of the universal enveloping algebra is easy in many concrete symmetric monoidal categories, e.g. the symmetric monoidal category of bounded chain complexes (giving the universal enveloping [[differential graded algebra|dg-algebra]] of a [[differential graded Lie algebra|dg-Lie algebra]]), but not true in general. 

First of all if $C$ admits countable coproducts, form the tensor algebra $TL=\coprod_{n=0}^\infty L^{\otimes n}$ on the object $L$; this is a monoid in $C$.
In most standard cases, one can also form the smallest 2-sided ideal (i.e. $A$-subbimodule) $I$ in monoid $A$ among those ideals whose inclusion into $A$ is factorizing the map $([,]-m_{TL}+m_{TL}\circ\tau)\circ \otimes :L\otimes L\to TL$; if the coequalizers exist in $C$ then we can form the quotient object $TL/I$ and there is an induced monoid structure in it. Under mild conditions on $C$, the natural morphism $i_L:L\to TL/I$ is an universal enveloping monoid of $L$ in $C$. If $C$ is an abelian tensor category and some flatness conditions on the tensor product are satisfied, then the enveloping monoid $i_L:L\to TL/I$ is a monic morphism in $C$ and $U(L\coprod L)\cong U(L)\otimes U(L)$.

## Properties

### Isomorphism problem
 {#IsomorphismProblem}

Notice that the enveloping algebras of two Lie algebras may be [[isomorphism|isomorphic]] as [[associative algebras]] even if the two Lie algebras they arise from are not isomorphic to each other. 

This happens even in [[characteristic zero]], in which case, however, at least the [[dimension]] of the Lie algebra is encoded in its universal enveloping algebra, in the guise of the *Gelfand-Kirillov dimension* $GK\big(U(L)\big)$. 

### Poisson algebra structure on $U(\mathfrak{g})$

The universal enveloping algebra $U(\mathfrak{g})$ of a [[Lie algebra]] is naturally a (non-commutative) [[Poisson algebra]] with the restriction of the Poisson bracket to generators being the original [[Lie bracket]]

### Hopf algebra structure on $U(\mathfrak{g})$

Suppose the universal enveloping algebras of Lie algebras exist in a $k$-linear symmetric monoidal category $C$ and the functorial choice $L\mapsto U(L)$ realizing the above construction with tensor products is fixed. For example, this is true in the category of $k$-[[modules]] where $k$ is a [[commutative ring]]. Then the projection $L\to 0$ (where $0$ is the trivial Lie algebra) induces the counit $\epsilon:U(L)\to U(0)=\mathbf{1}$. The coproduct $\Delta:U(L)\to U(L\times L)\cong U(L)\otimes U(L)$ is induced by the [[diagonal]] map $L\to L\times L$ whereas the antipode $S=U(-id):U(L)\to U(L)$. One checks that these morphisms make $U(L)$ into a [[Hopf algebra]] in $C$. (e.g [Milnor-Moore 65, section 5](#MilnorMoore65)) The _[[Milnor-Moore theorem]]_ states conditions under which the converse holds (hence under which a primitively generated Hopf algebra is a universal enveloping algebra of a Lie algebra).

If the category is simply the vector spaces over a field $k$, then for $l\in L$, after we identify $L$ with its image in $U(L)$, $\Delta(l) = l\otimes 1 + 1\otimes l$, i.e. the elements in $L$ are the [[primitive element]]s in $U(L)$. 

### PBW theorem

The [[Poincaré–Birkhoff–Witt theorem]] states that the 
[[associated graded]] algebra of an enveloping algebra $U(g)$ in [[characteristic zero]] is canonically isomorphic to a [[symmetric algebra]] $Sym(g)$, and $U(g)$ is isomorphic to $S(g)$ as a coalgebra, via the projection map $U(g)\to Gr U(g)$. 

### Relation to formal deformation quantization

See at _[[formal deformation quantization]]_ the section _[Relation to universal enveloping algebras](formal+deformation+quantization#RelationToUniversalEnvelopingAlgebras)_.


### Relation to the group algebra
 {#RelationToTheGroupAlgebra}

> The universal enveloping algebra of a Lie algebra is the analogue of the usual [[group algebra]] of a group. It has the analogous function of exhibiting the [[category]] of [[Lie algebra modules]] as a category of [[modules]] for an [[associative algebra]]. This becomes more than an analogy when the universal enveloping algebra is viewed with its full [[Hopf algebra]] structure. By dualization, one obtains a commutative Hopf algebra which, in the case where the Lie algebra is that of an irreducible [[algebraic group]] over a [[field]] of [[characteristic 0]], contains the algebra of polynomial functions of that group as a sub Hopf algebra in a natural fashion. 

(quoted from [Hochschild 1981, p. 221](#Hochschild81), see [ibid. Thm. 3.1 on p. 230](#Hochschild81); [Tjin 1992, Thm. 1](#Tjin92))

## Examples

\begin{example}\label{WeylAlgebraAndHeisenbergAlgebra}
Consider the standard [[symplectic form]] on the [[Cartesian space]] $\mathbb{R}^{2n}$, making a [[symplectic vector space]]. This gives rise to the corresponding [[Heisenberg Lie algebra]].

Depending on conventions, the [[universal enveloping algebra]] of the [[Heisenberg Lie algebra]] either already is the [[Weyl algebra]] on $2n$ generators or else it becomes so after after forming the [[quotient algebra]] in which the central generator is identified with the [[unit element]] of the [[ground field]] -- whereas in the former case (considered eg. in [Kravchenko 2000, Def. 2.1](#Kravchenko00); [Bekaert 2005, p. 9](#Bekaert05)) the central generator plays the role of the formal [[Planck constant]] $\hbar$ with the Weyl algebra regarded as a [[formal deformation quantization]] of the [[symplectic manifold]] $\mathbb{R}^{2m}$.

Accordingly, given a [[Heisenberg Lie n-algebra|Heisenberg Lie $n$-algebra]] it makes sense to call its [[universal enveloping E-n algebra|universal enveloping $E_n$-algebra]] a _[[Weyl n-algebra|Weyl $n$-algebra]]_.
\end{example}

\begin{example}
**(Universal enveloping of a tangent Lie algebra)**
\linebreak
The universal enveloping algebra of the [[tangent Lie algebra]] of a  finite-dimensional [[Lie group]] $G$ over the real or complex numbers is canonically isomorphic to the algebra of the left invariant  [[differential operators]] on $G$.
\end{example}

## Related concepts

* [[Hausdorff series]]

* [[Poincaré–Birkhoff–Witt theorem]]

* [[coexponential map]]

* [[Duflo isomorphism]] 

* [[oidification]] to [[universal enveloping algebroid]]

* [[universal enveloping E-n algebra]]

## References

* {#Serre64} [[Jean-Pierre Serre]]: *Universal Algebra of a Lie Algebra*, Chapter III in: *Lie Algebras and Lie Groups -- 1964 Lectures given at Harvard University*, Lecture Notes in Mathematics **1500**, Springer (1992) &lbrack;[doi:10.1007/978-3-540-70634-2](https://doi.org/10.1007/978-3-540-70634-2)&rbrack;

* {#Dixmier74} [[Jacques Dixmier]]; _[[Algèbres Enveloppantes]]_, Cahiers Scientifique (1974), Engl transl: _Enveloping Algebras_, Graduate Studies in Mathematics **11** American Mathematical Society (1996) &lbrack;[ams:gsm-11](https://bookstore.ams.org/gsm-11)&rbrack;

* [[Nicolas Bourbaki]], §I.2 in: _Lie groups and Lie algebras -- Chapters 1-3_, Springer (1975, 1989) &lbrack;[ISBN:9783540642428](https://link.springer.com/book/9783540642428)&rbrack;

* {#Hochschild81} [[Gerhard P. Hochschild]], *The Universal Enveloping Algebra*, Chapter XVI in: *Basic Theory of Algebraic Groups and Lie Algebras*, Graduate Texts in Mathematics **75**, Springer (1981) &lbrack;[doi:10.1007/978-1-4613-8114-3_16](https://doi.org/10.1007/978-1-4613-8114-3_16)&rbrack; 

Further discussion in the context of [[quantum groups]]:

* {#Tjin92} [[Tjark Tjin]], *An introduction to quantized Lie groups and algebras*, Int. J. Mod. Phys. A **7** (1992) 6175-6213 &lbrack;[arXiv:hep-th/9111043](https://arxiv.org/abs/hep-th/9111043), [doi:10.1142/S0217751X92002805](https://doi.org/10.1142/S0217751X92002805)&rbrack;
    

Discussion in the generality of [[super Lie algebras]] such as notably of the [[Whitehead Lie algebras]] arising in [[algebraic topology]]:

* {#MilnorMoore65} [[John Milnor]], [[John Moore]], §5 in _On the structure of Hopf algebras_, Annals of Math. __81__ (1965) 211-264 &lbrack;[doi:10.2307/1970615](https://doi.org/10.2307/1970615), [pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/milnor-moore-ann-math-1965.pdf)&rbrack;

* {#MayPonto12} [[Peter May]], [[Kate Ponto]], Def. 22.1.3 in: *More concise algebraic topology -- Localization, Completion, and Model Categories*, University of Chicago Press (2012) &lbrack;[ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf)&rbrack;


See also:

* Wikipedia: *[Universal enveloping algebra](http://en.wikipedia.org/wiki/Universal_enveloping_algebra)*, *[PBW theorem](http://en.wikipedia.org/wiki/Poincar%C3%A9%E2%80%93Birkhoff%E2%80%93Witt_theorem)*

* F. A. Berezin, _Some remarks about the associated envelope of a Lie algebra_, Func. Analysis and Its Appl. 1967, 1:2, 91&#8211;102; Rus. original in Fun. Anal. Pril. 1:2 (1967) 1&#8211;14 [Rus. pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2813&volume=1&year=1967&issue=2&fpage=1&what=fullt&option_lang=eng) [MR219671](http://www.ams.org/mathscinet-getitem?mr=219671)

* MathOverflow question [What is the universal enveloping algebra](http://mathoverflow.net/questions/25020/what-is-the-universal-enveloping-algebra) which is looking for a rather general construction in a class of symmetric monoidal [[pseudoabelian category|pseudoabelian categories]].

[[!redirects universal enveloping algebras]]

