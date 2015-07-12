## Idea 

The **ultraproduct** construction is an important tool in [[model theory]] that permits to produce a new structure from an infinite family of structures. The construction has a decidedly 'algebraic' flavor and hence occurs naturally in applications of model theory to [[algebra]].

It is closely related via the [[?o? ultraproduct theorem]] to the [[compactness theorem]]: suppose one is given a set of formulas $S$ in some first-order language and a family of structures such that any finite subset of formulas is modeled by all but a finite number of structures. Then an ultraproduct of those structures may be used to model the entire set $S$.[^compact] 

[^compact]: Due to the outstanding importance of the compactness theorem, it is possible to prove 'almost all' results in model theory by the use of ultra products. This approach to model theory is pursued in [Bell-Slomson (1969)](#BellSlomson). For contrast, compare with the more sober view of [Hodges (1993)](#Hodges93).

In slightly greater detail, given a family of [[structures]] of the same signature in the sense of [[model theory]] (or more specially, [[universal algebra]]), one can (assuming the [[ultrafilter principle]], a weak form of the [[axiom of choice]]) use [[ultrafilters]] to form a certain [[congruence]] on the [[direct product]] and construct a [[quotient object]], a new structure of the same signature, called an __ultraproduct__. As long as the ultrafilter is [[free ultrafilter|free]] (contains the filter of cofinite subsets), the last sentence of the preceding paragraph is validated. 

An ultraproduct of some number of copies of the same structure is called an __ultrapower__.

Another important facet, somewhat reminiscent of [[Morita equivalence]], is the [[Keisler-Shelah theorem]]: Two structures are elementary equivalent $\mathfrak{A}\equiv\mathfrak{B}$ iff they have isomorphic ultrapowers: $\mathfrak{A}^I / \mathcal{U} \cong \mathfrak{B}^I / \mathcal{U}$ for some set $I$ and ultrafilter $\mathcal{U}$.

## Definition 

First we present the bare-bones set-theoretic construction; then we discuss structures and models. 

### Set-theoretic 

+-- {: .num_defn} 
###### Definition 
Let $X$ be a set, and let $U$ be an [[ultrafilter]] on $X$, which may be regarded as an element $U: 1 \to \beta X$ of the [[Stone-Cech compactification]] $\beta X = \hom_{Bool}(2^X, 2)$ with its usual topology. The **ultrapower functor** over $U$ is the functor 

$$Set/X \simeq Sh(X_{disc}) \stackrel{i_\ast}{\to} Sh(\beta X) \stackrel{U^\ast}{\to} Set$$ 

where $i_\ast$ is the [[direct image functor]] between categories of [[sheaves]] induced from the [[inclusion map|inclusion]] $i: X \to \beta X$ of $X$ as a [[discrete space|discrete]] [[subspace]], and the [[inverse image functor]] $U^\ast$ is also known as the "taking the [[stalk]]" functor at the point $U \in \beta X$. 
=-- 

Let us extract a more concrete description. Let $\{Y_x: x \in X\}$ be an $X$-indexed family of sets, which we can view as an object $Y \to X$ of $\Set/X$. We may view this object as a sheaf over $X$ as discrete space; as a presheaf, it takes an open set (an arbitrary subset $A \subseteq X$) to the set of sections over $A$ which is $\prod_{x \in A} Y_x$. The direct image functor $i_\ast$ takes this presheaf to the presheaf which sends an arbitrary open set $\mathcal{V} \subseteq \beta X$ to $\prod_{x \in X \cap \mathcal{V}} Y_x$, and then the stalk functor $U^\ast$ sends this to the [[filtered colimit]] 

$$colim_{\mathcal{V} \ni U} \prod_{x \in X \cap \mathcal{V}} Y_x$$ 

and since the basic opens $\mathcal{V}_A = \{U' \in \beta X: A \in U'\}$ with $A \in U$ are [[cofinal functor|cofinal]] in the system of open neighborhoods of $U$ (ordered by reverse inclusion), the colimit may be written more simply as 

$$colim_{A \in U} \prod_{x \in A} Y_x$$ 

and this is the *ultraproduct*, often written as $\prod_{x \in X} Y_x/U$.[^note] When all the fibers $Y_x$ are the same set $Z$, this is written as $Z^X/U$ and called an *ultrapower* of $Z$. 

[^note]: The quotient notation is traditional but (ever so slightly) misleading. If all the $Y_x$ are [[inhabited sets]], then all the maps $\prod_{x \in A} Y_x \to \prod_{x \in B} Y_x$ ($B \subseteq A$) are quotient maps and the ultraproduct is a quotient of the full product $\prod_{x \in X} Y_x$; there the notation is apt. If one of the $Y_x$ is empty, then the full product is empty and thus the ultraproduct is not such a quotient. But it is useful to allow for empty models (when they exist)! The correct definition which works for all cases is as we have it: a filtered colimit over restricted products. 

### Ultraproducts of structures 

Now suppose each $Y_x$ carries a structure specified by a [[signature (in logic)|signature]]; in other words, for each function symbol $f$ and predicate symbol $R$ of the signature there are specified operations and subsets 

$$\omega_f: Y_x^{ar(f)} \to Y_x, \qquad \rho_R \rightarrowtail Y_x^{ar(R)}$$ 

where $ar$ denotes arity (constants being considered function symbols of arity zero). Then of course the products $\prod_{a \in A} Y_x$ carry structures canonically induced from those on the $Y_x$. As all of the function symbols $f$ and predicate symbols $R$ have finite arity, and since the taking of filtered colimits commutes with finite limits in $Set$, we get a canonically induced structure on the ultraproduct $\prod_{x \in X} Y_x/U$. More briefly: since $U^\ast i_\ast$ preserves finite limits, it takes an $X$-indexed finitary structure $Y_x$ in $Set/X$ to a finitary structure of the same type in $Set$. 

Intuitively (and adopting language used by Lawvere), what is going on is that we have a variable structure varying over some domain $X$, and we consider a point $U$ of its compactification $\beta X$ as some kind of "ideal point at infinity", and then we "freeze" (or localize) the variation by passing to germs of the variation at that point $U$. 

Notice that if we replace the word "ultrafilter" by the word "filter", the general structural facts mentioned here would remain true. That is to say: if $F$ is a filter consisting of subsets of $X$, then the colimit $colim_{A \in F} \prod_{x \in A}$ (with such $A$ ordered by reverse inclusion) is still directed or filtered, and we would still get a structure of given finitary type by passing to the colimit. Here, instead of ultrapowers and ultraproducts, one speaks of *reduced powers* and *reduced products*. 

### Ultraproducts of models 

To be written. 

## Examples 

The [[hyperreal number]]s ([wikipedia](http://en.wikipedia.org/wiki/Hyperreal_numbers)) and nonstandard integers in [[nonstandard analysis]] are obtained as [[denumerable set|countable]] ultrapowers with help of [[free ultrafilters]] on $\mathbb{N}$. Such ultrafilters contain all [[cofinite subset|cofinite]] subsets of integers, but not only them. See [wikipedia:ultraproduct](http://en.wikipedia.org/wiki/Ultraproduct).

From Michael Barr's [Models of Sketches](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1986__27_2/CTGDC_1986__27_2_93_0/CTGDC_1986__27_2_93_0.pdf)  

>Unlike [[limits]] and [[colimits]], an ultraproduct is not defined by any [[universal mapping property]]. Of course, if the category has limits and ([[filtered colimit|filtered]]) colimits, then it has ultraproducts constructed as colimits of [[products]] ... But usually the category of models of a [[coherent theory]] (such as the theory of [[discrete field|fields]]) lacks products and  hence does not have categorical ultraproducts.

## Related entries

* [[model theory]]

* [[ultrafilter monad]]

* [[large cardinal]]

## References

Standard references in model theory for ultra products are

* {#BellSlomson}[[John Bell|J. L. Bell]], A. B. Slomson, _Models and Ultraproducts: An Introduction_ , North-Holland Amsterdam 1969. (Dover reprint)

* P. C. Eklof, _Ultraproducts for Algebraists_ , pp.105-137 in Barwise (ed.), _Handbook of Mathematical Logic_ , Elsevier Amsterdam 1977.

For a more recent textbook treatment:

* {#Hodges93} [[Wilfrid Hodges]], _Model Theory_ , Cambridge University Press 1993. (sec. 9.5)

The categorical perspective on ultraproducts goes back to

* T. Okhuma, _Ultrapowers in categories_ , Yokohama Math. J. **14** (1966) pp.17-37.

* S. Fakir, L. Haddad, _Objets coh&#233;rents et ultraproduits dans les cat&#233;gories_  , Journal
of Algebra **21** (1972) pp.410&#8211;421.

For the vacuum engineering point of view of 'freezing variation' [^cont] in the context of non-standard analysis see

* [[F. William Lawvere]], _Variable sets etendu and variable structure in topoi_ , Lecture notes University of Chicago 1975.

[^cont]: This perspective was apparently inspired by joined work with [[Miles Tierney]] on the use of [[forcing]] in the context of the [[continuum hypothesis]] in early topos theory.

The following papers are relevant for understanding the ultraproduct construction via  [[codensity monad|codensity monads]]:

* D. P. Ellerman, _Sheaves of structures and generalized ultraproducts_ , Annals of
Mathematical Logic **7** (1974) pp.163&#8211;195.

* J. F. Kennison, _Triples and compact sheaf representation_ ,  JPAA **20** (1981) pp.13-38.

* [[Tom Leinster]], _Codensity and the Ultrafilter Monad_ , TAC **28** no. 13 (2013) pp.332-370. ([tac](http://www.tac.mta.ca/tac/volumes/28/13/28-13abs.html))

See also

* [[M. Makkai]], _Ultraproducts and categorical logic_ , Lectures Notes in Math. __1130__, Springer 1985, pp. 222&#8211;309

[[!redirects ultraproduct]]
[[!redirects ultraproducts]]
[[!redirects ultrapower]]
[[!redirects ultrapowers]]
[[!redirects reduced product]] 
[[!redirects reduced power]] 
[[!redirects reduced products]] 
[[!redirects reduced powers]] 