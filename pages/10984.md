
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An [[adjoint triple]] $F \dashv G \dashv H$ is called an _ambidextrous adjunction_ (or sometimes _ambijunction_, for short) if the [[left adjoint]] $F$ and the [[right adjoint]] $H$ of $G$ are [[equivalence|equivalent]] $F \simeq H$. Sometimes $F$ is said to be *biadjoint* to $G$ (not to be confused with [[biadjoint]] in the sense of a biadjunction).

 
## Properties

### Frobenius algebra structure

The [[monad]] induced by an ambidextrous adjunction is a [[Frobenius monoid]] object in [[endofunctors]]. (e.g. [Lauda 05, theorem 17](#Lauda05)), hence a [[Frobenius monad]].

### Fiberwise characterization of ambid. Kan extension
 {#FiberwiseCharacterization}

Let $\mathcal{D} \in Cat_\infty$ be an [[(∞,1)-category]] with small [[(∞,1)-colimits]]. For $f \;\colon\; X \longrightarrow Y$ a morphism of [[∞-groupoids]], write 

$$
  f^\ast \;\colon\; [Y,\mathcal{D}] \longrightarrow [X,\mathcal{D}]
$$

for the induced pullback of [[(∞,1)-functor (∞,1)-categories]] (which one may think of as the categories of $\mathcal{D}$-valued [[local systems]] over $X$ and $Y$, respectively). The [[left adjoint]] and [[right adjoint]] (if it exists) of this are left and right [[(∞,1)-Kan extension]].


+-- {: .num_defn #AmbidextrousKanExtension}
###### Definition

Say that a morphism $f$ is $\mathcal{D}$-ambidextrous if $(f_! \dashv f^\ast)$  is an ambidextrous adjunction $(f_! \simeq f_\ast)$ and in addtion all pullbacks of $f$ satisfy some property (...). 

Say that an [[∞-groupoid]] $A \in Grpd_\infty$ is _$\mathcal{D}$-ambidextrous_ if its [[terminal object in an (∞,1)-category|terminal]] map is.

=--

([Hopkins-Lurie 14, def. 4.1.11](#{#HopkinsLurie14})) 




+-- {: .num_prop}
###### Proposition

A morphism $f \colon X \to Y$ between [[∞-groupoids]], is $\mathcal{D}$-ambidextrous, def. \ref{AmbidextrousKanExtension}, precisely if each [[homotopy fiber]] $X_y$ of $f$ is.

=--

([Hopkins-Lurie 14, prop. 4.3.5](#HopkinsLurie14))



## Examples

+-- {: .num_example}
###### Example
**(coincident limits and colimits)**

Let $\mathcal{C}$ be a [[small category]] and $\mathcal{D}$ any category and consider the functor $const \mathcal{D} \longrightarrow [\mathcal{C}^{op}, \mathcal{D}]$ that sends objects to constant [[presheaves]] with this value. Then the [[right adjoint]] of this functor is, if it exists, the [[limit]] construction, and the [[left adjoint]] is, if it exists, the [[colimit]] construction. (See also at _[[Kan extension]]_.) Therefore if both exist as an ambidextrous adjounction, then this means that limits in $\mathcal{D}$ over [[diagrams]] of shape $\mathcal{C}$ coincide with the [[colimits]] over these diagrams. If $\mathcal{C}$ is a [[finite set]], then this situation is traditionally referred to as _[[biproducts]]_. Generally therefore this is sometimes called _[[bilimits]]_ (but see the discussion of the terminology there). 

In ([Hopkins-Lurie 14, section 4.3](#HopkinsLuire14)) such $\mathcal{C}$ is called _$\mathcal{D}$-ambidextrous_ (or rather, they consider $\mathcal{C}$ an [[∞-groupoid]] and hence call it a _$\mathcal{D}$-ambidextrous space_). Concrete examples of this include those discussed at _[[K(n)-local stable homotopy theory]]_.

=--

+-- {: .num_example}
###### Example
**(Yoga of six functors)**

A [[Wirthmüller context]] in the presence of an un-twisted [[Wirthmüller isomorphism]] is an ambidextrous adjunction.

###### Example

Every [[self-adjoint functor]] forms an ambidextrous adjunction.

=--

## Related concepts

* [[Wirthmüller context]]

* [[infinitesimal cohesion]]

## References

* [[Ross Street]], _Frobenius monads and pseudomonoids_, J. Math. Phys. 45.(2004) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.91.2686))


* [[Aaron Lauda]], _Frobenius algebras and ambidextrous adjunctions_ ([arXiv:math/0502550](http://arxiv.org/abs/math/0502550))
 {#Lauda05}


* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_ (2014)

[[!redirects ambidextrous adjunctions]]

[[!redirects ambidextrous space]]
[[!redirects ambidextrous spaces]]

[[!redirects biadjoint pair]]