<div class="rightHandSide toc">
[[!include higher geometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea {#Idea}

A standard model for general [[∞-groupoid]]s is given by [[simplicial set]]s that are [[Kan fibration|Kan fibrant]]: [[Kan complex]]es. It is straightforward to [[internalization|internalize]] the [[horn]]-filler condition that characterizes [[Kan complex]]es from the [[category]] [[SSet]] of [[simplicial object]]s in [[Set]] to one of [[simplicial objects]] in any category $C$ with a bit of suitable structure. 

* This is described in [Internal horn filler condition](#InternalHornFillers), below.

But for the [[simplicial object]]s in question to be usefully identified as [[∞-groupoid]]s internal to $C$, the horn filler condition is -- while necessary -- typically not sufficient. At least one has to be a bit careful about what it is one wants to model.

A very well understood special case that serves to give some feeling for the general situation is that where $C$ is a [[Grothendieck topos]]. In that case [[simplicial object]]s in $C$ are [[simplicial presheaf|simplicial sheaves]]. There is a well developed theory of [[model structure on simplicial presheaves|model structures on simplicial sheaves]] that are known to be [[models for ∞-stack (∞,1)-toposes]]. 

* This is described in [Simplicial sheaves](#SimplicialSheaves), below.

In terms of this the true $\infty$-groupoids internal to $C$ are those simplicial sheaves that are fibrant objects in the given [[model category]]. These fibrant simplicial sheaves in particular satisfy the internal Kan filler conditon, but they are characterized by a much stronger condition: in addition they satisfy a [[descent]] condition. 

* This is described in [Comparison](#Comparison), below.

Another issue highlighted by this example is that the right notion of morphisms of internal Kan complexes are not just the internal morphisms of simplicial objects: for the case of $C$ a Grothendieck topos and using the model structure on simplicial sheaves as above, the right notion of morphism between two internal Kan complexes $X$ and $A$ is a morphism of simplicial objects $\hat X \to A$ out of a cofibrant replacement of $X$, as discussed at [[derived hom space]]. So the right notion of morphisms of internal $\infty$-groupoids are $\infty$-[[anafunctor]]s.

A little bit of theory for this exists for the slightly more general case that $C$ is an arbitrary [[elementary topos]]. See [[model structure on simplicial objects in a topos]].

For more general $C$ not much is known. 


## Definition


### Internal horn filler condition {#InternalHornFillers}

The [[Kan complex]] definition of [[∞-groupoid]] may be [[internalization|internalized]] to more general categories. Namely:

*  We can define a [[simplicial object]] $X$ in any [[category]] $C$, as a [[contravariant functor]] to $C$ from the [[simplex category]] $\Delta$;
*  Given a simplicial object $X$, we define the object $X^{\Lambda^n_k}$ of $k$-horns of $n$-simplices of $X$ (if it exists) as the [[weighted limit]] of $X\colon \Delta^{op} \to C$ weighted by the standard horn (thought of as a simplicial set) $\Lambda^n_k\colon \Delta^{op} \to Set$.
*  If we have a distinguished class of 'surjections', then we require that each morphism $X_n \to X^{\Lambda^n_k}$ is 'surjective'.

In particular, if $C$ is a [[left exact category]] equipped with a [[Grothendieck pretopology]], then the limits in (2) exist and one can choose single arrow coverings as distinguished 'surjections'. So we define a __Kan object__ in such a $C$ to be a simplicial object in $C$ satisfying the Kan conditions (3).  Then we may define an __$\infty$-groupoid in $C$__ to be simply a Kan object in $C$.  (Recall that one way to define an ordinary $\infty$-groupoid is as a [[Kan complex]], that is a Kan object in [[Set]].)

Another, almost equivalent, way to describe the Kan conditions expressed in this way is by saying that "the Kan conditions are satisfied" is true in the [[internal logic]] of the [[site]] $C$, or equivalently the internal logic of its [[Grothendieck topos]] of sheaves (after applying the [[Yoneda embedding]] to obtain a simplicial object in this topos).  Of course, if $C$ is itself a Grothendieck topos, then it is equivalent to the topos of sheaves on itself for its [[canonical topology]].  (This is only "almost equivalent" if the Grothendieck pretopology is in fact a topology.)


### In terms of simplicial sheaves {#SimplicialSheaves}

If the category $C$ is a [[Grothendieck topos]], i.e. a [[category of sheaves]] (of sets) $C = Sh(S)= Sh(S,Set)$ on some small [[site]], then [[simplicial object]]s in $C$ are the same as [[simplicial sheaves]] on $S$

$$
  [\Delta^{op}, C)] \simeq Sh(S, SSet)
  \,.
$$

There are various ([[Quillen equivalence|Quillen equivalent]]) [[model category]] structures on the categories of simplicial sheaves or presheaves on a small site; see [[model structure on simplicial presheaves]] and [[model structure on simplicial sheaves]] for more.  An $\infty$-groupoid in $C$ may be taken to be a fibrant object with respect to one of these model category structures.

### Comparison {#Comparison}

The two definitions are *not* equivalent.  Consider, for instance, a Grothendieck topos $C = Sh(S)$ and an [[internal groupoid]] in $C$, i.e. a sheaf of groupoids on $S$, but which is not a [[stack]].  Then the [[nerve]] of this internal groupoid will satisfy the Kan conditions in the sense of the first definition (by repeating the usual proof that the nerve of a groupoid is a Kan complex in the internal logic), but it will not be fibrant as a simplicial sheaf (since it is not a stack).

+--{: .query}
[[Mike Shulman]]: I'm guessing that the converse is true, though: that every fibrant simplicial sheaf satisfies the Kan conditions in the internal logic.  But I don't know enough about the model structures on simplicial sheaves to prove that.

[[Urs Schreiber]]: yes, should be true. I typed the argument in the following:
=--

1. The fibrant objects in any local [[model structure on simplicial sheaves]] in particular have the property that they are sheaves with values in Kan complexes.

   Here a reminder on why this is so. The local [[model structure on simplicial sheaves|model structures on simplicial sheaves]] are left [[Bousfield localization]]s of the injective or projective [[global model structure on functors]]. So their fibrant objects are in particular fibrant in $[S^{op},SSet]_{proj/inj}$. The fibrant objects in $[S^{op}, SSet]_{proj}$ are (by definition of projective fibrations) precisely the objectwise Kan complexes. The fibrant objects in $[S^{op},SSet]_{inj}$ are less, but still contained in the collection of objectwise Kan complexes.
So also the fibrant objects in $Sh(S,SSet)_{inj,proj}^{loc}$ are in particular Kan complex valued sheaves (that in addition satisfy a [[descent]] condition).

1. The [[weighted limit]]s over simplicial sheaves, or analogously the [[power]]ing of $Sh(S,SSet)$ over [[SSet]] works objectwise, so that for $X \in Sh(S,SSet)$ we have

   $$
     X^{\Lambda_k[n]} : U \mapsto SSet(\Lambda_k[n],X(U))
   $$

   and of course

   $$
     X_n = X^{\Delta[n]} : U \mapsto SSet(\Delta[n],X(U)) = X(U)_n
     \,.
   $$

Therefore fibrant $X \in Sh(S,SSet)$ have the property that for all $n, k$ the canonical morphism $X_n \to X^{\Lambda_k[n]}$ is a surjection when pulled back to any representable $U \to X$. In particular, the morphism is a [[stalk]]wise epimorphism, hence an [[epimorphism]] of sheaves.

## Examples

Here are some examples of internal $\infty$-groupoids according to the first definition (that is, internal Kan complexes).

* A classical example consists of the __topological $\infty$-groupoids__. The [[nerve]] construction makes a topological $\infty$-groupoid from a [[topological groupoid]]. This is actually a characterization of topological groupoids among topological categories.

* In particular, if $G$ is a [[topological group]], then $N(\mathbf{B}G)$ is a topological $\infty$-groupoid. This is relevant to the construction of the [[classifying spaces]] for continuous [[principal bundles]].

* Another classical example consists of the [[∞-Lie groupoids]].


[[!redirects Internal infinity-groupoid]]
[[!redirects Internal ∞-groupoid]]
[[!redirects internal ∞-groupoid]]
[[!redirects infinity-groupoid object]]
[[!redirects ∞-groupoid object]]
[[!redirects internal Kan complex]]
