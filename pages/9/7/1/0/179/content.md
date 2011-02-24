

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

An _$\infty$-Lie algebroid_ is a [[smooth ∞-groupoid]] (or rather a [[synthetic-differential ∞-groupoid]]) all whose [[k-morphism]]s for all $k$ have _[[infinitesimal space|infinitesimal]] extension_ (are infinitesimal neighbours of an identity $k$-morphism).

$\infty$-Lie algebroids are to [[∞-Lie groupoids]] as [[Lie algebras]] are to [[Lie groups]]:

* [[Lie group]] - [[Lie algebra]]

* [[Lie groupoid]] - [[Lie algebroid]]

* [[∞-group|∞-Lie group]] - [[L-infinity-algebra|∞-Lie algebra]]

* [[∞-Lie groupoid]] - **$\infty$-Lie algebroid** .


## Definition

We discuss $\infty$-Lie algebroids in the [[cohesive (∞,1)-topos]] $\mathbf{H}_{th} := $[[SynthDiff∞Grpd]] of [[synthetic differential ∞-groupoid]]s. This is an <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalCohesion">infinitesimal cohesive neigbourhood</a> of the cohesive $(\infty,1)$-topos $\mathbf{H} :=$ [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s, which is exhibited by the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalPaths">infinitesimal path</a> [[(∞,1)-geometric morphism]]

$$
  (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf}) : 
  SynthDiff\infty Grpd
   \to
  Smooth\infty Grpd
  \,.
$$


### General abstract definition
 {#GeneralAbstractDefinition}

There is a <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#LieAlgebroids">general abstract definition of ∞-Lie algebroid</a> in infinitesimal cohesive neighbourhoods such as $\Pi_{inf} : SynthDiff\infty Grpd \to Smooth\infty Grpd$. 

+-- {: .num_defn #TheGeneralAbstractDefinition}
###### Definition

An object $X \in SynthDiff\inftfy Grpd$ is an 
**infinitesimal synthetic-differential $\infty$-groupoid** if 
$\mathbf{\Pi}_{inf} X \simeq *$.

An [[∞-group]] object $\mathfrak{g} \in SynthDiff\infty Grpd$ that is infinitesimal we call an **[[∞-Lie algebra]]** . 

For $X \in \mathbf{H}$ any object, we say 
$\mathfrak{a} \in \mathbf{H}_{th}$ is an 
**$\infty$-Lie algebroid over $X$** if $\mathbf{\Pi}_{inf}(\mathfrak{a}) \simeq \mathbf{\Pi}_{inf}(X)$; equivalently: if there is a morphism

$$
  \mathfrak{a} \to \mathbf{\Pi}_{inf}(X)
$$

that serves as [[generalized the|the]] $(i^* \dashv i_*)$-[[unit of an adjunction|unit]] on $\mathfrak{a}$, hence as the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalPathsAndReduction">infinitesimal path inclusion</a> for $\mathfrak{a}$.

=--

### Presentation by Chevalley-Eilenberg algebras

We consider _presentations_ of the 
general abstract definition \ref{TheGeneralAbstractDefinition} of $\infty$-Lie algebroids by constructing in the standard [[model structure]]-[[presentable (∞,1)-category|presentation]] of $SynthDiff\infty Grpd$ by [[simplicial presheaves]] on [[CartSp]]${}_{synthdiff}$ certain classes of simplicial presheaves in the image of [[semifree dga|semi-free]] [[differential graded algebra]]s under the [[monoidal Dold-Kan correspondence]]. This amounts to identifying the traditional description of of [[Lie algebra]]s, [[Lie algebroid]]s and [[L-∞ algebra]]s by their [[Chevalley-Eilenberg algebra]]s as a convenient characterization of the corresponding [[cosimplicial algebra]]s whose formal dual simplicial presheaves are manifest presentations of infinitesimal [[smooth ∞-groupoid]]s.



+-- {: .num_defn}
###### Definition

Let

$$
  L_\infty Algd \hookrightarrow dgCAlg_{\mathbb{R}}^{op}
$$

be the [[full subcategory]] on the [[opposite category]] of cochain [[dg-algebra]]s over $\mathbb{R}$ on those dg-algebras that are

* graded-commutative;

* concentrated in non-negative degree (the [[differential]] being of degree +1 );

* in degree 0 of the form $C^\infty(X)$ for $X \in$ [[SmoothMfd]];

* [[semifree dga|semifree]]: their underlying [[graded algebra]] is [[isomorphic]] to an [[exterior algebra]] on a $\mathbb{N}$-graded locally free [[projective object|projective]] $C^\infty(X)$-[[module]]

* of finite [[rank]];

=--

We call this the category of **$L_\infty$-algebroids**.

=--

More in detail, an object $\mathfrak{a} \in L_\infty Algd$ may be identified (non-canonically) with a pair $(CE(\mathfrak{a}), X)$, where

* $X \in SmoothMfd$ is a [[smooth manifold]] -- called the **base space** of the $L_\infty$-algebroid ;

* $\mathfrak{a}$ is the module of smooth [[section]]s of an $\mathbb{N}$-graded [[vector bundle]] of degreewise finite [[rank]];

* $CE(\mathfrak{a}) = (\wedge^\bullet_{C^\infty(X)} \mathfrak{a}^*, d_{\mathfrak{a}})$ is a [[semifree dga]] on $\mathfrak{a}^*$ -- a [[Chevalley-Eilenberg algebra]] -- where

  $$
    \wedge^\bullet_{C^\infty(X)}\mathfrak{a}^* = 
      C^\infty(X) 
       \; \oplus \;
      \mathfrak{a}^*_0
       \; \oplus \;
      (
      \mathfrak{a}^*_0 \wedge_{C^\infty(X)} \mathfrak{a}^*_0
       \oplus
      \mathfrak{a}^*_1
      )
      \; \oplus \; \cdots
  $$

  with the $k$th summand on the right being in degree $k$.

We now construct an embedding of $L_\infty Algs$ into $SynthDiff\infty Grpd$. 

The functor

$$
  \Xi : Ch^\bullet_+(\mathbb{R}) \to Vect_{\mathbb{R}}^{\Delta}
$$

of the [[Dold-Kan correspondence]] from non-negatively graded [[cochain complex]]es of [[vector space]]s to [[cosimplicial object|cosimplicial]] vector spaces is a [[lax monoidal functor]] and hence induces (see [[monoidal Dold-Kan correspondence]]) a functor (which we shall denote by the same symbol)

$$
  \Xi : dgAlg_{\mathbb{R}}^+ \to Alg_{\mathbb{R}}^{\Delta}
$$

from non-negatively graded cochain [[dg-algebra]]s to [[cosimplicial algebra]]s (over $\mathb{R}$).


+-- {: .num_defn #PresentationByMonoidalDoldKan}
###### Definition

Write

$$
  \Xi : L_\infty Algd \to (CAlg_{\mathbb{R}}^\Delta)^{op} 
$$

for the restriction of the above $\Xi$ along the inclusion $L_\infty Algd \hookrightarrow dgAlg^{op}_{\mathbb{R}}$:

for $\mathfrak{a} \in L_\infty Algd$ the underlying cosimplicial vector space of $\Xi \mathfrak{a}$ is given by 

$$
  \Xi \mathfrak{a} 
   : 
  [n]
    \mapsto
  \bigoplus_{i = 0}^{n}
  CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
$$

and the product of the $\mathbb{R}$-algebra structure on the right is given on homogeneous elements $(\omega,x), (\lambda,y) \in CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n$ in the [[tensor product]] by

$$
  (\omega , x)\cdot (\lambda ,y) = (\omega \wedge \lambda , x \wedge y)
  \,.
$$

=--

Notice that $\Xi \mathfrak{a}$ is indeed a _commutative_ cosimplicial algebra, since $\omega$ and $x$ in $(\omega,x)$ are by definition in the same degree.

We shall refine the image of $\Xi$ to cosimplicial [[smooth algebra]]s. Let $T := $[[CartSp]]${}_{smooth}$ be the category of [[Cartesian space]]s and [[smooth function]]s between, them, regarded as a [[Lawvere theory]]. Write 

$$
  SmoothAlg := T Alg
$$

for its category of [[algebra over a Lawvere theory|algebras]]: these are the [[smooth algebra]]s.

Notice that there is a canonical [[forgetful functor]]

$$
  U : SmoothAlg \to CAlg_{\mathbb{R}}
$$

to the category of [[associative algebra|comutative associative algebras]] over the [[real number]]s.

+-- {: .num_prop #SmoothMonoidalDoldKan}
###### Proposition

There is a unique factorization of the functor $\Xi : L_\infty Algd \to (CAlg_{\mathbb{R}}^\Delta)^{op}$ from def. \ref{PresentationByMonoidalDoldKan} through the [[forgetful functor]]
$(SmoothAlg_{\mathbb{R}}^\Delta)^{op} \to (CAlg_{\mathbb{R}}^\Delta)^{op}$ such that for any $\mathfrak{a}$ over base space $X$ the degree-0 algebra of smooth functions $C^\infty(X)$ lifts to its canonical structure as a [[smooth algebra]]

$$
  \array{
    && (SmoothAlg^{\Delta})^{op}
    \\
    & \nearrow & \downarrow^{\mathrlap{U}}
    \\
    L_\infty Algd &\to& (CAlg_{\mathbb{R}}^\Delta)^{op}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Observe that for each $n$ the algebra $(\Xi \mathfrak{a})_n$ is a finite nilpotent extension of $C^\infty(X)$. The claim then follows with using [[Hadamard's lemma]] to write every smooth function of sums as a finite Taylor expansion with a smooth rest term. See the examples at [[smooth algebra]] for more details on this kind of argument.

=--

+-- {: .num_defn}
###### Definition

Write $i : L_\infty Algd \to SynthDiff\infty Grpd$ for the composite [[(∞,1)-functor]]

$$
  L_\infty Algd 
     \stackrel{\Xi}{\to} 
  (SmoothAlg^{\Delta})^{op}
    \stackrel{j}{\to} 
  [CartSp_{synthdiff}^{op}, sSet]
   \stackrel{P Q}{\to}
  ([CartSp_{synthdiff}^{op}, sSet]_{loc})^\circ
  \simeq
  SynthDiff\infty Grpd
  \,,
$$

where the first morphism is the [[monoidal Dold-Kan correspondence]] as in prop. \ref{SmoothMonoidalDoldKan}, the second is the external degreewise [[Yoneda embedding]] and $P Q$ is any fibrant-cofibrant [[resolution]] functor in the local [[model structure on simplicial presheaves]]. The last equivalence holds as discussed there and at [[models for ∞-stack (∞,1)-toposes]].

=--

+-- {: .num_remark}
###### Remark

We do not consider the standard [[model structure on dg-algebras]] and do not consider $L_\infty Algd$ itself as a [[model category]] and do not consider an [[(∞,1)-category]] spanned by it. Instead, the functor $i : L_\infty Algd \to SynthDiff\infty Grpd$ only serves to exhibit a class of objects in $SynthDiff\infty Grpd$, which below in the seciton [ModelsForTheAbstractAxioms](#ModelsForTheAbstractAxioms) we show are indeed $\infty$-Lie algebroids by the general abstract definition, \def{TheGeneralAbstractDefinition}. All the [[homotopy theory]] of objects in $L_\infty Algd$ we is that of $SynthDiff\infty Grpd$ after this embedding.

=--


## Properties

### As models for the abstract axioms
 {#ModelsForTheAbstractAxioms}

Above we have given a general abstract definition, 
def. \ref{TheGeneralAbstractDefinition} of $\infty$-Lie algebroids, and then a concrete construction in terms of [[dg-algebra]]s, def. \ref{PresentationByMonoidalDoldKan}. Here we discuss that this concrete construction is indeed a presentation for objects satisfying the abstract axioms.

+-- {: .un_lemma }
###### Lemma


The object $\mathbf{B}\mathfrak{g} \in [ThCartSp^{op}, sSet]_{proj,loc}$ is cofibrant.

=--

+-- {: .proof}
###### Proof

The [[coend]] over the [[tensoring]] 

$$
  \int^{[k] \in \Delta}
  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj} \times
  [\Delta^{op}, (T Alg^\Delta_{proj})^{op}]_{inj}
  \to 
  (T Alg^\Delta_{proj})^{op}
$$

for the projective and injective [[global model structure on functors]] on the [[simplex category]] and its opposite is a [[Quillen bifunctor]] (as discussed there). We have moreover

1. The [[fat simplex]] is cofibrant in $[\Delta, sSet_{Quillen}]_{proj}$. 

1. Because every representable $ThCartSp \hookrightarrow [ThCartSp^{op}, sSet]_{proj}$ is cofibrant the object $\mathfrak{g}_\bullet \in [\Delta^{op}, [ThCartSp^{op}, sSet]_{proj}]_{inj}$ is cofibrant.

Therefore also $\mathbf{B}\mathfrak{g}$ is cofibrant.

=--


+-- {: .un_lemma }
###### Lemma

The image of $\mathbf{B}\mathfrak{g}$ under the [[(∞,1)-functor]] $\mathcal{O} : \mathbf{H} \to \mathbf{L}$ described at [[function algebras on ∞-stacks]] is weakly equivalent to the object modeled by $\int^{[k] \in \Delta} \Delta[k] \cdot \mathfrak{g}_k$ (meaning: with the ordinary instead of the fat simplex).

=--


+-- {: .proof}
###### Proof

As described at [[function algebras on ∞-stacks]] the $(\infty,1)$-functor $\mathcal{O}$ is modeled by a [[Quillen adjunction]]

$$
  (T Alg^\Delta_{proj})^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\to}
  [ThCartSp^{op}, sSet]_{proj}
  \,,
$$

where $T = $ [[CartSp]] is the [[Lawvere theory]] of [[smooth algebra]]s.

We use now the [[Reedy model structure]]s over the [[simplex category]]: 

In $[\Delta^{op}, (T Alg^{\Delta}_{proj})^{op}]_{Reedy}$ we have that $[k] \mapsto \mathfrak{g}_k$ is cofibrant, because the inclusion of the degenerate $k$-cells into all $k$-cells is dually a surjection of algebras, hence dually a fibration. 

The [[coend]] over the [[tensoring]] 

$$
  \int^{[k] \in \Delta}
  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{Reedy} \times
  [\Delta^{op}, (T Alg^\Delta_{proj})^{op}]_{Reedy}
  \to 
  (T Alg^\Delta_{proj})^{op}
$$

is a [[Quillen bifunctor]] (as discussed there).

Since both the simplex $\Delta$ as well as the [[fat simplex]] $\mathbf{\Delta}$ [[Reedy model structure|are Reedy cofibrant]] and the map $\mathbf{\Delta} \to \Delta$ a weak equivalence, it follows (by the [[factorization lemma]]) that 

$$
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{g}_k
    \stackrel{\simeq}{\to} 
  \int^{[k] \in \Delta} \Delta[k] \cdot \mathfrak{g}_k
$$

is a weak equivalence in $(T Alg^\Delta_{proj})^{op}$.

=--



+-- {: .un_corollary }
###### Corollary

The image of $\mathbf{B}\mathfrak{g}$ under the [[(∞,1)-functor]] $\Pi : \mathbf{H} \to \infty Grpd$ described ar [[locally ∞-connected (∞,1)-topos]] is [[contractible]]

$$
  \Pi \mathbf{B}\mathfrak{g} \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since by the above lemma $\mathbf{B}\mathfrak{g}$ is cofibrant, the $(\infty,1)$-functor $\Pi$ acts degreewise by replacing the representable presheaf by the point

$$
  \Pi : 
  \mathbf{B}\mathfrak{g}
  =
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{g}_{k} 
  \mapsto 
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot *
  \,.
$$ 

That this is equivalent to the point follows from the fact that $\emptyset \to \mathbf{\Delta}$ is an acylic cofibration in $[\Delta, sSet_{Quillen}]_{proj}$, and that

$$
  \int^{[k] \in \Delta}
  (-)\times (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj}
  \times
  [\Delta^{op}, sSet_{Qillen}]_{inj}
  \to 
  sSet_{Quillen}
$$

is a [[Quillen bifunctor]], using that $* \in [\Delta^{op}, sSet_{Quillen}]_{inj}$ is cofibrant.


=--

+-- {: .un_corollary }
###### Corollary

The image of $\mathbf{B}\mathfrak{g}$ under the [[global section]] [[(∞,1)-functor]] $\Gamma : \mathbf{H} \to \infty Grpd$ is [[contractible]]

$$
  \Gamma \mathbf{B}\mathfrak{g} \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since [[ThCartSp]] is an [[(∞,1)-cohesive site]] and using the main theorem there, we have that $\Gamma$ is modeled by the functor that evaluates on the point, and that this is a left Quillen functor

$$
  Hom(*,-) : [ThCartSp^{op}, sSet]_{proj,loc} \to sSet_{Quillen}
  \,.
$$

Therefore $\Gamma \mathbf{B}\mathfrak{g}$ is modeled by degreewise evaluating $\mathfrak{g}_k$ on the point. But since this is by assumption an [[infinitesimal space]] it has only a single point, so that

$$
  \Gamma \mathbf{B}\mathfrak{g}_k  = \int^{[k] \in \Delta} \mathbf{\Delta}[k]
  \,.
$$

As in the previous corollary, this is equivalent to the point.

=--

+-- {: .un_corollary }
###### Corollary

The canonical morphism

$$
  \Gamma \mathbf{B}\mathfrak{g} \to \Pi \mathbf{B}\mathfrak{g}
$$


is an [[equivalence in a quasi-category|equivalence]] in [[∞Grpd]].

=--

By the discussion at [[cohesive (∞,1)-topos]] this characterizes $\mathbf{B}\mathfrak{g}$ intrinsically as an infinitesmal object.


### Lie algebroids regarded as $\infty$-Lie algebroids

We discuss the traditional notion of [[Lie algebroid]]s as a presentation for [infinitesimal synthetic differential 1-groupoids](#GeneralAbstractDefinition).


#### Smooth loci of infinitesimal simplices 

It turns out that regarded as infinitesimal [[synthetic-differential ∞-groupoid]]s Lie algebroids are build from spaces of infinitesimal simplices, as described in ([Kock](#Kock)).

An **infinitesimal $k$-[[simplex]]** in $R^n$ based at the origin is a collection $(\vec \epsilon_i \in R^n)_{i = 1}^k$ of points in $R^n$, such that each is an infinitesimal neighbour of the origin

$$
  \forall i : \;\; \vec \epsilon_i \sim 0
$$ 

and each are infinitesimal neighbours of each other

$$
  \forall i,j: \;\; (\vec \epsilon_i - \vec \epsilon_j) \sim 0
  \,.
$$

Following ([Kock, section 1.2](#Kock))
we write $\tilde D(k,n)$ for the space of all infinitesimal $k$-simplices in $R^n$. More precisely, this is defined as the formal dual of the algebra $C^\infty(\tilde D(k,n))$ defined as follows.

Functions on spaces of infinitesimal $k$-simplices turn out to be degree $k$-differential forms. This provides a "synthetic" way of precisely thinking of wedge produts $d x \wedge dy$ etc as products of infinitesimals. As the following computations do show, the skew-commutativity of the wedge product is an inherent consequence of the nature of infinitesimals.

+-- {: .un_def}
###### Definition

The algebra $C^\infty(\tilde D(k,n))$ is the 
commutative $\mathbb{R}$-algebra generated from $k \times n$ generators $(\epsilon_i^j)_{1 \leq i \leq n, 1 \leq j \leq n}$ subject to the relations

$$
  \forall i, j,j' : \;\; \epsilon_i^{j} \epsilon_i^{j'} = 0
$$

and

$$
  \forall i,i',j,j'   : \;\;\; 
  (\epsilon_i^j - \epsilon_{i'}^j) (\epsilon_i^{j'} - \epsilon_{i'}^{j'}) = 0
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

By multiplying out the latter set of relations and using the former, these relations are seen to be equivalent to the set of relations

\[
  \forall i,i',j,j' : \;\;\;
  \epsilon_i^j \epsilon_{i'}^{j'} 
  + \epsilon_{i'}^j \epsilon_{i}^{j'} = 0
  \,.
\]

Notice that this implies also that

$$
  \forall i,i', j: \;\;\;  \epsilon_i^{j} \epsilon_{i'}^j = 0
  \,.
$$

=--

A general element $f$ of this algebra we think of as a function on a certain infinitesimal neightbourhood of the origin of $R^{k \cdot n}$, interpreted as the space of infinitesimal $k$-simplices in $R^n$ based at 0.

Since $C^\infty(\tilde D(k,n))$ is a [[infinitesimally thickened point|Weil algebra]] in the sense of [[synthetic differential geometry]], its structure as an $\mathbb{R}$-algebra extends uniquely to the structure of a [[smooth algebra]] (as discussed there) and we may think of $\tilde D(k,n)$ as an infinitesimal [[smooth locus]].

+-- {: .un_example}
###### Example

For $n = 2$ and $k = 2$ we have that $C^\infty(\tilde D(2,2))$ consists of elements of the form

$$
  \begin{aligned}
    f
    +
    a \cdot \epsilon_1 
     + b \cdot \epsilon _2 
     + (\omega \cdot \epsilon_1) (\lambda \cdot \epsilon_2) 
    &= 
    f + 
    a_1 \epsilon_1^1 
     + a_2 \epsilon_1^2 
     + b_1 \epsilon_2^1 
     + b_2 \epsilon_1^2
    \\
    & + (\omega_1 \lambda_2 - \omega_2 \lambda_1) 
      \frac{1}{2}(\epsilon_1^1 \epsilon_2^2 - \epsilon_1^2 \epsilon_2^1)
  \end{aligned}
$$

for $f \in \mathbb{R}$ and $(a, b, \omega, \lambda \in (\mathbb{R}^n)^*)_{1 \leq i \leq n}$ a collection of ordinary covectors and with "$\cdot$" denoting the evident contraction, and where in the last step we used the above relations.

It is noteworthy here that the coefficient of the term which is multilinear in each of the $\epsilon_i$ is the [[wedge product]] of two [[covector]]s $\omega$ and $\lambda$: we may naturally identify the subspace of $C^\infty(\tilde D(2,2))$ on those elements that vanish if either $\epsilon_1$ or $\epsilon_2$ are set to 0 as the space $\wedge^2 T_0^* \mathbb{R}^2$ of 2-forms at the origin of $\mathbb{R}^2$. 

Of course for this identification to be more than a coincidence we need that this is the beginning of a pattern that holds more generally. But this is indeed the case.

=--


Let $E$ be the set of _square_ submatrices of the $k \times n$-matrix $(\epsilon_i^j)$. As a set this is isomorphic to the set of pairs of subsets of the same size of $\{1, \cdots, k\}$ and $\{1, \cdots , n\}$, respectively. For instance the square submatrix labeled by $\{2,3,4\}$ and  $\{1,4,5\}$ is

$$
  e 
  =
  \left(
    \array{
       \epsilon_1^2 & \epsilon_4^2 & \epsilon_5^2
       \\
       \epsilon_1^3 & \epsilon_4^3 & \epsilon_5^3
       \\
       \epsilon_1^4 & \epsilon_4^4 & \epsilon_5^4
    }
  \right)
  \,.
$$


For $e \in E$ an $r\times r$ submatrix, we write 

$$
  det(e) = 
    \sum_{\sigma} sgn(\sigma) 
    \epsilon_{1}^{\sigma(1)} \epsilon_2^{\sigma(2)}
    \cdots 
    \epsilon_r^{\sigma(r)}
  \in
  C^\infty(\tilde D(k,n))
  \,.
$$ 

for the corresponding [[determinant]], given as a product of generators in $C^\infty(\tilde D(k,n))$. Here the sum runs over all [[permutation]]s $\sigma$ of $\{1, \cdots, r\}$ and $sgn(\sigma) \in \{+1, -1\} \subset \mathbb{R}$ is the [[signature]] of the permutation $\sigma$.


+-- {: .un_prop}
###### Proposition


The elements $f \in C^\infty(\tilde D(k,n))$ are precisely of the form

$$
  f = \sum_{e \in E} f_e \; det(e) 
$$

for _unique_ $\{f_e \in \mathbb{R} | e \in E\}$. In other words, the map of [[vector space]]s

$$
  \mathbb{R}^{|E|} \to C^\infty(\tilde D(k,n))
$$

given by 

$$
  (f_e)_{e \in E} \mapsto \sum_{e \in E} f_e det(e) 
$$ 

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

This is a direct extension of the argument in the above example: a general product of $r$ generators in $C^\infty(\tilde D(k,n))$ is

$$
  \epsilon_{i_1}^{j_1} \epsilon_{i_2}^{j_2} 
   \cdots \epsilon_{i_r}^{j_r}
  \,.
$$

By the relations in $C^\infty(\tilde D(k,n))$, this is non-vanishing precisely if none of the $i$-indices repeats and none of the $j$-indices repeats. Furthermore by the relations, for any permutation $\sigma$ of $r$ elements, this is equal to

$$
  \cdots = sgn(\sigma) 
   \epsilon_{i_1}^{j_{\sigma(1)}} 
   \epsilon_{i_1}^{j_{\sigma(2)}}
   \cdots 
   \epsilon_{i_1}^{j_{\sigma(r)}}
  \,.
$$

It follows that each such element may be written as

$$
  \cdots = \frac{1}{r!} det(e)
  \,,
$$

where $e$ is the $r \times r$ subdetermined given by the subset $\{i_1, \cdots, i_r\}$ and $(\{j_1, \cdots, j_r\})$ as discussed above.
=--

+-- {: .un_remark}
###### Remark

In ([Kock, section 1.3](#Kock)) effectively this proposition appears as the "[[Kock-Lawvere axiom]] scheme for $\tilde D(k,n)$" when $\tilde D(k,n)$ is regarded as an object of a suitable [[smooth topos]]. It is useful to record this simple but very crucial observation of Anders Kock here in the category $Alg_{\mathbb{R}}^{op}$ or in the category $C^\infty Alg^{op}$ of [[smooth loci]], as we do here, where it is just a simple observation. The point of the Kock-Lawvere axiom scheme is effectively to ensure that the properties of $C^\infty(\tilde D(k,n)) \in C^\infty Alg^{op}$ are preserved under [[Yoneda embedding]] into a corresponding [[sheaf topos]]. But it has been observed that it serves to clarify what is going on in parts of Ander Kock's book by separating the combinatorial and algebraic arguments from their internalization into suitable [[smooth topos]]es.

=--


#### Lie algebroids by smooth loci of infinitesimal simplices

+-- {: .un_prop}
###### Observation

Let $\mathfrak{g}$ be a [[Lie algebroid]] of rank $n$ over $X$, then $\Xi CE(\mathfrak{g})$ is at $x \in X$ the smooth locus $\tilde D(k, n)$ of infinitesimal $k$-simplices at the origin of $\mathbb{R}^n$.

=--

Proof.

Let $\{t^i\}$ be a basis for $\mathfrak{g}^*$ and $\{k_j\}$ a basis for $\mathbb{R}^n$. Then identify

$$
  \epsilon^i_j := t^i \otimes k_j
  \,.
$$


## Examples

### Classes of examples

* a $\infty$-Lie algebroid over the [[point]], $\mathfrak{a} = *$ is an **[[L-∞-algebra]]**;

* an $n$-[[truncated]] $\infty$-Lie algebroid is a **Lie $n$-algebroid**;

* an $\infty$-Lie algebroid the differential of whose [[Chevalley-Eilenberg algebra]] is "co-binary", i.e. $d : \mathfrak{a}^* \to a^* \oplus a^* \wedge g^*$, is **strict**.

So in particular

* a 1-Lie algebroid is a **[[Lie algebroid]]**;

* a 1-Lie algebroid over the point is a **[[Lie algebra]]**;

* a Lie $n$-algebroid over a point is a **[[Lie n-algebra]]**.

* a _[[BRST-complex]]_ is the [[Chevalley-Eilenberg algebra]]
  of an action-$\infty$-Lie algebroid of the 
  [[action]] of an $L_\infty$-algebra, see [[Lie ∞-algebroid representation]];

  more generally, the complexes appearing in [[BV-BRST formalism]] are 
  derived $\infty$-Lie algebroids, whose Chevalley-Eilenberg algebra may have generators in negative degree.

* a [[symplectic Lie n-algebroid]] is a Lie $n$-algebroid equipped with a non-degrenerate bilinear [[invariant polynomial]] of degree $n+2$. For low $n$ this is

  * $n = 0$: a [[symplectic manifold]];

  * $n = 1$: a [[Poisson Lie algebroid]];

  * $n = 2$: a [[Courant algebroid]]

* Standard examples of [[exterior differential system]]s are [[Chevalley?Eilenberg algebras]] of $L_\infty$-algebroids.




### Tangent Lie algebroid {#TangentLieAlgebroid}

The following example is in a way the archetypical example on which all others are modeled in a sense.

For $X$ any [[smooth manifold]], there is a standard notion of the [[Lie algebroid]] which is the [[tangent Lie algebroid]] of $X$. As an $\infty$-Lie algebroid, this is the [[simplicial object|simplicial]] [[smooth locus]] given by the [[infinitesimal singular simplicial complex]] 

$$
  T X = 
  \left(
      \cdots 
      X^{(\Delta^2_{inf})} 
        \stackrel{\to}{\stackrel{\to}{\to}} 
        X^{(\Delta^1_{inf})} 
       \stackrel{\to}{\to} X
  \right)
$$

of $X$. By the central observation on combinatorial [[differential forms in synthetic differential geometry]] by [[Anders Kock]], the [[Chevalley-Eilenberg algebra]] of this is indeed isomorphic to the [[de Rham complex]] of $X$:

$$
  CE(T X) := N C^\infty(T X) \simeq (\Omega^\bullet(X), d_{dR})
  \,.
$$

For more details on the computations involved see [Spaces of infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) at [[infinitesimal object]].

In particular for $X = \mathbb{R}^n$ a [[Cartesian space]], we have

$$
  T \mathbb{R}^n
  =
  \left(
      \cdots 
      \mathbb{R}^n \times \tilde D(2,n)
        \stackrel{\to}{\stackrel{\to}{\to}} 
        \mathbb{R}^n \times \tilde D(1,n)
       \stackrel{\to}{\to} 
       \mathbb{R}^n
  \right)   
  \,,
$$

where $\tilde D(k,n)$ is the [[smooth locus]] of [infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) based at the origin in $\mathbb{R}^n$.


### Lie algebra {#LieAlgebra}


Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$. We describe how $\mathfrak{g}$ looks when regarded as a special case of an $\infty$-Lie algebroid.

Write 

$$
  \mathbf{B}G =
  \left(
     \cdots G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} * 
  \right)
$$

for the [[delooping]] [[groupoid]] of $G$, regarded as an an [[∞-Lie groupoid]] modeled by a simplicial [[smooth space]].

We claim that a morphism 

$$
  \omega : T U \to \mathbf{B}G
$$

from the tangent Lie algebroid of some $U \in $ [[CartSp]] is [[groupoid of Lie-algebra valued forms|flat Lie-algebra valued form]] and how that can be used to find the [[Lie algebra]] $\mathfrak{g}$ as the infinitesimal sub-$\infty$-groupoid

$$
  \mathbf{b}\mathfrak{g} \hookrightarrow \mathbf{B}G
$$

inside $\mathbf{B}G$.

Since $\mathbf{B}G$ is [[simplicial skeleton|2-coskeletal]] (being the [[nerve]] of a [[groupoid]]) a morphism $T U \to \mathbf{B}G$ is fixed already under its 2-[[truncated|truncation]]

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    G \times G
    \\
    \downarrow \downarrow \downarrow && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) &\stackrel{\omega_1}{\to}& G
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    U &\to& *
  }
  \,.
$$

It is clear that $\omega_1$ factors through the inclusion $\tilde D(1,dim(G)) \hookrightarrow G$ that sends the unique point of $\tilde D(1, dim(G))$ to the neutral element (by respect for the degeneracy maps).
Then from that one finds that $\omega_2$ factors through the inclusion $\tilde D(2, dim(G)) \hookrightarrow G \times G$ that sends the unique point of $\tilde D(2,dim(G))$ to $(e,e) \in G \times G$. And evidently these two factorizations are universal, in that every other factorization will uniquely factor through these

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    \tilde D(2,dim(G))
    &\hookrightarrow&
    G \times G
    \\
    \downarrow \downarrow \downarrow 
     && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    &&
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) 
    &\stackrel{\omega_1}{\to}& 
    \tilde D(1, dim(G))
    &\hookrightarrow&
    G
    \\
    \downarrow \downarrow 
    && \downarrow \downarrow
    && \downarrow \downarrow
    \\
    U &\to& * &\to& *
  }
  \,.
$$

The universal object found this way we claim is the Lie algebra $\mathfrak{g}$ in its incarnation as an infinitesimal $\infty$-Lie groupoid

$$
  \begin{aligned}
    b \mathfrak{g}
    &:=
    InitialObject( T U\downarrow \mathbb{L}^{Delta^{op}}\downarrow \mathbf{B}G)
    \\
    & =
    \left(
       \cdots
       \tilde D(2,dim(G))
       \stackrel{\to}{\stackrel{\to}{\to}}
     \tilde D(1,dim(G))\stackrel{\to}{\to} *
    \right)
  \end{aligned}  
  \,. 
$$

+-- {: .un_prop}
###### Proposition

The normalized cochain complex of the cosimplicial alghebra of functions on this $b \mathfrak{g}$ is isomorphic to the ordinary [[Chevalley-Eilenberg algebra]] $(\wedge^\bullet \mathfrak{g}^*, [-,-]^*)$ of $\mathfrak{g}$.

=--

+-- {: .proof}
###### Proof

By the discussion at [Spaces of infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) we have that for $C^\infty(\tilde D(k,dim(G)))_{top} \subset C^\infty(\tilde D(k,n))$ the subspace of those functions that are in the joint kernel of the co-degeneracy maps is naturally isomorpic to $\wedge^k (\mathbb{R}^{dim(G)})^*$, so that we have a natural isomorphism of vector spaces

$$
  N C^\infty(b \mathfrak{g})_k \simeq \wedge^k \mathfrak{g}^*
  \,.
$$

By the fact that everything is [[simplicial skeleton|2-coskeletal]] it suffices to check that the differential in first degree

$$
  N C^\infty(\tilde D(1,dim(G)))
  \stackrel{p_1^* + p_2^* - (\cdot)^*}{\to}
  N C^\infty(\tilde D(2,dim(G)))
$$

is indeed the dual of the Lie bracket. But the product $\cdot_G : G \times G \to G$ restricted along $\tilde D(2,dim(G)) \hookrightarrow G \times G$ to the [[infinitesimal space]] $\tilde D(2, dim(G))$ linearizes in each of its arguments: for $(\vec x,\vec y) \in \tilde D(2,dim(G))$ we have

$$
  \vec x \cdot_G \vec y = 
  \vec x \cdot \nabla_x \cdot_G (0,0)
  + 
  \vec y \cdot \nabla_y \cdot_G (0,0)
  +
  \vec x \cdot \nabla_x 
  \vec y \cdot \nabla_y \cdot_G(0,0)
  \,.
$$

Since the origin here corresponds to the neutral element of $G$ and since with one of its arguments the neutral element the operaton $\cdot_G$ is the identity, and since the double derivative produces the Lie bracket (keeping in mind that $x^i y^j  + x^j y^i = 0$ in $\tilde D(2,dim(G))$), this is

$$
  \cdots = \vec x + \vec y + [\vec x, \vec y]
  \,.
$$

Accordingly the alternating sum of co-face maps is

$$
  \begin{aligned}
     d &= p_1^* + p_2^* - \cdot_G^* 
     \\ & = p_1^* + p_2^* - ( p_1^* + p_2^* + [-,-]^*)
     \\ & = - [-,-]^*
  \end{aligned}
$$

as it should be for the Chevalley-Eilenberg algebra of a Lie algebra.

=--

The infinitesimal reasoning involved in this proof is discussed in section 6.8 of 

* [[Anders Kock]], _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


### Tangent Lie algebroid of a Lie algebra {#TangentOfLieAlgebra}


We can form the tangent $\infty$-Lie algebroid of any $\infty$-Lie algebroid $\mathfrak{a}$ as

$$
  T \mathfrak{a}
  = 
  \int^{[n] \in \Delta} \Delta[n] \cdot T \mathfrak{a}_n
  =
  \int^{[n] \in \Delta} \Delta[n] \cdot (\mathfrak{a}_n)^{(\Delta^\bullet_{inf})}
  \,.
$$

We want to claim now that for $\mathfrak{g}$ a Lie algebra, we have a canonical isomorphism

$$
  CE(T b \mathfrak{g}) \simeq W(\mathfrak{g})
$$

that identifies the [[Chevalley-Eilenberg algebra]] of the tangent Lie algebra of $b \mathbf{g}$ with the [[Weil algebra]] of $\mathfrak{g}$.


The key observation for this is that in the [[bisimplicial set|bisimplicial object]]

$$
  \array{
    && \vdots && \vdots && \vdots
    \\
    &\cdots&
    \tilde D(3,dim(G))^{(\Delta^2_{inf})} && 
    \tilde D(3,dim(G))^{(\Delta^1_{inf})} && 
    \tilde D(3,dim(G))
    \\
    &&\downarrow \downarrow \downarrow  
    && \downarrow \downarrow \downarrow 
    && \downarrow \downarrow \downarrow
    \\
    &\cdots&
    \tilde D(1,dim(G))^{(\Delta^2_{inf})} && 
    \tilde D(1,dim(G))^{(\Delta^1_{inf})} && 
    \tilde D(1,dim(G))
    \\
    && \downarrow \downarrow  
    && \downarrow \downarrow && \downarrow \downarrow
    \\
     &\cdots& * &\stackrel{\to}{\stackrel{\to}{\to}}&  * 
    &\stackrel{\to}{\to}& *
  }
$$

* the functions on infinitesimal simplices in an infinitesimal space that vanish on degenerate simplices are already isomorphic to covectors at the origin;

* the functions on infinitesimal $r$-simplices in a $\tilde D(k,dim(G))$ for $r \gt k$ which vanish on degenerate simplices already vanish entirely.

Using this the total complex of $N C^\infty(-)$ of this bisimplicial set is manifestly isomorphic to the Weil algebra.






## Related concepts

* [[∞-Lie algebroid cohomology]]

* [[∞-Lie algebroid valued differential forms]]

* [[∞-Chern-Weil theory]]

## References

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[dg-algebra]]s or [[NQ-supermanifolds]] and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifolds]]". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model|Sullivan models]] in [[rational homotopy theory]], which is concerned with modelling _[[topological space]]s_ by [[dg-algebras]]. That these spaces can be regarded as [[∞-groupoids]] and as [[∞-Lie groupoids]] in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]], [[rational homotopy theory in an (∞,1)-topos]] and [[function algebras on ∞-stacks]].

The explicit term _$\infty$-Lie algebroid_ / _$L_\infty$-algebroid_ as such appears in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string- and  fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">ref</a>)

The term also appears in

* Andrew James Bruce, _From $L_{\infty}$-algebroids to higher Schouten/Poisson structures_ ([arXiv:1007.1389](http://arxiv4.library.cornell.edu/abs/1007.1389))

The smooth spaces of infinitesimal simplices $\tilde D(k,n)$ are considered in

* [[Anders Kock]],  _Synthetic differential geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))
{#Kock}

[[!redirects L-infinity-algebroid]]
[[!redirects L-infinity algebroid]]
[[!redirects L-infinity Lie algebroid]]

[[!redirects L-∞-algebroid]]
[[!redirects L-∞ algebroid]]
[[!redirects L-∞ Lie algebroid]]


[[!redirects Lie-∞-algebroid]]
[[!redirects Lie-∞-algebroids]]
[[!redirects Lie-∞ algebroid]]
[[!redirects Lie-∞ algebroids]]
[[!redirects Lie ∞-algebroid]]
[[!redirects Lie ∞-algebroids]]
[[!redirects L-infinity-algebroids]]
[[!redirects L-infinity algebroids]]
[[!redirects L-infinity Lie algebroids]]

[[!redirects ∞-Lie algebroid]]
[[!redirects ∞-Lie algebroids]]

[[!redirects infinity-Lie algebroid]]
[[!redirects infinity-Lie algebroids]]

[[!redirects Lie n-algebroid]]
[[!redirects Lie n-algebroids]]