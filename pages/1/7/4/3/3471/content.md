
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _global sections_ of a [[bundle]] are simply its [[sections]]. When bundles are replaced by their [[sheaves]] of [[local sections]], then forming global sections corresponds to the [[direct image]] operation on sheaves with respect to the morphism to the [[terminal object|terminal]] [[site]]. This definition generalizes to objects in a general [[topos]] and [[(∞,1)-topos]].


## Definition

We start describing the more explicit notions of global sections of bundles and then work our way towards the more abstract notions in terms of [[topos]] theory.


### Of bundles

A __global [[section]]__ of a [[bundle]] $E \overset{p}\to B$ is simply a [[section]] of $p$, that is a map $s\colon B \to E$ such that $p \circ s = \id_B$.  

$$
  \array{
    && E
    \\
    & {}^{\mathllap{s}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    B &\stackrel{id}{\to}& B
  }
  \,.
$$

The adjective 'global' here is used to distinguish from a **[[local section]]**: a *generalised* section over some subspace $i : U \hookrightarrow B$ which is a section of the map to $U$ 

$$
  i^* E := E|_U \to U
$$

from the [[pullback]]

$$
  \array{
    i^* E := E|_U &\to& E
    \\
    \downarrow && \downarrow
    \\
    U &\stackrel{i}{\to}& B
  }
  \,.
$$

Compare the notion of [[global point]], which is really the special case when $B$ is a [[terminal object]] (where the generalised section corresponds to a [[generalised element]]).  On the other hand, a global section of $E \overset{p}\to B$ in $\mathcal{C}$ *is* simply a global point in the [[slice category]] $\mathcal{C}/B$.

One often writes 

$$
  \Gamma_U(E) := Hom_{\mathcal{C}/U}(U , E|_U)
$$

for the **set of global sections** over $U$ (or $\Gamma(U,E)$ or similar).



### Of sheaves on topological spaces

Every [[sheaf]] $A \in Sh(X) = Sh(Op(X))$ on (the [[site]] that is given by the [[category of open subsets]] of) a [[topological space]] $X$ is the sheaf of _[[local sections]]_  of its [[etale space]] [[bundle]] $E \to X$ in that

$$
  A : U \mapsto \Gamma_U(E)
$$

for every $U \in Op(X)$. For this reasons one often speaks of the value of a [[sheaf]] on some object as a set of sections, even if the corresponding bundle is never mentioned and doesn't really matter. 

The set of global sections on $X$ is 

$$
  \Gamma_X(A) = A(X) = Hom_{Sh(X)}(X, A)
  \,,
$$

where $X \in Sh(X)$ denotes the [[terminal object]] of the [[category of sheaves]] $Sh(X)$. Often this is written just using different notation

$$
  \Gamma_X(A) = Hom_{Sh(X)}(*,A)
$$

One notices that $\Gamma_X(-) : Sh(X) \to Set$ defined this way is the [[direct image]] functor on [[Grothendieck toposes]] that is induced from the canonical morphism $X \to *$ of [[topological space]]s (now "$*$" really denotes the [[point]] topological space!) and hence from the corresponding morphism of [[site]]s.

Again, this expression for global sections induces a relative version, 
e.g. for sheaves on $S$-[[relative scheme|schemes]], the direct image functor goes into the base scheme $S$). 


### Of objects in a general Grothendieck topos {#GeneralTopos}

The definition of global sections of sheaves on topological spaces in terms of the [[direct image]] of the canonical morphism to the terminal [[site]] generalizes to [[Grothendieck topos|sheaf toposes]] over arbitrary [[sites]].

For every [[Grothendieck topos]] $\mathcal{T}$, there is a [[geometric morphism]] (the *[[terminal geometric morphism]]*)

$$
  \Gamma \;\colon\; \mathcal{T}  \stackrel{\leftarrow}{\to} Set : LConst
$$

called the **global sections** functor. It is given by the [[hom-set]] out of the [[terminal object]]

$$
  \Gamma(-) = Hom_{\mathcal{T}}({*}, -)
$$

and hence assigns to each object $A\in \mathcal{T}$ its set of [[global element]]s $\Gamma(A) = Hom_{\mathcal{T}}(*,A)$. 

The [[left adjoint]] $LConst : Set \to \mathcal{T}$ of the global section functor is the canonical [[Set]]-[[copower|tensoring]] functor

$$
  \otimes : Set \times \mathcal{T} \to \mathcal{T}
$$

applied to the [[terminal object]]

$$
  const = (-)\otimes {*} : Set \to \mathcal{T}
$$

which sends a set $S$ to the [[coproduct]] of $|S|$ copies of the terminal object

$$
  S \otimes {*} = \coprod_{s \in S} {*}
  \,.
$$

This is called the **constant object** of $\mathcal{T}$ on the set $S$. Notably when $\mathcal{T}$ is a [[Grothendieck topos|sheaf topos]] this is the **[[constant sheaf]]** $LConst_S$ on $S$. 

$$
  \mathcal{T} \stackrel{\stackrel{LConst}{\leftarrow}}{\overset{\Gamma}{\to}} Set
  \,.
$$

If the topos $\mathcal{T}$ is a [[locally connected topos]] then the left adjoint functor $LConst$ is also a right adjoint, its left adjoint being the functor $\Pi_0 : \mathcal{T} \to Set$ that sends an object to its set of connected components.

### Of objects in an $(\infty,1)$-topos

The previous abstract definition generalizes straightforwardly to every context of [[higher category theory]] where the required notions of [[adjoint functor]] etc. are provided.

Notably in [[(∞,1)-category]] theory the global section functor on an [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}$ is the [[hom-functor]]

$$
  \Gamma(-) 
  \;\coloneqq\; 
  \mathbf{H}(*,-) \colon 
  \;
  \mathbf{H} = Sh_{(\infty,1)}(C) \to Sh_{(\infty,1)}(*) = \infty Grpd
$$

of morphisms out of the terminal object.

This is indeed again the [[terminal geometric morphism]].

+-- {: .num_prop }
###### Proposition

Let $\mathbf{H}$ be an [[∞-stack]] [[(∞,1)-topos]]. Then the [[∞-groupoid]] $Geom(\mathbf{H}, \infty Grpd)$ of [[geometric morphism|geometric]] [[(∞,1)-functor]]s is [[contractible]].

So $\infty Grpd$ is the [[terminal object]] in the [[(∞,1)-category]] of [[(∞,1)-topos]]es and geometric morphisms.
 
=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT 6.3.4.1]]

=--

If the [[(∞,1)-topos]] is a [[locally contractible (∞,1)-topos]] then this is an [[essential geometric morphism]].

The composite [[(∞,1)-functor]] $\Gamma \circ LConst$ is the [[shape of an (∞,1)-topos|shape of]] $\mathbf{H}$.

## Related concepts

* [[local section]], [[flat section]]

* [[abelian sheaf cohomology]]

* [[ex-space]]

* [[global element]]

[[!redirects global sections]]

[[!redirects global sections functor]]
[[!redirects global section functor]]
[[!redirects global sections functors]]
[[!redirects global section functors]]


[[!redirects global section geometric morphism]]
[[!redirects global section geometric morphisms]]
[[!redirects global sections geometric morphism]]
[[!redirects global sections geometric morphisms]]