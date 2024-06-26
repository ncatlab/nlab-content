

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 


## Idea

The notion of  _2-group_ is a [[vertical categorification]] of the notion of _[[group]]_. 

It is the special case of an [[n-group]] for $n=2$, equivalently an [[∞-group]] which is [[n-truncated|1-truncated]]. Under the [[looping and delooping]]-equivalence, 2-groups are equivalent to [[pointed object|pointed]] [[n-connected|connected]] [[homotopy n-type|homotopy 2-types]].


Somewhat more precisely, a _$2$-group_ is a [[group object]] in the [[(2,1)-category]] of [[groupoids]].  Equivalently, it is a [[monoidal groupoid]] in which the [[tensor product]] with any [[object]] has an [[inverse]] up to [[isomorphism]].  Also equivalently, by the [[looping and delooping]]-equivalence, it is a [[pointed object|pointed]] [[2-groupoid]] with a single [[equivalence class]] of objects.

Like other notions of [[higher category theory]], $2$-groups come in weak and strict forms, depending on how you interpret the above.


### Strict $2$-groups

The earliest version studied is that of [[strict 2-group]]s.

A __strict $2$-group__ consists of:

* a collection of [[group]] homomorphisms of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
such that the composites $s\cdot i$ and $t\cdot i$ are the identity morphisms on $C_0$, and
  such that, writing  $C_1 \times_{t,s} C_1$ for the pullback, 
  $$
    \array{
      C_1 \times_{t,s} C_1 &\to& C_1
      \\
      \downarrow && \downarrow^{t}
      \\
      C_1 &\stackrel{s}{\to}& C_0
    }
  $$
  there is, in addition,  a homomorphism
  $$
     C_1 \times_{t,s} C_1 \stackrel{comp}{\to} C_1
  $$
  "respecting $s$ and $t$";

* such that the _composition_ $comp$ is associative
  and unital with respect to $i$ "in the obvious way".

See [[strict 2-group]] for further discussion and examples.


### Weak $2$-groups 

A __weak $2$-group__, or simply __$2$-group__, is a (weak) [[monoidal category]] where every morphism is invertible and *such that*:

*  given any object $x$, there exists an object $x^{-1}$ such that the monoidal products $x \otimes x^{-1}$ and $x^{-1} \otimes x$ are each [[isomorphism|isomorphic]] to the monoidal unit $1$.

A __coherent $2$-group__ is a monoidal category where every morphism is invertible and *equipped with*:

*  for each object $x$ a specific object $x^{-1}$ and specific [[isomorphism]]s from $x \otimes x^{-1}$ and $x^{-1} \otimes x$ to $1$ which form an [[adjoint equivalence]].

A theorem in HDA V (see references) shows that every weak $2$-group may be made coherent.  For purposes of [[internalization]], one probably wants to use the coherent version.


## Definition

+-- {: .num_defn}
###### Definition

The [[(2,1)-category]] $2Grp$ of **2-groups** is equivalently

* the [[full sub-(∞,1)-category|full sub-(2,1)-category]] of that of [[monoidal categories]] and [[strong monoidal functors]] on those that are [[groupoids]] and whose [[tensor product]] has weak [[inverses]] for each object;

* the [[full sub-(∞,1)-category]] of that of [[∞-groups]] on the [[n-truncated|1-truncated]] objects;

* the [[full sub-(∞,1)-category]] of that of [[group object in an (∞,1)-category|group objects]] in [[∞Grpd]] on the [[n-truncated|1-truncated]] objects;

* the [[full sub-(∞,1)-category]] 

  $$
    \infty Grpd_{1 \leq \bullet \leq 2}^{*/}
    \hookrightarrow
    \infty Grpd^{*/}
  $$

  of [[∞Grpd]]$^{*/}$ on those objects which are both [[n-connected|connected]] as well as [[n-truncated|2-truncated]].

=--

+-- {: .num_remark}
###### Remark

The last equivalent characterization is related to the previous ones by the [[looping and delooping]]-equivalence

$$
  \array{
    Grp(\infty Grpd)
    &\stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}&
    \infty Grpd^{*/}_{\geq 1}
    \\
    \uparrow^{\mathrlap{full\;inc.}}
    &&
    \uparrow^{\mathrlap{full\;inc.}}    
    \\
    2 Grp
    &\stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}&
    2Grpd_{\geq 1}^{*/}
  }
  \,.
$$

Here $(-)^{*/}$ denotes taking [[pointed objects]], hence the [[over-(∞,1)-category|slice under]] the point, and $(-)_{\geq}$ denotes the full [[sub-(∞,1)-category|full inclusion]] on [[n-connected|connected]] objects.


=--


By replacing in the last of these equivalent characterizations the ambient [[(∞,1)-topos]] [[∞Grpd]] with any other one, to be denoted $\mathbf{H}$, obtains notions of 2-groups with extra structure. For instance for $\mathbf{H} = $ [[Smooth∞Grpd]] the $(\infty,1)$-topos of [[smooth ∞-groupoids]] one obtains:

+-- {: .num_defn}
###### Definition

The [[(2,1)-category]] $Smooth2Grp$ of **smooth 2-groups** is 

$$
  \array{
    Grp(Smooth \infty Grpd)
    &\stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}&
    Smooth\infty Grpd^{*/}_{\geq 1}
    \\
    \uparrow^{\mathrlap{full\;inc.}}
    &&
    \uparrow^{\mathrlap{full\;inc.}}    
    \\
    Smooth 2 Grp
    &\stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}&
    Smooth2Grpd_{\geq 1}^{*/}
  }
  \,.
$$


=--

Below in [presentation by crossed modules](#PresentationByCrossedModules) are discussed more explict presentations of $2Grp$ and $Smooth2Grpd$ etc. by explicit algebraic data. 

## Properties

### Presentation by crossed modules
 {#PresentationByCrossedModules}

By the discussion there, every _[[∞-group]]_ has a _presentation_ by a [[simplicial group]]. More precisely, the [[(∞,1)-category]], $\infty Grp$, is [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial groups]] (for instance under [[simplicial localization]])

$$
  \infty Grpd \simeq L_W Grp^{\Delta^{op}}
  \,.
$$

Moreover, if $G \in Grp^{\Delta^{op}}$ is an [[n-group]], then it is equivalent to a [[coskeleton|n-coskeletal]] simplicial group. For $n = 2$ one finds that these are naturally identified with _[[crossed modules]]_ of groups (see there for more details).

In conclusion, this means that 

+-- {: .num_prop #PresentationOf2GrpByCrossedModules}
###### Proposition

The [[(2,1)-category]] $2Grp$ of 2-groups is [[equivalence of (infinity,1)-categories|equivalent]] to the [[simplicial localization]] of the [[category with weak equivalences]] whose

* objects are [[crossed modules]]

* morphisms are [[homomorphisms]] of crossed modules;

* weak equivalences are those morphisms of crossed modules which correspond to [[weak homotopy equivalences]] of the corresponding simplicial groups.

=--

A straightforward analysis shows that

+-- {: .num_prop #HomotopyGroupsOfCrossedModule}
###### Proposition

For $(G_1 \stackrel{\delta}{\to} G_0, G_0 \stackrel{\alpha}{\to} Aut(G_1))$ a [[crossed module]], the [[homotopy groups]] of the corresponding [[2-group]]/[[simplicial group]] are

* $\pi_0 = G_0 / im(\delta)$ (the [[quotient]] of $G_0$ by the [[image]] of $\delta$, which is necessarily a [[normal subgroup]] of $G_0$);

* $\pi_1 = ker(\delta)$ (the [[kernel]] of $\delta$).

Accordingly, a weak equivalence of crossed modules $f : G \to H$ is a morphism of crossed modules which induces an [[isomorphism]] of kernel and cokernel of $\delta_G$ with that of $\delta_H$.

=--

Similar statements hold for 2-groups with extra structure. For instance the $(2,1)$-category $Smooth2Grp$ of smooth 2-groups is equivalent to the [[simplicial localization]] of the category whose

* objects are [[sheaves]] of [[crossed modules]] on [[CartSp]]${}_{smooth}$;

* weak equivalences are those morphisms of sheaves of crossed modules which on every [[stalk]] induce weak equivalences of crossed modules as above.

(See the discussion at [[Smooth∞Grpd]] for more on this.)


## Examples 

### Specific examples

#### Picard 2-group

* [[Picard 2-group]]

#### Automorphism 2-groups 

For $C$ any [[2-category]] and $c \in C$ any object of it, the category $Aut_C(c) \subset Hom_C(c,c)$ of auto-equivalences of $c$ and invertible 2-morphisms between these is naturally a 2-group, whose group product comes from the horizontal composition in $C$.

If $C$ is a [[strict 2-category]] there is the notion of strict [[automorphism 2-group]]. See there for more details on that case.

For instance if $C = Grp_2 \subset Grpd$ is the 2-category of [[group]] obtained by regarding groups as one-object [[groupoid]]s, then for $H \in Grp$ a group, its automorphism 2-group obtained this way is the strict 2-group

$$
  AUT(H) := Aut_{Grp_2}(H)
$$

corresponding to the [[crossed module]] $(H \stackrel{Ad}{\to} Aut(H))$, where $Aut(H)$ is the ordinary [[automorphism group]] of $H$.

#### Inner automorphism 2-groups

See [[inner automorphism 2-group]].

#### String 2-group

See [[string 2-group]].

#### Platonic 2-group

See _[[Platonic 2-group]]_

### Equivalences of 2-groups
 {#ExamplesForEquivalencesOf2Groups}

We discuss some weak equivalences in the [[category with weak equivalences]] of [[crossed modules]] and crossed module homomorphisms, which presents $2Grp$ by the discussion [above](#PresentationByCrossedModules).

#### From inclusions of normal subgroups
 {#FromInclusionsOfNormalSubgroups}

Let $G$ be a [[group]] and $N \hookrightarrow G$ the inclusion of a [[normal subgroup]]. Equipped with the canonical [[action]] of $G$ on $N$ by [[conjugation]], this inclusion constitutes a [[crossed module]]. There is a canonical morphism of crossed modules from $(N \hookrightarrow G)$ to $(1 \to G/N)$, hence to the ordinary [[quotient]] group, regarded as a crossed module.

+-- {: .num_prop}
###### Observation

The morphism $(N \hookrightarrow G) \to G/N$ is a weak equivalence of crossed modules,  prop. \ref{PresentationOf2GrpByCrossedModules}. Accordingly, it presents an [[equivalence in an (infinity,1)-category|equivalence]] of 2-groups.

=--

+-- {: .proof}
###### Proof

The canonical morphism in question is given by the commuting diagram of groups

$$
  \array{
    N &\stackrel{f_1}{\to}& 1
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{f_0}{\to}& G/N
  }
  \,.
$$

By prop. \ref{HomotopyGroupsOfCrossedModule} we need to check that this induces an isomorphism on the [[kernel]] and [[cokernel]] of the vertical morphisms.

The kernel of the left vertical morphism is the trivial group, because $N \hookrightarrow G$ is an inclusion, by definition. Clearly also the kernel of the right vertical morphisms is the trivial group. Hence $f_1$ restricted to the kernels is the unique morphism from the trivial group to itself, hence is an isomrphism.

Moreover, the cokernel of the left vertical morphism is of course the quotient $G/N$ and $f_0$, being the quotient map, is manifestly an isomorphism on cokernels.

=--

This class of weak equivalence plays an important role as constituting [[∞-anafunctor|2-anafunctors]] that exhibit long [[fiber sequence]] extensions of [[short exact sequences]] of [[central extensions]] of groups.

+-- {: .num_prop}
###### Observation

Let $A \to \hat G$ be the inclusion of a [[center|central]] subgroup, exhibiting a [[central extension]] $A \to \hat G \to G$ with $G := \hat G/A$. Then this [[short exact sequence]] of groups extends to a long [[fiber sequence]] of 2-groups

$$
  A \to \hat G \to G \to \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G \to \mathbf{B}^2 A
  \,,
$$

where $\mathbf{B}A$ denotes the 2-group given by the [[crossed module]] $(A \to 1)$, and similarly for the other cases.

Here the [[connecting homomorphism]] $G \to \mathbf{B}A$ is presented in the category of crossed modules by a zig-zag / [[anafunctor]] whose left leg is the above weak equivalence:

$$
  (1 \to G) \stackrel{\simeq}{\leftarrow}
  (A \to \hat G)
   \to 
  (A \to 1)
  \,.
$$

=--

+-- {: .num_example}
###### Example

For smooth 2-groups, useful examples of the above are smooth refinements of various [[universal characteristic classes]]:

* the second [[Stiefel-Whitney class]] 

  $$
    w_2 : \mathbf{B}SO \to \mathbf{B}^2\mathbb{Z}_2
  $$ 

  is induced this way from the central extension $\mathbb{Z}_2 \to Spin \to SO$ of the [[special orthogonal group]] by the [[spin group]];

* the first [[Chern class]]

  $$
    c_1 : \mathbf{B}U(1) \to \mathbf{B}^2 \mathbb{Z}
  $$

  induced from the central extension $\mathbb{Z} \to \mathbb{R} \to U(1)$.


=--


## Related concepts

* [[group]]

  * [[groupoid]], [[monoidal groupoid]]

  * **2-group**, [[crossed module]], [[differential crossed module]]

    * [[braided 2-group]], [[symmetric 2-group]]

    * [[quantum 2-group]]

  * [[3-group]], [[2-crossed module]] / [[crossed square]], [[differential 2-crossed module]]

  * [[n-group]]

  * [[∞-group]], [[simplicial group]], [[crossed complex]], [[hypercrossed complex]]

  * [[group stack]]

    [[smooth 2-group]]

* [[higher gauge symmetry]]

* [[generalized global symmetry]]


[[!include homotopy n-types - table]]


## References 
 {#References}

### Original articles
 {#OriginalArticles}

The notion of 2-groups first appears in

* {#Solian72} [[Alexandru Solian]], *Groupe dans une catégorie*, C. R. Acad. Sc. Paris **275** (1972) &lbrack;[ark:/12148/bpt6k57310477/f7](https://gallica.bnf.fr/ark:/12148/bpt6k57310477/f7.item)&rbrack;

* {#Solian80} [[Alexandru Solian]], *Coherence in categorical groups*,  Communications in Algebra **9** 10 (1980) 1039-1057 &lbrack;[doi:10.1080/00927878108822631](https://doi.org/10.1080/00927878108822631)&rbrack;
 
and in

* {#Sinh73} [[Hoàng Xuân Sính]], _Gr_-catégories, PhD thesis, Hanoi (1973, 1975) &lbrack;[web](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/sinh.html), [pdf](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/sinh_I.pdf), [[Sinh_Gr-Categories.pdf:file]]&rbrack;

[Sinh (1973)](#Sinh73) was supervised by [[Alexander Grothendieck]] and showed that 2-groups are classified, up to equivalence, by quadruples consisting of:

* a group $G$
* an abelian group $A$
* an action of $G$ as automorphisms of $A$
* an element of $H^3(G,A)$, often called the *Sinh invariant*.

She later published two papers on the subject:

* {#Sinh78} [[Hoàng Xuân Sính]],  *Gr-catégories strictes*, Acta Mathematica Vietnamica **3** 2 (1978) 47-59 &lbrack;[web](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/sinh.html), [pdf](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/Hoang_Xuan_Sinh_Gr_categories_strictes.pdf)&rbrack;

* {#Sinh83} [[Hoàng Xuân Sính]], *Catégories de Picard restreintes*, Acta Mathematica Vietnamica **7** 1 (1983) 117-122 &lbrack;[pdf](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/Hoang_Xuan_Sinh_Categories_de_Picard_restreintes.pdf), [web](https://pnp.mathematik.uni-stuttgart.de/lexmath/kuenzer/sinh.html)&rbrack;

[Sinh 1978](Sinh78) appears to prove that every 2-group is equivalent to a [[strict 2-group]] arising from a [[crossed module]].  The second calls a [[symmetric 2-group]] (i.e. a [[symmetric monoidal category]] with all objects and morphisms invertible) a *[[Picard category]]*, and calls a Picard category *restrained* if the [[braiding]] $B_{x,x} \colon x \otimes x \to x \otimes x$ is the [[identity morphism|identity]] for all objects $x$. The article then proves that every Picard category is equivalent to one arising from a 2-term [[chain complex]] of abelian groups.

Computational enumeration of geometrically [[discrete group|discrete]] 2-groups using the computer program [XMod](http://pages.bangor.ac.uk/~mas023/chda/xmod/xmod244.html):

* Murat Alp, Christopher Wensley, _Enumeration of $Cat^1$-groups of low order_,  Int. J. Algebra Comput. 10, 407 (2000) &lbrack;[doi:10.1142/S0218196700000170](http://www.worldscientific.com/doi/abs/10.1142/S0218196700000170)&rbrack;

* [[Graham Ellis]], Luyen Van Le, *Homotopy 2-types of Low order*, Experimental Mathematics **23** 4 (2014)  &lbrack;[doi:10.1080/10586458.2014.912059](https://doi.org/10.1080/10586458.2014.912059), [pdf](http://hamilton.nuigalway.ie/preprints/2t.pdf)&rbrack;


### Review

An early textbook account on [[strict 2-groups]] and explaining the relation to [[crossed modules]]:

* [[Saunders MacLane]], §XII.8 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

Exposition of general 2-groups as [[monoidal categories]] with all objects and morphisms invertible (sometimes called [[Picard 2-groups]]):

*  {#BaezLauda03} [[John Baez]], [[Aaron Lauda]], _HDA V: 2-Groups_, Theory and Applications of Categories **12** 14 (2004) 423-491 &lbrack;[arXiv:math.QA/0307200](http://arxiv.org/abs/math.QA/0307200), [tac:12-14](http://www.tac.mta.ca/tac/volumes/12/14/12-14abs.html)&rbrack;


### Geometric 2-groups

Beware that most of the above discussion is about [[discrete infinity-group|geometrically discrete]] 2-groups.

Discussion of geometrically structured 2-groups (notably [[smooth 2-groups]], hence "Lie 2-groups"):

* {#Schommer-Pries11} [[Chris Schommer-Pries]], *Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group* Geometry & Topology **15** (2011) 609-676 &lbrack;[arXiv:0911.2483](http://arxiv.org/abs/0911.2483), [doi:10.2140/gt.2011.15.609](https://doi.org/10.2140/gt.2011.15.609)&rbrack;

and via [[group stacks]]:

* [[Urs Schreiber]], §2.6.5 & §3.4.2 of: _[[schreiber:differential cohomology in a cohesive topos]]_ &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;

For more on this see the references at *[[string 2-group]]*.

### Examples

A key example due to its universality for [[higher central extensions]] of [[compact Lie groups]] by the [[circle 2-group]] to [[smooth 2-groups]] is 

* the *[[string 2-group]]* -- see [there](string+2-group#References) for references.

Further on [[2-group]]-[[higher central extensions|extensions]] by the [[circle 2-group]]:

of [[tori]] (see also at *[[T-duality 2-group]]*):

* [[Nora Ganter]], _Categorical Tori_, SIGMA 14 (2018), 014, 18 ([arXiv:1406.7046](https://arxiv.org/abs/1406.7046))

of [[finite subgroups of SU(2)]] (to [[Platonic 2-groups]]):

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, Higher Structures 1(1):122-146, 2017 ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192), [hs:30](https://journals.mq.edu.au/index.php/higher_structures/article/view/30))

{#ReferencesInCondensedMatterPhysics} Arguments that 2-groups play a role in [[symmetry protected topological phases of matter]]:

* [[Anton Kapustin]], [[Ryan Thorngren]], *Higher symmetry and gapped phases of gauge theories*, in *Algebra, Geometry, and Physics in the 21st Century*, Progress in Mathematics, **324** (2017) 177-202 &lbrack;[arXiv:1309.4721](https://arxiv.org/abs/1309.4721), [doi:10.1007/978-3-319-59939-7_5](https://doi.org/10.1007/978-3-319-59939-7_5)&rbrack;

* {#BBCW19} [[Maissam Barkeshli]], [[Parsa Bonderson]], [[Meng Cheng]], [[Zhenghan Wang]], *Symmetry Fractionalization, Defects, and Gauging of Topological Phases*, Phys. Rev. B **100** 115147 (2019) &lbrack;[arXiv:1410.4540](https://arxiv.org/abs/1410.4540), [doi:10.1103/PhysRevB.100.115147](https://doi.org/10.1103/PhysRevB.100.115147), [talk pdf](http://helper.ipam.ucla.edu/publications/stq2015/stq2015_12401.pdf)&rbrack;

In this vein, 2-groups are now discussed by a vocal group of physicists under the term "[[generalized global symmetry|generalized symmetries]]" or similar.

[[!redirects 2-groups]]

[[!redirects weak 2-group]]
[[!redirects weak 2-groups]]