<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This entry is about the text

* [[Jacob Lurie]], _A Survey of Elliptic Cohomology_ ([pdf](http://www-math.mit.edu/~lurie/papers/survey.pdf))

It 

* reviews basics of [[elliptic cohomology]]

* indicates the construction of the [[tmf]]-[[spectrum]]

* and discusses this in the context of [[equivariant cohomology]].

The central theorem is 

* the realization of the moduli space of [[elliptic curve]]s as a [[structured (∞,1)-topos]] 

* with a structure [[(∞,1)-sheaf]] of [[E-∞ ring]]-valued functions 

* such that the [[tmf]]-[[spectrum]] is the [[E-∞ ring]] of global sections of this structure sheaf.

=--

#Table of Contents#

1. [Summary](#Summary)

   The following entry has some paragraphs that summarize central ideas.

   1. [gluing all elliptic cohomology theories to the tmf spectrum](#gluingallellipticcohomologytheoriestothetmfspectrum)

   1. [interpretation in terms of higher topos theory](#interpretationintermsofhighertopostheory)

1. Partial surveys

   These links point to pages that contain notes on aspects of the theory that are in the style of and originate from [a seminar on A Survey of Elliptic Cohomology](http://nd.edu/~rgrady/seminar.html):

   1. [[A Survey of Eilliptic Cohomology - cohomology theories]]

   1. [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

   1. [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

   1. [[A Survey of Elliptic Cohomology - elliptic curves]]

   1. [[A Survey of Elliptic Cohomology - equivariant cohomology]]

   1. [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

   1. [[A Survey of Elliptic Cohomology - A-equivariant cohomology]]

   1. [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves]]

1. towards geometric models

    These links point to pages that have an exposition of the Stolz-Teichner program for constructing [[geometric models for elliptic cohomology]].

* Outline of the constructions and statements

  * [[Axiomatic field theories and their motivation from topology]]

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

  * [[(2,1)-dimensional Euclidean field theories and tmf]]

* Definitions

  * [[bordism categories following Stolz-Teichner]]

  * [[(2,1)-dimensional Euclidean field theories]]

#Contents#

Here is the table of contents of the Survey reproduced. Behind the links are linked keyword lists for relevant terms.

* automatic table of contents goes here
{:toc}

#Summary {#Summary}

The text starts with showing or recalling that 

* the collection of all [[elliptic cohomology]] theories 
and 

* the gluing of their representing [[spectrum|spectra]] into the single [[tmf]] spectrum 

is best understood in terms of global sections of the structure sheaf of functions on the refinement of the moduli [[space]] of all elliptic curves to a [[structured (∞,1)-topos]].

Then it uses this [[higher topos theory|higher topos theoretic]] [[derived algebraic geometry]] perspective to analyze further properties of [[elliptic cohomology]] theories, in particular their refinements to [[equivariant cohomology]].

## gluing all elliptic cohomology theories to the tmf spectrum {#gluingallellipticcohomologytheoriestothetmfspectrum}

The triple of [[generalized (Eilenberg-Steenrod) cohomology]] theories

1. periodic ordinary [[integral cohomology]]

1. complex [[K-theory]]

1. [[elliptic cohomology]]

constitutes the collection of all possible [[generalized (Eilenberg-Steenrod) cohomology]] theories with the extra [[stuff, structure, property|property]] that they are

* [[multiplicative cohomology theory|multiplicative]]

and

* [[periodic cohomology theory|periodic]].

It so happens that all multiplicaive periodic generalized Eilenberg-Steenrod cohomology theories $A$ are characterized by the [[formal group]] (an [[infinitesimal space|infinitesimal]] [[group]]) whose [[ring]] of functions is the [[cohomology ring]] $A(\mathbb{C}P^\infty)$ obtained by evaluating $A$ on the complex projective space $\mathbb{C}P^\infty \simeq \mathcal{B} U(1)$ -- the [[classifying space]] for complex [[line bundle]]s -- and whose group product is induced from the morphism $\mathbb{C}P^\infty \times \mathbb{C}P^\infty \to \mathbb{C}P^\infty$ that representes the [[tensor product]] of complex [[line bundle]]s.

There are precicely three different types of such formal groups:

* the additive formal group (a single one)

* the multiplicative formal group (a single one)

* a formal group defined by an [[elliptic curve]] (many).

The first case corresponds to periodic [[integral cohomology]]. The second corresponds to complex [[K-theory]]. Each element in the third family corresponds to one flavor of [[elliptic cohomology]].

It is therefore natural to subsume all elliptic cohomology theories into one single cohomology theory. This is the theory called [[tmf]].

It turns out that the right way to formalize what "subsume" means in the above sentence involves formulating the way in which an [[elliptic cohomology]] theory is associated to a given [[elliptic curve]] in the correct [[higher category theory|higher categorical]] language:

The collection of all 1-dimensional [[elliptic curve]]s forms a generalized [[space]] $M_{1,1}$ -- a [[stack]] -- defined by the property that it is the [[classifying space]] for elliptic curves in that elliptic curves over a ring $R$ correspond to classifying maps $\phi : Spec R \to M_{1,1}$.

Then the classical assignment of an [[elliptic cohomology]]  theory to an [[elliptic curve]] is an assignment

$$
  \{\phi : Spec R \to M_{1,1}\}
  \to
  CohomologyTheories
  \,.
$$

We may think of maps $Spec R \to M_{1,1}$ as picking certain subsets of the generalized [[space]] $M_{1,1}$ and of morphisms

$$
  \array{
     Spec(R) &&\to&& Spec(R')
     \\   
     & \searrow && \swarrow
     \\
     && M_{1,1}
  }
$$

as maps between such subsets. Hence the assignment of cohomology theories to elliptic curves is much like a [[sheaf]] of cohomology theories on the moduli [[space]] ([[stack]]) of [[elliptic curve]]s.

In order to _glue_ all elliptic cohomology theories in some way one would like to take something like the [[category of elements]] of this [[sheaf]], i.e. its [[homotopy limit]]. In order to say what that should mean, one has to specify the suitable nature of the codomain, the collection of "all cohomology theories".

As emphasized at [[generalized (Eilenberg-Steenrod) cohomology]], the best way to do this is to identify a generalized (Eilenberg-Steenrod) cohomology theory with the [[spectrum]] that represents it. It is and was well known how to do this for each elliptic curve seperately. What is not so clear is how this can be done coherently for all elliptic curves at once: we need a lift of the above cohomology-theory-valued sheaf to a sheaf of representing [[spectrum|spectra]]

$$
  \array{
    && Spectra
    \\
    & {}^{?}\nearrow & \;\;\;\downarrow^{represent}
    \\
    \{\phi : Spec R \to M_{1,1}\}
    &\to&
    CohomologyTheories
  }
  \,.
$$

In this generality this turns out to be a hard problem. But by definition here we are really interested just in the special case where all cohomology theories in question are [[multiplicative cohomology theory|multiplicative cohomology theories]] and where hence all spectra in question are [[commutative ring spectrum|commutative ring spectra]]

$$
  \array{
    && CommRingSpectra
    \\
    & {}^{O_{M^{der}}}\nearrow & \downarrow
    \\
    \{\phi : Spec R \to M_{1,1}\}
    &\to&
    MultiplicativeCohomologyTheories
  }
  \,.
$$

As indicated, this problem does turn out to have a solution: Goerss, [[Mike Hopkins|Hopkins]] and Miller showed that the desired lift denoted $O_{M^{der}}$ above exists.

Accordingly, one can then obtain the [[tmf]] spectrum as the [[homotopy limit]] of this sheaf of [[E-∞ ring]]s $O_{M^{der}}$. Recall from the discussion at [[limit in a quasi-category]] that such a homotopy limit computes global sections. It is an $\infty$-version of computing sections in a [[Grothendieck construction]], really, as described there.

## interpretation in terms of higher topos theory {#interpretationintermsofhighertopostheory}

What is noteworthy about the above construction is that, as the notation above suggests, sheaves of [[E-infinity ring]]s generalize sheaves of rings as thery are familiar from the theory of [[ringed space]]s, where they are called **structure sheaves**.

Accordingly, the morphism $O_{M^{der}}$ makes the moduli [[space]] of elliptic curves into a [[structured (∞,1)-topos]].

This perspective embeds the theory of [[elliptic cohomology]] and of the [[tmf]] spectrum as an application into the general context of [[higher topos theory]] and [[derived algebraic geometry]]. 

## equivariant elliptic cohomology {#equivariantellipticcohomology}


...



# Contents {#Contents}


## 1. Elliptic Cohomology {#EllipticCohomology}

### 1.1 Cohomology Theories {#CohomologyTheories}


* [[cohomology]]

  * [[generalized (Eilenberg-Steenrod) cohomology]]

  * [[integral cohomology]]

  * [[K-theory]]

  * [[elliptic cohomology]]

* [[multiplicative cohomology theory]]

* [[periodic cohomology theory]]

* [[topological modular form]]

### 1.2 Formal Groups from Cohomology Theories {#FormalgroupsFromCohomologyTheories} 

* [[formal group]]

### 1.3 Elliptic Cohomolohy {#EllipticCohomology}

* [[elliptic curve]]

* [[elliptic cohomology]]

* [[E-∞ ring]]


## 2 Derived Algebraic geometry {#DerivedAlgebraicCohomology}

* [[derived algebraic geometry]]

  * [[higher topos theory]]

  * [[higher algebra]]



### 2.1 $E_\infty$ rings

* [[commutative algebra in an (∞,1)-category]]

* [[E-∞ ring]]

* [[commutative ring spectrum]]

### 2.2 Derived Schemes

* [[structured (∞,1)-topos]]

* [[derived scheme]]

## 3 Derived Group Schemes and Orientations

* [[group scheme]]

### 3.1 Orientations of the Multiplicative Group

### 3.2 Orientations of the Additive Group

### 3.3 The Geometry of Preorientations

### 3.4 Equuivariant $A$-Cohomology for Abelian Groups

### 3.5 The Nonabelian Case

## 4 Oriented Elliptic Curves

### 4.1 Construction of the Moduli Stack

### 4.2 The Proof of Theorem 4.4: The Local Case

### 4.3 Elliptic Cohomology near $\infty$

## 5 Applications


### 5.1 2-Equivariant Elliptic Cohomology


### 5.2 Loop Group Representations

* [[loop group]]

### 5.3 String Orientation

* [[string structure]]

### 5.4 Higher Equivariance


### 5.5 Elliptic Cohomology and Geometry


# further references {#furtherreferences}

Lots of literature on [[modular form]]s is collected at.

* [[Nora Ganter]], [Topological modular forms literature list](http://www.math.uiuc.edu/~ganter/talbot/index.html)

In its currently underdeveloped state, a canonmical reference for aspects of the theory of [[derived algebraic geometry]] over [[E-infinity ring]]s has become the set of slides

* [[Paul Goerss]], [[Topological Algebraic Geometry - A Workshop]]

Now this article has appeared

* [[Paul Goerss]], _Topological modular forms (aftern Hopkins, Miller, and Lurie)_ ([arXiv](http://arxiv.org/abs/0910.5130))

