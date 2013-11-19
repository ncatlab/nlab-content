
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #tStruc}
###### Definition

Let $\mathcal{D}$ be a [[triangulated category]]. A _t-structure_ on $\mathcal{D}$ is a [[pair]] of [[full subcategories]]

$$
   \mathcal{D}_{\geq 0}, \mathcal{D}_{\leq 0} \hookrightarrow \mathcal{D}
$$

such that

1. for all $X \in \mathcal{D}_{\geq 0}$ and $Y \in \mathcal{D}_{\leq 0}$ the [[hom object]] is the [[zero object]]: $Hom_{\mathcal{D}}(X, Y[-1]) = 0$;

1. the subcategories are closed under [[suspension]]/desuspension: $\mathcal{D}_{\geq 0}[1] \subset \mathcal{D}_{\geq 0}$ and $\mathcal{D}_{\leq 0}[-1] \subset \mathcal{D}_{\leq 0}$.

1. For all [[objects]] $X \in \mathcal{D}$ there is a [[fiber sequence]] $Y \to X \to Z$ with $Y \in \mathcal{D}_{\geq 0}$ and $Z \in \mathcal{D}_{\leq 0}[-1]$.
 
=--

+-- {: .num_defn }
###### Definition

Given a t-structure, its _heart_ is the intersection

$$
  \mathcal{D}_{\geq 0} \cap \mathcal{D}_{\leq 0}
  \hookrightarrow
  \mathcal{D}
  \,.
$$

=--


+-- {: .num_defn }
###### Definition

A t-structure on a [[stable (∞,1)-category]] is a t-structure on its [[homotopy category of an (∞,1)-category]], according to def. \ref{tStruc}.

=--

([[Higher Algebra|Higher Algebra, def. 1.2.1.4]]).

## Properties

### General

+-- {: .num_prop }
###### Proposition

The heart of a stable $(\infty,1)$-category is an [[abelian category]]. 

=--

([BBD 82](#BBD82), [[Higher Algebra|Higher Algebra, remark 1.2.1.12]])


### Application to spectral sequence

If a the heart of a t-structure on a [[stable (∞,1)-category]] with [[sequential limits]] is an [[abelian category]], then the [[spectral sequence of a filtered stable homotopy type]] converges (see there).

## References

Related $n$Lab entries include [[Bridgeland stability]]. 

For triangulated categories

* S. I. Gelfand, [[Yuri Manin]], _Methods of homological algebra_, Nauka 1988, Springer 1998, 2003

* [[Donu Arapura]], _Triangulated categories and $t$-structures_ ([pdf](http://www.math.purdue.edu/~dvb/preprints/perv2.pdf))

* [[Alexander Beilinson]], [[Joseph Bernstein]], [[Pierre Deligne]], _Faisceaux pervers_, Asterisque __100__, Volume 1, 1982
 {#BBD82}
* D. Abramovich, A. Polishchuk, _Sheaves of t-structures and valuative criteria for stable complexes_, J. reine angew. Math. __590__ (2006), 89&#8211;130
* A. L. Gorodentsev, S. A. Kuleshov, A. N. Rudakov, _t-stabilities and t-structures on triangulated categories_, Izv. Ross. Akad. Nauk Ser. Mat. __68__ (2004), no. 4, 117&#8211;150
* A. Polishchuk, _Constant families of t-structures on derived categories of coherent sheaves_, Moscow Math. J. __7__ (2007), 109&#8211;134
* John Collins, [[Alexander Polishchuk]], _Gluing stability conditions_, [arxiv/0902.0323](http://arxiv.org/abs/0902.0323)

For [[stable (∞,1)-categories]]

* [[Jacob Lurie]], _[[Higher Algebra]]_


[[!redirects t-structures]]

[[!redirects t-structure on a stable (∞,1)-category]]
[[!redirects t-structures on a stable (∞,1)-category]]

[[!redirects t-structure on a stable (infinity,1)-category]]
[[!redirects t-structures on a stable (infinity,1)-category]]


[[!redirects heart]]
[[!redirects hearts]]

[[!redirects heart of a t-structure]]
[[!redirects hearts of t-structures]]

[[!redirects heart of a stable (∞,1)-category]]
[[!redirects hearts of stable (∞,1)-categories]]

[[!redirects heart of a stable (infinity,1)-category]]
[[!redirects hearts of stable (infinity,1)-categories]]
