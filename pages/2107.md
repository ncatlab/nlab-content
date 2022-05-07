
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Leibniz algebra_ is like a [[Lie algebra]], but without the condition that the [[magma|product]], often still written as a bracket $[-,-]$, is skew-symmetric.  The [[Jacobi identity]] however is retained as a condition in its form as the [[derivation]]-property of the product over itself. In view of the analogous [[product law]] of [[differentiation]] (also a [[derivation]]-property) attributed to [[Gottfried Leibniz]], this is then called the _Leibniz identity_ which gives Leibniz algebras their modern name ([Loday 93](#Loday93), [Loday-Pirashvili 93](#LodayPirashvili93)) even though the concept itself is older ([Blokh 65](#Blokh65)).

Leibniz algebras were motivated in [Cuvier 91](#Cuvier91), [Loday-Pirashvili 93](#LodayPirashvili93) as generalizing the relation between [[Lie algebra cohomology]] and [[cyclic homology]] ([Loday-Quillen 84](cyclic+homology#LodayQuillen84)) to one between _Leibniz cohomology_ and [[Hochschild homology]]: Where the nilpotency of the [[differential]] in the [[Chevalley-Eilenberg algebras]] that compute [[Lie algebra cohomology]] is equivalent to the [[Jacobi identity]] in the corresponding Lie algebra, Leibniz cohomology is defined on non-skew symmetric [[dg-algebras]] where now it is the generalization of the [[Jacobi identity]] in form of the _Leibniz rule_ (eq:LeibnizRule) which still guarantees the nilpotency of the differential.

More recently, Leibniz algebras have been argued to clarify the nature of the [[embedding tensor]] and the resulting [[tensor hierarchies]] in [[gauged supergravity]] ([Lavau 17](#Lavau17)).

## Definition

Let $k$ be a [[commutative ring]] (typically a [[field]]).

+-- {: .num_defn #LeftLeibnizAlgebra}
###### Definition
**(left Leibniz algebra)**

A _left Leibniz $k$-algebra_ (or: _left Loday algebra_) is 

* a $k$-[[module]] $A$ (hence a $k$-[[vector space]] if $k$ is a [[field]] and then often required to be [[finite-dimensional vector space|finite-dimensional]])  

equipped with 

* a [[linear map]], the _[[magma|product]]_

  $$
    \array{
      A \otimes A &\longrightarrow& A
      \\
      (v,w) &\mapsto& v \cdot w
    }
  $$

such that

* the product satisfies the _left Leibniz identity_, saying that

  \[
    \label{LeibnizRule} 
    v_1 \cdot (v_ 2 \cdot v_3)
    \;=\;
    (v_1 \cdot v_2) \cdot v_3
    \;+\;
    v_2 \cdot (v_1 \cdot v_3)
  \]

  for all $v_i \in A$.

This says equivalently that the operations $v \cdot (-) \colon A \to A$ of left-multiplication by elements $v \in A$ via the given [[magma|product]] is a [[derivation]] of the product itself, whence the name (paying tribute to [[Gottfried Leibniz]]'s [[product rule]] of [[differentiation]]).

=--

Analogously there is the concept of _right Leibniz algebras_ in the evident way.



## Properties

### Relation to Lie algebras in Loday-Pirashvili category

There is a remarkable observation of Loday and Pirashvili that in the [[Loday–Pirashvili tensor category]] of linear maps with (exotic) "infinitesimal tensor product", the category of internal Lie algebras has the category of, say left, Leibniz $k$-algebras as a full subcategory.  



### Corepresentation, representation, crossed module

Both a representation and a corepresentation of a right Leibniz $k$-algebra $\mathfrak{g}$ involve a $k$-module $M$ and two $k$-linear maps "actions" $M\otimes\mathfrak{g}\to M$ and $\mathfrak{g}\otimes M\to M$  with 3 axioms. 

For representations:

$$[m, [x, y]] = [[m, x], y] - [[m, y], x]$$
$$[x, [a, y]] = [[x, m], y] - [[x, y], m]$$
$$[x, [y, m]] = [[x, y], m] - [[x, m], y]$$

for $x,y\in\mathfrak{g}$ and for $m\in M$. 

For corepresentatons:

$$[[x, y], m] = [x, [y, m]] - [y, [x, m]] $$
$$[y, [a, x]] = [[y, m], x] - [m, [x, y]] $$
$$[[m, x], y] = [m, [x, y]] - [[y, m], x].$$

If the two "actions" are symmetric, i.e. $[x,m] + [m,x] = 0$ for all $m\in M$, $x\in\mathfrak{g}$ then all the 6 axioms of representation or corepresentation are equivalent. If $M$ is underlying a Leibniz algebra then an action of $\mathfrak{g}$ on $M$ is by definition symmetric, hence all the 6 equivalent conditions hold. 

A map $t : \mathfrak{g}\to\mathfrak{b}$ together with an action of $\mathfrak{b}$ on $\mathfrak{g}$ is a Leibniz crossed module if

$$
t([b,g])= [b,t(g)],\,\,\,t([g,b])=[t(g),b],\,\,\,\, for all\,\,\, b\in\mathfrak{b}, g' \in\mathfrak{g}$$

$$
[g, t(g')] = [g, g'] = [t(g), g'],\,\,\,\, for all\,\,\, g, g' \in\mathfrak{g}
$$

### Abelian extensions

Abelian extension of right Leibniz algebras is a split short exact sequence of $k$-modules

$$ 0\to M \to \mathfrak{h}\to \mathfrak{g}\to 0 $$

where the mapping $\mathfrak{h}\to\mathfrak{g}$ is a morphism of Leibniz algebras, and $M$ is equipped with induced action of $\mathfrak{g}$. The isomorphisms of extensions of $\mathfrak{g}$ by $M$ with fixed action are defined as usual. This way we obtain a set of equivalence classes $Ext(\mathfrak{g},M)$. To classify the extensions one looks for compatible Leibniz brackets on $M\oplus \mathfrak{g}$. The general form of a bracket is

$$ [(m_1,x_1),(m_2,x_2)] = ([m_1, x_2] + [x_1, m_2] + f(x_1, x_2), [x_1, x_2]),$$

where $f(x_1,x_2)$ satisfy the following 2-cocycle identity:

$$
[x, f(y, z)] + [f(x, z), y] - [f(x, y), z] =
f([x, y], z) - f([x, z], y) - f(x, [y, z]) 
$$

The extension is __split__ in the category of Leibniz algebras if $f$ is a *boundary* i.e. there exists a $k$-module map $g:\mathfrak{g}\to M$ such that 

$$
f(x, y) = [x, g(y)] + [g(x), y] - g([x, y]), \,\,\,x,y,\in\mathfrak{g}
$$

As for the Lie algebras, the group of abelian extensions agrees with the 2-cohomology $HL^2(\mathfrak{g},M)$. 

A $k$-linear __derivation__ of a right Leibniz algebra $\mathfrak{g}$ with values in its representation $M$ is a $k$-linear map satisfying the Leibniz property with respect to the bracket:

$$
\delta([x,y]) = [\delta(x),y]+[x,\delta(y)]
$$

Such derivations form a $k$-module $Der(\mathfrak{g},M)$. 

### Homology and cohomology

The homology and cohomology of Leibniz algebra $\mathfrak{g}$ with abelian $k$-module of coefficients, which is a corepresentation $A$ in the case of homology and a representation $M$ in the case of cohomology: 

$$ HL_*(\mathfrak{g},A) = Tor^{U\mathfrak{g}}_*(U(\mathfrak{g}_{Lie}),A) ,$$

$$ HL^*(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(U(\mathfrak{g}_{Lie}),A) $$

where $U(\mathfrak{g}_{Lie})$ is the universal enveloping of the maximal Lie algebra quotient $\mathfrak{g}_{Lie}$ of $\mathfrak{g}$ and $U\mathfrak{g}$ is the universal enveloping of a Leibniz algebra $\mathfrak{g}$. 

Fopr $n\geq 0$, the $n$-cocycles are elements in $C^n(\mathfrak{g}, M) = Hom_k(\mathfrak{g}^{\otimes n}, M)$, satisfying the corresponding abelian cocycle condition determined by the differential 

$$ d^n : C^n(\mathfrak{g}, M)\to C^{n+1}(\mathfrak{g}, M) $$

$$ (d^n f) (x_1, . . . , x_{n+1}) = [x_1,f(x_2,\ldots,x_{n+1})] +\sum_{n+1}^{i=2} (-1)^i [f(x_1,\ldots, \hat{x}_i, \ldots, x_{n+1}), x_i] $$

Notice a difference from the Lie algebra cocycles where instead of a tensor power we have an external power. Then $HL^*(\mathfrak{g},M) = H^*(C^*(\mathfrak{g}, M),d^*)$. 

There are standard interpretations of cocycles in low dimensions. For example for $n=0$, $HL^0(\mathfrak{g}, M)$ is the submodule of invariants.
For $n=1$ there is a natural projection $Der(\mathfrak{g},M)\to HL^1(\mathfrak{g},M)$ whose kernel is generated by inner derivations. 

### Relation to Zinbiel algebras

The Leibniz operad is quadratic Koszul algebra whose Koszul dual operad is called the operad of dual Leibniz algebras
or of [[Zinbiel algebra]]s, see there. 

### Lie's third theorem for Leibniz algebras
 {#LieThirdTheorem}

In complete analogy to the [[equivalence of categories|equivalence]] between the [[category]] of [[Lie algebras]] and the category of [[local Lie groups]] ([[Lie's third theorem]]), the [[category]] of Leibniz algebras is equivalent to the category of local pointed augmented Lie [[racks]].
See [Covez 10](#Covez10).

This equivalence restricts to the equivalence between [[Lie algebras]] and [[local Lie groups]].

Here a local pointed augmented Lie [[rack]]
is a pointed augmented [[rack]] object in the category of germs of pointed smooth manifolds.
An __augmented rack__ is a triple $(G,X,p\colon X\to G)$,
where $G$ is a [[group]], $X$ is a [[G-set]], and $p$ is a [[function|map of sets]] such that $p(g\cdot x)=g p(x)g^{-1}$.
An augmented rack is __pointed__ if there is an element $1\in X$
such that $p(1)=1$ and $g\cdot 1=1$ for all $g\in G$.

If $(G,X,p)$ is an augmented rack, then $X$ can be made into a [[rack]] as follows: $x\triangleright y = p(x)\cdot y$. If $(G,X,p)$ is a pointed augmented rack, then $X$ is a pointed [[rack]],
meaning there is $1\in X$ such that $1\triangleright x=x$
and $x\triangleright 1=1$.

## Examples

### Basic examples

* Every [[Lie algebra]] is a Leibniz algebra that happens to have skew-symmetric product. Conversely, a Leibniz algebra with skew-symmetric product is a Lie algebra.

### From Lie modules and embedding tensors
 {#FromLieModulesAndEmbeddingTensors}


+-- {: .num_prop #LeibnizAlgebraFromLieModuleAndEmbeddingTensor}
###### Proposition
**([[Leibniz algebra]] from [[Lie module]] with [[embedding tensor]])**

Let 

* $\mathfrak{g}$ be a [[Lie algebra]],

* $\mathfrak{g} \otimes V \overset{\rho}{\longrightarrow} V $ be a [[Lie algebra representation]] of $\mathfrak{g}$,

* $\Theta \colon V \longrightarrow \mathfrak{g}$ be an [[embedding tensor]], hence a [[linear map]] such that the "quadratic constraint" is satisfied: for all $v_1, v_2 \in V$ we have

    \[
      \label{QuadraticConstraintForEmbeddingTenson}
      [\Theta(v_1), \Theta(v_2)] 
        \;=\; 
      \Theta
      \big(
        \rho_{\Theta(v_1)}(v_2)
      \big)
    \]

Then $V$ becomes a [[Leibniz algebra]] with product defined by

\[
  \label{LeibnizProductFromEmbeddingTensor}
  v_1 \cdot v_2 
  \;\coloneqq\;
  \rho_{\Theta(v_1)}(v_2)
\]

and with respect to this the _quadratic constraint_ (eq:QuadraticConstraintForEmbeddingTenson) becomes the condition that $\Theta$ is a [[homomorphism]] of [[Leibniz algebras]].

=--

([Lavau 17, Example 3](#Lavau17))

+-- {: .proof}
###### Proof

We directly check the Leibniz rule (eq:LeibnizRule) as follows:

$$
  \begin{aligned}
    v_1 \cdot (v_2 \cdot v_3)
    & =
    \rho_{\Theta(v_1)}
    \big(
      \rho_{\Theta(v_2)}(v_3)
    \big)
    \\
    & = 
    \rho_{
      \underset{
        = \rho_{\Theta(v_1)}(v_2)
      }{
        \underbrace{
          [\Theta(v_1), \Theta(v_2)]
        }
      }
    }(v_3)
    +
    \rho_{\Theta(v_2)}
    \big(
      \rho_{\Theta(v_1)}(v_3)
    \big)
    \\
    & = 
    (v_1 \cdot v_2) \cdot v_3
    +
    v_2 \cdot (v_1 \cdot v_3)
  \end{aligned}
$$

Here the first line is the definition (eq:LeibnizProductFromEmbeddingTensor), the second line is the [[Lie action property]] ([here](Lie+algebra+representation#eq:LieActionProperty)), under the brace we use the quadratic constraint (eq:QuadraticConstraintForEmbeddingTenson) on the embedding tensor, and in the last line we observe again the definition (eq:LeibnizProductFromEmbeddingTensor).

=--

### From dg-Lie algebras
 {#LeibnizAlgebrasFromDgLieAlgebras}

+-- {: .num_prop #LeibnizAlgebraFromdgLieAlgebra}
###### Proposition
**([[Leibniz algebra]] from [[dg-Lie algebra]])**

Let $((V_\bullet, \partial), [-,-])$ be a [[dg-Lie algebra]] with underlying [[chain complex]] $(V_\bullet, \partial)$ and with [[super Lie bracket]] $[-,-]$.

On the [[graded vector space]] which is the [[direct sum]] 

$$
  \mathbf{V}
  \;\coloneqq\;
  \underset{n}{\oplus} V_n
  \;\in\;
  Vect
$$

of all the component [[vector spaces]], consider the [[magma|product]] given by the formula

\[
  \label{LeibnizProductFromdgLieAlgebra}
  \array{
    \mathbf{V} \otimes \mathbf{V}
    &\longrightarrow&
    \mathbf{V}
    \\
    (v,w)
    &\mapsto&
    v \cdot w
    \mathrlap{
      \;\coloneqq\;
      [\partial v, w]
    }
  }
\]

Then: Restricted to $V_1 \subset \mathbf{V}$ this product gives a left Leibniz algebra $(V_1, \cdot)$ (Def. \ref{LeftLeibnizAlgebra}), i.e. satisfies the Leibniz condition (eq:LeibnizRule).

=--

This statement is highlighted in [Lavau-Palmkvist 19, 2.1](#LavauPalmkvist19).

+-- {: .proof}
###### Proof

We directly compute as follows:

$$
  \begin{aligned}
    v_1 \cdot (v_2 \cdot v_3)
    & =
    \big[
      \partial v_1
      ,
      [
        \partial
        v_2, 
        v_3
      ]
    \big]
    \\
    & =
    \big[
      [
        \partial v_1
        , 
        \partial v_2
      ],
      v_3
    \big]
    \;+\;
    (-1)^{
      \overset{= 0}{
      \overbrace{
        (deg(v_1)-1)
        (deg(v_2)-2)
      }
      }
     }
     \big[
       \partial v_2,
       [\partial v_1, v_3] 
     \big]
    \\
    & =
    \big[
      \partial
      [
        v_1
        , 
        \partial v_2
      ],
      v_3
    \big]
    \;+\;
     \big[
       \partial v_2,
       [\partial v_1, v_3] 
     \big]
    \\
    & =
    (v_1 \cdot v_2) \cdot v_3
    \;+\;
    v_2 \cdot (v_1 \cdot v_3)
    \,.
  \end{aligned}
$$

Here the first line is the definition (eq:LeibnizProductFromdgLieAlgebra), the second line is the [graded Jacobi identity](super+Lie+algebra#eq:GradedJacobiIdentity), the third line uses the [[derivation]]-property and the nilpotency of the [[differential]], and the last line invokes again the definition (eq:LeibnizProductFromdgLieAlgebra). Over the brace we used the assumption that $v_i \in V_1$.

=--

+-- {: .num_remark}
###### Remark

The construction in Prop. \ref{LeibnizAlgebraFromdgLieAlgebra} evidently extends to a [[functor]] from the [[category]] $dgLieAlg$ of [[dg-Lie algebras]] to the [[category]] $LeibAlg$ of [[Leibniz algebras]] (both over the given [[ground ring]]/[[ground field]]):

\[
  \label{FunctorFromdgLieAlgebrasToLeibnizAlgebras}
  (-)_{1}
  \;\colon\;
  dgLieAlg 
  \longrightarrow
  LeibAlg
  \,.
\]

Notice the analogy to the evident functor that extract the [[Lie algebra]] in degree 0:

\[
  \label{FunctorFromdgLieAlgebrasToLeibnizAlgebras}
  (-)_{0}
  \;\colon\;
  dgLieAlg 
  \longrightarrow
  LieAlg
  \,.
\]



=--



## References

### General

Named after [[G. W. Leibniz]].

The idea of _Leibniz algebra_, though not by this name, is given already in 

* {#Blokh65} A. Blokh, _A generalization of the concept of Lie algebra_, Dokl. Akad. Nauk SSSR, 165:471–473 (1965) ([mathrunet:dan31825](http://mi.mathnet.ru/eng/dan31825))

The concept was revived (and apparently the name _Leibniz algebra_ was first chosen) in

* {#Loday93} [[Jean-Louis Loday]], _Une version non commutative des algèbres de Lie: les algèbres de Leibniz_,  Les rencontres physiciens-mathématiciens de Strasbourg -RCP25, Volume 44  (1993), Talk no. 5, 25 p.  ([numdam:RCP25_1993__44__127_0](http://www.numdam.org/item/?id=RCP25_1993__44__127_0))

* {#LodayPirashvili93} [[Jean-Louis Loday]], [[Teimuraz Pirashvili]], _Universal enveloping algebras of Leibniz algebras and (co)homology_, Math. Ann. __296__, 139-158 (1993) ([doi:10.1007/BF01445099](https://doi.org/10.1007/BF01445099), [pdf](http://www-irma.u-strasbg.fr/~loday/PAPERS/93LodayPira%28Leibniz%29.pdf))

Early review is in

* {#Cuvier94} [[Christian Cuvier]], _Algèbres de Leibnitz: définitions, propriétés_,  Annales scientifiques de l'École Normale Supérieure, Serie 4, Volume 27 (1994) no. 1, p. 1-45 ([doi:10.24033/asens.1687](https://doi.org/10.24033/asens.1687))

See also

* Wikipedia, _[Leibniz algebra](https://en.wikipedia.org/wiki/Leibniz_algebra)_

Relaization of Leibniz algebras as [[Lie algebra objects]] in a suitable [[tensor category]]:

* {#LodayPirashvili98} [[Jean-Louis Loday]], [[Teimuraz Pirashvili]], _The tensor category of linear maps and Leibniz algebras_, Georg. Math. J. vol. 5, n.3 (1998) 263--276 ([doi:10.1023/B:GEOR.0000008125.26487.f3](https://link.springer.com/article/10.1023/B:GEOR.0000008125.26487.f3))


Relation to [[Hochschild homology]]:

* {#Cuvier91} [[Christian Cuvier]], _Homologie de Leibniz et homologie de Hochschild_, C.R. Acad. Sci. Paris, Ser. A-B313, 569-572 (1991)

* Jerry M. Lodder, _Leibniz homology, characteristic classes and K-theory, [K-theory archive/0493](http://www.math.uiuc.edu/K-theory/0493); _Leibniz cohomology and the calculus of variations_ ([arXiv:math/9808036](http://arxiv.org/abs/math/9808036))

* [[Jean-Louis Loday]], _Algebraic K-theory and the conjectural Leibniz K-theory_, K-Theory 09/2003; 30(2):105-127, [pdf](http://www-irma.u-strasbg.fr/~loday/PAPERS/2003Loday%28LeibnizConj%29.pdf) [doi](http://dx.doi.org/10.1023/B:KTHE.0000018382.90150.ce)


This is partly based on earlier insights of Kinyon and Weinstein:

* Michael K. Kinyon, _Leibniz algebras, Lie racks, and digroups_, J. Lie Theory __17__:1 (2007) 099--114, [arxiv:math.GR/0403509](http://arxiv.org/abs/math/0403509)


### Relation to dg-Lie algebras and tensor hierarchies

Relation of [[Leibniz algebras]] to [[dg-Lie algebras]] such as the [[tensor hierarchies]] in [[gauged supergravity]]:

* {#Lavau17} [[Sylvain Lavau]], _Tensor hierarchies and Leibniz algebras_, J. Geom. Phys. 144:147-189 (2019) ([arXiv:1708.07068](https://arxiv.org/abs/1708.07068))

* {#LavauPalmkvist19} [[Sylvain Lavau]], [[Jakob Palmkvist]], _Infinity-enhancing of Leibniz algebras_ ([arXiv:1907.05752](https://arxiv.org/abs/1907.05752))

* [[Sylvain Lavau]], [[Jim Stasheff]], _$L_\infty$-algebra extensions of Leibniz algebras_ ([arXiv:2003.07838](https://arxiv.org/abs/2003.07838))

### Lie integration

A generalization of [[Lie integration]] to conjectural Leibniz groups has been conjectured by [[J-L. Loday]]. A local version via local Lie [[racks]] has been proposed in

* [[Simon Covez]], _L'int&#233;gration locale des alg&#232;bres de Leibniz_, Thesis (2010) ([pdf](http://tel.archives-ouvertes.fr/docs/00/49/54/69/PDF/THESE_Simon_Covez.pdf))

* {#Covez10}  [[Simon Covez]], _The local integration of Leibniz algebras_,  Annales de l'Institut Fourier, Volume 63 (2013) no. 1, p. 1-35 ([arXiv:1011.4112](http://arxiv.org/abs/1011.4112), [doi:10.5802/aif.2754](https://doi.org/10.5802/aif.2754))

* [[Simon Covez]], _On the conjectural cohomology for groups_, Journal of K-theory __10__:03, Dec 2012, pp 519-563  ([arXiv:1202.2269](http://arxiv.org/abs/1202.2269), [doi:10.1017/is011011011jkt195](http://dx.doi.org/10.1017/is011011011jkt195))



[[!redirects Leibniz algebras]]
[[!redirects Loday algebra]]



[[!redirects Leibniz rule]]
[[!redirects Leibniz rules]]
[[!redirects Leibniz's rule]]
[[!redirects Leibniz's rules]]
[[!redirects Leibniz\'s rule]]
[[!redirects Leibniz\'s rules]]
[[!redirects Leibniz's rule]]
[[!redirects Leibniz's rules]]

[[!redirects Leibniz identity]]
[[!redirects Leibniz identities]]


[[!redirects Leibniz law]]
[[!redirects Leibniz laws]]
[[!redirects Leibniz's law]]
[[!redirects Leibniz's laws]]
[[!redirects Leibniz\'s law]]
[[!redirects Leibniz\'s laws]]
[[!redirects Leibniz's law]]
[[!redirects Leibniz's laws]]

