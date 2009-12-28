
#Contents#
* automatic table of contents goes here
{:toc}


## Definition

### In terms of internal horn filler conditions

The [[Kan complex]] definition of [[∞-groupoid]] may be [[internalization|internalized]] to more general categories. Namely:

*  We can define a [[simplicial object]] $X$ in any [[category]] $C$, as a [[contravariant functor]] to $C$ from the [[simplex category]] $\Delta$;
*  Given a simplicial object $X$, we define the object $X^{\Lambda^n_k}$ of $k$-horns of $n$-simplices of $X$ (if it exists) as the [[weighted limit]] of $X\colon \Delta^{op} \to C$ weighted by the standard horn (thought of as a simplicial set) $\Lambda^n_k\colon \Delta^{op} \to Set$.
*  If we have a distinguished class of 'surjections', then we require that each morphism $X_n \to X^{\Lambda^n_k}$ is 'surjective'.

In particular, if $C$ is a [[left exact category]] equipped with a [[Grothendieck pretopology]], then when the limits in (2) exist and one can choose single arrow coverings as distinguished 'surjections'. So we define a __Kan object__ in $C$ to be a simplicial object in $C$ satisfying the Kan conditions (3).  Then we may define an __$\infty$-groupoid in $C$__ to be simply a Kan object in $C$.  (Recall that one way to define an ordinary $\infty$-groupoid is as a [[Kan complex]], that is a Kan object in [[Set]].)

+--{: .query}
[[Mike Shulman]]: I think in an "arbitrary category" it's not at all clear what the Kan conditions mean.  In $Set$ the Kan conditions can be interpreted by saying that the map of sets $X_n \to X^{\Lambda^n_k}$ is surjective for all $n$ and $k$, where $X^{\Lambda^n_k}$ is a certain limit of the $X_m$ for $m\lt n$---I think in fact it's the [[weighted limit]] of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$.  If $C$ has enough limits (probably finite limits are enough), you can define $X^{\Lambda^n_k}$ for a simplicial object in $C$, but then you need to say what kind of "surjective" you want.  An [[epimorphism]]?  A [[regular epimorphism]]?  For sufficiently good behavior, I'd guess you'd want $C$ to be a [[regular category]] and ask the maps $X_n \to X^{\Lambda^n_k}$ to be regular epimorphisms.

Alternately, you could ask that $X$ be "representably" a Kan complex, i.e. for each $Z\in C$ the simplicial set $C(Z,X_\bullet)$ is a Kan complex.  But I think this is just the same as asking each $X_n \to X^{\Lambda^n_k}$ to be [[split epimorphism|split epic]], which is probably stronger than you want.

[[Domenico Fiorenza]]: I agree: an "arbitray category" makes no sense, just as it would make no sense talking of group objects in an arbitrary category. So two things need to be specified. First we need to say what is a [[horn]] for a simplicial object in $C$, and here I agree that it could be defined as the weighted limit of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$. So the highest generality one can speak of horns is tautologically a "category with horns", i.e., a category where precisely these limits exist. I find this, however, an almost useless level of generality, and asking for all finite limits seems a better idea. Next one should specify what the Kan condition is, namely what one requires from the morphisms $X_n \to X^{\Lambda^n_k}$. Only hints here are that for [[Set]] one asks surjectivity and for [[Diff]] one asks the morphism to be a surjective submersion (at least it is so at the [[Kan complex]] entry). So a possibility would be to consider a [[pretopology]] on $C$ and ask $X_n \to X^{\Lambda^n_k}$ to be a cover. 

_Toby_:  That sounds right, so I put it in.  But we still need to check that finite limits and a Grothendieck pretopology are sufficient for the entire construction, yes?  (So if anybody moves or removes this query box, keep the previous sentence up here.)

[[Mike Shulman]]: Looks good to me.  Toby, what are you thinking of beyond the definition?

_Toby_:  I was thinking that we hadn\'t clarified exactly what kind of limit produces $X^{\Lambda^n_k}$, but I see that in fact Domenico seem to consider that settled.  So I clarified further above, and it\'s all good if Domenico\'s happy.

[[Domenico Fiorenza]] I'm happy with the editings, too. So we can now maybe remove the query box. As far as concerns which limits $C$ needs to have in order to speak of horns, I'm still convinced that one could introduce "horns" as a particula shape of finite limits, but also that it is not the case of giving a definition for such a particular issue: the informal way it is written above seems perferct to me. A more serious issue is the question: are single arrow coverings a 'good' distinguished class of 'surjections' (where 'good' stands for 'that produces a notion of Kan object one can conveniently work with')? Here I have no idea, except that with single arrow coverings one can reproduce the only two examples I have in mind, namely, $Sets$ and $Lie$.
=--


### In terms of simplicial sheaves {#SimplicialSheaves}

If the category $C$ is a [[Grothendieck topos]], i.e. a [[category of sheaves]] $C = Sh(S)$ on some [[site]], then [[simplicial object]]s in $C$ are [[simplicial presheaf|simplicial presheaves]] on $C$

$$
  [\Delta^{op}, C)] \simeq [S^{op}, SSet]
  \,.
$$

There are various ([[Quillen equivalence|Quillen equivalent]]) [[model category]] structures on such categories of simplicial presheaves. See [[model structure on simplicial presheaves]] for more. 

An $\infty$-groupoid in $C$ may be taken to be a fibrant object with respect to one of these model category structures.


## Examples

* A classical example consists of the __topological $\infty$-groupoids__. The [[nerve]] construction makes a topological $\infty$-groupoid from a [[topological groupoid]]. This is actually a characterization of topological groupoids among topological categories.

* In particular, if $G$ is a [[topological group]], then $N(\mathbf{B}G)$ is a topological $\infty$-groupoid. This is relevant to the construction of the [[classifying spaces]] for continuous [[principal bundles]].

* Another classical example consists of the [[∞-Lie groupoids]].


[[!redirects Internal infinity-groupoid]]
[[!redirects Internal ∞-groupoid]]
[[!redirects internal ∞-groupoid]]
[[!redirects infinity-groupoid object]]
[[!redirects ∞-groupoid object]]
