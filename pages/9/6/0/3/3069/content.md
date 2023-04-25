
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The **[[Jon Beck|Beck]]--[[Claude Chevalley|Chevalley]] condition**, also sometimes called just the *Beck condition* or the *Chevalley condition*, is a "commutation of [[adjoint functor|adjoint]]s" property that holds in many "[[base change|change of base]]" situations.

## Motivation

The Beck-Chevalley condition may be understood as a natural compatibility  condition for

**[(1)](#MotivationFromIntegralTransforms)** [[integral transforms]] in [[geometry]]

**[(2)](#MotivationFromLogicAndTypeTheory)** [[quantifiers]] in [[formal logic]]/[[type theory]]

### From integral transforms
 {#MotivationFromIntegralTransforms}

From the point of view of [[geometry]], in contexts such as of [[integral transforms]] one considers [[correspondences]] between [[spaces]] $A$, $B$ given by [[spans]] of [[maps]] between them:

\begin{tikzcd}[sep=20]
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  \\
  A && B
\end{tikzcd}


Via [[composition]] of such correspondences by [[fiber product]] of adjacent legs, they form the [[1-morphisms]] in a [[2-category]] *[[Span]]*.

Assuming some [[base change]] [[adjoint pair]] $f^\ast \vdash f_\ast$, thought of as

* *push-forward* $f_\ast \,\colon\, \mathcal{D}(X) \longrightarrow \mathcal{D}(A)$

and

* *pull-back* $f^\ast \,\colon\, \mathcal{D}(A) \longrightarrow \mathcal{D}(X)$

is [[functor|functorially]] associated with [[maps]] $f$ (i.e. such that there are [[natural isomorphisms]] $(f_2 f_1)_\ast \,\simeq\, (f_2)_\ast (f_1)_\ast$ and dually), the [[integral transform]] encoded by any span as above is the "pull-push" operation given by $g_* f^*$. 

Now the Beck-Chevalley condition (on such assignment of [[base change]] adjoints to maps) essentially says that this pull-push construction is ([[2-functor|2-]])[[functor|functorial]] under [[composition]] of [[spans]]:

Concretely, given a pair of composable spans:

\begin{tikzcd}[sep=20]
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \ar[dr, "k"]
  \\
  A && B && C
\end{tikzcd}

and their composite in [[Span]] formed by the [[fiber product]] of the adjacent legs

\begin{tikzcd}[sep=20]
  &&
  X \times_B Y
  \ar[dl, "q"{swap}]
  \ar[dr, "p"]
  \ar[dd, phantom, "{\lrcorner}"{rotate=-45, pos=.3}]
  \\
  & 
  X
  \ar[dl, "f"{swap}]
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \ar[dr, "k"]
  \\
  A && B && C
\end{tikzcd}

then functoriality of pull-push means that the
 *two* different ways to pull-push through the diagram coincide:

Pull-pushing through the spans separately results in

$$
  (k_\ast h^\ast)
  \circ
  (g_\ast f^\ast)
  \;=\;
  k_\ast 
  \,
  \underbrace{h^\ast \, g_\ast}
  \,
  f^\ast
  \,,
$$

while pull-pushing through the composite span results in

$$
  (k p)_* (f q)^* 
  = 
  k_* 
  \,
  \underbrace{p_* \, q^*}
  \,
  f^*
  \,.
$$

For these two operations to coincide, up to [[isomorphism]], hence for pull-push to respect composition of spans, we need an isomorphism between the operations shown over braces, hence of the form

\[
  \label{BCConditionInMotivationFromIntegralTransform}
  h^\ast \, g_\ast
  \;\simeq\;
  p_* \, q^*
\]

between the two ways of  push-pulling along the sides of any [[pullback square]]

\begin{tikzcd}[sep=20]
  &
  X \times_B Y
  \ar[dl, "q"{swap}]
  \ar[dr, "p"]
  \ar[dd, phantom, "{\lrcorner}"{rotate=-45, pos=.3}]
  \\
  X
  \ar[dr, "g"]
  &&
  Y
  \ar[dl, "h"{swap}]
  \\
  & B &
\end{tikzcd}

This (eq:BCConditionInMotivationFromIntegralTransform) is the Beck-Chevalley condition:  A natural necessary condition to ensure that [[integral transforms]] by pull-push [[base change]] through [[correspondences]] is functorial under [[composition]] of [[correspondences]] by [[fiber product]] of adjacent legs.

More motivation along these lines also be found at *[[dependent linear type theory]]*. As a formulation of propagation in cohomological [[quantum field theory]] this is [Sc14](dependent+linear+type+theory#Schreiber14) there.


### From logic and type theory
 {#MotivationFromLogicAndTypeTheory}

From the point of view of [[formal logic]] and [[dependent type theory]], the three items $f_! \dashv f^\ast \vdash f_\ast$ in a [[base change]] [[adjoint triple]] constitute the [[categorical semantics]] of [[quantification]] and [[context extension]] ([[existential quantification]]/[[dependent pair type]] $\dashv$ [[context extension]] $\dashv$ [[universal quantification]]/[[dependent product type]]), and so the Beck-Chevalley condition says that these are compatible with each other: concretely that [[substitution]] of [[free variables]] commutes with [[quantification]] --- a condition which [[syntax|syntactically]] is "self-evident", at least it is evidently desirable.

For more on this logical aspect see [below](#InTypeTheory).



## Definition

Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functors]]:
$$\array{ & \overset{f^*}{\to} & \\
  ^{g^*}\downarrow && \downarrow^{k^*}\\
  & \underset{h^*}{\to} & }$$
in which $f^*$ and $h^*$ have [[left adjoint]]s $f_!$ and $h_!$, respectively. (The classical example is a [[Wirthmüller context]].)  Then the [[natural isomorphism]] that makes the square commute 

$$
  k^* f^* \to h^* g^*
$$

has a [[mate]]

$$ 
  h_! k^* \to g^* f_! 
$$

defined as the composite

$$ 
  h_! k^* \overset{\eta}{\to} h_! k^* f^* f_! \overset{\cong}{\to} h_! h^* g^* f_! \overset{\epsilon}{\to} g^* f_!   
  \,.
$$

We say the original square satisfies the **Beck--Chevalley condition** if this mate is an [[isomorphism]].

More generally, it is clear that for this to make sense, we only need a transformation $k^* f^* \to h^* g^*$; it doesn't need to be an isomorphism.  We also use the term *Beck--Chevalley condition* in this case,



### Left and right Beck--Chevalley condition

Of course, if $g^*$ and $k^*$ also have [[left adjoints]], there is also a Beck--Chevalley condition stating that the corresponding mate $k_! h^* \to f^* g_!$ is an isomorphism, and this is not equivalent in general.  Context is usually sufficient to disambiguate, although some people speak of the "left" and "right" Beck--Chevalley conditions.

Note that if $k^* f^* \to h^* g^*$ is not an isomorphism, then there is only one possible Beck-Chevalley condition.




### Dual Beck--Chevalley condition

If $f^*$ and $h^*$ have *right* adjoints $f_*$ and $h_*$, there is also a dual Beck--Chevalley condition saying that the mate $g^* f_* \to h_* k^*$ is an isomorphism.  By adjointness, if $f^*$ and $h^*$ have right adjoints and $g^*$ and $k^*$ have left adjoints, then $g^* f_* \to h_* k^*$ is an isomorphism if and only if $k_! h^* \to f^* g_!$ is.

### For bifibrations

Originally, the Beck-Chevalley condition was introduced in ([B&#233;nabou-Roubaud, 1970](#BenabouRoubaud70)) for [[bifibrations]] over a base category with pullbacks. In *loc.cit.* they call this condition **Chevalley condition** because he introduced it in his 1964 seminar. 


A [[bifibration]] $\mathbf{X} \to \mathbf{B}$ where $\mathbf{B}$ has pullbacks satisfies the **Chevalley condition** iff for every commuting square
$$\array{ & \overset{\psi^\prime}{\rightarrow} & \\
  \downarrow^{\varphi^\prime} && \downarrow^{\varphi}\\
  & \underset{\psi}{\rightarrow} & }$$
in $\mathbf{X}$ over a pullback square in the base $\mathbf{B}$ where $\varphi$ is [[cartesian morphism|cartesian]] and $\psi$ is cocartesian it holds that $\varphi^\prime$ is cartesian
iff $\psi^\prime$ is cocartesian. Actually, it suffices
to postulate one direction because the other one follows.
The nice thing about this formulation is that there is no
mention of "canonical" morphisms and no mention of [[cleavages]]. 

A fibration $P$ has products satisfying the Chevalley condition iff the opposite fibration $P^{op}$ is 
a bifibration satisfying the Chevalley condition in the above sense.

According to the [[Benabou–Roubaud theorem]], the Chevalley condition  is crucial for establishing the connection between the descent in the sense of fibered categories and the [[monadic descent]].



### "Local" Beck--Chevalley condition {#Local}

Suppose that $f^*$ and $h^*$ do not have entire left adjoints, but that for a particular object $x$ the left adjoint $f_!(x)$ exists.  This means that we have an object "$f_! x$" and a morphism $\eta_x\colon x \to f^* f_! x$ which is initial in the [[comma category]] $(x / f^*)$.  Then we have $k^*(\eta) \colon k^* x \to k^* f^* f_! x \to h^* g^* f_! x$, and we say that the square satisfies the *local Beck-Chevalley condition at $x$* if $k^*(\eta)$ is initial in the comma category $(k^* x / h^*)$, and hence exhibits $g^* f_! x$ as "$h_! k^* x$" (although we have not assumed that the entire functor $h_!$ exists).

If the functors $f_!$ and $h_!$ do exist, then the square satisfies the (global) Beck-Chevalley condition as defined above if and only if it satisfies the local one defined here at every object.

## In logic / type theory
 {#InTypeTheory}

If the functors in the formulation of the Beck-Chevalley condition are [[base change]] functors in the [[categorical semantics]] of some [[dependent type theory]] (or just of a [[hyperdoctrine]]) then the BC condition is equivalently stated in terms of logic as follows. 

A [[commuting diagram]]  

$$
  \array{
    D &\stackrel{h}{\to}& C 
    \\
    {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    A &\stackrel{f}{\to}& B
  }
$$

is interpreted as a morphism of [[contexts]]. The [[pullback]] (of [[slice categories]] or of fibers in a [[hyperdoctrine]]) $h^*$ and $f^*$ is interpreted as the [[substitution]] of [[variables]] in these contexts. And the [[left adjoint]] $\sum_k \coloneqq k_! $ and $\sum_q \coloneqq g_!$, the [[dependent sum]] is interpreted (up to [[truncated|(-1)-truncation]], possibly) as [[existential quantifier|existential quantification]]. 

In terms of this the Beck-Chevalley condition says that if the above diagram is a [[pullback]], then **substitution commutes with existential quantification**

$$
  \sum_k h^* \phi \stackrel{\simeq}{\to} f^* \sum_g \phi
  \,.
$$

+-- {: .num_example}
###### Example

Consider the diagram of [[contexts]]

$$
  \array{
    [\Gamma, x : X] &\stackrel{}{\to}& [\Gamma, x : X, y : Y]
    \\
    \downarrow && \downarrow
    \\
    \Gamma &\to& [\Gamma, y : Y]
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{
    \Gamma \times X &\stackrel{(p_1,p_2,t)}{\to}& \Gamma \times X \times Y
    \\
    {}^{\mathllap{p_1}}\downarrow && \downarrow^{\mathrlap{(p_1,p_3)}}
    \\
    \Gamma &\stackrel{(id,t)}{\to} & \Gamma \times Y
  }
  \,,
$$

with the horizontal morphism coming from a [[term]] $t : \Gamma \to Y$ in [[context]] $\Gamma$ and the vertical morphisms being the evident [[projection]], then the condition says that we may in a [[proposition]] $\phi$ substitute $t$ for $y$ before or after quantifying over $x$:

$$
 \sum_{x : X} \phi(x,t) \simeq (\sum_{x : X} \phi(x,y))[t/y]
 \,.
$$

=--

## Examples

### Various

* The [[codomain fibration]] of any [[category]] with [[pullbacks]] is a bifibration, and satisfies the Beck--Chevalley condition at every pullback square. In particular, [[locally cartesian closed categories]] always satisfy the Beck--Chevalley condition.

* If $C$ is a [[regular category]] (such as a [[topos]]), the bifibration $Sub(C) \to C$ of [[subobjects]] satisfies the Beck--Chevalley condition at every pullback square.

* The [[family fibration]] $Fam(C)\to Set$ of any category $C$ with small sums satisfies the Beck--Chevalley condition at every pullback square in $Set$.

* [Mackey's restriction formula](double+coset#MackeyFormula) for group representations.


### For categories of presheaves
 {#PullbacksOfOpfibrations}

+-- {: .num_prop #BCForPresheavesOnPullbacksOfOpfibrations}
###### Proposition

If $\phi : D \to C$ is an [[opfibration]] of [[small categories]] and 

$$
  \array{
    D' &\stackrel{\beta}{\to}& D
    \\
    \downarrow^{\mathrlap{\psi}} && \downarrow^{\mathrlap{\phi}}
    \\
    C' &\stackrel{\alpha}{\to}& C
  }
$$

is a [[pullback]] diagram (in the _1-category_ [[Cat]]), and for $\mathcal{C}$ a [[category]] with all [[small colimits]], then the induced diagram of [[presheaf categories]]

$$
  \array{
    [D', \mathcal{C}] &\stackrel{\beta^*}{\longleftarrow}& [D, \mathcal{C}]
    \\
    \uparrow^{\mathrlap{\psi}^*} 
      && 
    \uparrow^{\mathrlap{\phi}^*}
    \\
    [C', \mathcal{C}] &\stackrel{\alpha^*}{\longleftarrow}& [C,\mathcal{C}]
  }
  \,,
$$

satisfies the Beck-Chevalley condition: for $\psi_!$ and $\phi_!$ denoting the left [[Kan extension]] along $\psi$ and $\phi$, respectively, then we have a [[natural isomorphism]]

$$
  \psi_! \beta^* \simeq \alpha^* \phi_!
  \,.
$$

=--

(This is maybe sometimes called the _projection formula_. But see at _[[projection formula]]_.)

For this statement in the more general context of [[quasicategories]] see [Joyal 2008, prop. 11.6](#Joyal08).


+-- {: .proof}
###### Proof

Since $\phi$ is [[opfibration|opfibered]], for every object $c \in C$ the embedding of the [[fiber]] $\phi^{-1}(c)$ into the [[comma category]] $\phi/c$ is a [[final functor]]. Therefore the pointwise formula for the left [[Kan extension]] $\phi_!$ is equivalently given by taking the colimit over the fiber, instead of the comma category

$$
  \phi_1(X)_c \simeq \lim_{\underset{\phi^{-1}(c)}{\to}} X
  \,,
$$

and so wwe have a sequence of [[isomorphisms]]

$$
  \begin{aligned}
    (\psi_! \beta^* X)(c')
    & \simeq
    \lim_{\underset{\psi^{-1}(c')}{\to}} (X\circ \beta)
    \\
    & \simeq 
    \lim_{\underset{\phi^{-1}(\alpha(c'))}{\to}} X
    \\
    & \simeq
    (\alpha^* \phi_! X)(c')
  \end{aligned}
$$

all of them [[natural isomorphism|natural]] in $c'$.

=--


For an example that prop. \ref{BCForPresheavesOnPullbacksOfOpfibrations} may fail without the condition that $D \to C$ is an opfibration:

Consider $C=$ the [[interval category]] $(0\to 1)$, $D=C'=$ the [[terminal category]], $\phi=0$, $\alpha=1$, so that $D'=\emptyset$, but $\alpha^*\phi_!$ is the identity functor.

### Proper base change in &#233;tale cohomology

For [[coefficients]] of [[torsion group]], [[étale cohomology]]
satisfies Beck-Chevalley along [[proper morphisms]]. This is the statement of the  _[[proper base change theorem]]_. See there for more details.

### Grothendieck six operations

A kind of Beck-Chevalley condition appears in the axioms of Grothendieck's [[six operations]]. See there for more.

## Related pages

* [[exact square]]
* [[Benabou-Roubaud theorem]]


## References
 {#References}

> The Beck-Chevalley condition has arisen in the theory of [[monadic descent|descent]] - as developed from [[Grothendieck]] 1959. [[Jon Beck]] and [[Claude Chevalley]] studied it independently from each another. &lbrack;...&rbrack; It is conspicuous that neither of them ever published anything on it. &lbrack;[Pavlović 1991, §14](#Pavlović91)&rbrack;

Original articles:

* {#BenabouRoubaud70} [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, Ser. A **270**  (1970) 96-98 &lbrack;[gallica:12148/bpt6k480298g/f100](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), [[BenabouRoubaud-MonadesEtDescente.pdf:file]],   English translation (by [[Peter Heinig]]): [MO:q/279152](https://mathoverflow.net/q/279152)&rbrack;

  > (proving the [[Bénabou-Roubaud theorem]])

* {#Lawvere70} [[William Lawvere]], p. 8 of: *[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]*, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970) 1-14 &lbrack;[pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf)&rbrack;

  > (in terms of [[base change]] as the [[categorical semantics]] for [[universal quantification]]/[[dependent product]] and [[existential quantification]]/[[dependent sum]])

Review:

* {#Pavlović91} [[Duško Pavlović]], Section 1 of: *Categorical interpolation: Descent and the Beck-Chevalley condition without direct images*, in: *Category Theory*, Lecture Notes in Mathematics **1488** (1991) &lbrack;[doi:10.1007/BFb0084229](https://doi.org/10.1007/BFb0084229), [pdf](http://www.isg.rhul.ac.uk/dusko/papers/1990-BCDE-Como.pdf)&rbrack;

* [[Paul Balmer]], around §7.5 of: *Stacks of group representations*, J. European Math. Soc. **17** 1 (2015) 189-228 &lbrack;[arXiv:1302.6290](https://arxiv.org/abs/1302.6290), [doi:10.4171/jems/501](https://doi.org/10.4171/jems/501)&rbrack;

and in the generality of [[(infinity,1)-categories|$\infty$-categories]]:

* [[Urs Schreiber]], around Def. 5.5 of: *[[schreiber:Quantization via Linear homotopy types]]* &lbrack;[arXiv:1402.7041](https://arxiv.org/abs/1402.7041)&rbrack;

* {#GaitsgoryLurie} [[Dennis Gaitsgory]], [[Jacob Lurie]], Section 2.4.1 of: _Weil's conjecture for function fields_ (2014-2017) &lbrack;["first volume of expanded account" pdf](https://www.math.ias.edu/~lurie/papers/tamagawa-abridged.pdf)&rbrack;


Discussion for [[subobject lattices]]:

* [[Saunders MacLane]], [[Ieke Moerdijk]], chapter IV.9 (around p. 205) of: _[[Sheaves in Geometry and Logic]]_,   Springer (1992) &lbrack;[doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0)&rbrack;

Discussion for presheaf categories in the context of [[quasicategories]] ([[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]]):

* {#Joyal08} [[André Joyal]], [p. 175](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=27) of: *[[The Theory of Quasi-Categories and its Applications]]*, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM (2008) &lbrack;[pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]]&rbrack;

Discussion for [[Goursat categories]]:

* [[Marino Gran]], [[Diana Rodelo]], *Beck-Chevalley condition and Goursat categories*, Journal of Pure and Applied Algebra **221** 10 (2017) 2445-2457 &lbrack;[arXiv:1512.04066](https://arxiv.org/abs/1512.04066), [doi:10.1016/j.jpaa.2016.12.031](https://doi.org/10.1016/j.jpaa.2016.12.031)&rbrack;


[[!redirects Beck-Chevalley conditions]]

[[!redirects Beck-Chevalley_Condition]]
[[!redirects Beck-Chevalley Condition]]
[[!redirects Beck–Chevalley condition]]
[[!redirects Beck--Chevalley condition]]
[[!redirects Beck condition]]
[[!redirects Chevalley condition]]
[[!redirects Beck-Chevalley property]]
[[!redirects Beck–Chevalley property]]
[[!redirects Beck--Chevalley property]]

[[!redirects Beck-Chevalley transformation]]
[[!redirects Beck-Chevalley transformations]]

[[!redirects Beck-Chevalley relation]]
[[!redirects Beck-Chevalley relations]]

[[!redirects Beck-Chevalley]]

