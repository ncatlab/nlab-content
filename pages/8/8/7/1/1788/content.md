+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***
##### Correspondences of groupoids 
 {#CorrespondencesOfGroupoids}

+-- {: .num_defn}
###### Definition

Write [[Grpd]] for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]] $\mathcal{G}$;

* [[morphisms]] are [[functors]] $f \colon \mathcal{G} \to \mathcal{K}$;

* [[2-morphisms]] are [[homotopies]] between these.

=--

+-- {: .num_defn}
###### Definition

Write $Span_1(Grpd)$ for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]];

* [[morphisms]] are [[spans]] of [[functors]]

  $$
    \array{
     A
      &\leftarrow&
      X
      &\rightarrow&
     B
     }
     \,;
  $$

* [[2-morphisms]] are [[diagrams]] of the form

  $$
    \array{  
      && X_1
      \\
      & \swarrow &\downarrow& \searrow
      \\
      A &\seArrow& \downarrow^{\mathrlap{\simeq}} &\swArrow& B
      \\
      & \nwarrow &\downarrow& \nearrow
      \\
      && X_2
    }
    \,.
  $$

=--

+-- {: .num_prop #GroupoidInSpanOneIsSelfDual}
###### Proposition

Every [[groupoid]] $X \in Grpd \hookrightarrow Span_1(Grpd)$ 
is a [[dualizable object]] in 
$Span_1(Grpd)$, and in fact is self-dual.

The [[evaluation map]] is given by the [[span]]

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && && [\Pi_1(S^0),\mathbf{B}G] &\simeq& \mathbf{B}G \times \mathbf{B}G
  }
$$

and the [[coevaluation map]] by the reverse span.

=--

+-- {: .num_prop}
###### Proposition

For $X \in Grpd \hookrightarrow Span_1(Grpd)$ any object,
the [[trace]] of the [[identity]] on it is its 
[[free loop space object]], prop. \ref{FreeLoopSpaceOfGroupoid}:

$$
  tr(id_X) \simeq 
  \left(
    \array{
      && [\Pi_1(S^1), X]
      \\
      & \swarrow && \searrow
      \\
      \ast && && \ast
    }
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{GroupoidInSpanOneIsSelfDual}
the [[trace]] of the identity is given by the composite span

$$
  \array{
    && && X \underset{[\Pi_1(S^1), X]}{\times} X
    \\
    && & \swarrow && \searrow
    \\
    && X && \swArrow && X
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast
    &&
    &&
    [\Pi_1(S^0),X]
    &&
    &&
    \ast
  }
  \,.
$$

By prop. \ref{FreeLoopSpaceOfGroupoid} we have

$$
  X \underset{[\Pi_1(S^1), X]}{\times} X
  \simeq [\Pi_1(S^1), X]
  \,.
$$

=--

##### 1d DW local field theory 
 {#1dDWLocalFieldTheory}

+-- {: .num_defn}
###### Definition

Write $Span_1(Grpd, \flat\mathbf{B}U(1))$
for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]] $X$ equipped with a morpism

  $$
    \left[
      \array{
         X
         \\
         \downarrow^{\mathrlap{f}}
         \\
         \mathbf{B}\flat U(1)
      }
    \right]
  $$

* [[morphisms]] are [[spans]] $X_1 \leftarrow Y \rightarrow X_2$ equipped with a [[homotopy]] $\phi$ in 

  $$
    \array{
       && Y
       \\
       & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
       \\
       X_1 && \swArrow_{\phi} && X_2
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}\flat U(1)
    }
  $$

* [[2-morphisms]] are ...

=--

+-- {: .num_prop}
###### Proposition

$Span_1(Grpd, \mathbf{B}\flat U(1))$ carries the structure of a
[[symmetric monoidal (infinity,n)-category|symmetric monoidal (2,1)-category]] where the [[tensor product]] is given by

$$
  \left[
    \array{  
       X_1
       \\
       \downarrow^{\mathrlap{f_1}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \otimes
  \left[
    \array{  
       X_2
       \\
       \downarrow^{\mathrlap{f_2}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
    \array{  
       X_1 \times X_2
       \\
       \downarrow^{\mathrlap{f_1 \circ p_1 + f_2 \circ p_2}}
       \;\;\;\;\;\;\;\;
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Every object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \in Span_1(Grpd,\mathbf{B}\flat U(1))
$$

is a [[dualizable object]], with dual object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{-\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
$$

and with [[evaluation map]] given by

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\mathrlap{\simeq}} && X \times X
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{f \circ p_1 - f \circ p_2}}
    \\
    && \mathbf{B}\flat U(1)
  }
  \,.
$$


=--


+-- {: .num_prop}
###### Proposition

The prequantum field theory defined by a [[group character]]

  $$
    \left[
      \array{
	    \mathbf{Field}
		\\
                \downarrow^{\mathrlap{S}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]
	\;\;
	:=
	\;\;
    \left[
      \array{
	    \mathbf{B}G
		\\
                \downarrow^{\mathrlap{c}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]	
      \in Span_1(Grpd,\mathbf{B}\flat U(1))
  $$

  assigns to the [[circle]] the [[trace]] of the idenity on this object, which is 


$$
  \array{
    && && [\Pi_1(S^1), \mathbf{B}G]
    \\
    && & \swarrow && \searrow
    \\
    && \mathbf{B}G && \swArrow && \mathbf{B}G
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast && && \mathbf{B}G \times \mathbf{B}G && && \ast
    \\
    &{}_0\searrow & && \downarrow^{\mathrlap{S(p_1) - S(p_2)}}
    &&& \swarrow_{0}
    \\
    &&&& \mathbf{B}\flat U(1)
  }
  \;\;\;
   \simeq
  \;\;\;
  \array{
    && [\Pi(S^1), \mathbf{B}G]
    \\
    && \downarrow^{\mathrlap{c}}
    \\
    && \flat U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \;\;\;
$$

Here the [[action functional]] on the right  sends a [[field configuration]] $g \in G = [\Pi(S^1), \mathbf{B}G]_0$
  to its value $c(g) \in U(1) = (\flat \mathbf{B}U(1))_1$.

=--

(...)

#### 2d Dijkgraaf-Witten theory

(...)

#### 3d Dijkgraaf-Witten theory
 {#3dDWLocalPrequantumFieldTheory}

The [[group character]] $c : G \to U(1)$ which defines 
1-dimensional prequantum Dijkgraaf-Witten theory
in [1d Dijkgraaf-Witten theory](#1dDWTheory) is equivalently a [[cocycle]] in degree-1 [[group cohomology]]

$$
  [c] \in H_{\mathrm{Grp}}(G,U(1))
  \,.
$$

In view of this it is plausible that one may interpret a cocycle in degree-$n$ group cohomology, for 
all $n \in \mathbb{N}$ as a higher order [[action functional]]
$\mathbf{B}G \to \flat\mathbf{B}^n U(1)$ and induce an 
$n$-dimensional local prequantum Dijkgraaf-Witten-type theory
from it. 

Here we review how to formalize this and then consider the
example of DW theory in dimension 3.



### Higher Chern-Simons local prequantum field theory
 {#HigherChern-SimonsLocalPrequantumFieldTheory}

(...)

#### $d = n + 1$, Universal topological Yang-Mills theory

(...)

#### $d = n + 0$, Higher Chern-Simons field theories

(...)


#### $d = n-1$, Topological Chern-Simons boundaries

(...)

#### $d = n-k$, Dimensional reduction

(...)

#### $d = n-1$, Wess-Zumino-Witten field theories

(...)

#### $d = n-2$, Wilson loop/Wilson surface field theories

(...)

## Related concepts

* [[prequantum geometry]]

* [[higher prequantum geometry]]

## References

The idea of formulating local prequantum field theory by spans in a slice over a "space of phases" in [[higher geometry]] has been expressed in the unpublished note

* [[Urs Schreiber]], _[[schreiber:Nonabelian cocycles and their quantum symmetries]]_ (2008)

A formulation of the idea for [[Dijkgraaf-Witten theory]]-type field theories is indicated in section 3 of 

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2010)
 {#FHLT}

based on the considerations in section 3.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ (2009).
 {#LurieTFT}

Based on the general formulation of the more general [[QFT with defects|field theory with defects]] described in section 4.3 there, in

* [[Domenico Fiorenza]], [[Alessandro Valentino]], _Boundary conditions in local TFTs_ (in preparation)
 {#FiorenzaValentino}

the structure of such [[domain walls]]/defects/[[branes]] are analyzed in the prequantum theory, hence with coefficients in an [[(∞,n)-category of spans]].

The study of local prequantum [[schreiber:∞-Chern-Simons theory]] with its codimension-1 [[∞-Wess-Zumino-Witten theory]] and codimension 2-[[Wilson line]]-theory in this fashion, in an ambient [[cohesive (∞,1)-topos]] is discussed in 

* [[Domenico Fiorenza]], [[Urs Schreiber]] et al., _[[schreiber:Higher Chern-Simons local prequantum field theory]]_
 {#hCSlpQFT}

Much of the content of this entry here are or arose as lecture notes for

* [[Urs Schreiber]], _Lectures on higher Chern-Simons field theory_, at the workshop _[Chern-Simons Theory: Geometry, Topology and Physics](http://www.pitt.edu/~jdeblois/CS.html)_ University of Pittsburgh (May 2013)
 {#SchreiberPittLectures}

This forms one section of the more comprehensive lecture notes at

* _[[geometry of physics]]_



[[!redirects prequantum field theory]]
[[!redirects prequantum field theories]]
[[!redirects local prequantum field theory]]
[[!redirects local prequantum field theories]]

[[!redirects extended prequantum field theory]]
[[!redirects extended prequantum field theories]]

[[!redirects higher prequantum field theory]]
[[!redirects higher prequantum field theories]]



***

category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]