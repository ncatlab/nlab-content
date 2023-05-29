
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

An [[adjoint triple]] $F \dashv G \dashv H$ is called an _ambidextrous adjunction_ (or sometimes _ambiadjunction_ or _ambijunction_, for short) if the [[left adjoint]] $F$ and the [[right adjoint]] $H$ of $G$ are [[equivalence|equivalent]] $F \simeq H$, or
more precisely: equipped with a specified equivalence.  Sometimes $F$ is said to be *biadjoint* to $G$ (not to be confused with [[biadjoint]] in the sense of *[[biadjunction]]*). Functor $G$ which has a left and right adjoint which are equivalent is said to be [[Frobenius functor]]. 

In the special case that $G$ is a [[fully faithful functor]] with an ambidextrous adjoint one also speaks of an *[[essential localization]]* (cf. *[[bireflective subcategory]]*).

 
## Properties

### Frobenius algebra structure

The [[monad]] induced by an ambidextrous adjunction is a [[Frobenius monoid]] object in [[endofunctors]]. (e.g. [Lauda 05, theorem 17](#Lauda05)), hence a [[Frobenius monad]].

### Fiberwise characterization of ambidextrous Kan extension
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

Let $\mathcal{C}$ be a [[small category]] and $\mathcal{D}$ any category and consider the functor $const \mathcal{D} \longrightarrow [\mathcal{C}^{op}, \mathcal{D}]$ that sends objects to constant [[presheaves]] with this value. Then the [[right adjoint]] of this functor is, if it exists, the [[limit]] construction, and the [[left adjoint]] is, if it exists, the [[colimit]] construction. (See also at _[[Kan extension]]_.) Therefore if both exist as an ambidextrous adjunction, then this means that limits in $\mathcal{D}$ over [[diagrams]] of shape $\mathcal{C}$ coincide with the [[colimits]] over these diagrams. If $\mathcal{C}$ is a [[finite set]], then this situation is traditionally referred to as _[[biproducts]]_. Generally therefore this is sometimes called _[[bilimits]]_ (but see the discussion of the terminology there). 

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

On [[bireflective subcategories]]:

* [[Peter Freyd]], [[Peter O’Hearn]],  [[A. John Power]], [[M. Takeyama]], [[Ross Street]], [[Robert D. Tennent]], *Bireflectivity*, Theoretical Computer Science **228** 1–2 (1999) 49-76 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00354-5">doi:10.1016/S0304-3975(98)00354-5</a>&rbrack;


The concept of Frobenius monads:
 
* {#Street04} [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Phys. **45** 3930 (2004) &lbrack;[doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852)&rbrack;

* {#Lauda05} [[Aaron Lauda]], *Frobenius algebras and ambidextrous adjunctions*, Theory and Applications of Categories **16** 4 (2006) 84-122 &lbrack;[arXiv:math/0502550](http://arxiv.org/abs/math/0502550), [tac:16-04](http://www.tac.mta.ca/tac/volumes/16/4/16-04abs.html)&rbrack;

See also:
 
* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], *[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]* (2014)

with some review in:

* [[Peter Haine]], *Ambidexterity* (2018) &lbrack;[pdf](https://math.berkeley.edu/~phaine/files/Ambidexterity_4.pdf), [[Haine-Ambidexterity.pdf:file]]&rbrack;


On the issue of equipping an ambidextrous adjunction $F \dashv G \dashv H$  with a specific equivalence between $F$ and $H$:

* [[Qiaochu Yuan]], [MO:377104](https://mathoverflow.net/a/377104)

Connection to [[Hopf adjunction]]s

* Harshit Yadav, _Frobenius monoidal functors from (co)Hopf adjunctions_, [arXiv:2209.15606](https://arxiv.org/abs/2209.15606)

[[!redirects ambidextrous adjunctions]]

[[!redirects ambidextrous adjoint]]
[[!redirects ambidextrous adjoints]]

[[!redirects ambidextrous space]]
[[!redirects ambidextrous spaces]]

[[!redirects biadjoint pair]]

[[!redirects ambiadjunction]]
[[!redirects ambiadjunctions]]
[[!redirects ambijunction]]
[[!redirects ambijunctions]]
