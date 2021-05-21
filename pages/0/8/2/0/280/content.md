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
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Actions
* table of contents
{: toc}


## Idea
 {#Idea}

There are various variants of the notion of something _acting_ on something else. They are all closely related.

The simplest concept of an action involves one [[set]], $X$, acting on another set $Y$ and such an action is given by a [[function]] from the [[product]] of $X$ with $Y$ to $Y$

$$
  act\colon X \times Y \to Y
  \,.
$$ 

For fixed $x \in X$ this produces an [[endofunction]] $act(x,-) \colon Y \to Y$ and hence some "transformation" or "action" on $Y$. In this way the whole of $X$ acts on $Y$.

Here $(x\mapsto act(x,-))$ is the _[[currying|curried]]_ function $\widehat{act}\colon X \to Y^Y$ of the original $act$, which maps $X$ to the [[function set|set]] of [[endofunctions]] on $Y$.  Quite generally one has these two perspectives on actions.

Usually the key aspect of an action of some $X$ is that $X$ itself carries an algebraic structure, such as being a [[group]] (or just a [[monoid]]) or being a [[ring]] or an [[associative algebra]], which is also possessed by $Y^Y$ and preserved by the curried action $\widehat{act}$.  Note that if $Y$ is any set then $Y^Y$ is a monoid, and when $X$ acts on it one calls it an [[MSet|X-set]].  For $Y^Y$ to have a ring/algebra structure, $Y$ must be some sort of [[abelian group]] or [[vector space]] with the action by [[linear functions]]; then one calls the action also a _[[module]]_ or _[[representation]]_.

In terms of the uncurried action $X\times Y\to Y$, the "preservation" condition says roughly speaking that acting consecutively with two elements in $X$ is the same as first multiplying them and then acting with the result:

$$
  act(x_2,act(x_1,y)) = act(x_2\cdot x_1, y)
  \,.
$$

To be precise, this is the condition for a *left action*; a *right action* is defined dually in terms of a map $Y\times X\to Y$.  If $X$ has no algebraic structure, or if its relevant structure is commutative, then there is no essential difference between the two; but in general they can be quite different.

This _action property_ can also often be identified with a [[functor]] property: it characterizes a [[functor]] from the [[delooping]] $\mathbf{B}X$ of the [[monoid]] $X$ to the [[category]] (such as [[Set]])  of which $Y$ is an object. The distinction between left and right actions is mirrored in the variance; acting on the left yields a covariant functor, whereas acting on the right is expressed via contravariance.

In this way essentially every kind of [[functor]], [[n-functor]] and [[enriched functor]] may be thought of as defining a generalized kind of action. This perspective on actions is particularly prevalent in [[enriched category theory]], where for instance [[coends]] may be thought of as producing [[tensor products]] of actions in this general functorial sense.

Under the [[Grothendieck construction]] (or one of its variants), this perspective turns into the perspective where an action of $X$ is some [[bundle]] $Y/X$ over $\mathbf{B}X$, whose [[fiber]] is $Y$:

$$
  \array{
    Y &\longrightarrow& Y/X
    \\
    && \downarrow
    \\
    && \mathbf{B}X
  }
  \,.
$$

Here the total space $Y/X$ of this bundle is typically the "weak" [[quotient]] (for instance: [[homotopy quotient]]) of the action, whence the notation. If one thinks of $\mathbf{B}X$ as the [[classifying space]] for the $X$-[[universal principal bundle]], then this bundle $Y/X \to \mathbf{B}X$ is the $Y$-[[fiber bundle]] which is [[associated bundle|associated]] via the action to this universal bundle. For more on this perspective on actions see at _[[∞-action]]_.




## Definitions

### Actions of a group

An **action** of a [[group]] $G$ on an [[object]] $S$ in a [[category]] $\mathcal{C}$ is a [[representation]] of $G$ on $S$, that is a [[group homomorphism]] $\rho \colon G \to Aut(S)$, where $Aut(S)$ is the [[automorphism group]] of $S$ in $\mathcal{C}$.

Group actions, especially [[continuous function|continuous]] actions on [[topological spaces]], are also known as _transformation groups_ (starting around [Klein 1872, Sec. 1](#Klein1872), see also [Koszul 65](#Koszul65) [Bredon 72](#Bredon72), [tom Dieck 79](#tomDieck79), [tom Dieck 87](#tomDieck87)).  Alternatively, if the group $G$ that acts is understood, one calls ([Bredon 72, Ch. II](#Bredon72)) the space $X$ equipped with an action by $G$ a _[[topological G-space]]_ (or *[[G-set]]*, *[[G-manifold]]*, etc., as the case may be).

As indicated above, a more abstract but equivalent definition regards the group $G$ as a category (a [[groupoid]]), denoted $\mathbf{B} G$, with a single object $\ast$.  Then an _action_ of $G$ in the category $C$ is equivalently a [[functor]] of the form
$$
  \rho \colon \mathbf{B} G \to \mathcal{C}
$$   
Here the object $S$ of the previous definition is the $\rho(\ast)$ of that single object.

Concretely, if $\mathcal{C}$ is a category like [[Set]], then an action is equivalently a [[function]]
$$
  \array{
    G \times S &\longrightarrow& S
    \\
    (g,s) &\mapsto& \rho(g)(s)
  }
$$
which satisfies the _action property_
\[
  \label{ActionPropertyOfGroupActions}
  \underset{
    g_1, g_2, s
  }{\forall}
  \;\;\;
  \rho(g_1 \cdot g_2)(s)
  \;=\;
  \rho(g_1)
  \big(
    \rho(g_2)(s)
  \big)
\]


### Actions of a monoid

More generally we can define an _action_ of a [[monoid]] $M$ in the category $C$ to be a functor
$$\rho: \mathbf{B} M \to C $$
where $\mathbf{B} M$ is (again) $M$ regarded as a one-object category.

The _category of actions_ of $M$ in $C$ is then defined to be the [[functor category]] $C^{\mathbf{B} M}$. When $C$ is $Set$ this is called [[MSet]].

Considering this in [[enriched category theory]] yields the [[internalization|internal]] notion of _[[action objects]]_.

### Actions of a category

One can[^2] also define an [[action of a category on a set|action of a category]] $D$ on the category $C$ as a functor from $D$ to $C$, but usually one just calls this a [[functor]].

[^2]: One example of this relatively rare usage is [[William Lawvere]]: _Qualitative Distinctions Between Some Toposes of Generalized Graphs_, Contemporary Mathematics 92 (1989) in which this sense of action is routinely used.

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

As an example, only [[locally compact topological space|locally compact topological spaces]] have well-behaved topological automorphism groups, and thus actions of topological spaces on topological spaces must either be restricted to actions on locally compact spaces, or else be defined as above. 

As another example, within the category of [[profinite group|profinite groups]] viewed as topological groups, not all objects have automorphism groups for which the natural topology is profinite. Thus profinite group actions on (the underlying topological space of) a profinite group must either be given in this form, or else be restricted to actions on profinite groups for which the automorphism group is naturally profinite. 

### Actions of a monoid object

Suppose we have  a category, $C$, with binary [[product]]s and a [[terminal object]] $*$. There is an alternative way of viewing monoid actions in [[Set]], so that we can talk about an action of a [[monoid object]], $M$, in $C$ on an object, $X$, of $C$.

By the adjointness relation between cartesian product, $A\times ?$, and function set, $?^A$, in [[Set]], a monoid homomorphism

$$\alpha: M\to End(X)$$ 
corresponds to a function

$$act: M\times X\to X$$
which will have various properties encoding that $\alpha$ was a homomorphism of monoids:  

$$act(m_1m_2,x) = act(m_1,act(m_2,x))$$

$$act(1,x) = x$$

and these can be encoded diagrammatically.

Because of this, we can **define** an action of a monoid object, $M$, in $C$ on an object, $X$, of $C$ to be a morphism
$$act:M\times X\to X$$
satisfying conditions that certain diagrams (left to the reader) encoding these two rules, commute.

The advantage of this is that it does not require the category $C$ to have internal endomorphism monoid objects for all objects being considered.

### Actions of a set

The action of a set on a set was defined above; it consists of a function $act: X\times Y\to Y$.  This can equivalently be represented by a [[quiver]] with $Y$ as its vertices, with its edges labeled by elements of $X$, and such that each vertex has exactly one arrow leaving it with each label.  (This is a sort of "Grothendieck construction".)  It is also the same as a simple (non halting) [[deterministic automaton]], with $Y$ the set of states and $X$ the set of inputs.


That an action is a type of edge labeled quiver can be seen by explicitly giving the product [[projection]] functions, $p_1$ and $p_2$, of $X\times Y$.

$$X\overset{\quad p_1 \quad}{ \leftarrow}X\times Y\underoverset{\quad act \quad}{p_2}{\rightrightarrows}Y$$

The shape of this diagram corresponds to that of an edge labeled quiver:

$$Labels\overset{\quad label \quad}{ \leftarrow}Edges\underoverset{\quad target \quad}{source}{\rightrightarrows}Vertices$$


While the set $X$ has no algebraic structure to be preserved, the action $act$ generates a unique **[[free category]] action** $act^{*}:X^{*}\times Y\to Y$ where $X^{*}$ is the [[free monoid]] on $X$ containing [[path|paths]] of $X$ elements. The monoidal structure of $X^*$ is preserved: two actions in succession is equal to the action of the concatenation of their paths.

$$act^{*}(x^{*}_2,act(x^{*}_1,y)) = act^{*}(x^{*}_2\cdot x^{*}_1, y) $$ 


## Examples

* A [[representation]] is a "linear action".

* In [[symplectic geometry]] one considers [[Hamiltonian actions]].

* In [[topology]]: [[topological G-space]]

  * [[circle action]]

  * [[group action on an n-sphere]]

(...)

## Related concepts
 {#RelatedConcepts}

* [[action object]]

* **action**, [[∞-action]],

  * [[conjugation action]], [[adjoint action]]

  * [[diagonal action]]

  * [[transitive action]], [[free action]], [[regular action]]

  * [[proper action]], [[properly discontinuous action]]

* [[coaction]]

* [[representation]], [[∞-representation]]

* [[module]], [[∞-module]]

* [[action monad]]

* [[associated bundle]], [[associated ∞-bundle]]

* [[quotient]], [[quotient stack]], [[quotient type]]

* [[representation theory]], [[invariant theory]]

* [[equivariant homotopy theory]]

  * [[Borel model structure]]


## References


### Group actions

On [[group actions]], mostly in [[TopologicalSpaces]], hence in the form of [[topological G-spaces]]:

Historical origins:

* {#Klein1872} [[Felix Klein]], _[[Vergleichende Betrachtungen über neuere geometrische Forschungen]]_ (1872) Mathematische Annalen volume 43, pages 63–100 1893  ([doi:10.1007/BF01446615](https://doi.org/10.1007/BF01446615))

  English translation by M. W. Haskell:

  _A comparative review of recent researches in geometry_, Bull. New York Math. Soc. 2, (1892-1893), 215-249. ([euclid:1183407629](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-2/issue-10/A-comparative-review-of-recent-researches-in-geometry/bams/1183407629.full), LaTeX version retyped by Nitin C. Rughoonauth: [arXiv:0807.3161](https://arxiv.org/abs/0807.3161))

Textbook accounts:

* {#Bredon72} [[Glen Bredon]], *[[Introduction to compact transformation groups]]*, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1)
, [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))

* {#tomDieck79} [[Tammo tom Dieck]], *[[Transformation Groups and Representation Theory]]*, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))

* {#tomDieck87} [[Tammo tom Dieck]], *[[Transformation Groups]]*, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))


Lecture notes:

* {#Koszul65} [[Jean-Louis Koszul]], _Lectures on Groups of Transformations_, Tata Institute 1965 ([pdf](http://www.math.tifr.res.in/~publ/ln/tifr32.pdf), [[KoszulGroupsOfTransformations.pdf:file]])

* [[Patrick Morandi]], _Group actions_ ([[MorandiGroupActions.pdf:file]])

[[!redirects action]]
[[!redirects actions]]
[[!redirects group action]]
[[!redirects group actions]]
[[!redirects monoid action]]
[[!redirects monoid actions]]

[[!redirects left action]]
[[!redirects left actions]]

[[!redirects right action]]
[[!redirects right actions]]

[[!redirects transformation group]]
[[!redirects transformation groups]]