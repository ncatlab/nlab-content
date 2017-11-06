
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An [[(∞,1)-site]] is **locally $\infty$-connected** if it has properties that ensure that  the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[locally ∞-connected (∞,1)-topos]]


## Definition

+-- {: .num_defn}
###### Definition

Call an [[(∞,1)-site]] $C$ **locally contractible** if every constant [[(∞,1)-presheaf]] on it is an [[(∞,1)-sheaf]] in the [[(∞,1)-topos]] over $C$.

=--

More explicitly, this means that every covering sieve $R$ on an object $U\in C$, regarded as a subcategory of $C/U$, is weakly contractible, i.e. its nerve $N(R)$ (which is just itself, if it is incarnated as a [[quasicategory]]) is contractible in the [[Kan-Quillen model structure]] on simplicial sets.  For the sheaf condition for a constant presheaf on $X\in \infty Gpd$ is that the map $Const(X)(U) = X \to \lim_R Const(X)$ is an equivalence, but $\lim_R Const(X) = Map(N(R),X)$, and this is equivalent to $X$ for all $X$ if and only if $N(R)$ is contractible as an $\infty$-groupoid.


## Properties

+-- {: .num_defn}
###### Proposition

By the general notion of [[(∞,1)-colimit]] the constant $(\infty,1)$-presheaf functor has a left [[adjoint (∞,1)-functor]] given by taking colimits

$$
  Sh_{(\infty,1)}(C)
    \underoverset{\hookrightarrow}{\overset{L}{\longleftarrow}}{\bot}
  PSh_{(\infty,1)}(C)
    \stackrel{
       \overset{\lim_\to}{\longrightarrow}
    }
    {
       \underset{Const}{\leftarrow}
    }
  \infty Grpd
  \,.
$$

Since the [[(∞,1)-category of (∞,1)-sheaves]] sits by a [[full and faithful (∞,1)-functor]] inside presheaves and by assumption that every constant $(\infty,1)$-presheaf is an $(\infty,1)$-sheaf, this implies that we have also [[natural transformation|natural]] [[equivalence in an (∞,1)-category|equivalences]]

$$
  \begin{aligned}
     Sh(X, L Const S) 
       &\simeq 
     PSh(X, Const S)
     \\
       & \simeq  
     \infty Grpd(\lim_\to X , S)
  \end{aligned}
  \,.
$$

=--

## Examples

+-- {: .num_defn}
###### Proposition

Let $C$ be an 1-[[site]] such that every object $U$ has a [[split hypercover]] $Y \to U$ such that contracting all representables to points yields a weak equivalence. Equivalently, if the [[colimit]] functor $\lim_\to : [C^{op}, sSet] \to sSet$ sends this to a weak equivalence

$$
  \lim_\to Y \stackrel{\simeq}{\longrightarrow} \lim_\to U = *
  \,
$$

Then $C$ is locally $\infty$-connected.

=--

+-- {: .proof}
###### Proof

We may [[presentable (∞,1)-category|present]] $Sh_{(\infty,1)}(C)$ by the projective [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{proj}$ [[Bousfield localization of model categories|left Bousfield localized]] at the [[Cech nerve]] projections $C(\coprod_i U_i) \to U$ for each [[covering]] family $\{U_i \to U\}$ in $C$.

It is immediate that we have a [[Quillen adjunction]] $(\underset{\rightarrow}{\lim} \dashv const)$ for the [[global model structure on simplicial presheaves]] on both sides. Now by the [recognition theorem for simplicial Quillen adjunctions](http://ncatlab.org/nlab/show/simplicial+Quillen+adjunction#Recognition) for this to descend to a Quillen adjunction on the local model structure it is sufficient that the left adjoint preserves the cofibrations of the local model structure and (already) that the right adjoint preserves the fibration objects. Since left [[Bousfield localization of model categories]] does not change the cofibrations, the first of these is immediate. 

This means that to establish the claim it is now sufficient to show that constant simplicial presheaves already satisfy [[descent]] for a locally $\infty$-connected site. This is what we do now.


By the discussion of [[cofibrant resolution]] at [[model structure on simplicial presheaves]] we have that a [[split hypercover]] $Y \to U$ is a cofibrant [[resolution]] in $[C^{op}, sSet]_{proj, loc}$ of $U$. 

For $S \in sSet$ a [[Kan complex]] let $Const S : C^{op} \to sSet$ the corresponding constant simplicial presheaf. This is fibrant in $[C^{op}, sSet]_{proj}$. Since every split hypercover is cofibrant, it follows that $Const S$ is an $\infty$-sheaf precisely if for all $U \in C$ and some split hypercover $Y \to U$ we have that the morphism on [[derived hom-space]]s

$$
  [C^{op}, sSet](U, Const S) \to [C^{op}, sSet](Y, Const S)
$$

is a weak equivalence (of [[Kan complex]]es, necessatily). But we have 

$$
  [C^{op}, sSet](Y, Const S)
  \simeq
   sSet(\lim_\to Y, S)
$$

and 

$$
  [C^{op}, sSet](U, Const S) \simeq S
  \,,
$$

so that the condition is that 

$$
  S \to sSet(\lim_\to Y, S)
$$

is a weak equivalence. This is the case for all $S$ precisely if $\lim_\to S$ is [[contractible]], which is precisely our assumption on $Y$.

=--

+-- {: .num_prop}
###### Corollary

Let $X$ be a [[locally contractible topological space]]. Then $\hat Sh_{(\infty,1)}(C)$ is a [[locally ∞-connected (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

The [[category of open subsets]] $Op(X)$ is not in general a locally $\infty$-connected site according to the above definition. But there is another site of definition for $\hat Sh_{(\infty,1)}(X)$ which is: the full [[subcategory]] $cOp(X) \hookrightarrow Op(X)$  on the [[contractible]] [[open subset]]s. 

=--


## Related concepts



* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / **locally ∞-connected (∞,1)-site**

  * [[connected site]] / [[∞-connected (∞,1)-site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects locally ∞-connected (∞,1)-site]]
[[!redirects locally ∞-connected (∞,1)-sites]]
[[!redirects locally infinity-connected (infinity,1)-sites]]

[[!redirects locally ∞-connected site]]
[[!redirects locally infinity-connected site]]

[[!redirects locally ∞-connected sites]]
[[!redirects locally infinity-connected sites]]


