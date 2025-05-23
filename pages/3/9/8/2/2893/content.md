* tic
{: toc}


## Idea ##

The full image of a [[functor]] $F\colon C \to D$ is a version of its [[image of a functor|image]] that gets its [[objects]] from the functor\'s [[source]] $C$ but its [[morphisms]] from the functor\'s [[target]] $D$. It is the object through which the [[(bo, ff) factorization system|(bo, ff) factorization]] of a functor factors.

You may think of it as (up to [[equivalence of categories|equivalence]]) the [[full subcategory]] of $D$ whose objects lie in the literal image of $F$.

We may call it the $1$-image of the functor, because it reduces (again, up to equivalence) to the ordinary [[image]] for a functor between $0$-[[0-category|categories]].


## Definition ##

Let $C$ and $D$ be [[categories]], and let $F\colon C \to D$ be a [[functor]].  Then the __full image__ of $F$ is the category $\overline{im} F$ with:

*  as objects, the objects of $C$;
*  as morphisms from $x$ to $y$, the morphisms in $D$ from $F(x)$ to $F(y)$.

If $C$ is a [[subcategory]] of $D$, then the full image is the [[full subcategory]] of $D$ whose objects belong to $C$.

The full image should be taken as equipped with a functor to $D$, which acts as $F$ on objects and the identity on morphisms.  This functor is [[fully faithful functor|fully faithful]], so $\overline{im} F$ is always equivalent to a full subcategory of $D$.

From in internal point of view, if $codisc(S)$ is the category with object set $S$ and a unique arrow between any ordered pair of objects (that is, $Mor(codisc(S)) = S\times S$), the full image can be defined as a pullback: 
$$
\begin{matrix}
  \overline{im} F& \to & D \\
  \downarrow&&\, \downarrow \\
  codisc(Obj(C))&\underset{codisc(F_0)}{\to} & codisc(Obj(D))
\end{matrix}
$$
in the category [[Cat]]. Here $F_0$ is the object component of $F$ and $codisc(F_0)$ is the obvious functor. This determines $\overline{im} F$ up to canonical isomorphism as a [[strict category]] (or other [[internal category]]).  (Note, though, that this pullback is not a (weak) [[2-pullback]].)

The full image of $F : C \to D$ is equivalently the [[Kleisli category]] for the trivial $F$-[[relative monad]] $F$.

## Full images of forgetful functors ##

Let $F$ be interpreted as a [[forgetful functor]], so that the objects of $C$ are thought of as objects of $D$ with some [[stuff, structure, property]].  Then the full image of $F$ consists of objects of $D$ with only a property: specifically the property that they are capable of taking the stuff or structure of being an object of $C$.

For example, any [[inhabited set]] is capable of taking the structure of a [[group]] (at least, assuming the [[axiom of choice]]).  So the full image of the forgetful functor from [[Grp]] to [[Set]] is equivalent to the category $Set \setminus \{\empty\}$ of inhabited sets.

[[!redirects full images]]
