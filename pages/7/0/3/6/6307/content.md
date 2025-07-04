
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Factorization categories
* table of contents
{: toc}

## Idea

The _factorization category_ (also called the _[[interval category]]_) $Fact(f)$ of a [[morphism]] $f$ in a [[category]] $C$ is a way of organizing its binary factorizations $f = p\circ q$ into a category. 


## Definition

The [[objects]] of $Fact(f)$ are factorizations 

\[
\begin{matrix}
  X &&\stackrel{f}{\to}&& Y
       \\
       & {}_{p_1} \searrow && \nearrow_{p_2}
       \\   
       && D
\end{matrix}
\]

so that $f = p_2 p_1$, and a [[morphism]] from $(p_1, D, p_2)$ to $(q_1, E, q_2)$ is a morphism $h \colon D \to E$ making everything in sight commute. There's an obvious projection [[functor]]
\[  
  P_f \colon Fact(f) \to C
\]
which maps $(p_1, D, p_2)$ to $D$ and $h\colon (p_1, D, p_2) \to (q_1, E, q_2)$ to $h$.  


### As iterated comma categories

In terms of [[slice categories]], a morphism $f: A \to B$ can be viewed as

1. an object in $C/B$
2. or an object in $A / C$

Now, taking over/under slices again yields only one new thing; it is easy to see that

* $(C/B)/f \cong C/A$, and 
* $f / (A / C) \cong B / C$

the cool fact is that the two other options yield $Fact(f)$

+-- {: .un_lemma }
###### Lemma

$Fact(f) \cong f/(C/B) \cong (A / C)/f$, and the following [[diagram]] [[commuting diagram|commutes]]
\[
\array{
    (A / C)/f &\stackrel{\cong}{\to}&   Fact(f)  & \stackrel{\cong}{\leftarrow} & f/(C/B)
    \\
    \pi^A_f \downarrow && P_f \downarrow && \pi^B_f 
    \\
    A / C & \underset{\pi_A}{\to} & C & \underset{\pi_B}{\leftarrow} & C/B  
  }
\]
=--

+-- {: .query}
[[Eduardo Pareja-Tobes]]: This should follow from properties of comma objects; I could add  here the proof from Lawvere-Menni paper below, but I think it would be better to have more conceptual proof 
=--


## Properties

### Characterization in terms of initial and terminal objects

There is a fairly simple characterization of the categories arising as factorization categories of some $f$ in a category $C$. First of all, note that $Fact(f)$ always has 

* an [[initial object]] $f = f\circ id$ 
* a [[terminal object]] $f = id \circ f$

conversely, for any category $D$ with initial and terminal objects $0, 1$ denoting the unique morphism $! \colon 0 \to 1$ we have that
\[
\pi_! \colon Fact(!) \to D
\]
is an [[equivalence]]. We get then

> a category is equivalent to some $Fact(f)$ iff it has initial and terminal objects  


### Factorization categories vs the category of factorizations

We can view $Fact(f)$ as a full [[reflective subcategory]] of the [[over-category]] $tw(C) / f$; here $f$ is viewed as an object of the [[category of factorizations]] $tw(C)$ of its ambient category $C$. There's a functor

\[
  U_f \colon Fact(f) \to tw(C) / f
\]

which on objects is

\[
  U_f(p_1, p_2) = 
\begin{matrix}
  X              & \overset{1_X}{\leftarrow}   & X            \\
  p_1\downarrow  &                           & \downarrow f \\
  D              & \underset{p_2}{\to}       & Y
\end{matrix}

\]

and on arrows $U(h) = (h, id)$.

This functor has a _[[left adjoint|left]]_ [[adjoint functor|adjoint]]

\[
  F_f \colon tw(C)/f \to Fact(f)
\]

* $F_f$ on objects: 
\[
  F_f\left(\, 
\begin{matrix}
  A             & \overset{h}{\leftarrow}   & X            \\
  g \downarrow  &                           & \downarrow f \\
  D             & \underset{q}{\to}         & Y
\end{matrix}
\, \right) \, = \quad
\begin{matrix}
  X &&\stackrel{f}{\to}&& Y
  \\
  & {}_{gh} \searrow && \nearrow_{q}
  \\   
  && D
\end{matrix}
\]

* $F_f$ on arrows: picks the morphism which goes between $D$ and $D'$.

It is immediate to check that $F_f \circ U_f = 1_{Fact(f)}$.


## References

* [[Bill Lawvere]], [[Matias Menni]], The Hopf algebra of M&#246;bius 
intervals, _Theory and Applications of Categories_, 24:10 (2010), 221-265. ([tac](http://www.tac.mta.ca/tac/volumes/24/10/24-10abs.html))
* B. Klin, [[Vladimiro Sassone]], P. Sobocinski, _Labels from reductions: Towards a general theory,_ Algebra and coalgebra in computer science: first international conference, CALCO 2005


[[!redirects factorization category]]
[[!redirects factorisation category]]
[[!redirects factorization categories]]
[[!redirects factorisation categories]]

category:computer science