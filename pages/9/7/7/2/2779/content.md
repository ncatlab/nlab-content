#Contents#

* automatic table of contents goes here
{:toc}

## Idea ##

On this page, we work work through several of the key examples of **[[limits]]** in the category [[Set]]. This is part of a bigger project: [[Understanding Constructions in Categories]].

Recall that a limit, or universal cone, over a [[diagram]] $F:J\to Set$ is a [[cone]] $T$ over $J$ such that, given any cone $T'$, there is a unique [[cone function]] from $T'$ to $T$.

## Terminal Object ##

A [[terminal object]] is a universal cone over the empty diagram. In this section, we demonstrate how this leads us to the statement:

+-- {: .standout}
Any [[singleton]] (a one-element set) is a [[terminal object]] in $Set$.
=--

To demonstrate, first note that a cone over an empty diagram is just a set and a corresponding cone function is just a function. Therefore, we are looking for a "universal set" $\bullet$ such that for an other set $C$, there is a unique function 

$$f:C\to\bullet.$$

Singletons fill the bill because for any element $c\in C$ we have the unique function defined by

$$f(c) = *.$$

Therefore any singleton is a terminal object in $Set$.

## Product ##

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

## Equalizer ##

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

Let's first define the set
$$Eq = \left\{x\in X|f(x)=g(x)\right\}$$
with two functions $Eq_X:Eq\to X$ and $Eq_Y:Eq\to Y$ defined by
$$Eq_X(x) = x\quad\text{and}\quad Eq_Y(x) = f(x)$$
and verify that it is indeed a cone. The only thing we need to check is that
$$g\circ Eq_X = Eq_Y$$
which amounts to showing that $f(x) = g(x)$ for all $x\in Eq$, but that is the definition of $Eq$, so we do have a cone.

Now let $\phi,\psi: T\to Eq$ be two cone functions. For any element $t\in T$, we have

$$T_X(t) = Eq_X\circ\phi(t) = Eq_X\circ\psi(t)\implies \phi(t)=\psi(t)$$

so that $\phi = \psi$ and the cone function is unique.

Since every cone function $\phi:T\to Eq$ is unique, it follows that $Eq$ together with $Eq_X:Eq\to X$ and $Eq_Y:Eq\to Y$ is a universal cone, i.e. $Eq$ is an equalizer.

## Pullbacks ##

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

To demonstrate, first note that a cospan $F:J\to Set$ produces three sets $X,Y,Z$ with two functions $f:X\to Z$ and $g:Y\to Z$. A cone over the cospan consists of a set $T$ and three components 

$$T_X:T\to X,\quad T_Y:T\to Y,\quad\text{and}\quad T_Z:T\to Z$$

satisfying

$$f\circ T_X = T_Z\quad\text{and}\quad g\circ T_Y = T_Z,$$

which implies, of course,

$$f\circ T_X = g\circ T_Y.$$

Therefore, we are looking for a universal cone $Pb$ such that for any other cone $T$, there is a unique function

$$f:T\to Pb.$$

Let's first define the set
$$Pb = \left\{(x,y)|f(x)=g(y)\right\}$$
with three functions $\pi_X:Pb\to X$, $\pi_Y:Pb\to Y$, and $T_X:Pb\to Z$ defined by
$$\pi_X(x,y) = x,\quad\text{and}\quad \pi_Y(x,y) = y,\quad\text{and}\quad T_Z(x,y) = f(x)$$
and verify that it is indeed a cone. The only thing we need to check is that
$$f\circ\pi_X = g\circ \pi_Y = T_Z$$
which amounts to showing that $f(x) = g(y)$ for all $(x,y)\in Pb$, but that is the definition of $Pb$, so we do have a cone.

Now let $\phi,\psi: T\to Eq$ be two cone functions with 
$$\phi(t) = (\phi_X(t),\phi_Y(t)\quad\text{and}\quad\psi(t) = (\psi_X(t),\psi_Y(t)$$
for functions
$$\phi_X,\psi_X:T\to X\quad\text{and}\quad\phi_Y,\psi_Y:T\to Y.$$
For any element $t\in T$, we have
$$T_X(t) = \pi_X\circ\phi(t) = \pi_X\circ\psi(t)\implies \phi_X(t)=\psi_X(t).$$
Similarly
$$T_Y(t) = \pi_Y\circ\phi(t) = \pi_Y\circ\psi(t)\implies \phi_Y(t)=\psi_Y(t)$$
so that $\phi = \psi$ and the cone function is unique.

Since every cone function $\phi:T\to Pb$ is unique, it follows that $Pb$ together with $\pi_X:Pb\to X$, $\pi_Y:Pb\to Y$, and $T_Z:Pb\to Z$ is a universal cone, i.e. $Pb$ is a pullback.

## Fibred Products ##

**Under Construction**
[[fibred products]]

