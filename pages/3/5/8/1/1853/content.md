
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

Recall from the discussion at [[cohomology]] that every notion of cohomology (e.g. [[group cohomology]], [[abelian sheaf cohomology]], etc) is given by Hom-spaces in an [[(∞,1)-topos]] $\mathbf{H}$. Cohomology on an object $X \in \mathbf{H}$ with coefficients in an object $A \in \mathbf{H}$ is

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

The _cup product_ is an operation on cocycles with coefficients $A_1$ and $A_2$ that is induced from a pairing of coefficients given by some morphism

$$
  A_1 \times A_2 \longrightarrow A_3
$$

in $\mathbf{H}$. In applications this is often a pairing operation with $A_1 = A_2$, i.e. $A \times A \to A'$, and typically it is the product morphism $A \times A \to A$ for a [[ring object]] structure on the [[coefficients]] $A$. (See at _[[multiplicative cohomology theory]]_).

If $g_1 : X \to A_1$ and $g_2 : X \to A_2$ are two cocycles in $\mathbf{H}(X,A_1)$ and $\mathbf{H}(X,A_2)$, respectively, then their cup product with respect to this pairing is the cocycle

$$
  g_1 \cdot g_2 : X \stackrel{(id,id)}{\longrightarrow}
  X \times X
  \stackrel{g_1 \times g_2}{\to}
  A_1 \times A_2
  \to
  A_3
$$

in $\mathbf{H}(X,A_3)$ obtained by combining the pairing with precomposition by the [[diagonal]] map $\Delta_X = (id_X, id_X)$.

## Examples

### Via the Dold-Kan correspondence
 {#ViaTheDoldKanCorrespondence}

When the coefficient object $A \in $ [[∞Grpd]] is "sufficiently abelian" in that under the [[Dold-Kan correspondence]] it is represented by a [[chain complex]] then using the [[lax monoidal functor|lax monoidalness]] of the Dold-Kan correspondence (see at _[[monoidal Dold-Kan correspondence]]_) one obtains a chain complex model for the cup product which makes the origin of the typical grading shift manifest.

Write 

* $(Ch_{\bullet \geq 0}, \otimes)$ for the [[category of chain complexes]] of [[abelian groups]], in non-negative degrees;, regarded as a [[symmetric monoidal category]] with the standard [[tensor product of chain complexes]] $\otimes$;

* $(sAb, \otimes)$ for the [[category]] of [[simplicial abelian groups]], regarded as a [[symmetric monoidal category]] with the degreewise [[tensor product of abelian groups]];

* $U \;\colon\; sAb \longrightarrow KanCplx \to sSet$ for the [[forgetful functor]] to the underlying [[simplicial sets]] (which happens to land in [[Kan complexes]]);
 
* $\Gamma \;\colon \; Ch_{\bullet \geq 0} \stackrel{\simeq}{\longrightarrow} sAb$ for the [[equivalence of categories]] given by the [[Dold-Kan correspondence]];

* $DK \;\colon\; Ch_{\bullet \geq 0} \underoverset{\simeq}{\Gamma}{\longrightarrow} sAb \stackrel{F}{\longrightarrow} KanCplx \hookrightarrow sSet$ for the composite.

Now:

* $\Gamma$ is a [[lax monoidal functor]], the lax monoidal structure $\gamma_{A,B} \;\colon\; \Gamma(A) \otimes \Gamma(B) \to \Gamma(A \otimes B)$ being induced [dually](oplax+monoidal+functor#OplaxAdjointToLax) by the [[Alexander-Whitney map]];

* $U$ is a [[strong monoidal functor]];

* for the [[tensor product of abelian groups]] $A \otimes B$ there are canonical natural [[bilinear maps]] of underlying sets

  $$
     p_{A,B} 
      \;\colon\; 
     U(A)\times U(B) 
     \longrightarrow
     U(A \otimes B)
  $$

Using all this, then for

$$
  f \;\colon\; V_\bullet \otimes W_\bullet \longrightarrow Z_\bullet
$$

a given [[chain map]], this induces a map of the corresponding Kan complexes

$$
  \cup_{DK}
  \;\colon\;
  DK(V_\bullet) \times DK(W_\bullet)
  \longrightarrow
  DK(Z_\bullet)
$$

as the following [[composition|composite]]

$$
  \cup_{DK}
  \;\colon\;
  DK(V_\bullet)\times DK(W_\bullet)
  =
  U(\Gamma(V_\bullet)) \times U(\Gamma(W_\bullet))
  \stackrel{p_{\Gamma(V_\bullet), \Gamma(W_\bullet)} }{\to}
  U(\Gamma(V_\bullet)\otimes \Gamma(W_\bullet))
  \stackrel{U(\gamma)}{\longrightarrow}
  U(\Gamma(V_\bullet \otimes W_\bullet))
  \stackrel{U(\Gamma(f))}{\to}
  U(\Gamma(Z_\bullet))
  =
  DK(Z_\bullet)
  \,.
$$

With this in hand then for $X$ any [[homotopy type]], the cup product on its [[cohomology]] with [[coefficients]] in $DK(V_\bullet)$ and $DK(W_\bullet)$ is induced by just homming $X$ into this morphism:

$$
  \mathbf{H}(X, DK(V_\bullet)) \times
  \mathbf{H}(X, DK(W_\bullet))
  \simeq
  \mathbf{H}(X, DK(V_\bullet) \times DK(W_\bullet))
  \stackrel{\mathbf{H}(X,\cup_{DK})}{\longrightarrow}
  \mathbf{H}(X, DK(Z_\bullet))
  \,.
$$

For example if 

$$
  V_\bullet = \mathbb{Z}[n_1]
  \,,
  \;\;\;
  W_\bullet = \mathbb{Z}[n_2]
$$

is the [[chain complex]] concentrated in degree $n_1$ and $n_2$, respectively, on the group of [[integers]], then

$$
  DK(V_\bullet) \simeq B^{n_1} \mathbb{Z} \simeq K(\mathbb{Z},n_1)
$$

is the corresponding [[Eilenberg-MacLane space]] which classifies [[ordinary cohomology]] ([[singular cohomology]]) with integral coefficients in the given degree. By the nature of the [[tensor product of chain complexes]] one has

$$
  V_\bullet \otimes W_\bullet \simeq \mathbb{Z}[n_1 + n_2]
  \,.
$$

Hence we may take $Z_\bullet \coloneqq \mathbb{Z}[n_1 + n_2]$ and $f = id$ and we get a cup product

$$
  \cup \;\colon\; H^{n_1}(X, \mathbb{Z}) \times H^{n_2}(X, \mathbb{Z})
  \to 
  H^{n_1 + n_2}(X, \mathbb{Z})
  \,.
$$ 


### On Moore complexes of cosimplicial algebras 

For $A = (A^\bullet)$ any [[cosimplicial algebra]], its dual [[Moore complex|Moor cochain complex]] $N^\bullet(A)$ naturally inherits the structure of a [[dg-algebra]] under the cup product.

> The general formula is literally the same as that for the case where $A^\bullet$ is functions on the singular complex of a space, which is discussed below. For the moment, see below.

This cup product operation on $N^\bullet(A)$ is not in general commutative. However, it is a standard fact that it becomes commutative after passing to [[chain homology and cohomology|cochain cohomology]].

This suggests that the cup product should be, while not commutative, homotopy commutative in that it makes $N^\bullet(A)$ a [[commutative algebra in an (∞,1)-category|homotopy commutative monoid object]]. 

This in turn should mean that $N^\bullet(A)$ is an [[algebra over an operad]] for the [[E-k-operad|E-∞ operad]].

That this is indeed the case is the main statement in ([Berger-Fresse 01](#BergerFresse01))


### In singular cohomology ###
 {#InSingularCohomology}

A special case of the cup product on Moore complexes is the complex of [[singular cohomology]], which is the Moore complex of the cosimplicial algebra of functions on the singular simplicial set of a topological space.

Often in the literature by _cup product_ is meant specifically the realization of the cup product on [[singular cohomology]]. 

For $X$ a [[topological space]], let $\Pi(X)_\bullet := X^{\Delta_{Top}^\bullet}$ be the [[simplicial set]] of $n$-[[simplex|simplices]] in $X$ -- the [[fundamental ∞-groupoid]] of $X$.

For $R$ some [[ring]], let $Maps(\Pi(X),R)^{\bullet}$ be the [[cosimplicial algebra|cosimplicial ring]] of $R$-valued functions on the spaces of $n$-simplices. The corresponding [[Moore complex|Moore cochain complex]] $C^\bullet(X)$ is the cochain complex whose [[chain homology and cohomology|cochain cohomology]] is the [[singular cohomology]] of the space $X$: a homogeneous element $\omega_p \in C^p(X)$ is a function on $p$-simplices in $X$.

Write, as usual, for $p \in \mathbb{N}$, $[p] = \{0 \lt 1 \lt \cdots \lt p\}$ for the [[poset|totally ordered set]] with $p+1$ elements. For $\mu : [p] \to [p+q]$ an injective order preserving map and $K$ some [[simplicial object|cosimplicial object]], write $d_\mu^* K : K^p \to K^{p+q}$ for the image of this map under $K$.

Specifically, for $p,q \in \mathbb{N}$ let $L : [p] \to [p+q]$ be the map that sends $i \in [p]$ to $i \in [p+q]$ and let $R : [q] \to [p+q]$ be the map that sends $i \in [q]$ to $i+q \in [p+q]$. 

Then the **cup product** 

$$
  \smile : C^\bullet(X) \otimes C^\bullet(X)
   \to C^\bullet(X)
$$

is the cochain map that on homogeneous elements $a \otimes b \in C^p(X) \otimes C^q(X) \subset C^\bullet(X) \otimes C^\bullet(X)$ is defined by the formula

$$
  a \smile b = (d_L^* a) \cdot (d_R^* b)
  \,.
$$

> There is some glue missing here to connect this back to the above general definition, something involving the [[Eilenberg-Zilber map]].

This means that $(a \smile b)_{i_0, \cdots, i_{p+q}} = a_{i_0, \cdots, i_p} \cdot b_{i_p, \cdots, i_{p+q}}$.

+-- {: .num_prop }
###### Proposition

This cup product enjoys the following properties:

* it is indeed a cochain complex morphism as claimed, in that it respects the differential: for any homogeneous $a\otimes b \in C^p(X) \otimes C^q(X)$ as above we have
  
  $$
    d(a \smile b) = (d a) \smile b + (-1)^p a \smile (d b)
    \,.
  $$
 
* the image of the cup product on [[chain homology and cohomology|cochain cohomology]]

  $$
     \smile :  H^\bullet(C^\bullet(X))\otimes H^\bullet(C^\bullet(X)) \to H^\bullet(C^\bullet(X))
  $$

  is associative and distributes over the addition in $H^\bullet(C^\bullet(X))$.

=--


Accordingly, the cup product makes $H^\bullet(C^\bullet(X)) = H^\bullet(X,R)$ into a [[ring]]: the **cohomology ring** on the [[Eilenberg-MacLane spectrum|ordinary cohomology]] of $X$.


See for instance section 3.2 of 

* Hatcher, _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html) [pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))


## In abelian sheaf cohomology ##

Traditionally the cup product is considered for 
abelian cohomology, such as [[generalized (Eilenberg-Steenrod) cohomology]] and more generally [[abelian sheaf cohomology]].

In that case all coefficient objects $A_i$ are complexes $(A_i)_\bullet$ of sheaves and the pairing that one usually considers is the [[tensor product]] of [[chain complex]]es

$$
  (A_1)_\bullet \times (A_2)_\bullet \to (A_1 \otimes A_2)_\bullet
$$

where

$$
  (A_1 \otimes A_2)_n = \oplus_p (A_1)_p \otimes (A_2)_{n-p}
  \,.
$$

with differential 

$$
  d (a_1 \otimes a_2) = (d a_1) \otimes a_2 + (-1)^{|a_1|} a_1 \otimes d a_2
  \,.
$$

### In abelian &#268;ech cohomology ###

The cup product has a simple expression in abelian [[?ech cohomology]].

For $A_1$ and $A_2$ two [[chain complex]]es (of [[sheaves]] of [[abelian group]]s) construct a morphism of &#268;ech complexes

$$
  \phi : C^\bullet(\{U_i\}, A_1) \otimes
         C^\bullet(\{U_i\}, A_2)
         \to 
         C^\bullet(\{U_i\}, A_1 \otimes A_2)
$$

by sending $\alpha \in C^p(U,A_1)_\bullet$ and $\beta \in C^q(U,A_2)_\bullet$ to 

$$
  \phi(\alpha \otimes \beta)_{i_0, \cdots , i_{p + q}}
  \;:=\;
  \alpha_{i_0, \cdots, i_p} \otimes \beta_{i_p, \cdots i_{p+q}}
  \,.
$$


For instance ([Brylinski, section (1.3)](#Brylinski)) spring

### In &#268;ech-Deligne cohomology (ordinary differential cohomology)


For the case that of [[?ech cohomology|?ech]] [[hypercohomology]] with coefficients in [[Deligne complex]]es the above yields the _[[Beilinson-Deligne cup-product]]_ for [[ordinary differential cohomology]]. 


## Related concepts

* [[cap product]]

* [[intersection pairing]]

* [[Baer sum]]

* [[cohomology operation]]

* [[power operation]]

* [[Massey product]]

* [[cup product in differential cohomology]]

  * [[cup product in ordinary differential cohomology]]

* [[Euler class]] takes [[Whitney sum]] to [[cup product]], see [this Prop.](Euler+class#EulerClassOfWhitneySumIsCupProductOfEulerClasses)




## References 

* {#Adams74} [[Frank Adams]], part III, sections 2 and 3 of _[[Stable homotopy and generalised homology]]_, 1974


* {#May} [[Peter May]], 18.3 and 22.3 of _A concise course in algebraic topology_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/maybook.pdf))

The cup product in &#268;ech cohomology is discussed for instance in section 1.3 of

* [[Jean-Luc Brylinski]], _Loop spaces and characteristic classes_

Recall from the discussion at [[models for ∞-stack (∞,1)-toposes]] that all [[hypercompletion|hypercomplete]] [[∞-stack]] [[(∞,1)-topos]]es are modeled by the [[model structure on simplicial presheaves]]. Accordingly understanding the cup product on simplicial presheaves goes a long way towards the most general description. For a bit of discussion of this see around page 19 of

* [[John Frederick Jardine]] _Lectures on simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))


An early treatment of cup product can be found in this classic

* Whitney, _On Products in a Complex_ ([JSTOR](http://www.jstor.org/pss/1968795))

See also 

* {#BergerFresse01} [[Clemens Berger]], [[Benoit Fresse]] _Combinatorial operad actions on cochains_, Math. Proc. Cambridge Philos. Soc. 137 (2004), 135-174. ([arXiv:math/0109158](http://arxiv.org/abs/math/0109158))


[[!redirects cup products]]

[[!redirects cup product in abelian Cech cohomology]]
[[!redirects cup product in Cech cohomology]]