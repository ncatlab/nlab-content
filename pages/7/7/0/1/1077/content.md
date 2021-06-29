
> This entry is about [[coproducts]] coinciding with [[products]]. For the notion of biproduct in the sense of [[bicategory]] theory see at [[2-limit]]. See at _[[bilimit]]_ for general disambiguation.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+-- {: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

## Idea 

A _biproduct_ in a [[category]] $\mathcal{C}$ is an operation that is both a [[product]] and a [[coproduct]], in a compatible way. Morphisms between finite biproducts are encoded in a [[matrix calculus]].

Finite biproducts are best known from [[additive category|additive categories]]. A category which has biproducts but is not necessarily [[enriched category|enriched]] in [[Ab]], hence not necessarily [[additive category|additive]], is called a _semiadditive category_.


## Definition 

Let $\mathcal{C}$ be a [[category]] with [[zero morphisms]]; that is, $C$ is [[enriched category|enriched]] over [[pointed sets]] (for example, $C$ might have a [[zero object]]).  For $c_1, c_2$ two objects in $C$, suppose a [[product]] $c_1 \times c_2$ and a [[coproduct]] $c_1 \sqcup c_2$ both exist.  

+-- {: .num_defn #TheCanonicalComparisonMorphism}
###### Definition

Write 

$$
  r_{c_1,c_2} : c_1 \sqcup c_2 \to c_1 \times c_2
$$

for the [[morphism]] which is uniquely defined (via the [[universal property]] of [[coproduct]] and [[product]]) by the condition that
$$
  \left(
    c_i \to c_1 \sqcup c_2 \stackrel{r}{\to} c_1 \times c_2 \to c_j
  \right)
  =
  \left\{
    \array{
      Id_{c_i} & if \; i = j
      \\
      0_{i,j} & if \; i \neq j
    }
  \right.
  \,
$$

where the last and first morphisms are the [[projections]] and [[co-projections]], respectively, and 
where $0_{i,j}$ is the [[zero morphism]] from $c_i$ to $c_j$. Thus $r_{c_1, c_2} = (Id_{c_1}, 0_{1,2}) \sqcup (0_{2,1}, Id_{c_2})$, where $(f, g): d \to a \times b$ denotes the map induced by $f : d \to a$ and $g : d \to b$.

=--

+-- {: .num_defn #Biproduct}
###### Definition

If the morphism $r_{c_1,c_2}$ in def. \ref{TheCanonicalComparisonMorphism}, is an [[isomorphism]], then the isomorphic objects $c_1 \times c_2$ and $c_1 \sqcup c_2$ are called [[generalized the|the]] __biproduct__ of $c_1$ and $c_2$.  This object is often denoted $c_1 \oplus c_2$, alluding to the [[direct sum]] (which is often an example).

If $r_{c_1,c_2}$ is an isomorphism for all objects $c_1, c_2 \in \mathcal{C}$ and hence a [[natural isomorphism]] 

$$
  r \;\colon\; (-)\sqcup (-) \stackrel{\simeq}{\longrightarrow} (-) \times (-)
$$

then $\mathcal{C}$ is called a [semiadditive category](#SemiadditiveCategories).

=--

+-- {: .num_remark}
###### Remark

Definition \ref{Biproduct} has a straightforward generalization to biproducts of any number of objects (although this requires extra structure on the category in [[constructive mathematics]] if the set indexing these objects might not have [[decidable equality]]).  

A [[zero object]] is the biproduct of no objects.

=--

## Point-free definition

Suppose $C$ is an arbitrary category, without any assumption of pointedness, additivity, etc.

The __biproduct__ of $c_1$ and $c_2$
is a tuple
$$(c_1\oplus c_2,p_1:c_1\oplus c_2\to c_1,p_2:c_1\oplus c_2\to c_2,i_1:c_1\to c_1\oplus c_2,i_2:c_2\to c_1\oplus c_2)$$
such that $(c_1\oplus c_2,p_1,p_2)$ is a product tuple,
$(c_1\oplus c_2,i_1,i_2)$ is a coproduct tuple,
and
$$p_1 i_1=id,$$
$$p_2 i_2=id,$$
$$i_1 p_1 i_2 p_2 = i_2 p_2 i_1 p_1.$$

See Definition 3.1 in [Karvonen](#Karvonen).


## Semiadditive categories 
 {#SemiadditiveCategories}

A category $C$ with all finite biproducts is called a **semiadditive category**.  More precisely, this means that $C$ has all finite products and coproducts, that the unique map $0\to 1$ is an isomorphism (hence $C$ has a zero object), and that the canonical maps $c_1 \sqcup c_2 \to c_1 \times c_2$ defined above are isomorphisms.

Amusingly, for $C$ to be semiadditive, it actually suffices to assume that $C$ has finite products and coproducts and that there exists *any* [[natural transformation|natural]] family of isomorphisms $c_1 \sqcup c_2 \cong c_1 \times c_2$ --- not necessarily the canonical maps constructed above.  A proof can be found in ([Lack 09](#Lack09)).

An [[additive category]], although normally defined through the theory of [[enriched categories]], may also be understood as a semiadditive category with an [[extra property]], as explained below at _[Properties -- Biproducts imply enrichment](#BiproductsImplyEnrichment)_.

## Properties

### Semiadditivity as structure/property
 {#SemiadditivityAsStructureProperty}

Given a category $\mathcal{C}$ with [[zero morphisms]], one may imagine equipping it with the [[structure]] of a chosen [[natural isomorphism]]

$$
  \psi_{(-),(-)} : (-)\sqcup (-) \stackrel{\simeq}{\longrightarrow} (-)\times(-)
  \,.
$$


+-- {: .num_prop}
###### Proposition

([Lack 09, proof of theorem 5](#Lack09)). 
If a [[category]] $\mathcal{C}$ with finite [[coproducts]] and [[products]] carries any [[natural isomorphism]] $\psi_{(-),(-)}$ from [[coproducts]] to [[products]], then 
$$ \array {
  c_1\sqcup c_2 & \overset{\psi_{c_1, 0} + \psi_{0, c_2}}\rightarrow & c_1 \sqcup c_2 \\
    & \searrow^{r_{c_1, c_2}}           & \downarrow^{\psi_{c_1, c_2}} \\
    &                        & c_1 \times c_2
} $$
commutes for any two object $c_1$ and $c_2$.


=--

 Hence $r_{c_1, c_2}$ is an isomorphism so that $\mathcal{C}$ is semi-additive. See [[non-canonical isomorphism]] for more. 


### Biproducts imply enrichment -- Relation to additive categories
 {#BiproductsImplyEnrichment}

A semiadditive category is automatically [[enriched category|enriched]] over the [[monoidal category]] of [[commutative monoids]] with the usual [[tensor product]], as follows.

Given two morphisms $f, g: a \to b$ in $C$, let their sum $f + g: a \to b$ be
$$ a \to a \times a \cong a \oplus a \overset{f \oplus g}{\to} b \oplus b \cong b \sqcup b \to b .$$
One proves that $+$ is associative and commutative. Of course, the zero morphism $0: a \to b$ is the usual [[zero morphism]] given by the zero object:
$$ a \to 1 \cong 0 \to b .$$
One proves that $0$ is the neutral element for $+$ and that this matches the $0$ morphism that we began with in the definition.  Note that in addition to a zero object, this construction actually only requires biproducts of an object with itself, i.e. biproducts of the form $a\oplus a$ rather than the more general $a\oplus b$.

If additionally every morphism $f: a \to b$ has an inverse $-f: a \to b$, then $C$ is enriched over the category $Ab$ of [[abelian groups]] and is therefore (precisely) an __[[additive category]]__.

If, on the other hand, the addition of morphisms is idempotent ($f+f=f$), then $C$ is enriched over the category $SLat$ of [[semilattices]] (and is therefore a kind of [[2-poset]]).


### Biproducts as enriched Cauchy colimits 

Conversely, if $C$ is already known to be enriched over abelian monoids, then a binary biproduct may be defined purely diagrammatically as an object $c_1\oplus c_2$ together with injections $n_i:c_i\to c_1\oplus c_2$ and projections $p_i:c_1\oplus c_2 \to c_i$ such that $p_j n_i = \delta_{i j}$ (the [[Kronecker delta]]) and $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$.  It is easy to check that makes $c_1\oplus c_2$ a biproduct, and that any binary biproduct must be of this form.  Similarly, an object $z$ of such a category is a zero object precisely when $1_z= 0_z$, its identity is equal to the zero morphism. It follows that functors enriched over abelian monoids must automatically preserve finite biproducts, so that finite biproducts are a type of [[Cauchy colimit]].  Moreover, any product _or_ coproduct in a category enriched over abelian monoids is actually a biproduct.

For categories enriched over [[suplattices]], this extends to all small biproducts, with the condition $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$ replaced by $\bigvee_{i} n_i p_i = 1_{\bigoplus_i c_i}$.  In particular, the category of suplattices has all small biproducts.

### Biproducts from duals

The existence of [[dual objects]] tends to imply (semi)additivity; see ([Houston 08](#Houston06), [MO discussion](http://mathoverflow.net/questions/14402/semiadditivity-and-dualizability-of-2/21307)).



## Examples

Categories with biproducts include:

* The category of abelian groups. More generally, any [[ abelian category ]]. 

* The category of (finitely generated) [[ projective module | projective modules ]] over a given ring. 

* Any [[ triangulated category ]], in particular the derived category of a ring, or the homotopy category of spectra. 

* The category of abelian categories and exact functors. 

* [[K(n)-local stable homotopy theory]] ([Hopkins-Lurie 14](#HopkinsLurie14))


## Related concepts

* [[bilimit]]

* [[semiadditive (∞,1)-category]]

## References

* {#Lack09} [[Stephen Lack]], _Non-canonical isomorphisms_, ([arXiv:0912.2126](http://arxiv.org/abs/0912.2126)).

* {#Houston06} [[Robin Houston]], _Finite Products are Biproducts in a Compact Closed Category_, Journal of Pure and Applied Algebra, Volume 212, Issue 2, February 2008, Pages 394-400 ([arXiv:math/0604542](http://arxiv.org/abs/math/0604542))


* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_ (2014)


* {#Karvonen} Martti Karvonen, _Biproducts without pointedness_, [arXiv](https://arxiv.org/abs/1801.06488).


A related discussion is archived at $n$[Forum](http://nforum.mathforge.org/discussion/4966/zero-morphism-and-additive-categories/?Focus=39983#Comment_39983).


[[!redirects biproducts]]
[[!redirects semiadditive category]]
[[!redirects semiadditive categories]]
[[!redirects semi-additive category]]
[[!redirects semi-additive categories]]