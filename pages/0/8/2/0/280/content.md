> this entry is about the notion of _action_ in algebra (of one algebraic object on another object). For the notion of _[[action functional]]_ in [[physics]] see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

# Actions
* table of contents
{: toc}


## Idea

There are various variants of the notion of something _acting_ on something else. They are all closely related.

The simplest notion of action involves one set, $X$, acting on another $Y$ as the function $act\colon X \times Y \to Y$. This can be [[currying|curried]] as $ \hat{act}\colon Y \to Y ^ X $ where $Y ^ X$ is the (monoidal) [[function set|set of functions]] from $X$ to $Y$.[^SetActions]

[^SetActions]: In the category [[Set]] there is no difference between the above left action and the right action  $actR\colon Y \times X \to Y$ because the product commutes. However for the action of a [[monoid]] on a set (sometimes called [[MSet| M-set]] or M-act) the product of a monoid and a set does not  commute so the left and right actions are different.  The action of a set on a set is the same as an arrow labeled [[directed graph]] $arrows\colon vertices \times labels \to vertices$ which specifies  that each vertex must have a set of arrows leaving it with one arrow per label, and is also the same as a simple (non halting) [[deterministic automaton]]  $transition\colon inputs \times states \to states$.

Generalized notions of action use entities from categories other than $Set$ and involve an [[exponential object]] such as  $Y ^ X$.

For an entity $K$ to be able to act on anything else in the first place, $K$ needs to have some notion of composition or product with itself. Quite generally this is modeled by realizing $K$ as an [[n-category]] of sorts. In particular, if $K$ is a monoidal entity with a product $K \otimes K \to K$ there is usually a [[delooping]] $\mathbf{B} K$ which encodes the same information.

From this perspective one fundamental way to realize an action of some entity $K$ on some entity in the [[category]] or [[n-category]] $C$ is an ($n$-)functor

$$
  \rho : K \to C
$$
or
$$
  \rho : \mathbf{B} K \to C
$$


Here the collection $\coprod_{k \in Obj(k)} \rho(k)$ of objects in $C$ in the image of objects of $K$ is "what $K$ is acting on" and the images of the morphisms in $K$ under $\rho$ produce the action itself.

## Definitions

### Actions of a group

An **action** of a [[group]] $G$ on an [[object]] $x$ in a [[category]] $C$ is a [[representation]] of $G$ on $x$, that is a group [[homomorphism]] $\rho : G \to Aut(x)$, where $Aut(x)$ is the [[automorphism group]] of $x$.  


As indicated above, a more sophisticated but equivalent definition treats the group $G$ as a category denoted $\mathbf{B} G$ with one object, say $*$.  Then an _action_ of $G$ in the category $C$ is just a [[functor]] 
$$\rho : \mathbf{B} G \to C.$$  
Here the object $x$ of the previous definition is just $\rho(*)$. 


### Actions of a monoid

More generally we can define an _action_ of a [[monoid]] $M$ in the category $C$ to be a functor
$$\rho: \mathbf{B} M \to C $$
where $\mathbf{B} M$ is (again) $M$ regarded as a one-object category.

The _category of actions_ of $M$ in $C$ is then defined to be the [[functor category]] $C^{\mathbf{B} M}$.

### Actions of a category

One can also define an [[action of a category on a set|action of a category]] $D$ on the category $C$ as a functor from $C$ to $D$, but usually one just calls this a [[functor]]. 

Another perspective on the same situation is: a (small) category is a [[monad]] in the category of [[span]]s in [[Set]]. An action of the category is an algebra for this monad. See [[action of a category on a set]]. 

On the other hand, an action of a [[monoidal category]] (not _in_ a monoidal category, as above) is called an [[actegory]]. This notion can be expanded of course to actions _in_ a [[monoidal bicategory]], where in the case of $Cat$ as monoidal bicategory it specializes to the notion of actegory. 

### Actions of a group object

Suppose we have  a category, $C$, with binary [[product]]s and a [[terminal object]] $*$. There is an alternative way of viewing group actions in [[Set]], so that we can talk about an action of a [[group object]], $G$, in $C$ on an object, $X$, of $C$.

By the adjointness relation between cartesian product, $A\times ?$, and function set, $?^A$, in [[Set]], a group homomorphism

$$\alpha: G\to Aut(X)$$
corresponds to a function

$$act: G\times X\to X$$
which will have various properties encoding that $\alpha$ was a homomorphism of groups:  

$$act(g_1g_2,x) = act(g_1,act(g_2,x))$$

$$act(1,x) = x$$

and these can be encoded diagrammatically.

Because of this, we can **define** an action of a group object, $G$, in $C$ on an object, $X$, of $C$ to be a morphism
$$act: G\times X\to X$$
satisfying conditions that certain diagrams (left to the reader) encoding these two rules, commute.

The advantage of this is that it does not require the category $C$ to have internal automorphism group objects for all objects being considered.

As an example, within the category of [[profinite group]]s, not all objects have automorphism groups for which the natural topology is profinite, because of that profinite group actions are sometimes given in this form or are restricted to actions on objects for which the automorphism group is naturally profinite. 


## Examples

* A [[representation]] is a "linear action".

* In [[symplectic geometry]] one considers [[Hamiltonian actions]].

* In [[topology]]: [[topological G-space]]

(...)

## Related concepts

* **action**, [[∞-action]],

  * [[conjugation action]], [[adjoint action]]

  * [[diagonal action]]

* [[coaction]]

* [[representation]], [[∞-representation]]

* [[module]], [[∞-module]]

* [[associated bundle]], [[associated ∞-bundle]]

* [[quotient]], [[quotient stack]], [[quotient type]]

* [[representation theory]], [[invariant theory]]

* [[equivariant homotopy theory]]

  * [[Borel model structure]]


## References

* [[Patrick Morandi]], _Group actions_ ([pdf](http://sierra.nmsu.edu/morandi/notes/groupactions.pdf))

[[!redirects action]]
[[!redirects actions]]
[[!redirects group action]]
[[!redirects group actions]]