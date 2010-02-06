
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

...

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