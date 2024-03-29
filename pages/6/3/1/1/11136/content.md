


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called the _maybe monad_ is a simple [[monad in computer science]] which is used to implement the most basic kind of "[[exceptions]]" indicating the failure of a computation in terms of [[functional programming]]: The maybe monad models the exception which witnesses a failure without however producing any further information.

On the type system the [[maybe monad]] is the operation $X \mapsto X \sqcup \ast$ of forming the [[coproduct type]] with the [[unit type]]. (The [[exception monad]] for the [[unit type]].)

The idea here is that a function $X \longrightarrow Y$ in its [[Kleisli category]] is in the original category a function of the form $X \longrightarrow Y \coprod \ast $ so either returns indeed a value in $Y$ or else returns the unique element of the [[unit type]]/[[terminal object]] $\ast$ -- it is a _[[partial function]]_. The latter case is naturally interpreted as "no value returned", hence as indicating a "failure in computation".

## Properties

> under construction

### Kleisli category

The [[Kleisli category]] of the maybe monad on $Set$ is the category whose objects are sets, and whose morphisms are [[partial functions]]. 

This observation generalizes as follows: if $\mathbf{C}$ is an [[extensive category]] and has a [[terminal object]] $\ast$, then a morphism $g: X \to Y \coprod \ast$ as an object of the [[overcategory]] $\mathbf(C)/(Y \coprod \ast)$ determines (uniquely up to canonical isomorphism) an object 

$$(f: X_1 \to Y, !: X_2 \to \ast) \in \mathbf{C}/Y \times \mathbf{C}/\ast$$ 

such that $g = f \coprod !$, in other words a partial morphism $f: X \rightharpoonup Y$ whose domain of definition is a subobject $X_1 \hookrightarrow X$ with complement $X_2 \hookrightarrow X$. In brief, maps in the Kleisli category are partial maps with complemented domain. 

In particular, in the case of a [[Boolean topos]], the Kleisli category is the category of objects and partial maps; see also [[partial map classifier]]. 


### EM-category and Relation to pointed objects
 {#EMCategoryAndRelationToPointedObjects}

The [[algebra over a monad|algebras]] over the maybe monad are  [[pointed objects]]. 

Moreover, assuming $\mathbf{C}$ has [[finite products]] and an appropriate form of [[distributive category|distributivity]] (which obtains if for example $\mathbf{C}$ is [[extensive category|lextensive]]), the maybe monad on $\mathbf{C}$ is a [[monoidal monad]] on the [[cartesian monoidal category]] $\mathbf{C}$. It follows (by the discussion at _[[commutative monad]]_, see also ([Seal 12](#Seal12))) that its [[Eilenberg-Moore category]] of algebras canonically inherits the structure of a [[monoidal category]], at least under the mild assumption that it has [[reflexive coequalizers]]. Note that the maybe monad $T$ preserves reflexive coequalizers, so the monadic functor [[created limit|creates]] reflexive coequalizers if the base category has them; in this abstract setting the monoidal product on algebras $(X, \alpha: T X \to X)$, $(Y, \beta: T Y \to Y)$ is given explicitly as the [[coequalizer]] of $T(\alpha \times \beta): T(T X \times T Y) \to T(X \times Y)$ and 

$$T(T X \times T Y) \stackrel{T(\phi_{X, Y})}{\to} T T(X \times Y) \stackrel{\mu}{\to} T(X \times Y)$$ 

where $\phi$ is one of the structural constraints on the monoidal monad $T$ and $\mu$ is the multiplication on $T$. One finds that this coequalizer yields the usual [[smash product]] of pointed objects.

+-- {: .num_remark} 
###### Remark 
The smash product as the correct monoidal product can also be deduced in a perhaps more perspicuous manner if we assume more of the base category: that it is [[cartesian closed category|cartesian closed]], [[finite limit|finitely complete]], and finitely cocomplete. In that case we construct the [[internal hom]] of $T$-algebras, i.e., the internal hom of pointed objects $(Y, \beta: T Y \to Y)$ and $(Z, \gamma: T Z \to Z)$ directly as an [[equalizer]] of maps 

$$\array{
Z^Y & \to & T Z^{T Y} \\ 
 & \mathllap{Z^\beta} \searrow & \downarrow \mathrlap{\gamma^{T Y}} \\
 & & Z^{T Y}
}$$ 

where the top arrow expresses [[enriched functor|enriched functoriality]] of $T$ (which in turn is closely related to the [[strong functor|strength]] on $T$). The success of this is guaranteed by the [[commutative monad|commutativity]] of the monad (which here takes a particularly simple form, being given by the commutative _[[monoid]]_ $\ast$ with respect to coproduct $\coprod$). Then, by taking the monoidal product that is [[adjunct|adjoint]] to the [[internal hom]], one is led to the [[smash product]] $(X \wedge Y)_\ast$ all the same: that is, one can read off the smash product from the fact that pointed maps $X_\ast \to \hom_\ast(Y_\ast, Z_\ast)$ should correspond to pointed maps $(X \wedge Y)_\ast \to Z_\ast$. 
=-- 


### Relation to natural number objects

Regarding just the underlying [[endofunctor]] of the maybe monad, its [[initial algebra over an endofunctor]] is a [[natural numbers object]].

### On the augmented simplex category

We may view the [[simplex category|augmented simplex category]] as the subcategory of $\Set$ whose objects are the finite [[von Neumann ordinals]] and whose morphisms are the monotone functions between them. Then the maybe monad on $\Set$ restricts to $\Delta_a$ to give the monad that sends the object $\mathbf{n}$ to $\mathbf{n+1}$ and the morphism $f:\mathbf{n}\to\mathbf{m}$ to the morphism $T(f):\mathbf{n+1}\to\mathbf{m+1}$ defined by

$$T(f)(k) = \begin{cases}
f(k) & k \lt n\\
m & k = n
\end{cases}$$

In fact, $\Delta_a$ is freely generated by this structure and $\mathbf{0}$ in the sense that its objects are given by $\mathbf{n}=T^n\mathbf{0}$, the face maps are given by $\delta_i^n=T^{n-i-1}\eta_\mathbf{i}$, the degeneracy maps are given by $\sigma_i^n=T^{n-i-1}\mu_\mathbf{i}$, and the [[simplicial identities]] are precisely the monad axioms. Another way to put this is that $(\Delta_a,T,\mathbf{0})$ is the initial object of the $2$-category whose objects are categories equipped with a monad and an object.

This means that if C is some other category equipped with a **co**monad and an object then we get a canonical functor $\Delta_a^\mathrm{op}\to C$ and hence an augmented [[simplicial object]] in $C$. In particular when $C$ is the [[Eilenberg-Moore category| category of algebras]] of a monad on $D$ we get a simplicial object for each algebra, whose underlying simplicial object in $D$ is the [[bar construction]].

The comonad $T^\mathrm{op}$ on $\Delta_a^\mathrm{op}$ induces the [[decalage#DecalageComonad|Décalage comonad]].

## Related concepts

* [[exception monad]]

* [[state monad]]

* [[continuation monad]]

* [[successor monad]]

## References

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ &lbrack;[arXiv:1205.0101](http://arxiv.org/abs/1205.0101)&rbrack;

Around (0.4.24.2) in 

* {#Durov07} [[Nikolai Durov]], _New Approach to Arakelov Geometry_ ([arXiv:0704.2030](http://arxiv.org/abs/0704.2030))

the algebraic structure of the would be "[[field with one element]]" is regarded as being the maybe monad, hence [[modules]] over $\mathbb{F}_1$ are defined to be [[algebra over a monad|monad-algebras]] over the maybe monad, hence [[pointed sets]].



[[!redirects maybe monads]]