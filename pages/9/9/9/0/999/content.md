
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Contents 
* table of contents
{: toc}

## Idea

An [[object]] of a [[category]] is called *compact* if it is "finite" or "small" in some precise sense. There are however different formalizations of this idea. Here discussed is the notion, usually going by this term, where an object $X$  is called _compact_ if mapping out of it [[preserved colimit|preserves]] [[filtered colimits]]. 

This means that if any other object $A$ is given as the [[colimit]] of a "suitably increasing" family of objects $\{A_i\}$, then every morphism 

$$
  X 
  \longrightarrow 
  A 
   = 
  \underset{\underset{i}{\longrightarrow}}{\lim} A_i
$$

out of the compact object $X$ into that colimit factors through one of the [[coprojections]] $A_i \to \underset{\underset{i}{\longrightarrow}}{lim A_i}$.

The notion of _[[small object]]_ is essentially the same, with a bit more flexibility on when the family $\{A_i\}$ is taken to be "suitably increasing". An important application of the above factorization property is accordingly named the _[[small object argument]]_.
On the other hand, there is also the notion of _[[finite object]]_ (in a [[topos]]) which, while closely related, is different. See also _[Subtleties and different meanings](#SubtletiesAndDifferentMeanings)_ below.



## Definition 
{#FinitelyPresentableObject}

+-- {: .num_defn }
###### Definition

Let $C$ be a [[locally small category]] that admits [[filtered colimits]]. Then an [[object]] $X \in C$ is **compact**, or **finitely presented** or **finitely presentable**, or **of finite presentation**, if the [[corepresentable functor]]

$$
  Hom_C(X,-) \colon C \to Set
$$

[[preserved limit|preserves]] these [[filtered colimits]].  This means that for every [[filtered category]] $D$ and every functor $F : D \to C$, the canonical morphism

$$
  \underset{\underset{d}{\to}}{\lim} C(X,F(d)) \xrightarrow{\simeq}
  C(X, \underset{\underset{d}{\to}}{\lim} F(d))
$$

is an [[isomorphism]].

More generally, if $\kappa$ is a [[regular cardinal]], then an object $X$ such that $C(X,-)$ commutes with $\kappa$-[[filtered colimits]] is called **$\kappa$-compact**, or **$\kappa$-presented**, or **$\kappa$-presentable**.  An object which is $\kappa$-compact for some regular $\kappa$ is called a [[small object]].

=--


## Properties
  {#Properties}


\begin{proposition}
\label{SmoothColimitsOfCompactObjectsAreCompact}
**(smooth colimits of compact objects are compact)**
\linebreak
A $\kappa$-small [[colimit]] of $\kappa$-compact objects is again a $\kappa$-compact object.
\end{proposition}

\begin{proof}
Let $D$ be a $\kappa$-[[small category]] and $X : D \to C$ a [[diagram]] of $\kappa$-compact objects. Let $I$ be a $\kappa$-[[filtered category]] and $A : I \to C$ a $\kappa$-filtered diagram in $C$. Then

$$
  Hom
  \Big(
    \underset{\underset{d}{\longrightarrow}}{\lim}
    X_d
    ,\, 
    \underset{\underset{i}{\longrightarrow}}{\lim}
    A_i
  \Big)
  \;\simeq\;
  \underset{\underset{d}{\longleftarrow}}{\lim}
  \;
   Hom
   \Big(
     X_d
     ,\, 
    \underset{\underset{i}{\longrightarrow}}{\lim}
     A_i
   \Big)
$$

by [[hom-functor preserves limits|general properties of]] the [[hom functor]]. Now using that every $X_d$ is $\kappa$-compact and $I$ is $\kappa$-filtered this is

$$
  \cdots 
  \;\simeq\;
  \underset{\underset{d}{\longleftarrow}}{\lim}
  \;
  \underset{\underset{i}{\longrightarrow}}{\lim}
  \;
  Hom\big(X_d, A_i\big)
  \,.
$$

Since this (co)limit is taken in [[Set]], the $\kappa$-small limit over $D$ [[limits commuting with colimits|commutes]] with the $\kappa$-filtered colimit

$$
  \cdots 
  \;\simeq\;
  \underset{\underset{i}{\longrightarrow}}{\lim}
  \;
  \underset{\underset{d}{\longleftarrow}}{\lim}
  \,
  Hom\big(X_d, A_i\big)
  \,.
$$

Finally we make take the limit again to a colimit in the first argument

$$
  \cdots 
  \;\simeq\;
  \underset{\underset{i}{\longrightarrow}}{\lim}
  \;
  Hom
  \big(
    \underset{\underset{d}{\longrightarrow}}{\lim}
    X_d
    ,\, 
    A_i
  \big)
  \,,
$$

which yields the claim.
\end{proof}

+-- {: .num_prop}
###### Proposition
In a $\lambda$-[[accessible category]], if $\lambda$ is [[sharply smaller cardinal|sharply smaller]] than $\kappa$, then every $\kappa$-compact object is a [[retract]] of a $\kappa$-small $\lambda$-filtered colimit of $\lambda$-compact objects.
=--
+-- {: .proof}
###### Proof
See [Adamek-Rosicky, Remark 2.15](#AdamekRosicky94).  It is noted there that with the more technical proof of [Makkai-Pare, Proposition 2.3.11](#MakkaiPare89) the words "a retract of" can be omitted.
=--

If we weaken the hypothesis to $\lambda\le \kappa$, then we retain all of the result except for $\lambda$-filteredness of the colimit.

+-- {: .num_prop}
###### Proposition
In a locally $\lambda$-[[locally presentable category|presentable category]], if $\lambda\le \kappa$, then every $\kappa$-compact object is a [[retract]] of a $\kappa$-small colimit of $\lambda$-compact objects.
=--
+-- {: .proof}
###### Proof
See [Adamek-Rosicky, Remark 1.30](#AdamekRosicky94).  It is claimed there that the words "a retract of" can be omitted by reference to an argument in Makkai-Pare, but it seems unclear how this argument is intended to be used.  An alternative proof of this improvement is proposed [at this mathoverflow question](https://mathoverflow.net/q/325278).
=--



## Examples 
 {#Examples}

* In $C = $ [[Set]] an object is compact precisely if it is a [[finite set]].
For this to hold constructively, [[filtered categories]] (appearing in the definition of _[[filtered colimit]]_) have to be understood as categories admitting cocones of every _Bishop-finite_ diagram.
(An object of Set is a [[finite set|Kuratowski-finite]] precisely if it is a [[finitely generated object]], or equivalently if it is [[compact space|compact]] when regarded as a [[discrete object|discrete]] topological space.)

* For $C$ a [[topos]], $X$ is compact if:
    * $C$ is a [[Grothendieck topos | sheaf topos]] on a site whose topology is generated by finite covering families and $X$ is a representable sheaf;

    * in particular if $C$ is a [[coherent topos]] and $X$ is a [[coherent object]].

However, there exist compact objects which are not coherent, c.f. the [[Elephant]], D3.3.12.

* In $C = $ [[Grp]] an object is compact precisely if it is [[finitely presented group|finitely presented]] as a group.

* More generally, if $C$ is any [[variety of algebras]], then an object is compact precisely if it is [[finitely presented algebra|finitely presented]] as an algebra.  A proof may be found in  [Ad&#225;mek-Rosick&#253; 94, Corollary 3.13 ](#AdamekRosicky94).

* Let $X$ be a [[topological space]] and let $C = Op(X)$ be the [[category of open subsets]] of $X$. Then an [[open subset]] $U \in C$ is a compact object in $C$ precisely if it is a [[compact space|compact topological space]].  (It is *not* true that $X$ is a compact object of $Top$ iff it is a compact topological space; see below.)

* A [[finite-dimensional vector space]] is compact in [[Vect]], see [here](finite-dimensional+vector+space#CompactClosure).

## Subtleties and different meanings 
 {#SubtletiesAndDifferentMeanings}

One has to be careful about the following variations of the theme of compactness.

(Some of these subtleties are resolved by noticing that there is a hierarchy of notions of compact objects that are secretly different but partly go by the same name. Some discussion of this is currently at _[[compact topos]]_, but more detailed discussion should eventually be somewhere...)

In the [[Elephant]], what Johnstone calls _compact objects_ are those objects such that the [[top]] element of the [[poset of subobjects]] $\operatorname{Sub}(C)$ is a [[compact element]]; he reserves the term _finitely-presented_ for the notion of compact on this page.

### Compactness in additive categories 
  {#CompactnessInAdditiveCategories}

When $C$ is an [[additive category]] (often a [[triangulated category]]), an object $x$ in $C$ is called **compact** if for every set $S$ of objects of $C$ such that the coproduct $\coprod_{s\in S} s$ exists, the canonical map
$$
\coprod_{s\in S} C(x,s)\to C(x,\coprod_{s\in S}s)
$$
is an [[isomorphism]] of [[commutative monoid|commutative monoids]]. 

Here is an application of this concept to characterize which abelian categories are categories of modules of some ring:

+-- {: .un_theorem}
###### Theorem

Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a compact [[projective object| projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any [[compact projective object|compact projective]] generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--


+-- {: .proof}
###### Proof

This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

+--{.query}
Zoran: While Ginzburg's reference is surely a worthy to look at, it would be better not to give false impression that this [[reconstruction theorem]] is due Ginzburg or at all new. It is rather a classical and well know fact probably from early 1960s, essentially small strengthening of a variant of a circle of abelian reconstruction theorems including the Gabriel-Popescu theorem(probably our variant could be read off from classical algera book by Faith for example, or Popescu's book on abelian categories, in any case it is well known in [[noncommutative algebraic geometry]]). In fact for this fact, if I think better, the reconstruction belongs usually to expositions which treat classical Morita theory for rings. 
=--

A triangulated category is __compactly generated__ if it is generated (see [[generator]]) by a _set_ of compact objects.

The notion can be modified for categories [[enriched category|enriched]] over a [[closed monoidal category]] (compare to the notions of finite and/or rigid objects in various contexts).

Compact objects in the derived categories of quasicoherent sheaves over a scheme are called [[perfect complexes]]. Any [[compact object]] in the [[category of modules]] over a perfect ring is finitely generated as a module.  


In non-additive contexts, the above definition is not right.  For instance, with this definition a [[topological space]] would be compact iff it is [[connected space|connected]].  In general one should expect to instead preserve filtered colimits, as above.


### Compact objects in $Top$
 {#CompactObjectsInTop}

Recall the above example of [[compact space|compact topological spaces]].  Notice that the statement which one might expect, that a [[topological space]] $X$ is [[compact space|compact]] if it is a compact object in [[Top]], is not quite right in general.

A [[counterexample]] is given for instance in [Hovey (1999), page 49](#Hovey99), which itself was corrected by Don Stanley (see the [errata](http://hopf.math.purdue.edu/Hovey/model-err.pdf) of that book). See also the blog discussion 
[here](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html#c023790).

Namely, the two-element set with the [[indiscrete topology]] is a compact space $X$ for which 
 \[
 Hom(X, -)  
  M\colon 
  Top \rightarrow Top
\]
doesn't preserve filtered colimits, in fact not even [[sequential colimit|colimits of sequences]] (functors out of the [[poset|ordered set]] of [[natural numbers]]). 

For example, consider the sequence of spaces 
 \[
 X_n=[n,\infty) \times \{0,1\}
\]
where the [[open sets]] are of the form 
\[
 [n, \infty] \times \{0\} \cup [m,\infty) \times \{1\}
\]
(where $m \geq n$), plus the empty set. Define $X_n \rightarrow X_{n+1}$ so that it sends a pair $(k, \epsilon)$ to itself if $k \gt n$, and $(n,\epsilon)$ to $(n+1,\epsilon)$. This defines a functor 
\[
F: \mathbb{N} \rightarrow Top 
\]
The colimit $X_\infty$ of this sequence is the two-element set $\{0,1\}$ with the indiscrete topology. However, the identity map on this space does not factor through any of the canonical maps $X_n \rightarrow X_\infty$. It follows that 
the comparison map 
\[
 \underset{n}{colim}\ Hom(X_\infty, X_n) \rightarrow Hom(X_\infty, X_\infty)
\]
is not surjective, and therefore not an isomorphism. 

+--{.query}
_[[Todd Trimble|Todd]]_ (posted from n-category cafe): I don't know if the story is any different for $X$ compact _Hausdorff_, but it could be worth considering. 
=--

But with a bit of care on the assumptions, similar results do hold:

\begin{proposition} {#CompactSpace} 
If $Y \in Top$ is a [[compact topological space]], then 
$hom(Y,-)$ preserves colimits of functors mapping out of [[limit ordinals]], provided that the arrows of the cocone diagram, 
 \[
 X_\alpha \rightarrow X_\beta,
\]
are [[closed map|closed]] inclusions of [[separation axiom|$T_1$-spaces]], and $X_\beta$ is the colimit of earlier $X_\alpha$ if $\beta$ is itself a limit ordinal. 
\end{proposition} 

This applies for example to the sequence of inclusions of $n$-skeleta in a [[CW-complex]]. By considering the cases $Y=S^k$ and $Y = S^k \times I$, this implies that the functor $\pi_k$ also preserves colimits of such sequences. Applications also occur in the theory of [[classifying space|classifying bundles]]. For example, the total space $EO(n)$ of the [[orthogonal group|$O(n)$]]-[[universal principal bundle]] can be constructed as the colimit $\underset{k \to \infty}{colim} \; V_n(\mathbb{R}^{n+k})$ of [[Stiefel manifolds]] of orthonormal $n$-frames in $\mathbb{R}^{n+k}$. To show $EO(n)$ is weakly contractible, it suffices, by this result, to show that for each $j$, the [[homotopy group]] $\pi_j(V_n(\mathbb{R}^{n+k}))$ vanishes for sufficiently large $k$. 

\begin{proof} 
Let $X$ denote the colimit of the diagram mapping out of the limit ordinal $\kappa$. We must show that every map $f \colon Y \to X$ factors through one of the universal cocone components $i_\alpha \colon X_\alpha \to X$, where $\alpha \lt \kappa$. Suppose not. Starting from any $\alpha \lt \kappa$, pick a point $x_0 \in f(Y)$ not in the image $i_\alpha(X_\alpha)$. There is a minimal $\alpha_1 \lt \kappa$ such that $x_0 \in i_{\alpha_1}(X_{\alpha_1})$. Proceeding inductively, choose $x_n \in f(Y)$ such that $x_n \notin i_{\alpha_n}(X_{\alpha_n})$, and let $\alpha_{n+1}$ be the minimal ordinal such that $x_n \in i_{\alpha_{n+1}}(X_{\alpha_{n+1}})$. Then let $\beta$ be the limit of the $\alpha_n$, and let $S$ be the set $\{x_n: n \in \mathbb{N}\}$, so that $S \subseteq i_\beta(X_\beta)$. Any subset $K$ of $S$ is closed, because closure of $K \subseteq i_\beta(X_\beta)$ is equivalent to closure of of each $K \cap i_{\alpha_n}(X_{\alpha_n})$ (since that is how the colimit topology on $X_\beta$ is defined), and all these intersections are finite and therefore closed by the $T_1$ condition. It follows that $f^{-1}(S)$ is an infinite discrete subspace of $Y$, but this contradicts compactness. 
\end{proof} 

This proof is essentially that given in [Hovey (1999), page 50](#Hovey99), where this result is needed towards the [[small object argument]] on the way to establishing the [[classical model structure on topological spaces]], see [this lemma](classical+model+structure+on+topological+spaces#CompactSubsetsAreSmallInCellComplexes).

## Related concepts

* [[compact element]] (in a [[(0,1)-category]])

* [[compact projective object]]

* [[compact topos]]

* [[compact object in an (∞,1)-category]]

* [[small object]], [[small object argument]]

* [[finitely generated object]]

* [[locally presentable category]], [[accessible category]]

* [[compactly generated (∞,1)-category]]

[[!include finite objects -- table]]


## References {#references}

Compact objects are discussed under the term "finitely presentable" or "finitely-presentable" objects for instance in

* {#AdamekRosicky94} [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally Presentable and Accessible Categories]]_, Cambridge University Press in the London Mathematical Society Lecture Note Series, number 189, (1994)

* {#MakkaiPare89} [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989.

*  [[Masaki Kashiwara]], [[Pierre Schapira]], around Definition 6.3.3 of _[[Categories and Sheaves]]_;

* [[Peter Johnstone]], _[[Stone Spaces]]_, Definition VI.1.8;

* [[Peter Johnstone]], the _[[Elephant]]_, D2.3.1.

For the pages quoted in the context of the discussion of compact objects in [[Top]] see

* {#Hovey99} [[Mark Hovey]], _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999).  [ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s) [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063) [pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), (errata: [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats-errata.pdf))
.

For the general definition with an eye towards the definition of [[compact object in an (infinity,1)-category]]  see section A.1.1 section 5.3.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_



[[!redirects compact object]]
[[!redirects compact objects]]

[[!redirects finitely presentable object]]
[[!redirects finitely presentable objects]]

[[!redirects finitely-presentable object]]
[[!redirects finitely-presentable objects]]

[[!redirects presentable object]]
[[!redirects presentable objects]]