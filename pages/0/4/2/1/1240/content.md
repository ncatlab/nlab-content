
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

Given a [[group]] $G$ with [[subgroup]] $H \xhookrightarrow{\iota} G$ then the evident operation $\iota^\ast$ of [[restricted representation|restricting]] [[linear representations]] of $G$ to $H$-representations has both a [[left adjoint]] $i_!$ and a [[right adjoint]] $i_\ast$ [[functor]]. For $V \in H Rep$, the image $i_! V \in G Rep$ is called the *left induced representation* and the image $i_\ast V \in G Rep$ is called the *right induced representation* or *co-induced representation* of $V$.

Often this is considered for [[finite groups]] or at least for [[subgroups]] of [[finite number|finite]] [[index of a subgroup|index]], in which case these left and right adjoints agree (to make an [[ambidextrous adjunction]]) and are both traditionally denoted $ind_H^G$ and just called *the induced representation*. The [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the [[adjoint functor|adjunction]] in this case is traditionally known as *[[Frobenius reciprocity]]*.


## Definition

### Traditional formulation
 {#TraditionalFormulation}

Consider:

* $G$ a [[group]],

* $\mathbb{K}$ a [[ground field]] (or [[ground ring]]), 

* $\mathbb{K}[G] \,\coloneqq\, Span_{\mathbb{K}}\big( g \in G \big)$ the $\mathbb{K}$-[[linear span]] of the [[elements]] of $G$, equipped with the [[structure]] of the [[group algebra]] of $G$ [[associative algebra|over $\mathbb{K}$]], to be regarded canonically as a [[module]] ([[bimodule]]) over itself,

* $G Rep_{\mathbb{K}} \,\simeq\, \mathbb{K}[G]\text{-}Mod_{\mathbb{K}}$ the [[category of representations|category of]] $\mathbb{K}$-[[linear representations]] $G \curvearrowright V$ of $G$,

  $$
    \begin{array}{ccc}
      G \times V &\longrightarrow& V
      \\
      (g,v) &\mapsto& g \cdot v
      \mathrlap{\,,}
    \end{array}
  $$

  with [[intertwiners]] between them as [[morphisms]], 

  [[equivalence of categories|equivalently]] the [[category of modules|category of]] [[module|$\mathbb{K}[G]$-modules]], with [[hom-spaces]] to be denoted

  $$
    Hom_G(-,-) \,\equiv\, Hom_{\mathbb{K}[G]}(-,-)
    \mathrlap{\,,}
  $$

*  $H \xhookrightarrow{\iota} G$ a [[subgroup]] inclusion.

Write
\[
  \label{FunctorOfRestrictedRepresentation}
  \iota^\ast
  \;\colon\;
  G Rep_{\mathbb{K}}
  \xrightarrow{\;}
  H Rep_{\mathbb{K}}
\]
for the functor forming [[restricted representations]] along $\iota \colon H \hookrightarrow G$ (letting $H$ act on a given $G$-representation via its inclusion $\iota$ into $G$).

\begin{proposition}
**(left induced representation)**
  The functor $\iota^\ast$ (eq:FunctorOfRestrictedRepresentation) has a [[left adjoint]] $\iota_! \colon H Rep_{\mathbb{K}} \xrightarrow{\;} G Rep_{\mathbb{K}}$ given by
  \[
    \label{LeftInducedRepresentation}
    V \in H Rep_{\mathbb{K}}
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    \iota_{!} V
    \;\coloneqq\;
    \mathbb{K}[G]
      \otimes_{\mathbb{K}[H]}
    V
    \,,
  \]
  where on the right we have the $\mathbb{K}$-[[vector space]] (or [[module|$\mathbb{K}$-module]]) [[underlying]] the [[tensor product of modules|tensor product of]] (right-with-left) [[module|$\mathbb{K}[H]$-modules]] equipped with the $G$-[[group action]] given by
\[
  \label{ActionOnLeftInducedRep}
  \left.
  \begin{array}{l}
    [a,v] \,\in\, \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
    \\
    g \,\in\, G
  \end{array}
  \right\}
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  g \cdot [a,v] \,\coloneqq\, [g \cdot a, v]
  \,.
\]
\end{proposition}
\begin{proof}
We claim that the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is given by [[evaluation]] at the [[neutral element]] $\mathrm{e} \in G$:
$$
  \left.
  \begin{array}{l}
    V \,\in\, H Rep_{\mathbb{K}}
    \\
    W \,\in\, G Rep_{\mathbb{K}}
  \end{array}
  \right\}
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  \frac{
    \overset{
      \iota_! V
    }{
      \overbrace{
        \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
      }
    }
    \xrightarrow{\;\; f \;\;}
    W
  }{
    V 
    \xrightarrow{ f([\mathrm{e},-]) }
    \iota^\ast W
  }
$$
To see this, just observe that 
$$
  \left.
  \begin{array}{l}
    f \,\in\, Hom_G\big(
      \mathbb{C}[G] \otimes_{\mathbb{C}[H]} V
      ,\,
      W
    \big)
    \\
    h \,\in\, H
    \\
    v \,\in\, V
  \end{array}
  \right\}
  \;\;\;\;\;
  \vdash
  \;\;\;\;\;
  \begin{array}{rcl}
  f\big(
    [\mathrm{e}, h \cdot v]
  \big)
  &=&
  f\big(
    [\mathrm{e} \cdot h, v]
  \big)  
  \;=\;
  f\big(
    [h, v]
  \big)  
  \\  
  &=&
  f\big(
    [h \cdot \mathrm{e}, v]
  \big)
  \;=\;
  f\big(
    h \cdot [\mathrm{e}, v]
  \big)  
  \;=\;
  h \cdot
  \Big(
    f\big(
      [\mathrm{e}, v]
    \big)  
  \Big)
  \,,
  \end{array}
$$
where the first equality is by definition of the [[tensor product of bimodules|tensor product]], the second-but-last is (eq:ActionOnLeftInducedRep) and the last one is by the $G$-[[equivariance]] of $f$.
This shows that $f\big([\mathrm{e},-]\big)$ is $H$-[[equivariant]] and that it uniquely determines $f$, hence that we have a [[bijection]] of [[hom-sets]]

$$
  Hom_G\Big(
    \mathbb{K}[G] \otimes_{\mathbb{K}[H]} V
    ,\,
    W
  \Big)
  \;\;\simeq\;\;
  Hom_H\Big(
    V
    ,\,
    \iota^\ast W
  \Big)
  \,.  
$$

Finally, it is manifest that this bijection $f \mapsto f([\mathrm{e},-])$ is [[natural transformation|natural]] in $V$ and $W$, and so this establishes a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) exhibiting the claimed [[adjoint functor|adjunction]] $\iota_! \dashv \iota^\ast$.
\end{proof}


\begin{proposition}
**(right induced representation)**
  The functor $\iota^\ast$ (eq:FunctorOfRestrictedRepresentation) has a [[right adjoint]] $\iota_\ast \colon H Rep_{\mathbb{K}} \xrightarrow{\;} G Rep_{\mathbb{K}}$ given by
  \[
    \label{RightInducedRepresentation}
    V \in H Rep_{\mathbb{K}}
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    \iota_{\ast} V
    \;\coloneqq\;
    hom_H\big(
      \mathbb{K}[G]
      ,\,
      V
    \big)
    \,,
  \]
  where on the right we have the $\mathbb{K}$-[[vector space]] (or [[module|$\mathbb{K}$-module]]) of $H$-[[equivariant map|equivariant]] $\mathbb{K}$-[[linear maps]] equipped with the $G$-[[group action]] given by
\[
  \label{ActionOnRightInducedRep}
  \left.
  \begin{array}{l}
    f \,\colon\, \mathbb{K}[G] \xrightarrow{\;} V
    \\
    g \,\in\, G
    \\
    a \,\in\, \mathbb{K}[G]
  \end{array}
  \right\}
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  (g \cdot f)(a) \,\coloneqq\, f(a \cdot g)
  \,.
\]
\end{proposition}
\begin{proof}
We claim that the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is given by [[evaluation]] at the [[neutral element]] $\mathrm{e} \in G$:
$$
  \left.
  \begin{array}{l}
    V \,\in\, H Rep_{\mathbb{K}}
    \\
    W \,\in\, G Rep_{\mathbb{K}}
  \end{array}
  \right\}
  \;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;
  \frac{
  W 
  \xrightarrow{\;\;\;\; f \;\;\;\;}
  \overset{\iota_\ast V}{
  \overbrace{
    hom_{H}\big(
      \mathbb{K}[G]
      ,\,
      V
    \big)
  }
  }
  }{
    \iota^\ast W 
    \xrightarrow{\;\; f(-)(\mathrm{e}) \;\;} 
    V
  }
$$
To see this, just observe that 
$$
  \left.
  \begin{array}{l}
    f \,\in\, 
    Hom_G\Big(
      W
      ,\,
      hom_H\big(
       \mathbb{K}[G]
       ,\,
       V
      \big)
    \Big)
    \\
    h \,\in\, H
    \\
    w \,\in\, W
  \end{array}
  \right\}
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  \begin{array}{rcl}
  f(h \cdot w)(\mathrm{e})
  &=&
  \big( h \cdot f(w) \big)(\mathrm{e})  
  \;=\;
  f(w)(\mathrm{e} \cdot h)
  \;=\;
  f(w)(h)
  \\
  &=&
  f(w)(h \cdot \mathrm{e})
  \;=\;
  h\cdot\big(f(w)(\mathrm{e})\big)
  \end{array}
  \,,
$$
where the first equality is the $G$-[[equivariance]] of $f$, the second is (eq:ActionOnRightInducedRep) and the last one is the $H$-[[equivariance]] of $f(w)$. This shows that $f(-)(\mathrm{e})$ is $H$-equivariant and that it uniquely determines $f$, hence that we have a [[bijection]] of [[hom-sets]]:
$$
  Hom_G\Big(
    W 
    ,\,
    hom_H\big(
      \mathbb{K}[G]
      ,\,
      V
    \big)
  \Big)
  \;\;\simeq\;\;
  Hom_H\big(
    \iota^\ast W 
    ,\,
    V
  \big)
$$

Finally, it is manifest that this bijection $f \mapsto f([\mathrm{e},-])$ is [[natural transformation|natural]], and so this establishes a [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) exhibiting the claimed [[adjoint functor|adjunction]] $\iota^\ast \dashv \iota_{\ast}$.
\end{proof}


### General abstract formulation
 {#GeneralAbtractDefinition}

We formulate induction and coinduction of representations abstractly in [[homotopy type theory]]. (Hence the following is automatically the [[(∞,1)-category theory]]-version, which in parts is sometimes referred to as _[[cohomological induction]]_.)

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]]. By the discussion at _[[∞-action]]_, for $G \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence an [[∞-group]], the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ over its [[delooping]] is the [[(∞,1)-category]] of $G$-[[∞-actions]] 

$$
  Act(G) \simeq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

(A genuine _[[∞-representation]]/[[∞-module]]_ over $G$ may be taken to be a an abelian $\infty$-group object in $Act(G)$, but we can just as well work in the more general context of possibly non-linear representations, hence of actions.)

Accordingly, for $f \colon H \to G$ a homomorphism of [[∞-groups]], hence for a morphism $\mathbf{B}f \colon \mathbf{B}H \to \mathbf{B}G$ of their [[deloopings]], there is the corresponding [[base change geometric morphism]]

$$
  \textstyle{\big(\sum_f \dashv f^* \dashv \prod_f\big)}
  \;\colon\;
  Act(H)
   \stackrel{\overset{\sum_f}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{\prod_f}{\to}}}
  Act(G)
  \,.
$$

Here

* the [[inverse image]]/[[(∞,1)-pullback]] functor $f^*$ produces the "[[restricted representation|restricted]]" $\infty$-representations along $f$;

* the [[dependent sum]] $\sum_f$ is the _induced representation_ ∞-functor;

* the [[dependent product]] $\prod_f$ is the _coinduced representation_ ∞-functor.
 
{#LawvereInduced} For the case of [[permutation representations]] of [[discrete groups]]  this perspective is made explicit by [Lawvere 1069 p. 14](#Lawvere69), [1970 p. 5](#Lawvere70).






## Properties

\begin{proposition}
\label{LeftAndRightInductionCoincideForFiniteIndex}
Given a [[subgroup]] inclusion $H \subset G$,
if the [[index of a subgroup|index]] $[G\colon H]$ is [[finite number|finite]] then (left) induction coicides with coinduction (right induction).

In particular, the two coincide as soon as $G$ (and thus also $H$) is a [[finite group]].
\end{proposition}
(cf. [Hristova 2019 p 1](Frobenius+reciprocity#Hristova19))



\begin{proposition} 
**([[Brauer induction theorem]])**
\linebreak
Over the [[complex numbers]], the [[virtual representations]] of a [[finite group]] are all virtual combinations of [[induced representations]] of 1-dimensional representations.
\end{proposition}



## Examples and Applications

### Basic examples

\begin{example}
if $V = \mathbf{1}$ is the [[trivial representation]] of [[dimension]] 1 then its induced representation is the basic [[permutation representation]] spanned by the [[coset]]-space $G/H$:

$$
  ind_H^G
  \left( 
    \mathbf{1}
  \right)
  \;=\;
  k[G/H]
  \,.
$$

For more see at _[[induced representation of the trivial representation]]_.

\end{example}

(cf. [tom Dieck 2009, Chapter 4](#tomDieck09))


### Centralizer algebra / Hecke algebra
 {#HeckeAlgebra}

Let 

$$
  i \colon H \hookrightarrow G
$$ 

be a group homomorphism (often assumed to be a [[subgroup]] inclusion, and sometimes with $G$ assumed to be a [[finite group]]). For $E \in H Rep$ some $H$-representation (often taken to be the trivial $H$-representation), let $Ind_i E \in G Rep$ be the induced $G$-representation. Then the [[endomorphism ring]] $End_G(Ind_i E)$ of $Ind_i E$ in $G Rep$ is called the _centralizer algebra_ or also the _[[Hecke algebra]]_ or _[[Iwahori-Hecke algebra]]_ $Hecke(E,i)$ of the induced representation. (Basics are in [Woit, def. 2](#Woit), details are in [Curtis & Reiner 1981, section 67](#CurtisReiner81), a quick survey of related theory is given by [Srinivasan](#Srinivasan).

In terms of the notation in _[General abstract formulation](#GeneralAbtractDefinition)_ above and for $i \colon H \to G$ any homomorphism of $\infty$-groups, we have the [[∞-monoid]]

$$
  Hecke(E,i)
  \;\coloneqq\;
  \textstyle{
    \underset{\mathbf{B}G}{\prod}
    \left[
      \underset{\mathbf{B}i}{\sum} E
      ,\, 
      \underset{\mathbf{B}i}{\sum} E 
    \right]
  }
  \,,
$$

where $[-,-]$ is the [[internal hom]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G} \simeq G Act(\mathbf{H})$.

For $V \in Act(G)$ any other representation, there is a canonical [[∞-action]] of $Hecke(E,i)$ on $\underset{\mathbf{B}G}{\prod} \left[\underset{\mathbf{B}i}{\sum} E , V \right]$. If here $E$ is the trivial representation then by adjointness this is the [[invariants]] $V^G$ of $V$ and hence the Hecke algebra acts on the invariants. (See for instance [Woit, def. 2](#Woit)). This is sometimes called the _Hecke algebra action on the Iwahori fixed vectors_ ([e.g. here, p. 9](#http://sporadic.stanford.edu/bump/bbf.pdf))

### Zuckerman functors: Coinduction on Harish-Chandra modules

Coinduction on [[Harish-Chandra modules]] is referred to as
_[[Zuckerman induction]]_. See there for more details.


## Related concepts

* The identification of representation induction as the extra left adjoint in a [[base change]] morphism, as discussed in the _[General abstract discussion](#GeneralAbtractDefinition)_ above, puts induced representations in the same general abstract framework as [[existential quantification]] in [[logic]] and generally of [[dependent sum]] in [[dependent type theory]] (see there for more details). This relation has first been amplified in ([Lawvere](#Lawvere)).

* If the modules over a group are considered as comodules over the function Hopf algebra over the group, then one can instead consider the induction for comodules. See [[cotensor product]]. 

* The [[derived functor]] of the representation induction functor is often referred to as _[[cohomological induction]]_.

* [[Dirac induction]]

* The [[character]] of an induced representation is an [[induced character]].

* [[Artin induction theorem]]

* [[Brauer induction theorem]]

* [[Artin-Lam induction exponent]]

[[!include homotopy type representation theory -- table]]


## References

### Traditional formulation
 {#ReferencesTraditionalFormulation}

Original articles:

* {#Mackey52} [[George Mackey]], *Induced representations of locally compact groups I*, Annals of Mathematics **55** 1 (1952) 101-139 &lbrack;[doi:10.2307/1969423](https://doi.org/10.2307/1969423), [jstor:1969423](https://www.jstor.org/stable/1969423)&rbrack;

* {#Mackey53} [[George Mackey]]: _Induced representations of locally compact groups II_, Annals of Mathematics **58** 2 (1953) 193-221 &lbrack;[doi:10.2307/1969786](https://doi.org/10.2307/1969786), [jstor:1969786](https://www.jstor.org/stable/1969786)&rbrack; 

* {#Mackey68} [[George Mackey]]: *Induced representations of groups and quantum mechanics*, W. A. Benjamin, New York (1968) &lbrack;[ark:/13960/t6841m201](https://archive.org/details/inducedrepresent0000mack)&rbrack;
  > (cf. *[[Wigner classification]]*)

Textbook accounts:

* {#Serre77} [[Jean-Pierre Serre]], section 3.3 of: *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;

* {#CurtisReiner62} [[Charles Curtis]], [[Irving Reiner]]: *Induced Representations*, chapter VII in: _Representation theory of finite groups and associative algebras_, AMS (1962) &lbrack;[ISBN:978-0-8218-4066-5](https://bookstore.ams.org/chel-356.h)&rbrack;

* {#CurtisReiner81} [[Charles Curtis]], [[Irving Reiner]]: *Methods of representation theory -- With applications to finite groups and orders -- Vol. I*, Wiley (1981) &lbrack;[ark:/13960/t8gf4wd3x](https://archive.org/details/methodsofreprese00curt/page/n1/mode/2up)&rbrack;

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], section 3.3 of: _Representation Theory: a First Course_, Springer (1991) &lbrack;[doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9)&rbrack;

* [[Pavel Etingof]], [[Dmitry Vaintrob]], et al., section 4.8 of: *Introduction to representation theory*, Student Mathematical Library **59**, AMS (2011) &lbrack;[arXiv:0901.0827](https://arxiv.org/abs/0901.0827), [ams:stml-59](https://bookstore.ams.org/stml-59)&rbrack;
 
* {#Steinberg12} [[Benjamin Steinberg]], section 8.2 of: *Representation Theory of Finite Groups -- An Introductory Approach*, Springer (2012) &lbrack;[doi:10.1007/978-1-4614-0776-8](https://doi.org/10.1007/978-1-4614-0776-8)&rbrack;

Lecture notes:

* {#tomDieck09} [[Tammo tom Dieck]], Chapter 4 of _Representation theory_ (2009) &lbrack;[pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf)&rbrack;

See also: 

* [[eom]]: *[induced representation](https://www.encyclopediaofmath.org/index.php/Induced_representation)*
 
* *Wrong-way Frobenius reciprocity for finite groups representations* &lbrack;[MO:q/132272](https://mathoverflow.net/q/132272/381)&rbrack;

* {#Srinivasan} Bhama Srinivasan; *Modular Representations, Old and New*, &lbrack;[pdf](http://homepages.math.uic.edu/~srinivas/bfggpaper.pdf), [[Srinivasan-ModularRepresentations.pdf:file]]&rbrack;




### General abstract formulation

The [general abstract formulation](#GeneralAbtractDefinition) above is mentioned (for [[discrete groups]] and their [[permutation representations]]) in 

* {#Lawvere69} [[William Lawvere]]: _[[Adjointness in Foundations]]_, Dialectica **23** (1969) 281-296,  Reprints in Theory and Applications of Categories, **16** (2006) 1-16 &lbrack;[pdf](http://www.tac.mta.ca/tac/reprints/articles/16/tr16.pdf)&rbrack;
 
* {#Lawvere70} [[William Lawvere]]: _[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970) 1-14 &lbrack;[pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf)&rbrack;

 

[[!redirects induced module]]
[[!redirects induced representations]]
[[!redirects induction functor]]
[[!redirects induction functors]]

[[!redirects coinduced representation]]
[[!redirects coinduced representations]]
[[!redirects coinduction functor]]
[[!redirects coinduction functors]]

[[!redirects induced action]]
[[!redirects induced actions]]

[[!redirects left induced representation]]
[[!redirects left induced representations]]

[[!redirects right induced representation]]
[[!redirects right induced representations]]

[[!redirects left induced action]]
[[!redirects left induced actions]]

[[!redirects right induced action]]
[[!redirects right induced actions]]

