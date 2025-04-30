
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

An [[adjoint triple]] $F \dashv G \dashv H$ is called an _ambidextrous adjunction_ (or sometimes _ambiadjunction_ or _ambijunction_, for short) if the [[left adjoint]] $F$ and the [[right adjoint]] $H$ of $G$ are [[isomorphic]] $F \simeq H$, or, more precisely: equipped with a specified isomorphism.  

In fact, often $F$ is *identified* with $H$, which is the situation of a *strongly adjoint pair* $(F \dashv G \dashv F)$ originally considered by [Morita 1965](#Morita65). Some authors refer to this situation by saying that $G$ is a *[[Frobenius functor]]* (ie. a functor which has a [[left adjoint]] that is also a [[right adjoint]]). In this case, ambidexterity is a *property* of a pair of functors, rather than *structure* on a triple of functors.

Sometimes $F$ is said to be *biadjoint* to $G$ (not to be confused with [[biadjoint]] in the sense of *[[biadjunction]]*). Functor $G$ which has a left and right adjoint which are equivalent is said to be [[Frobenius functor]]. 

In the special case that $G$ is a [[fully faithful functor]] with an ambidextrous adjoint one also speaks of an *essential localization* (cf. *[[bireflective subcategory]]*).

 
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
 {#Examples}

\begin{example}
Every [[self-adjoint functor]] forms an ambidextrous adjunction.
\end{example}

\begin{example}
If $F \dashv G$ is an [[adjoint equivalence]], then there are ambidextrous adjunctions $F \dashv G \dashv F$ and $G \dashv F \dashv G$.
\end{example}

\begin{example}
**(coincident limits and colimits)**
\linebreak
Let $\mathcal{C}$ be a [[small category]] and $\mathcal{D}$ any category and consider the functor $const \mathcal{D} \longrightarrow [\mathcal{C}^{op}, \mathcal{D}]$ that sends objects to constant [[presheaves]] with this value. Then the [[right adjoint]] of this functor is, if it exists, the [[limit]] construction, and the [[left adjoint]] is, if it exists, the [[colimit]] construction. (See also at _[[Kan extension]]_.) Therefore if both exist as an ambidextrous adjunction, then this means that limits in $\mathcal{D}$ over [[diagrams]] of shape $\mathcal{C}$ coincide with the [[colimits]] over these diagrams. If $\mathcal{C}$ is a [[finite set]], then this situation is traditionally referred to as _[[biproducts]]_. Generally therefore this is sometimes called _[[bilimits]]_ (but see the discussion of the terminology there). 

In [Hopkins & Lurie 2014, section 4.3](#HopkinsLuire14) such $\mathcal{C}$ is called _$\mathcal{D}$-ambidextrous_ (or rather, they consider $\mathcal{C}$ an [[∞-groupoid]] and hence call it a _$\mathcal{D}$-ambidextrous space_). Concrete examples of this include those discussed at _[[K(n)-local stable homotopy theory]]_.
\end{example}

\begin{example}\label{FrobeniusReciprocity}
**([[Frobenius reciprocity]])**
For $H \xhookrightarrow{\iota} G$ a [[subgroup]]-inclusion of [[finite number|finite]] [[index of a subgroup|index]] the left and right [[induced representation]]-functors (adjoints to the functor $i^\ast \colon G Rep \to H Rep$ forming [[restricted representations]]) agree, $\iota_! \simeq \iota_\ast \,\colon\, H Rep \to G Rep$, making an ambidextrous adjunction  (see [there](induced+representation#Ambidexterity) for more).
\end{example}


\begin{example}
**([[yoga of six functors]])**
A [[Wirthmüller context]] in the presence of an un-twisted [[Wirthmüller isomorphism]] is an ambidextrous adjunction.
\end{example}



## Related concepts

* [[Wirthmüller context]]

* [[infinitesimal cohesion]]


## References

Ambidextrous adjunctions were maybe first considered under the name *strongly adjoint pairs* (of functors), in:

* {#Morita65} [[Kiiti Morita]], *Adjoint pairs of functors and Frobenius extensions*, Science Reports of the Tokyo Kyoiku Daigaku, Section A **9** 202/208 (1965) 40-71 &lbrack;[jstor:43698658](https://www.jstor.org/stable/43698658)&rbrack;

The terminology "[[Frobenius functors]]" for "strongly adjoint pairs" is due to 

* {#CaenepeelMilitaruZhu97}  [[Stefaan Caenepeel]], [[Gigel Militaru]], [[Shenglin Zhu]], *Doi-Hopf modules, Yetter-Drinfel’d modules and Frobenius type properties*, Trans. Amer. Math. Soc. **349** (1997) 4311-4342 &lbrack;[1997-349-11/S0002-9947-97-02004-7](https://www.ams.org/journals/tran/1997-349-11/S0002-9947-97-02004-7), [pdf](https://www.ams.org/journals/tran/1997-349-11/S0002-9947-97-02004-7/S0002-9947-97-02004-7.pdf)&rbrack;

* F. Castaño Iglesias, [[José Gómez Torrecillas]], C. Nastasescu, _Frobenius functors: applications_, Comm. Alg. __27__ 10  (1998) 4879-4900 &lbrack;[doi:10.1080/00927879908826735](https://doi.org/10.1080/00927879908826735)&rbrack;


The case of [[bireflective subcategories]]:

* [[Peter Freyd]], [[Peter O’Hearn]],  [[A. John Power]], [[M. Takeyama]], [[Ross Street]], [[Robert D. Tennent]], *Bireflectivity*, Theoretical Computer Science **228** 1–2 (1999) 49-76 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00354-5">doi:10.1016/S0304-3975(98)00354-5</a>&rbrack;

On the [[Frobenius monads]] induced by ambidextrous adjuntions:
 
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

[[!redirects strongly adjoint pair]]
[[!redirects strongly adjoint pairs]]

[[!redirects biadjoint pair]]

[[!redirects ambiadjunction]]
[[!redirects ambiadjunctions]]
[[!redirects ambijunction]]
[[!redirects ambijunctions]]
