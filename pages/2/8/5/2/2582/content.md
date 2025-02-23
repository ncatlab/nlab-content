
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _Whitehead tower_ of a [[pointed object|pointed]] [[homotopy type]] $X$ is an interpolation of the point inclusion $* \to X$ by a sequence of homotopy types

$$
  * \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} 
  \simeq X
$$

that are obtained from right to left by _removing [[homotopy groups]] from below_, hence such that 

* each $X^{(n)}$ is $(n-1)$-[[n-simply connected space|connected]] 

* and each [[morphism]] $X^{(n+1)} \to X^{(n)}$ induces an [[isomorphism]] on all [[homotopy groups]] in degree $k \geq (n+1)$ (and the inclusion $1 \to \pi_n(X^{(n)})$ in degree $n$ as well as the identity $1 = 1$ in degree $k \lt n$).

The notion of Whitehead tower is [[duality|dual]] to the notion of _[[Postnikov tower]]_, which instead is a factorization of the terminal morphism $X \to *$ into a tower, where homotopy groups are _added_ from right to left.

In fact, the Whitehead tower may be constructed by taking each stage $X^{(n+1)} \to X$ to be the _[[homotopy fiber]]_ of the corresponding map into the $(n+1)$st stage of the [[Postnikov tower]].


## Definition

The construction of Whitehead towers is traditionally done for [[topological spaces]] regarded up to [[weak homotopy equivalence]], hence as objects of the [[(∞,1)-category]] [[Top]]. The discussion directly generalizes to any [[(∞,1)-topos]].

The **Whitehead tower** of a [[pointed object|pointed]] [[homotopy type]] $X$ is a sequence of [[homotopy types]]

$$* \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X$$

where [[generalized the|the]] space $X^{(n)}$ is [[generalized the|the]] [[homotopy fiber]] of [[generalized the|the]] map $X \to X_{(n+1)}$ into the item $X_{(n+1)}$ in the [[Postnikov tower]] of $X$.

Here each [[homotopy pullback]]

$$
  \array{
    X^{(n)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& X_{(n+1)}
  }
$$

in the [[(∞,1)-category]] [[Top]] may be computed (as described at [[homotopy pullback]]) as an ordinary [[pullback]] in the 1-[[category]] [[Top]] of a fibrantly replaced diagram, for instance with the point $*$ replaced by the path fibration $P X_{(n+1)} \simeq *$, which is a [[Hurewicz fibration]] $P X_{(n+1)} \to X_{(n+1)}$. In this case also the ordinary [[pullback]] $X^{(n)}\to X$
  
$$
  \array{
    X^{(n)} &\to& P X_{(n+1)}
    \\
    \downarrow && \downarrow
    \\
    X &\to& X_{(n+1)}
  }
$$

is a fibration, and this is often taken as part of the definition of the Whitehead tower.

From this perspective the _Whitehead tower_ of a [[pointed space]] $(X,x)$ is a sequence of fibrations 

$$
\ldots \to X\langle n\rangle \to \ldots \to X\langle 1 \rangle \to X\langle 0 \rangle \to X
$$

where each $X\langle n\rangle \to X\langle n-1 \rangle$ induces isomorphisms on [[homotopy group]]s $\pi_i$ for $i\gt n$ and such that $X\langle n\rangle$ is $n$-[[n-connected|connected]] (has trivial [[homotopy group]]s $\pi_i$ for $i \leq n$).
The homotopy long exact sequence then shows that the fiber of $X\langle n\rangle \to X\langle n-1 \rangle$ is a $K(\pi_{n-1}(X,x),n-1)$ [[Eilenberg-Mac Lane space]]. One has a model for $K(\pi_{n-1}(X,x),n-1)$ which is an abelian topological group; this has a remarkable consequence when $(X,x)=(G,e)$ is a [[topological group]]. Indeed, in this case one sees inductively that $G\langle n\rangle$ has a model which is a topological group, which is an abelian group extension:

$$
1\to K(\pi_{n-1}(X,x),n-1) \to G\langle n\rangle \to G\langle n-1 \rangle \to 1
$$

For instance, the [[string group]] can be realized as a topological group as a $K(\mathbb{Z},2)$-extension of the [[spin group]].


For $n=0$ we require that $X\langle 0 \rangle \hookrightarrow X$ is the inclusion of the path-component of $x$. Really this is defined up to [[homotopy (as an operation)|homotopy]], but we have a canonical model. If $X$ is locally connected and semilocally path-connected, then $X\langle 1\rangle$ can be chosen as the [[universal covering space]]. 

In traditional models this construction is highly non-[[functor]]ial, except for nice spaces in low dimensions as remarked above. 


## Constructions 

### Whitehead's construction 

[Whitehead 1952](#Whitehead) answered the question, posed by [[Witold Hurewicz]], of the existence of what we would now call $n$-connected \'covers\' of a given space $X$, taking this to mean a fibration $X\langle n\rangle \to X$ with $X\langle n\rangle$ $n$-connected and otherwise inducing isomorphisms on homotopy groups. 

The construction proceeds as follows (using modern terminology). Given a pointed space $(X,x)$,

* Choose a representative for the [[Postnikov section]] $X_n$ such that $X \hookrightarrow X_n$ is a closed subspace (I would be tempted to make it a closed cofibration, but I don't know any reason for this to be necessary -DMR).

* Form the $\infty$-connected cover of $X_n$, i.e. the [[path fibration]] $P X_n$. This is a [[Hurewicz fibration]].

* Pull this back to $X$, to get $p\colon X\langle n\rangle \to X$, which is still a fibration. The induced maps on long exact sequences in homotopy can be compared, and show that $p$ has the desired properties. 

This gives us a single $n$-connected cover, but by considering the [[Postnikov tower]]
$$
X \to (\ldots \to X_n \to X_{n-1} \to \ldots \to X_1 \to X_0)
$$
of $X$, where each map $X \to X_n$ is the inclusion of a closed subspace, it is simple to see there are induced maps $X\langle n\rangle \to X\langle n-1\rangle$ over $X$ for all $n$.

One way of obtaining a Postnikov section as above is to choose representatives $\phi_g\colon S^{n+1} \to X$ of generators $g$ of $\pi_{n+1}(X,x)$ and attaching cells: $X(1)\coloneqq B^{n+2} \cup_{\{\phi_g\}} X$. We then choose representatives for the generators of $\pi_{n+2}(X(1),x)$ and attach cells and so on. The colimit $\lim_{\to n} X(n)$ is then a Postnikov section with the properties we require.

Understandably, this process is unbelievably non-canonical, and so we are generally reduced to existence theorems using this method -- unless there is a functorial way to construct Postnikov sections. Strictly speaking we can only say _an_ $n$-connected cover (except in special cases, like when $n=1$ and $X$ is a [[well-connected space]]).


### Functorial constructions 

The $n$th stage of the Whitehead tower of $X$ is the [[homotopy fiber]] of the map from $X$ to the $n$th (or so) stage of its [[Postnikov tower]], so one can use a functorial construction of the Postnikov tower plus a functorial construction of the homotopy fiber (such as the usual one using the [[path object|path space]] of the target).

The $n$th stage of the Whitehead tower of $X$ is also the cofibrant replacement for $X$ in the right [[Bousfield localization]] of [[Top]] with respect to the object $S^n$ (or so). Since [[Top]] is right proper and cellular this localization exists by the result of chapter 5 of Hirschhorn's book on [[localization]]s of [[model category|model categories]]. 

Another straightforward construction was mentioned by [Clausen 2010](#Clausen10): $ \ldots \to B^{3} \Omega^{3} (X) \to B^{2} \Omega^{2} (X) \to B \Omega (X) \to X$



## Examples 

### Whitehead tower of the orthogonal group 
 {#OfTheOrthogonalGroup}

The Whitehead tower of the [[classifying space]]/[[delooping]] of the [[orthogonal group]] $O(n)$ starts out as

$$
  \array{
    & \mathbf{\text{Whitehead tower}}
    \\
    &\vdots
    \\
    & B Fivebrane &\to& \cdots &\to& *
    \\
    & \downarrow && && \downarrow
    \\
    \mathbf{\text{second frac Pontr. class}} & B String &\to& \cdots &\stackrel{\tfrac{1}{6}p_2}{\to}&  B^8 \mathbb{Z}
    &\to& * 
    \\
    & \downarrow && && \downarrow && \downarrow
    \\
    \mathbf{\text{first frac Pontr. class}} & B Spin && && &\stackrel{\tfrac{1}{2}p_1}{\to}& B^4 \mathbb{Z} &\to & * 
    \\
    & \downarrow && && \downarrow && \downarrow && \downarrow
    \\
    \mathbf{\text{second SW class}} & B S O 
    &\to&
    \cdots
    &\to&
    &\to&
    & \stackrel{w_2}{\to} &
    \mathbf{B}^2 \mathbb{Z}_2
    &\to&
    *
    \\
    & \downarrow && && \downarrow && \downarrow &&  \downarrow && \downarrow
    \\
    \mathbf{\text{first SW class}} & B O 
    &\to&
    \cdots
    &\to&
    \tau_{\leq 8 } B O
    &\to&
    \tau_{\leq 4 } B O
    &\to&
    \tau_{\leq 2 } B O
    &\stackrel{w_1}{\to}&
    \tau_{\leq 1 } B O
    \simeq
    B \mathbb{Z}_2
    &
    \mathbf{\text{Postnikov tower}}
  }
$$

where each square and each composite rectangle is a [[homotopy pullback]] square (all controled by the [[pasting law]]),

where the stages are the deloopings of

...
$\to$
[[fivebrane group]]
$\to$
[[string group]]
$\to$
[[spin group]]
$\to$
[[special orthogonal group]]
$\to$
[[orthogonal group]],

where lifts through the stages correspond to 

* [[orthogonal structure]]

* [[orientation]]

* [[spin structure]]

* [[string structure]]

* [[fivebrane structure]]

and where the [[obstruction]] classes are the [[universal characteristic classes]]

* [[first Stiefel-Whitney class]] $w_1$

* [[second Stiefel-Whitney class]] $w_2$

* [[Pontryagin class|first fractional Pontryagin class]] $\tfrac{1}{2}p_1$

* [[Pontryagin class|second fractional Pontryagin class]] $\tfrac{1}{6}p_2$

and where every possible square in the above is a [[homotopy pullback]] square (using the [[pasting law]]).

For instance $w_2$ can be identified as such by representing $B O \to \tau_{\leq 2} B O \simeq BO/_{\sim_n}$ by a [[Kan fibration]] (see at [[Postnikov tower]]) between [[Kan complexes]] so that then the [[homotopy pullback]] (as discussed there) is given by an ordinary pullback. Since $sSet$ is a [[simplicial model category]], $sSet(S^2,-)$ can be applied and preserves the pullback as well as the homotopy pullback, hence sends $ B O \to \tau_{\leq 2} B O$ to an isomorphism on connected components. This identifies  $B SO \to B^2 \mathbb{Z}$ as being an [[isomorphism]] on the second [[homotopy group]]. Therefore, by the [[Hurewicz theorem]], it is also an isomorphism on the [[cohomology group]] $H^2(-,\mathbb{Z}_2)$. Analogously for the other characteristic maps.

In summary, more concisely, the tower is

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    B Fivebrane
    \\
    \downarrow
    \\
    B String &\stackrel{\tfrac{1}{6}p_2}{\to}& B^7 U(1) & \simeq B^8 \mathbb{Z}
    \\
    \downarrow
    \\
    B Spin &\stackrel{\tfrac{1}{2}p_1}{\to}& B^3 U(1) & \simeq B^4 \mathbb{Z}
    \\
    \downarrow
    \\
    B SO &\stackrel{w_2}{\to}& B^2 \mathbb{Z}_2
    \\
    \downarrow
    \\
    B O &\stackrel{w_1}{\to}& B \mathbb{Z}_2
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    B GL
  }
  \,,
$$

where each "hook" is a [[fiber sequence]].

Via the [[J-homomorphism]] this corresponds to the [[stable homotopy groups of spheres]]:

[[!include image of J -- table]]

## Whitehead tower in general $(\infty,1)$-toposes

While a notion of [[Postnikov tower in an (∞,1)-category]] depends on the _categorical_ [[homotopy groups in an (∞,1)-topos|homotopy groups in an (∞,1)-category]], the notion of Whitehead tower makes good sense with respect to the _geometric_ homotopy groups. 

A good notion of geometric [[homotopy groups in an (∞,1)-topos]] exist in a [[locally contractible (∞,1)-topos]]. The notion of Whitehead tower in this context is discussed at 

* [[Whitehead tower in an (∞,1)-topos]].

## Related concepts

* Applying the [[Hurewicz theorem]] stagewise to a [[Whitehead tower]] yields an method for computing the [[homotopy groups]] of the original [[space]]. This process, or rather the refinement thereof for Whitehead towers generalized to [[Adams resolutions]], is formalized by the _[[Adams spectral sequence]]_, see there for more.

* _[symmetric group -- Whitehead tower](https://ncatlab.org/nlab/show/permutation#WhietheadTowerAndSupersymmetry)_

[[!include Lurie spectral sequences -- table]]

## References 

The original reference is 

*  [[George Whitehead]], _Fiber Spaces and the Eilenberg Homology Groups_, PNAS **38**, No. 5 (1952)
 {#Whitehead}

A textbook account is around example 4.20 in

* {#Hatcher02} [[Allen Hatcher]], *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

A more detailed useful discussion happens to be in section 2.A, starting on p. 11 of 

* [[Linus Kramer]], _Homogeneous Spaces, Tits Buildings, and Isoparametric Hypersurface_,  Memoirs of the American Mathematical Society number 752 ([arXiv:math/0109133] (http://arxiv.org/abs/math/0109133), [doi:10.1090/memo/0752](http://dx.doi.org/10.1090/memo/0752), [GoogleBooks](http://books.google.com/books?id=SA8O6ihrDFkC&printsec=frontcover&hl=de&source=gbs_v2_summary_r&cad=0#v=onepage&q=&f=false))

Related Discussions

* {#Clausen10} [[Dustin Clausen]] (2010) &lbrack;[MO:a/27970](https://mathoverflow.net/a/27970/124549)&rbrack;

[[!redirects Whitehead tower]]
[[!redirects Whitehead towers]]
