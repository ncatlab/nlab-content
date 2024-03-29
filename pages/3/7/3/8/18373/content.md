
#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn }
###### Definition

The **infinitesimally thickened Sierpinski topos** is the topos of presheaves on the ordinal category $\mathbf{3}: \{ 0 \to 1 \to 2 \}$. The name emphasizes the view of this topos as exhibiting [[differential cohesion]] over the cohesive [[Sierpinski topos]] using the coreflective embedding $i : \mathbf{2} \hookrightarrow \mathbf{3}$ sending $0$ to $0$ and $1$ to $2$.

The objects of the category are diagrams $A_2 \to A_1 \to A_0$ in $Set$ and arrows are commuting squares.

=--

## Properties


### Differential cohesion
 {#DifferentialCohesion}

We can view objects of the topos as exhibiting a simple notion of differential cohesion: in $A_r \to A_{inf} \to A_p$ the $A_r$ are the "real" points, the $A_{inf}$ are the "infinitesimal" points and the $A_p$ are the "pieces", i.e., connected components.

The coreflective embedding above results in an adjoint quadruple

$$
 ( i_! \dashv i^* \dashv i_* \dashv i^! )
  :
  PSh(\mathbf{3})
  \stackrel{\overset{i_!}{\hookleftarrow}}{\stackrel{\overset{i^*}{\to}}{\stackrel{\overset{i_*}{\hookleftarrow}}{\stackrel{i^!}{\to}}}}

  PSh(\mathbf{2})
  \,.
$$

which are defined explicitly as follows:

$$ i_!(A_1 \to A_0) = A_1 \to A_1 \to A_0 $$
$$i^*(A_2 \to A_1 \to A_0) = A_2 \to A_0$$
$$i_*(A_1 \to A_0) =  A_1 \to A_0 \to A_0$$
$$ i^!(A_2 \to A_1 \to A_0) = A_2 \to A_1$$

This gives us elementary characterizations of the various subcategories of $Sh(\mathbf{3})$ involved in differential cohesion:

* The [[reduced object|reduced objects]] are the image of $i_!$: so they have the same real and infinitesimal points.
* The [[coreduced object|coreduced objects]] are the image of $i_*$: pieces all consist of exactly one infinitesimal point.

and the differential modalities are defined as:
$$ \Re(A_2 \to A_1 \to A_0) = A_2 \to A_2 \to A_0$$
$$ \Im(A_2 \to A_1 \to A_0) = A_2 \to A_0 \to A_0$$
$$ \&(A_2 \to A_1 \to A_0) = A_2 \to A_1 \to A_1$$

The cohesive structure

$$
  (\Pi \dashv \Disc \dashv \Gamma \dashv coDisc)
  : 
  Psh(\mathbf{3})
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  Set
  \,.
$$
factors through the cohesive structure of the Sierpinski topos and is defined as:

$$\Pi(A_2\to A_1 \to A_0) = A_0$$
$$\Disc(A) = A \to A \to A$$
$$\Gamma(A_2 \to A_1 \to A_0) = A_2$$
$$coDisc(A) = A \to 1 \to 1$$

Giving us two more subcategories:

* The [[discrete object| discrete objects]] are the image of $\Disc$: every piece consists of exactly one real point.
* The [[codiscrete object|codiscrete objects]] are the image of $coDisc$: they consist of exactly one piece with exactly one infinitesimal point that all of the real points are over.

This is reflective of the general phenomenon that discrete objects are reduced and coreduced, in fact here the discrete objects are *exactly* the intersection of reduced and coreduced objects.

And the cohesive modalities are defines as:
$$ &#643;(A_2 \to A_1 \to A_0) = A_0 \to A_0 \to A_0$$
$$ \flat(A_2 \to A_1 \to A_0) = A_2 \to A_2 \to A_2$$
$$ \sharp(A_2 \to A_1 \to A_0) = A_2 \to 1 \to 1$$

#### Constructions in Differential Cohesion

A morphism $f : A \to B$ is [[formally etale morphism|formally etale]] when the square

$$
  \array{
    A_1 &\to& A_0
    \\
    \downarrow^{\mathrlap{f_1}} && \downarrow^{\mathrlap{f_0}}
    \\
    B_1 &\to& B_0
  }
$$

is a pullback. This makes it easy to see explicitly that coreduced objects are exactly the objects with $A \to 1$ formally etale.

The [[infinitesimal disk bundle]] of $A_2 \overset{inf}{\to}A_1 \overset{pc}{\to} A_0$ is the pullback of the unit of $\Im$ along itself. Since pullbacks are computed pointwise in a presheaf topos, this is just:

$$TA = A_2 \to \{(x_i,y_i) \in A_1 | pc(x_i) = pc(y_i) \} \to A_0$$

with the fiber of some real point $x_r \in A_2$ given by:

$$\{x_r \} \to \{y_i \in A_1 | pc(y_i) = pc(inf(x_r)) \} \to \{pc(inf(x_r)) \}$$

which is an [[infinitesimally thickened point]].