+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Definition

Given a (small) [[category]] $C$ and given a [[set]] $S$ there are (at least) the following two equivalent ways to define an [[action]] of $C$ on $S$.

### Action as a functor

An **action of a category** $C$ on a [[set]] $S$ is nothing but a [[functor]] $\rho : C \to$ [[Set]]. 

The particular set $S$ that this functor defines an [[action]] on is the disjoint union of sets that the functor assigns to the objects of $C$:

$$
  S = \bigsqcup_{c \in Obj(C)} \rho(c) 
  \,.
$$

Given an element $s \in S$ which sits in the subset $\rho(c) \subset S$ associated with the object $c$ of $C$, it is acted on by all [[morphism]]s $c \stackrel{f}{\to} d$ in $C$ whose [[source]] is $c$. By the definition of [[functor]] every such morphism defines a map of sets

$$
  \rho(f) : (\rho(c) \subset S) \to (\rho(d) \subset S)
$$

and the the action of $f$ on $s \in \rho(c)$ under $\rho$ is 

$$
 \rho(f) :  (s \in \rho(c)) \mapsto (\rho(f)(s) \in \rho(d))
  \,.
$$

In the case that $C$ has just a single object $\bullet$ the category $C$ is just a [[monoid]] (might for instance be a [[group]]), there is just a single set $S = \rho(\bullet)$ and we recover the ordinary notion of a [[monoid]] or [[group]] acting on a set.


Indeed this generalizes the instance (the motivating example for the notion of action) where $\rho:G\rightarrow \mathbf{Aut}(S)$ is a group action on a set $S$, since the notion of coproduct is a generalization of the notion of automorphism group since naively a [[cardinal]] is an isomorphism class of sets and the notion of coproduct in turn generalizes that of cardinal ( see [[cardinal|there]]).  

### Action as an algebra for a monad

An equivalent perspective on the above situation is often useful. To motivate this, notice that the decomposition $S = \sqcup_{c \in Obj(c)} \rho(c)$ of the set $S$ into subsets corresponding to objects of the category $C$ can equivalently be encoded in a map of sets

$$
  \lambda : S \to Obj(C)
$$
which sends each element of $S$ to the object of $c$ it corresponds to under the action.

(In the case that our category $C$ is a [[groupoid]] or even a [[Lie groupoid]] this map may be familiar as the _anchor map_ or _moment map_ of the action.)

But also the category $C$ itself comes with maps to $Obj(C)$: the [[source]] map $s$ and [[target]] map $t$, which are suggestively drawn as a [[span]] in [[Set]] by writing:

$$
  \array{
     && Mor(C)
     \\
     & {}^{s}\swarrow
     && \searrow^{t}
     \\
     Obj(C)
     &&&&
     Obj(C)
  }
  \,.
$$

Recall from the above discussion that a morphism $f : c \to d$ in $C$ could act on an element $s \in S$ if the image of $s$ under the anchor map $\lambda$ coincides with the source of $f$, i.e. with the image of $f$ under the source map $s$. Formally this means that the pairs of elements of $S$ and morphisms of $C$ which can be paired by the action live in the [[pullback]] set $S {}_\lambda \times_s Mor(C)$ (the fiber product):

$$
  \array{
     &&
     S {}_\lambda \times_s Mor(C)
     \\
     & {}^{pr_1}\swarrow && \searrow^{pr_2}
     \\
     S
     &&
     && Mor(C)
     \\
     & \searrow^{\lambda}&
     & {}^{s}\swarrow
     && \searrow^{t}
     \\
     &&
     Obj(C)
     &&&&
     Obj(C)
  }
  \,.
$$

Above we have seen that the action of $C$ on $S$ sends every element in this fiber product, which is a pair

$$
  (s \in \rho(c) \subset S, (c \stackrel{f}{\to} d) \in Mor(C))
$$

to an element $\rho(f)(s) \in \rho(d)$. So this is a map of sets $\rho : S {}_\lambda \times_s C \to S$. But a special such map, in that it satisfies a couple of conditions. One condition is that $s \in \rho(c)$ is taken to $\rho(d)$ by $f : c \to d$. This can be encoded by saying that $\rho$ extends to a morphism of [[span]]s from the pullback span above back to $S$:

$$
  \array{
     && S {}_\lambda \times_s Mor(C)
     \\
     & \swarrow && \searrow^{t \circ pr_2}
      \\
     pt &&\downarrow^{\rho}&& Obj(C)
     \\
     & \nwarrow && \nearrow_{\lambda}
     \\
     &&
     S
  }
$$

But $\rho$ satisfies yet another compatibility condition: so far we have only used the source-target mathcing condition of the functor $\rho : C \to Set$. There is also its _functoriality_, i.e. its respect for composition. 

But composition in the category $C$ is itself naturally expressed in terms of morphisms of spans:

the set of composable morphisms $Mor(C) {}_t \times_s Mor(C)$ is itself the tip of a [[span]] arising from composing the [[span]] of $C$ with itself by [[pullback]]:

$$
  \array{ 
     &&&& Mor(C) {}_t\times_s Mor(C)
     \\
     &&& \swarrow
     && \searrow
     \\
     && Mor(C)
     &&&&
     Mor(C)
     \\
     & 
     {}^s\swarrow
     && \searrow^t
     && 
     {}^s\swarrow
     && \searrow^t
     \\  
     Obj(C)
     &&&&
     Obj(C)
     &&&&
     Obj(C)
  }
$$ 

and the composition operation $\circ$ in $C$ is a morphism from this composed span to the original span

$$
  \array{
     && Mor(C) {}_t \times_s Mor(C)
     \\
     & {}^{s \circ pr_1}\swarrow && \searrow^{t \circ pr_2}
      \\
     Obj(C) &&\downarrow^{\circ}&& Obj(C)
     \\
     & {}^{s}\nwarrow && \nearrow_{t}
     \\
     &&
     Mor(C)
  }
  \,.
$$


In total this gives us two different ways to map the total span with tip $S {}_\lambda \times_s Mor(C) {}_t \times_s Mor(C)$ obtained by composing the anchor map span with two copies of the span of $C$ back to the anchor map span

$$
  \array{
     && S {}_\lambda \times_s Mor(C) {}_t \times_s Mor(C)
     \\
     & {}^{}\swarrow && \searrow^{t \circ pr_3}
      \\
     pr &&\downarrow && Obj(C)
     \\
     & {}^{s}\nwarrow && \nearrow_{\lambda}
     \\
     &&
     S
  }
  \,.
$$

The **action property** of $\rho$, which is nothing but the functoriality of $\rho$ in the above description, says precisely that these two morphisms coincide.

Abstractly this says that

* a (small) [[category]] is a [[monad]] in [[span|spans]] in [[Set]];

* the [[action]] of a [[category]] on a [[set]] is an [[algebra]] for this [[monad]].

+--{.query}
Generalizing this slightly, it should be possible to associate an action of a category $C$ on a category $\coprod_{c\in C_0}\rho(c)$ to a functor $\rho:C\rightarrow \Cat$ with the expectation, that this then is just a module for $C$ as a monad.
=--
