

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **double complex** or **bicomplex** is a [[diagram]] of shape $\mathbb{Z}_{\leq} \times \mathbb{Z}_{\leq}$ (in some [[additive category]]):

$$
  \array{
   && \vdots && \vdots
   \\
   & & \downarrow^{\mathrlap{\partial^v}} && \downarrow^{\mathrlap{\partial^v}}
   \\
    \cdots &\to & 
    X_{n,m} &\stackrel{\partial^h}{\to}& X_{n-1,m}
    & \to & \cdots
   \\
   & & \downarrow^{\mathrlap{\partial^v}} && \downarrow^{\mathrlap{\partial^v}}
   \\
    \cdots &\to & 
    X_{n,m-1} &\stackrel{\partial^h}{\to}& X_{n-1,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{\mathrlap{\partial^v}} && \downarrow^{\mathrlap{\partial^v}}
   \\
   && \vdots && \vdots
  }
$$

such that each row and each column is a [[complex]] (the [[differentials]] square to 0: $\partial^v \circ \partial^v = 0$ and $\partial^h \circ \partial^h = 0$) and such that all the squares [[commuting diagram| commute]].

This means that a **double complex** is a [[complex]] in a category of [[complexes]]. 

Accordingly, a **double chain complex** is a [[chain complex]] in a [[category of chain complexes]]. 

$$
  X_{\bullet, \bullet} = 
  \left[
      \cdots \to X_{n,\bullet} \stackrel{\partial^h}{\to} X_{n-1,\bullet} \to \cdots
  \right]
  \,.
$$


In the presence of [[direct sums]], there is a _[[total complex]]_ $(Tot X)_\bullet$ associated to a double complex, which in degree $n$ is the direct sum of all terms of _total degree_ $n$

$$
  (Tot X)_n \coloneqq \oplus_{k+l = n} X_{k,l}.
$$

Often it is such total complexes that are of interest.


The [[differential]] of the total complex is the sum of the horizontal and the vertical differential _made anti-commutative by adjusting signs_. There is a second convention in which one often sees the double complex defined as above from a complex of complexes, but then with the differentials in every second row (or every second column) multiplied by $(-1)$. This is just a different way of sign-bookkeeping, a detailed discussion of this is below. Which convention to use is sometimes influenced by the context, the traditions of the sources in that application of double complexes, and largely a question of taste, that is which one the writer is used to.

Double chain complexes often arise from the application of bifunctors -- [[additive functors]] of two variables -- of [[additive category|additive categories]] $C_1, C_2, C_3$

$$
  F :  C_1 \times C_2 \to C_3
$$

to complexes in their two arguments. Combining this with the formation of [[total complexes]] then yields bifunctors from  categories of complexes to categories of complexes. 

$$
 \tilde F : Ch(C_1) \times Ch(C_2) \to Ch(C_3)
 \,.
$$

The most important examples of this are induced by the [[hom-functor]] and the [[tensor product]] functor together with their [[derived functors]], [[Ext]] and [[Tor]].

Notice that under the [[Dold-Kan correspondence]] and with sufficient [[resolutions]], such $\tilde F$ can be understood as the internal hom or tensor products, etc., between [[infinity-groupoid|higher groupoids]].


Although we suggest (and prefer) the 'complex of complexes' definition, as above, rather than the equivalent  _anticommutiing diagram_ one, we give both and will discuss how to go between them in some detail.

## Definition

### With commuting differentials


A double complex, $X$, is a commutative diagram in an additive category in which  the objects are bi-indexed by the integers, 

$$\{ X_{p,q} \mid p,q\in \mathbb{Z} \}$$

and with two classes of '[[differentials]]' or 'boundary morphisms':

* $d_X^v: X_{p,q}\to X_{p,q-1}$ called the 'vertical boundary morphisms' or 'vertical differentials', with $d_X^v d_X^v = 0$;

and

* $d_X^h: X_{p,q}\to X_{p-1,q}$ called the 'horizontal boundary morphisms' or 'horizontal differentials', with  $d_X^h d_X^h = 0$;

such that all [[commuting diagram|squares commute]]

* $d_X^h \circ d_X^v = d_X^v \circ d_X^h$. 

(To state the obvious, this means $d_X^h d_X^v - d_X^v d_X^h=0$, in contrast to the formula in the second version [below](#AntiCommutingDifferentials).)

This gives a commutative diagram:

$$
  \array{
   && \vdots && \vdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n,m} &\stackrel{d_X^h}{\to}& X_{n,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n-1,m} &\stackrel{d_X^h}{\to}& X_{n-1,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
   && \vdots && \vdots
  }
$$

### With anti-commuting differentials
 {#AntiCommutingDifferentials}


A double complex, $X$, is an anticommutative diagram in an additive category in which the objects are bi-indexed by the integers, 

$$\{ X_{p,q} \mid p,q\in \mathbb{Z} \}$$

and with two classes of 'differentials' or 'boundary morphisms':

* $d_X^v: X_{p,q}\to X_{p,q-1}$ called the 'vertical boundary morphisms' or 'vertical differentials', with $d_X^v d_X^v = 0$;

and

* $\bar{d}_X^h: X_{p,q}\to X_{p-1,q}$ called the 'horizontal boundary morphisms' or 'horizontal differentials', with  $\bar{d}_X^h \bar{d}_X^h = 0$;

in addition $\bar{d}_X^h d_X^v + d_X^v \bar{d}_X^h = 0$.

This gives an anticommutative diagram:
$$
  \array{
   && \vdots && \vdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n,m} &\stackrel{\bar{d}_X^h}{\to}& X_{n,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} & \swArr_{-1} & \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n-1,m} &\stackrel{\bar{d}_X^h}{\to}& X_{n-1,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
   && \vdots && \vdots
  }
$$


### Equivalence of the two definitions
 {#EquivalenceOfTheTwoDefinitions}

Which definition is 'better'? 'Commuting squares', i.e., the first version, is convenient if you want to define a double complex as a chain complex in the category of chain complexes. On the other hand, 'anticommuting squares' and version 2 is sometimes convenient for defining the total complex (for computing total homology). Does it matter which you use? The following says they are just two views of the same situation.



One makes a double complex $X$ with commutative squares into a double complex with anticommutative squares by using the same vertical differential $d^v$ but taking $\bar{d}^h : X_{p,q} \to X_{p,q-1}$ to be $(-1)^p d^h$. The same trick can, of course, be used to make a double complex with anticommutative squares into a double complex with commutative squares.

## Properties

### Total complex of a double complex

The **[[total complex]]** of a double complex (under the convention that squares commute) is

$$
  tot_{\oplus}^k = \bigoplus_{m+n=k} X_{n,m}
$$

$$
  d^k_{tot_\oplus}|_{X_{n,m}} = 
  d^v_X + (-1)^\bullet d_X^h 
$$

Similarly, one can define the product total complex as

$$
  tot_{\prod}^k = \prod_{m+n=k} X_{n,m}
$$
$$
  d^k_{tot_\prod}|_{X_{n,m}} = 
  d^v_X + (-1)^\bullet d_X^h 
$$

Note that these two coincide when the set of non-zero objects $X_{n,m}$ such that $n + m = k$ is finite, for example, when $X$ is a first quadrant double complex.

### Fundamental lemmas

There is series of basic [[lemmas]] in [[homological algebra]] 
which determine the horizontal/vertical [[homology groups]] of a double complex in some row or column from exactness information in other columns.
The most fundamental of these is maybe the 

* [[salamander lemma]]

from which a series of others follow:

* [[snake lemma]] (see also [[connecting homomorphism]] and [[long exact sequence in homology]])

* [[3x3 lemma]]

* [[5-lemma]]

* [[horseshoe lemma]] .

## Relation to homotopy colimits

The total complex of the double complex induced by a [[chain map]]
is a model for the [[mapping cone]] of that map, see at _[mapping cone -- via double complexes](mapping+cone#ConeViaDoubleComplex) for more.

[[!redirects double complexes]]

[[!redirects bicomplex]]
[[!redirects bicomplexes]]
[[!redirects bi-complex]]
[[!redirects bi-complexes]]

[[!redirects double chain complex]]
[[!redirects double chain complexes]]
