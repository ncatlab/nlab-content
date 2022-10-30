
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Separators
* table of contents
{: toc}

## Idea

An [[object]] $S$ (or family $\mathcal{S}$ of objects) in a [[category]] $\mathcal{C}$ is called a _separator_ or _generator_ if [[generalized elements]] with [[domain]] $S$ (or domain from $\mathcal{S}$) are sufficient to distinguish [[morphisms]] in $\mathcal{C}$.

The [[duality|dual]] notion is that of a _[[coseparator]]_.


## Caution on terminology

The term 'generator' is more ambiguous because of the use of 'generators' as in [[generators and relations]].


## Definitions

+-- {: .num_defn}
###### Definition

An [[object]] $S \in \mathcal{C}$ of a [[category]] $\mathcal{C}$ is called a __separator__ or a __generator__ or a __separating object__ or a __generating object__, or is said to __separate morphisms__ if:
* for every pair of [[parallel morphisms]] $f,g \colon X \to Y$ in $\mathcal{C}$, if
  * for every morphism $e\colon S \to X$,
  * $u \circ f = u \circ g$,
* then $f = g$.
=--

Assuming that $\mathcal{C}$ is [[locally small|locally small category]], we have equivalently say that $S$ is a separator if the [[hom functor]] $Hom(S,-) \colon \mathcal{C} \to $ [[Set]] is [[faithful functor|faithful]].


More generally:

+-- {: .num_defn}
###### Definition

A [[family]] $\mathcal{S} = (S_a ;|; a\colon A)$ of [[objects]] of a [[category]] $\mathcal{C}$ is a __separating family__ or a __generating family__ if:
* for every pair of [[parallel morphisms]] $f,g \colon X \to Y$ in $\mathcal{C}$, if
  * for every index $a$ and every morphism $e\colon S_a \to X$,
  * $e \circ f = e \circ g$,
* then $f = g$.
=--

Assuming again that $\mathcal{C}$ is [[locally small category|locally small]], we have equivalently say that $\mathcal{S}$ is a separating family if the family of [[hom functors]] $Hom(U_a,-) \colon \mathcal{C} \to $ [[Set]] is [[jointly faithful family of functors|jointly faithful]].

Since repetition is irrelevant in a separating family, we may also speak of a _separating [[class]]_ instead of a separating family.

+-- {: .num_defn}
###### Definition

A __separating set__ is a [[size issues|small]] separating class.
=--


## Examples and applications

* In [[Set]], any [[inhabited set]] is a separator; in particular, the [[point]] is a separator.

*  More generally, in any [[well-pointed category]], any [[terminal object]] is a separator.  More generally still, in any represented [[concrete category]], the representing object is a separator.

* The standard example of a separator in the category of $R$-[[modules]] over a [[ring]] $R$ is any [[free module]] $R^I$ (for $I$ an [[inhabited set]]) and $R$ (which is $R^I$ for $I$ a [[point]]) in particular.  If a separator is a finitely separated [[projective object]] in the category of $R$-modules, then the traditional terminology is _progenerator_.  Progenerators are important in classical Morita theory, see [[Morita equivalence]].

  +-- {: .query}
  [[Mike Shulman|Mike]]: The term "progenerator" seems unfortunate to me; it sounds to me like a [[pro-object]] that is a generator.  Is it well-established?  I've never heard it, though I have heard "projective generator" in the context of Morita theory.

  [[Zoran Škoda]]: It is an extremely frequent term in classical algebra and in many of the standard monographs in module theory over classical rings. I personally never use the expression and mentioned it only once in a survey. But as a link to that area of mathematics I tend to behave conservatively. Notice that the terminology subsumes finite generation. 
  =--

* The existence of a small separating family is one of the conditions in [[Giraud's theorem]] characterizing [[Grothendieck topos]]es.

* The existence of a small (co)separating family is one of the conditions in one version of the [[adjoint functor theorem]].


## Strengthened separators

+-- {: .num_theorem}
###### Motivating theorem

If $C$ is [[locally small category|locally small]] and has all small [[coproduct]]s, then a family $(S_a)_(a\colon A)$  is a separating family if and only if, for every $X\in C$, the canonical morphism
$$ \varepsilon_X\colon \coprod_{a\colon A, f\colon S_a \to X} S_a \longrightarrow X $$
is an [[epimorphism]].
=--

More generally:

+-- {: .num_defn}
###### Definition

If $\mathcal{E}$ is a subclass of epimorphisms, we say that $(S_a)_(a\colon A)$ is an __$\mathcal{E}$-separator__ or __$\mathcal{E}-generator__ if each morphism $\varepsilon_X$ (as above) is in $\mathcal{E}$.
=--

Of particular importance is the notion of __strong separator__ or __strong generator__, which is obtained by taking $\mathcal{E}$ to be the class of [[strong epimorphism]]s.  This can be expressed equivalently, without requiring local smallness or the existence of coproducts, by saying that the family $C(S_a,-)$ is jointly faithful and jointly [[conservative functor|conservative]].

If we take $\mathcal{E}$ to be the class of [[extremal epimorphism]]s, we might call the resulting notion "extremal separator," but __dense separator__ or __dense generator__ is more standard. The reason is that the family $(S_a)_(a\colon A)$ is an extremal separating family if and only if the inclusion of the [[full subcategory]] on the objects $(S_a)_(a\colon A)$ is [[dense functor|dense]] (and this definition makes sense without assuming coproducts or local smallness).  This is the strongest sort of separator.

If $C$ has [[pullbacks]], then extremal epis reduce to strong ones, and so extremal separators are necessarily strong. For this reason, some authors simply define "strong generator" to mean dense generator.

+-- {: .query}
[[Daniel Schaeppi]] Something seems to be wrong here: strong epimorphisms are extremal, so the notion of extremal generator is weaker than the notion of strong generator. In general, not every strong separator / strong generator is ($Set$-)dense (take the free abelian group on one separator, for example).
=--


## Related concepts

* [[coseparator]]


[[!redirects separator]]
[[!redirects separators]]
[[!redirects generator]]
[[!redirects generators]]

[[!redirects separating family]]
[[!redirects separating families]]
[[!redirects generating family]]
[[!redirects generating families]]

[[!redirects separating class]]
[[!redirects separating classes]]
[[!redirects generating class]]
[[!redirects generating classes]]

[[!redirects separating set]]
[[!redirects separating sets]]
[[!redirects generating set]]
[[!redirects generating sets]]

[[!redirects strong separator]]
[[!redirects strong separators]]
[[!redirects strong generator]]
[[!redirects strong generators]]

[[!redirects dense separator]]
[[!redirects dense separators]]
[[!redirects dense generator]]
[[!redirects dense generators]]
