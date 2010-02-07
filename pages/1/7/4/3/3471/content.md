
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A __global section__ of a [[bundle]] $E \overset{p}\to B$ is simply a [[section]] of $p$, that is a map $s\colon B \to E$ such that $p \circ s = \id_B$.  The adjective 'global' here is used to distinguish from a *generalised* section over some subspace $U \hookrightarrow B$ (which is a section of the map to $U$ from the [[pullback]]).

Compare the notion of [[global point]], which is really the special case when $B$ is a [[terminal object]] (where the generalised section corresponds to a [[generalised element]]).  On the other hand, a global section of $E \overset{p}\to B$ in $\mathcal{C}$ *is* simply a global point in the [[slice category]] $\mathcal{C}/B$.

...

More generally, the functor of global sections is the direct image functor into the terminal object (in some category of "spaces", e.g. for $S$-schemes, direct image functor into the base scheme $S$). 

## Of objects in a topos

For every [[topos]] $E$, there is a [[geometric morphism]]

$$
  \Gamma : E  \stackrel{\leftarrow}{\to} Set : const
$$

called the **global sections** functor. It is given by the [[hom-set]] out of the [[terminal object]]

$$
  \Gamma(-) = Hom_E({*}, -)
$$

and hence assigns to each object $A\in E$ its set of [[global element]]s $\Gamma(A) = Hom_E(*,A)$. If $E$ is a [[Grothendieck topos]] then one thinks of $A$ as a [[sheaf]] and of $\Gamma(A)$ as its set of **global sections**.

The [[left adjoint]] $const : Set \to E$ of the global section functor is the canonical [[Set]]-[[copower|tensoring]] functor

$$
  \otimes : Set \times E \to E
$$

applied to the [[terminal object]]

$$
  const = (-)\otimes {*} : Set \to E
$$

which sends a set $S$ to the [[coproduct]] of $|S|$ copies of the terminal object

$$
  S \otimes {*} = \coprod_{s \in S} {*}
  \,.
$$

This is called the **constant object** of $E$ on the set $S$. Notably when $E$ is a [[Grothendieck topos|sheaf topos]] this is the **[[constant sheaf]]** on $S$. 

[[!redirects global sections]]