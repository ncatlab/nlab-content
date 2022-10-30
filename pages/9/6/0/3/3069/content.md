
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

The **Beck--Chevalley condition**, also sometimes called just the *Beck condition* or the *Chevalley condition*, is a "commutation of [[adjoint functor|adjoint]]s" property that holds in many "[[base change|change of base]]" situations.


## Definition

Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functor]]s:
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

Of course, if $g^*$ and $k^*$ also have [[left adjoint]]s, there is also a Beck--Chevalley condition stating that the corresponding mate $k_! h^* \to f^* g_!$ is an isomorphism, and this is not equivalent in general.  Context is usually sufficient to disambiguate, although some people speak of the "left" and "right" Beck--Chevalley conditions.

Note that if $k^* f^* \to h^* g^*$ is not an isomorphism, then there is only one possible Beck-Chevalley condition.


### Dual Beck--Chevalley condition

If $f^*$ and $h^*$ have *right* adjoints $f_*$ and $h_*$, there is also a dual Beck--Chevalley condition saying that the mate $g^* f_* \to h_* k^*$ is an isomorphism.  By general nonsense, if $f^*$ and $h^*$ have right adjoints and $g^*$ and $k^*$ have left adjoints, then $g^* f_* \to h_* k^*$ is an isomorphism if and only if $k_! h^* \to f^* g_!$ is.

### "Local" Beck--Chevalley condition {#Local}

Suppose that $f^*$ and $h^*$ do not have entire left adjoints, but that for a particular object $x$ the left adjoint $f_!(x)$ exists.  This means that we have an object "$f_! x$" and a morphism $\eta_x\colon x \to f^* f_! x$ which is initial in the [[comma category]] $(x / f^*)$.  Then we have $k^*(\eta) \colon k^* x \to k^* f^* f_! x \to h^* g^* f_! x$, and we say that the square satisfies the *local Beck-Chevalley condition at $x$* if $k^*(\eta)$ is initial in the comma category $(k^* x / h^*)$, and hence exhibits $g^* f_! x$ as "$h_! k^* x$" (although we have not asumed that the entire functor $h_!$ exists).

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

### Pullbacks of opfibrations
 {#PullbacksOfOpfibrations}

+-- {: .num_prop}
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

is a [[pullback]] diagram (in the _1-category_ [[Cat]]), then the induced diagram of [[presheaf categories]]

$$
  \array{
    [D', \mathcal{C}] &\stackrel{\beta^*}{\leftarrow}& [D, \mathcal{C}]
    \\
    \uparrow^{\mathrlap{\psi}^*} && \uparrow^{\mathrlap{\phi}^*}
    \\
    [C', \mathcal{C}] &\stackrel{\alpha^*}{\leftarrow}& [C,\mathcal{C}]
  }
  \,,
$$

for $\mathcal{C}$ a category with all small colimits,
satisfies the Beck-Chevalley condition: for $\psi_!$ and $\phi_!$ denoting the left [[Kan extension]] along $\psi$ and $\phi$, respectively, we have a [[natural isomorphism]]

$$
  \psi_! \beta^* \simeq \alpha^* \phi_!
  \,.
$$

=--

This is sometimes called the _projection formula_. 

+-- {: .proof}
###### Proof

Since $\phi$ is [[opfibration|opfibered]], for every object $c \in C$ the embedding of the [[fiber]] $\phi^{-1}(c)$ into the [[comma category]] $\phi/c$ is a [[final functor]]. Therefore the pointwise formula for the left [[Kan extension]] $\phi_!$ is equivalently given by taking the colimit over the fiber, instead of the comma category

$$
  \phi_1(X)_c \simeq \lim_{\underset{\phi^{-1}(c)}{\to}} X
  \,.
$$

Therefore we have a sequence of [[isomorphisms]]

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


### Bifibrations

Originally, the Beck-Chevalley condition was introduced in ([B&#233;nabou-Roubaud, 1970](#BenabouRoubaud)) for [[bifibrations]] over a base category with pullbacks. In *loc.cit.* they call this condition **Chevalley condition** because he introduced it in his 1964 seminar. 

#### Definition

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

#### Examples

* The [[codomain fibration]] of any [[category]] with [[pullbacks]] is a bifibration, and satisfies the Beck--Chevalley condition at every pullback square.

* If $C$ is a [[regular category]] (such as a [[topos]]), the bifibration $Sub(C) \to C$ of [[subobjects]] satisfies the Beck--Chevalley condition at every pullback square.

* The [[family fibration]] $Fam(C)\to Set$ of any category $C$ with small sums satisfies the Beck--Chevalley condition at every pullback square in $Set$.

### Proper base change in &#233;tale cohomology

For [[coefficients]] of [[torsion group]], [[étale cohomology]]
satisfies Beck-Chevalley along [[proper morphisms]]. This is the statement of the  _[[proper base change theorem]]_. See there for more details.

### Grothendieck six operations

A kind of Beck-Chevalley condition appears in the axioms of Grothendieck's [[six operations]]. See there for more.

## Related pages

* [[Benabou-Roubaud theorem]]

## References

* [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98, ([link](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), Biblioth&#232;que nationale de France)
 {#BenabouRoubaud}


A textbook reference is for instance section IV.9 (page 205) of

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

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