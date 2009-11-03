**Warning: This page is under construction. Feedback welcome.**

See [[Understanding Constructions in Categories]]

## Idea

[[Set]]...

* [[Objects]] are [[sets]]
* [[Morphisms]] are [[functions]]

***

## Limits

Recall that a [[limit]], or universal cone, over a [[diagram]] $F:J\to Set$ is a [[cone]] $T$ over $J$ such that, given any cone $T'$, there is a unique [[cone function]] from $T'$ to $T$.

#### Terminal Object

A [[terminal object]] is a universal cone over the empty diagram. In this section, we demonstrate how this leads us to the statement:

+-- {: .standout}
Any [[singleton]] (a one-element set) is a [[terminal object]] in $Set$.
=--

To demonstrate, first note that a cone over an empty diagram is just an set and a corresponding cone function is just a function. Therefore, we are looking for a "universal set" $\bullet$ such that for an other set $C$, there is a unique function 

$$f:C\to\bullet.$$

Singletons fill the bill because for any element $c\in C$ we have the unique function defined by

$$f(c) = *.$$

Therefore any singleton is a terminal object in $Set$.

#### Product

A [[product]] is a universal cone over a discrete diagram. In this section, we demonstrate how this leads us to the statement:

+--{: .standout}
Any [[cartesian product]] is a [[product]] in $Set$.
=--

To demonstrate, first note that a discrete diagram $F:J\to Set$ produces a family of sets $(A_i)$ with no functions between them. A cone over the discrete diagram consists of a set $T$ and a single component 

$$\f_i:T\to A_i$$

for each set $A_i$. Therefore, we are looking for a universal cone $\prod_i A_i$ such that for any other cone $T$, there is a unique cone function

$$f:T\to\prod_i A_i.$$

Cartesian product fills the bill because for any $t\in T$, we have the unique function defined by

$$f(t) = \prod_i f_i(t).$$

This function is unique because with any other function

$$g:T\to\prod_i A_i$$

with $\pi_i\circ g = f_i$, then for any element $t\in T$

$$g(t) = \prod_i f_i(t) = \left(\prod_i f_i\right)(t) = f(t).$$

Therefore $f = g$.

#### Equalizer

An [[equalizer]] is the universal cone over a parallel diagram
$$\bullet\rightrightarrows\bullet.$$
In this section, we demonstrate how this leads us to the statement:

+--{: .standout}
The [[equalizer]] of two functions is the subset on which both functions coincide.
=--

To demonstrate, first note that a parallel diagram $F:J\to Set$ produces two sets $X,Y$ with two [[parallel morphism|parallel functions]] $f,g:X\to Y$. A cone over the parallel diagram consists of a set $T$ and two components 

$$T_X:T\to X\quad\text{and}\quad T_Y:T\to Y.$$

This is the first example we encounter where the diagram contains morphisms so recall that with a cone we also want the the component diagrams to commute, i.e. we want

$$f\circ T_X = T_Y\quad\text{and}\quad g\circ T_X = T_Y.$$

Therefore, we are looking for a universal cone $Eq$ such that for any other cone $T$, there is a unique function

$$f:T\to Eq.$$

**Is it a cone?**

Let's first define the set
$$Eq = \left\{x\in X|f(x)=g(x)\right\}$$
with two functions $Eq_X:Eq\to X$ and $Eq_Y:Eq\to Y$ defined by
$$Eq_X(x) = x\quad\text{and}\quad Eq_Y(x) = f(x)$$
and verify that it is indeed a cone. The only thing we need to check is that
$$g\circ Eq_X = Eq_Y$$
which amounts to showing that $f(x) = g(x)$ for all $x\in Eq$, but that is the definition of $Eq$, so we do have a cone.

**What is a cone function?**

Let $T$ be any set and $\phi:T\to Eq$ a function such that

$$T_X = Eq_X\circ \phi\quad\text{and}\quad T_Y = Eq_Y\circ \phi.$$

It follows that
$$f\circ T_X = f\circ Eq_X\circ \phi = Eq_Y\circ \phi = T_Y$$
and
$$g\circ T_X = g\circ Eq_X\circ \phi = Eq_Y\circ \phi = T_Y.$$
showing that $T$ is also a cone and $\phi$ is a cone function.

**Is the cone function unique?**

Let $\phi,\psi: T\to Eq$ be two cone functions. For any element $t\in T$, we have

$$T_X(t) = Eq_X\circ\phi(t) = Eq_X\circ\psi(t)\implies \phi(t)=\psi(t)$$

so that $\phi = \psi$ and the cone function is unique.

Since every cone function $\phi:T\to Eq$ is unique, it follows that $Eq$ is a universal cone and $Eq$ together with $Eq_X:Eq\to X$ and $Eq_Y:Eq\to Y$ is an equalizer.

#### Pullbacks

A [[pullback]] is a universal cone over a [[cospan]]
$$
  \array{
     && \bullet &&&& \bullet
      \\
      & 
      && \searrow
       &
       & \swarrow
      && 
     \\
     
     &&&&
     \bullet
     &&&&
  }.
$$
In this section, we demonstrate how this leads us to the statement:

+--{.standout}
The [[pullback]] of two functions of sets is the set of pairs $(x,y)$ such that $f(x)=g(y)$.
=--

**Under Construction**

Why?

#### Fibred Products

[[fibred products]]

***

## Colimits

[[colimits]]

#### Initial Object

The empty set $\emptyset$ is the [[initial object]] in Set.

Why?

#### Binary Coproducts

 binary [[coproducts]]

#### Arbitray Small Coproducts

arbitrary (but small) [[coproducts]]

#### Coequalizers
 
[[coequalisers]]

#### Pushouts

[[pushouts]]

#### Cofibred Products

[[cofibred coproducts]]

***

## Other Constructions ##

#### Exponential Objects

[[exponential objects]]

#### Dependent Products

[[dependent products]]

#### Power Objects

[[power objects]]

## Discussion ##

+--{.query}
[[Eric]]: How is this (note: terminal object) the universal cone over the empty diagram?

_Toby_:  It seems to me that this is really a question about terminal objects in general than about terminal objects in $Set$.  A cone over the empty diagram is simply an object, and a morphism of cones over the empty diagram is simply a morphism.  A universal cone over a diagram $J$ is a cone $T$ over $J$ such that, given any cone $C$, there is a unique cone morphism from $C$ to $T$.  So a univeral cone over the empty diagram is an object $T$ such that, given any object $C$, there is a unique morphism from $C$ to $T$.  In other words, a universal cone over the empty diagram is a terminal object.

I don\'t see the point of the last paragraph before this query box.  Already at the end of the previous paragraph, we\'ve proved that $\bullet$ is a terminal object, since there is a unique function (morphism) to $\bullet$ from any set (object) $C$.  It almost looks like you wrote that paragraph by modifying the paragraph that *I* had written in that place, but that paragraph did something different: it proved that ${!}$ was unique.  Apparently, you thought that this was obvious, since you simply added the word 'unique' to the previous paragraph.

Alternatively, if you *want* to keep a paragraph that proves unicity, then you can remove 'unique' and rewrite my original unicity proof in terminology more like yours, as follows:
> Now let ${!}'\colon C \to \bullet$ be any function. Then
> $$ {!}'(z) = * = {!}(z)$$
> for any element $z$ of $C$, so ${!}' = {!}$.

[[Eric]]: Thanks Toby. I think what I'm looking for is a way to understand that a singleton set is the universal cone over the empty diagram. All these items should be seen as special cases of [[limit]]. Unfortunately, I don't understand limit well enough to explain it. In fact, that is one of the reasons to create this page, i.e. so that I can understand limits :)

The preceding paragraph was my attempt to make it look like a limit, but I obviously failed :)

Ideally, this section would show how terminal object is a special case of limit somehow.

=--


[[!redirects Understanding Set]]
[[!redirects Understanding Constructions on Set]]
[[!redirects understanding constructions in Set]]
[[!redirects understanding Set]]
[[!redirects understanding constructions on Set]]
