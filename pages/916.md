# Idea #

A _partial function_ $f: A \to B$ is like a [[function]] from $A$ to $B$ except that $f(x)$ may not be defined for every element $x$ of $A$.  (Compare a [[multi-valued function]], where $f(x)$ may have several possible values.)

In some fields (including secondary-school mathematics even today), functions are often considered to be parital by default, requiring one to specify a _total_ function otherwise.  As category-theoretic and type-theoretic formalisation spreads, this is difficult to treat as the basic concept, and the most modern idea is that a function must be total.  If you want partial functions, then you can get them in terms of total functions as below.

# Definition #

Given [[set]]s $A$ and $B$, a __partial function__ $f$ from a $A$ to $B$ consists a [[subset]] $D$ of $A$ and a (total) function from $D$ to $B$.  In more detail, this is a [[span]]
$$ \array {
  &                & D \\
  & \swarrow_\iota &   & \searrow^f \\
A &                &   &            & B \\
} $$
of total functions, where $\iota: D \to A$ is an [[injection]].  (This condition can be dropped to define a partial [[multi-valued function]], which is simply a span.)

$A$ and $B$ are called the _[[source]]_ and _[[target]]_ of $f$ as usual; then $D$ is the __domain__ of $f$ and $\iota: D \to A $ is the __inclusion__ of the domain into the source.  By abuse of notation, the partial function $f$ is conflated with the (total) function $f: D \to B$.

Notice that the induced function $D \to A \times B$ is an [[injection]], so a partial function is the same as a [[functional relation]] seen from a different point of view.

We consider two partial functions (with the same given source and target) to be __equal__ if there is a [[bijection]] between their domains that makes the obvious diagrams commute.  You can get this automatically in a traditional set theory by requiring $D$ to be literally a [[subset]] of $A$ (with $\iota$ the inclusion map).

# Examples #

In secondary-school mathematics, one often makes functions partial by fiat, just to see if students can calculate the domains of composite functions and the like.  This is not (only) busywork, as in applications one often has a function given by a formula that is really valid only on a certain domain.  However, in a more sophisticated analysis (such as those that Lawvere and his followers propose for physics and synthetic geometry), these domains and the total functions on them become the primary objects of study, with the partial functions being secondary (as $\iota$ is seen as merely a way to place _coordinates_ on $D$).

In analysis, one often considers partial functions whose domains are required to be intervals (in the real line) or regions (in the complex plane).

In a [[field]], the multiplicative [[inverse]] is a partial function whose domain is the set of non-zero elements of the field.