
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #AdditiveCategory}
###### Definition

An **additive category** is a [[category]] which is

1. an [[Ab-enriched category]];

   (sometimes called a [[pre-additive category]]--this means that each [[hom-set]] carries the structure of an [[abelian group]] and composition is [[bilinear map|bilinear]])

1. which admits [[finite limit|finite]] [[coproducts]] 

   (and hence, by prop. \ref{ProductsAreBiproducts} below, finite [[products]] which coincide with the coproducts, hence finite [[biproducts]]).

The natural [[morphisms]] *between* additive categories are [[additive functors]].


=--

+-- {: .num_remark }
###### Remark

A [[pre-abelian category]] is an additive category which also has [[kernels]] and [[cokernels]].  Equivalently, it is an Ab-enriched category with all [[finite limits]] and finite [[colimits]].  An especially important sort of additive category is an [[abelian category]], which is a pre-abelian one satisfying the extra exactness property that all [[monomorphisms]] are [[kernels]] and all [[epimorphisms]] are [[cokernels]].  See at _[[additive and abelian categories]]_ for more.

=--

+-- {: .num_remark }
###### Remark

The [[Ab]]-enrichment of an additive category does not have to be given a priori.  Every [[semiadditive category]] (a category with finite [[biproducts]]) is automatically  [[enriched category|enriched]] over [[commutative monoids]] (as described at _[[biproduct]]_), so an additive category may be defined as a category with finite biproducts whose [[hom-object|hom-monoids]] happen to be [[groups]].  (The requirement that the hom-monoids be groups can even be stated in elementary terms without discussing enrichment at all, but to do so is not very enlightening.)  Note that the entire $Ab$-enriched structure follows automatically for [[abelian category|abelian categories]].

=--

+-- {: .num_remark }
###### Remark

Some authors use **additive category** to simply mean an Ab-enriched category, with no further assumptions. It can also be used to mean a $CMon$-enriched (commutative monoid enriched) category, with or without assumptions of products. 

=--




## Properties


+-- {: .num_prop #ProductsAreBiproducts}
###### Proposition

In an [[Ab-enriched category]] (or even just a $CMon$-enriched category), a [[finite product|finite]] [[product]] is also a [[coproduct]], and dually (hence a [[biproduct]]).  

This statement includes the zero-ary case: any [[terminal object]] is also an [[initial object]], hence a [[zero object]] (and dually), hence every additive category has a [[zero object]].  

More precisely, for $\{X_i\}_{i \in I}$ a [[finite set]] of objects in an Ab-enriched category, the unique morphism 

$$
  \underset{i \in I}{\coprod} X_i \longrightarrow \underset{j \in I}{\prod} X_j
$$

whose components are identities for $i = j$ and are [[zero morphism|zero]] otherwise is an [[isomorphism]].


=--

+-- {: .proof}
###### Proof

Consider first the nullary (i.e., zero-ary) case. Given a [[terminal object]] $\ast$, the unique morphism $id_\ast: \ast \to \ast$ is the zero morphism $0$ in its hom-object. For any object $A$, the zero morphism $0_A: \ast \to A$ must equal any morphism $f: \ast \to A$ on account of $f = f id_\ast = f 0 = 0_A$ where the last equation is by $CMon$-enrichment. Hence $\ast$ is initial. (N.B.: this argument applies more generally to categories [[enriched category|enriched]] in [[pointed sets]], and is self-[[formal duality|dual]].) 

Consider now the case of binary (co-)products. Using [[zero morphisms]], in addition to its canonical [[projection]] maps $p_i \colon X_1 \times X_2 \to X_i$, any binary [[product]] also admits "injection" maps $X_i \to X_1 \times X_2$, and dually for the [[coproduct]]:

$$
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{(id,0)}} && {}^{\mathllap{(0,id)}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow && X_1 \times X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    & \swarrow_{\mathrlap{p_{X_1}}} && {}_{\mathllap{p_{X_2}}}\searrow
    \\
    X_1 && && X_2
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\,,\;\;\;\;\;\;\;\;\;\;\;\;
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{i_{X_1}}} && {}^{\mathllap{i_{X_2}}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow 
     && X_1 \sqcup X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    & \swarrow_{\mathrlap{(id,0)}} && {}_{\mathllap{(0,id)}}\searrow
    \\
    X_1 && && X_2
  }
  \,.
$$

Observe some basic compatibility of the $Ab$-enrichment with the product: 

First, for $(\alpha_1,\beta_1), (\alpha_2, \beta_2)\colon R \to X_1 \times X_2$ then 

$$
  (\star)
  \;\;\;\;\;\;
  (\alpha_1,\beta_1) + (\alpha_2, \beta_2) 
    = 
  (\alpha_1+ \alpha_2 , \; \beta_1 + \beta_2)
$$

(using that the projections $p_1$ and $p_2$ are linear and by the universal property of the product).

Second, $(id,0) \circ p_1$ and $(0,id) \circ p_2$ are two projections on $X_1\times X_2$ whose sum is the identity:

$$
  (\star\star)
  \;\;\;\;\;\;
  (id, 0) \circ p_1
  +
  (0, id) \circ p_2
    =
  id_{X_1 \times X_2} 
  \,.
$$

(We may check this, via the [[Yoneda lemma]] on [[generalized elements]]: for $(\alpha, \beta) \colon R \to X_1\times X_2$ any morphism, then $(id,0)\circ p_1 \circ (\alpha,\beta) = (\alpha,0)$ and $(0,id)\circ p_2\circ (\alpha,\beta) = (0,\beta)$, so the statement follows with equation $(\star)$.)


Now observe that for $f_i \;\colon\; X_i \to Q$ any two morphisms, the sum 

$$
  \phi 
    \;\coloneqq\; 
  f_1 \circ p_1 + f_2 \circ p_2
    \;\colon\;
  X_1 \times X_2
    \longrightarrow
  Q
$$

gives a morphism of [[cocones]]

$$
  \array{  
    X_1 && && X_2
    \\
    & \searrow^{\mathrlap{(id,0)}} && {}^{\mathllap{(0,id)}}\swarrow
    \\
    {}^{\mathllap{id_{X_1}}}\downarrow && X_1 \times X_2 && \downarrow^{\mathrlap{id_{X_2}}}
    \\
    &  && 
    \\
    X_1 && \downarrow^{\mathrlap{\phi}} && X_2
    \\
    & {}_{\mathllap{f_1}}\searrow && \swarrow_{\mathrlap{f_2}}
    \\
    && Q
  }
  \,.
$$

Moreover, this is unique: suppose $\phi'$ is another morphism filling this diagram, then, by using equation $(\star \star)$, we get

$$
  \begin{aligned}
    \phi
    & = 
    \phi \circ id_{X_1 \times X_2}
    \\
    &= 
    \phi \circ ( (id_{X_1},0) \circ p_1 + (0,id_{X_2})\circ p_2 )
    \\
    & =
    \phi \circ (id_{X_1}, 0) \circ p_1 + \phi \circ (0, id_{X_2}) \circ p_2
    \\
    & = 
    f_1 \circ p_1 + f_2 \circ p_2
    \\
    & = 
    \phi' \circ (id_{X_1}, 0) \circ p_1 + \phi' \circ (0, id_{X_2}) \circ p_2
    \\
    & = 
    \phi' \circ ( (id_{X_1},0) \circ p_1 + (0,id_{X_2})\circ p_2 )
    \\
    &=
    \phi' \circ id_{X_1 \times X_2} 
    \\
    &=
    \phi'  
  \end{aligned}
  \,.
$$

This means that $X_1\times X_2$ satisfies the [[universal property]] of a [[coproduct]].

By a [[formal dual|dual]] argument, the binary coproduct $X_1 \sqcup X_2$ is seen to also satisfy the universal property of the binary product. By [[induction]], this implies the statement for all finite (co-)products.  (If a particular finite (co-)product exists but binary ones do not, one can adapt the above argument directly to that case.)

=--

+-- {: .num_remark}
###### Remark

Such products which are also coproducts as in prop. \ref{ProductsAreBiproducts} are sometimes called _[[biproducts]]_ or _[[direct sums]]_; they are [[absolute limit|absolute limits]] for [[Ab]]-[[enriched category|enrichment]].  

=--

+-- {: .num_remark}
###### Remark

The coincidence of products with biproducts in prop. \ref{ProductsAreBiproducts} does _not_ extend to infinite products and coproducts.) In fact, an [[Ab-enriched category]] is [[Cauchy complete category|Cauchy complete]] just when it is additive and moreover its [[idempotents]] split.

=--

Conversely:

+-- {: .num_defn #SemiadditiveCategory}
###### Definition

A **[[semiadditive category]]** is a [[category]] that has all [[finite products]] which, moreover, are [[biproducts]] in that they coincide with finite [[coproducts]] as in def. \ref{ProductsAreBiproducts}.

=--

+-- {: .num_prop #SemiAdditivityInducesAbelianMonoidEnrichment}
###### Proposition

In a [[semiadditive category]], def. \ref{SemiadditiveCategory}, the [[hom-sets]] acquire the structure of [[commutative monoids]] by defining the sum of two morphisms $f,g \;\colon\; X \longrightarrow Y$ to be

$$
  f + g 
    \;\coloneqq\;
  X \overset{\Delta_X}{\to} X \times X
  \simeq
  X \oplus X
  \overset{f \oplus g}{\longrightarrow}
  Y \oplus Y
  \simeq
  Y \sqcup Y
  \overset{\nabla_X}{\to}
  Y
  \,.
$$

With respect to this operation, [[composition]] is [[bilinear map|bilinear]].

=--

+-- {: .proof}
###### Proof

The [[associativity]] and commutativity of $+$ follows directly from the corresponding properties of $\oplus$. Bilinearity of composition follows from [[natural transformation|naturality]] of the [[diagonal]] $\Delta_X$ and [[codiagonal]] $\nabla_X$:

$$
  \array{
    W 
      &\overset{\Delta_W}{\longrightarrow}& 
    W \times W
      &\overset{\simeq}{\longrightarrow}&
    W \oplus W
    \\
    \downarrow^{\mathrlap{e}}
      &&
    \downarrow^{\mathrlap{e \times e}} 
      && 
    \downarrow^{\mathrlap{e \oplus e}}
    \\
    X 
      &\overset{\Delta_X}{\to}& 
    X \times X
      &\simeq&
    X \oplus X
      &\overset{f \oplus g}{\longrightarrow}&
    Y \oplus Y
      &\simeq&
    Y \sqcup Y
      &\overset{\nabla_X}{\to}&
    Y
    \\
      &&
      &&
      &&
    \downarrow^{\mathrlap{h \oplus h}}
      &&
    \downarrow^{\mathrlap{h \sqcup h}}
      &&
    \downarrow^{\mathrlap{h}}
    \\
      && 
      &&
      &&
    Z \oplus Z
      &\simeq&
    Z \sqcup Z
      &\overset{\nabla_Z}{\to}&
    Z
  }
$$

=--

+-- {: .num_prop #SemiaddtiveStructureUnderlyingAdditiveInducesOriginalEnrichment}
###### Proposition

Given an additive category according to def. \ref{AdditiveCategory}, then the enrichment in [[commutative monoids]] which is induced on it via prop. \ref{ProductsAreBiproducts} and prop. \ref{SemiAdditivityInducesAbelianMonoidEnrichment} from its underlying [[semiadditive category]] structure coincides with the original enrichment.

=--

+-- {: .proof}
###### Proof

By the proof of prop. \ref{ProductsAreBiproducts}, the [[codiagonal]] on any object in an additive category is the sum of the two projections:

$$
  \nabla_X \;\colon\; X \oplus X \overset{p_1 + p_2}{\longrightarrow} X
  \,.
$$

Therefore (checking on [[generalized elements]], as in the proof of prop. \ref{ProductsAreBiproducts}) for all morphisms $f,g \colon X \to Y$ we have [[commuting squares]] of the form

$$
  \array{
    X &\overset{f+g}{\longrightarrow}& Y
    \\
    {}^{\mathllap{\Delta_X}}\downarrow && \uparrow^{\mathrlap{\nabla_Y =}}_{\mathrlap{p_1 + p_2}}
    \\
    X \oplus X 
      &\underset{f \oplus g}{\longrightarrow}& 
   Y\oplus Y
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{SemiaddtiveStructureUnderlyingAdditiveInducesOriginalEnrichment} says that being an [[additive category]] is an extra [[property]] on a category, not extra [[structure]]. We may ask whether a given category is additive or not, without specifying with respect to which abelian group structure on the hom-sets.

=--


## Related concepts

* [[semiadditive category]]

* [[abelian category]]

* [[additive (∞,1)-category]]

* [[triangulated category]]

## References

Textbook accounts:

* [[Masaki Kashiwara]], [[Pierre Schapira]], Section 8 of: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;

Discussion in [[homological algebra]]:

* [[Charles Weibel]], *[[An Introduction to Homological Algebra]]*, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139644136](https://doi.org/10.1017/CBO9781139644136), [pdf](https://web.math.rochester.edu/people/faculty/doug//otherpapers/weibel-hom.pdf)&rbrack;

See also:

* {#IntroductionToLinearCategories} [[William Lawvere]], *Introduction to Linear Categories and Applications*, course lecture notes (1992) &lbrack;[pdf](https://github.com/mattearnshaw/lawvere/blob/192dac273e8bf352f307f87b9ec4fe8ef7dc85b9/pdfs/1992-introduction-to-linear-categories-and-applications.pdf), [[Lawvere-LinearCategories.pdf:file]]&rbrack;


Discussion of [[model category]] structures on additive categories is around def. 4.3 of 

* {#Beligiannis} Apostolos Beligiannis, _Homotopy theory of modules and Gorenstein rings_, Math. Scand. 89 (2001) ([pdf](http://users.uoi.gr/abeligia/mathscand.pdf))
 

Formalization of additive categories as [[univalent categories]] in [[univalent foundations of mathematics]] ([[homotopy type theory]]):

* [[unimath]], *Additive categories* &lbrack;[UniMath.CategoryTheory.Additive](https://unimath.github.io/doc/UniMath/4dd5c17/UniMath.CategoryTheory.Additive.html)&rbrack;


[[!redirects additive categories]]