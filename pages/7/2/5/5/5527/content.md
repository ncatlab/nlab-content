


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


The [[spectral sequence]] of a [[filtered object|filtered]] [[chain complex]] 

$$
  \cdots 
    \hookrightarrow
   F_{p-1}C_\bullet 
     \hookrightarrow 
   F_p C_\bullet 
     \hookrightarrow  
   \cdots 
     \hookrightarrow 
  C_\bullet
$$

is a tool for computing the [[chain homology]] of $C_\bullet$ from the chain homologies of the [[associated graded objects]] 

$$
  G_p C \coloneqq F_p C_\bullet/F_{p-1}C_\bullet
  \,;
$$

which is in general simpler. This is a special case of the [[spectral sequence of a filtered stable homotopy type]].


The sequence asymptotes to the homology of $C_\bullet$ by approximating [[cycles]] and [[boundaries]] of $C$ by their "$r$-approximation": an _$r$-almost cycle_ is a [[chain]] in filtering degree $p$ whose [[differential]] vanishes only up to terms that are $r$ steps lower in filtering degree, and an $r$-almost boundary in filtering degree $p$ is a cycle that is the differential of a chain which may be (only) up to $r$-degrees higher in filtering degree. The corresponding $r$-almost homology of $C_\bullet$ in filtering degree $p$ is the term $E^r_{p,\bullet}$ of the spectral sequence.

If the filtering is bounded then $r$-almost homology for sufficiently large $r$ ("$\infty$-almost homology") is clearly the genuine homology, and so the spectral sequence converges to the correct homology. But the point is that typically it reaches the correct value already at some low finite degree $r$ (it "collapses"), and so allows one to obtain the genuine homology from some finite $r$-almost homology.


One may also regard the spectral sequence of a filtered complex as a tool for organizing data derivable from the families of [[long exact sequence in homology]]

$$ 
  \cdots 
    \to 
  H_q (F_{p-1} C_\bullet) 
    \to 
  H_q (F_p C_\bullet) 
    \to 
  H_q(F_p C_\bullet / F_{q-1} C_\bullet) 
    \to 
  H_{q-1}(F_{p-1} C_\bullet)
   \to
 \cdots 
$$

which are induced by the short exact sequences 

$$
  0 \to F_{p-1}C_q \hookrightarrow F_p C_q \to F_p C_q / F_{p-1} C_q \to 0
$$

coming from the filtering.


## Definition

We give the definition 

* [via relative homology](#ExplicitDefinition)

and

* [via exact couples](#ViaExactCouples).

### Via relative homology
 {#ExplicitDefinition}

Let $R$ be a [[ring]] and write $\mathcal{A} = R$[[Mod]] for its [[category]] of [[modules]].

Let 

$$
  \cdots
  \hookrightarrow
  F_{p-1}C_\bullet \hookrightarrow F_p C_\bullet \hookrightarrow
  \cdots 
  \hookrightarrow
  C_\bullet
$$

be a [[filtered chain complex]] in $\mathcal{A}$, with [[associated graded]] complex denoted $G_\bullet C_\bullet$.

+-- {: .num_remark}
###### Remark

In more detail this means that

1. $[\cdots \stackrel{\partial_{n}}{\to} C_n \stackrel{\partial_{n-1}}{\to}] C_{n-1} \to \cdots]$ is a [[chain complex]], hence $\{C_n\}$ are [[objects]] in $\mathcal{A}$ ($R$-[[modules]]) and $\{\partial_n\}$ are [[morphisms]] (module [[homomorphisms]]) with $\partial_n \circ \partial_{n+1} = 0$;

1. For each $n \in \mathbb{Z}$ there is a [[filtered object|filtering]] $F_\bullet C_n$ on $C_n$ and all these filterings are compatible with the [[differentials]] in that 

   $$
     \partial(F_p C_n) \subset F_p C_{n-1}
   $$

1. The grading associated to the filtering is such that the $p$-graded elements are those in the [[quotient]]

   $$
     G_p C_n \coloneqq \frac{F_p C_n}{ F_{p-1} C_n}
     \,.
   $$

   Since the differentials respect the grading we have chain complexes $G_p C_\bullet$ in each filtering degree $p$.

The base category $\mathcal{A}$ can be any abelian category. In this case, we still use element-notation as if $\mathcal{A}$ were a category of [[modules]]. 

=--


#### $r$-Almost cycles and boundaries
 {#InterpretationOfTerms}


+-- {: .num_defn #AlmostChainsCyclesBoundaries}
###### Definition

Given a [[filtered chain complex]] $F_\bullet C_\bullet$ as above we say for all $r, p, q \in \mathbb{Z}$ that

1. $G_p C_{p+q}$ is the module of ***$(p,q)$-[[chains]]*** or of ***$(p+q)$-chains in filtering degree $p$***;


1. $\begin{aligned} Z^r_{p,q}  & \coloneqq \left\{ c \in G_p C_{p+q} | \partial c = 0 \, mod\, F_{p-r} C_{\bullet} \right\} \\ & =  \left\{ c \in F_p C_{p+q} | \partial(c) \in F_{p-r} C_{p+q-1} \right\}/ F_{p-1}C_{p+q} \end{aligned}$

   is the module of ***$r$-almost $(p,q)$-[[cycles]]*** (the $(p+q)$-chains whose differentials vanish modulo terms of filtering degree $p-r$);


1. $B^{r}_{p,q} \coloneqq \partial(F_{p+r-1} C_{p+q+1}) \,,$

   is the module of **$r$-almost $(p,q)$-[[boundaries]]**.

=--

Similarly we set

$$
  Z^\infty_{p,q} \coloneqq \{c \in F_p C_{p + q} | \partial c = 0 \}/F_{p-1}C_{p+q}
  = 
  Z(G_p C_{p+q})
$$

$$
  B^\infty_{p,q} = \partial( F_p C_{p+q+1} )
  \,.
$$

From this definition we immediately have that the differentials $\partial \colon C_{p+q} \to C_{p+q-1}$ restrict to the $r$-almost cycles as follows:

+-- {: .num_prop #DifferentialsOnAlmostChains}
###### Proposition

The [[differentials]] of $C_\bullet$ restrict on $r$-almost cycles to morphisms of the form

$$
  \partial^r 
   \colon
  Z^r_{p,q}
  \to
  Z^r_{p-r, q+r-1}
  \,.
$$

These are still [[differentials]]: $\partial^2 = 0$.

=--

+-- {: .proof}
###### Proof

By the very definition of $Z^r_{p,q}$ it consists of elements in filtering degree $p$ on which $\partial$ decreases the filtering degree to $p-r$. Also by definition of differential on a chain complex, $\partial$ decreases the actual degree $p+q$ by one. This explains that $\partial$ restricted to $Z^r_{p,q}$ lands in $Z^\bullet_{p-r,q+r-1}$. 

Now the image consists indeed of actual boundaries, not just $r$-almost boundaries. But since actual boundaries are in particular $r$-almost boundaries, we may take the codomain to be $Z^r_{p-r,q+r-1}$.

=--

+-- {: .num_prop }
###### Proposition

We have a sequence of canonical inclusions

$$
  B^0_{p,q}
  \hookrightarrow
  B^1_{p,q}
  \hookrightarrow
  \cdots
  B^\infty_{p,q}
  \hookrightarrow
  Z^\infty_{p,q}
  \hookrightarrow
  \cdots 
  \hookrightarrow
  Z^1_{p,q}
  \hookrightarrow
  Z^0_{p,q}
  \,.
$$

=--

+-- {: .num_prop #KernelsInsideAlmostCycles}
###### Proposition

The $(r+1)$-almost cycles are the $\partial^r$-kernel inside the $r$-almost cycles:

$$
  Z^{r+1}_{p,q}
  = 
  ker( Z^r_{p,q} \stackrel{\partial^r}{\to} Z^r_{p-r, q+r-1} )
  \,.
$$

=--


+-- {: .proof}
###### Proof

An element $c \in F_p C_{p+q}$ represents 

1. an element in $Z^r_{p,q}$ if $\partial c \in F_{p-r} C_{p+q-1}$

1. an element in $Z^{r+1}_{p,q}$ if even $\partial c \in F_{p-r-1} C_{p+q-1} \hookrightarrow F_{p-r} C_{p+q-1}$.

The second condition is equivalent to $\partial c$ representing the 0-element in the quotient $F_{p-r}C_{p+q-1}/ F_{p-r-1}C_{p+q-1}$. But this is in turn equivalent to $\partial c$ being 0 in $Z^r_{p-r,q+r-1} \subset F_{p-r} C_{p+q-1} / F_{p-r-1} C_{p+q-1}$.

=--


#### $r$-Almost homology groups: the spectral sequence

Let $F_\bullet C_\bullet$ be a [[filtered chain complex]] as above.

+-- {: .num_defn #ExplicitForm}
###### Definition

For $r, p, q \in \mathbb{Z}$ define the **$r$-almost $(p,q)$-[[chain homology]]** of the filtered complex to be the [[quotient]] of the $r$-almost $(p,q)$-cycles by the $r$-almost $(p,q)$-boundaries, def. \ref{AlmostChainsCyclesBoundaries}:

$$
  \begin{aligned}
    E^r_{p,q}
    & \coloneqq
    \frac{Z^r_{p,q}}{B^r_{p,q}}
    \\
    & = 
  \frac{
    \left\{
     x \in F_p C_{p+q} \,|\, \partial x \in F_{p-r} C_{p+q-1}
    \right\} + F_{p-1} C_{p+q}
  }
  {
    \partial( F_{p+r-1} C_{p+q+1} ) + F_{p-1} C_{p+q} 
  }
  \end{aligned}
$$

By prop. \ref{DifferentialsOnAlmostChains} the differentials of $C_\bullet$ restrict on the $r$-almost homology groups to maps

$$
  \partial^r : E^r_{p,q} \to E^r_{p-r, q + r - 1}
  \,.
$$


=--




+-- {: .num_prop #ExplicitDefIsIndeedSpectralSequ}
###### Proposition

Definition \ref{ExplicitForm} indeed gives a [[spectral sequence]] in that
$E^{r+1}_{\bullet, \bullet}$ is indeed the $\partial^r$-[[chain homology]] of $E^r_{\bullet, \bullet}$, i.e.

$$
  E^{r+1}_{p,q} 
  = 
 \frac{
    ker(\partial_r : E^r_{p,q} \to E^r_{p-r, q+r-1})
  }{
    im( \partial_r : E^r_{p+r, q-r+1} \to E^r_{p,q} )
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{KernelsInsideAlmostCycles}.

=--


### Via exact couples
 {#ViaExactCouples}

The spectral sequence may alternatively be obtained as the [spectral sequence of an exact coupl](exact+couple#SpectralSequencesFromExactCouples)

$$ D\overset{\varphi}{\to} D \to E \to D $$

where 

* $D \coloneqq \bigoplus_i H^{\bullet}(F_i) $

* and where $\varphi$ is the cohomology morphism induced by the inclusion of chain complexes $F_i\to F_{i+1}$ 

* and $E \coloneqq \bigoplus_i H^\bullet(F_i/F_{i-1})$ is the total cohomology of the associated bigraded complex.  

At every stage we have a new family of long exact sequences.



## Properties

### Low-degree pages
 {#InLowDegreePages}

We characterize the value of the spectral sequence $E^r_{p,q}$, def. \ref{ExplicitForm} for low values of $r$ and, below in prop. \ref{AbuttingFiltrationConvergesToHomology}, for $r \to \infty$.

+-- {: .num_prop #FirstPages}
###### Proposition

For the spectral sequence of a filtered complex $G_\bullet C_\bullet$ from def. \ref{ExplicitForm}, the first pages have the following form:

* $E^0_{p,q} = G_p C_{p+q} = F_p C_{p+q} / F_{p-1} C_{p+q}$ 

  is the [[associated graded|associated p-graded]] piece of $C_{p+q}$;

* $E^1_{p,q} = H_{p+q}(G_p C_\bullet)$

  is the [[chain homology]] of the [[associated graded|associated p-graded]] complex $G_p C_\bullet$.

=--

+-- {: .proof}
###### Proof

For $r = 0$ def. \ref{ExplicitForm} restricts to

$$
  E^0_{p,q} = \frac{ F_p C_{p+q}}{F_{p-1} C_{p+q}} = G_p C_{p+q}
$$

because for $c \in F_p C_{p+q}$ we automatically also have $\partial c \in F_p C_{p+q}$ since the differential respects the filtering degree by assumption. 

For $r = 1$ def. \ref{ExplicitForm} gives 

$$
  E^1_{p,q} = \frac{\{c \in G_p C_{p+q} | \partial c = 0 \in G_p C_{p+q}\} }{\partial(F_p C_{p+q})} = H_{p+q} (G_p C_\bullet)
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

There is, in general, a decisive difference between the homology of the associated graded complex $H_{p+q}(G_p C_\bullet)$ and the associated graded piece of the genuine homology $G_p H_{p+q}(C_\bullet)$: in the former the differentials of cycles are required to vanish only up to terms in lower degree, but in the latter they are required to vanish genuinely. The latter expression is instead the value of the spectral sequence for $r \to \infty$.

=--


### Convergence
 {#Convergence}

#### General definitions


+-- {: .num_defn #LimitTerm}
###### Definition

Let $\{E^r_{p,q}\}_{r,p,q}$ be a [[spectral sequence]] such that for each $p,q$ there is $r(p,q)$ such that for all $r \geq r(p,q)$ we have

$$
  E^{r \geq r(p,q)}_{p,q} \simeq E^{r(p,q)}_{p,q}
  \,.
$$

Then one says that

1. the [[bigraded object]]

   $$
     E^\infty 
      \coloneqq 
     \{E^\infty_{p,q}\}_{p,q} \coloneqq \{ E^{r(p,q)}_{p,q} \}_{p,q}
   $$

   is the **limit term** of the spectral sequence;

*  the spectral sequence **abuts** to $E^\infty$.

=--

+-- {: .num_example #Degeneration}
###### Example

If for a spectral sequence there is $r_s$ such that all [[differentials]] on pages after $r_s$ vanish, $\partial^{r \geq r_s} = 0$, then $\{E^{r_s}\}_{p,q}$ is limit term for the spectral sequence. One says in this cases that the spectral sequence **collapses** at $r_s$.

=--

+-- {: .proof}
###### Proof

By the defining relation

$$
  E^{r+1}_{p,q} \simeq ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q}) = E^r_{pq}
$$

the spectral sequence becomes constant in $r$ from $r_s$ on if all the differentials vanish, so that $ker(\partial^r_{p,q}) = E^r_{p,q}$ for all $p,q$.

=--


+-- {: .num_example #Collaps}
###### Example

If for a [[spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ there is $r_s \geq 2$ such that the $r_s$th page is concentrated in a single row or a single column, then the the spectral sequence degenerates on this page, example \ref{Degeneration}, hence this page is a limit term, def. \ref{LimitTerm}. One says in this case that the spectral sequence **collapses** on this page.

=--

+-- {: .proof}
###### Proof

For $r \geq 2$ the [[differentials]] of the spectral sequence

$$
  \partial^r \colon E^r_{p,q} \to E^r_{p-r, q+r-1}
$$ 

have [[domain]] and [[codomain]] necessarily in different rows an columns (while for $r = 1$ both are in the same row and for $r = 0$ both coincide). Therefore if all but one row or column vanish, then all these differentials vanish.

=--


+-- {: .num_defn #Convergence}
###### Definition

A [[spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ is said to **converge** to a [[graded object]] $H_\bullet$ with [[filtered chain complex|filtering]] $F_\bullet H_\bullet$, traditionally denoted

$$
  E^r_{p,q} \Rightarrow H_\bullet
  \,,
$$

if the [[associated graded]] complex $\{G_p H_{p+q}\}_{p,q} \coloneqq \{F_p H_{p+q} / F_{p-1} H_{p+q}\}$ of $H$ is the limit term of $E$, def. \ref{LimitTerm}:

$$
  E^\infty_{p,q} \simeq G_p H_{p+q} \;\;\;\;\;\;\; \forall_{p,q}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

In practice spectral sequences are often referred to via their first non-trivial page, often also the page at which it collapses, def. \ref{Collaps}, often the second page. Then one often uses notation such as

$$
  E^2_{p,q} \Rightarrow H_\bullet
$$

to be read as "There is a spectral sequence whose second page is as shown on the left and which converges to a filtered object as shown on the right."

=--

+-- {: .num_defn #BoundedSpectralSequence}
###### Definition

A spectral sequence $\{E^r_{p,q}\}$ is called a **bounded spectral sequence** if for all $n,r \in \mathbb{Z}$ the number of non-vanishing terms of the form $E^r_{k,n-k}$ is finite.

=--

+-- {: .num_example #QuadrantSpectralSequence}
###### Example

A [[spectral sequence]] $\{E^r_{p,q}\}$ is called

* a **first quadrant spectral sequence** if all terms except possibly for $p,q \geq 0$ vanish;

* a **third quadrant spectral sequence** if all terms except possibly for $p,q \leq 0$ vanish.

Such spectral sequences are bounded, def. \ref{BoundedSpectralSequence}.

=--

+-- {: .num_prop #BoundedSpectralSequenceHasLimitTerm}
###### Proposition

A bounded spectral sequence, def. \ref{BoundedSpectralSequence}, has a limit term, def. \ref{LimitTerm}.

=--

+-- {: .proof}
###### Proof

First notice that if a spectral sequence has at most $N$ non-vanishing terms of total degree $n$ on page $r$, then all the following pages have at most at these positions non-vanishing terms, too, since these are the homologies of the previous terms.

Therefore for a bounded spectral sequence for each $n$ there is $L(n) \in \mathbb{Z}$ such that $E^r_{p,n-p} = 0$ for all $p \leq L(n)$ and all $r$. Similarly there is $T(n) \in \mathbb{Z}$ such $E^r_{n-q,q} = 0$ for all $q \leq T(n)$ and all $r$.

We claim then that the limit term of the bounded spectral sequence is in position $(p,q)$ given by the value $E^r_{p,q}$ for 

$$
  r \gt max(  p-L(p+q-1), q + 1 - L(p+q+1) )
  \,.
$$

This is because for such $r$ we have

1. $E^r_{p-r, q+r-1} = 0$ because $p-r \lt L(p+q-1)$, and hence the [[kernel]] $ker(\partial^r_{p-r,q+r-1}) = 0$ vanishes;

1. $E^r_{p+r, q-r+1} = 0$ because $q-r + 1 \lt T(p+q+1)$, and hence the [[image]] $im(\partial^r_{p,q}) = 0$ vanishes.

Therefore

$$
  \begin{aligned}
    E^{r+1}_{p,q} 
    &= 
    ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q})
    \\
    & \simeq E^r_{p,q}/0
    \\
    & \simeq E^r_{p,q}
  \end{aligned}
  \,.
$$

=--

#### Convergence of bounded filtrations
 {#ConvergenceGeneral}


+-- {: .num_defn #BoundedFiltration}
###### Definition

A [[filtered chain complex|filtration]] $F_\bullet C_\bullet$ on a [[chain complex]] $C_\bullet$ is called a **bounded filtration** if for all $n \in \mathbb{Z}$ there is $L(n), T(n) \in \mathbb{Z}$ such that

$$
  F_{p \lt S(n)}C_n = 0
  \;\;\;\;\;
  F_{p \gt T(n)}C_n \simeq C_n
  \,.
$$

=--



+-- {: .num_prop }
###### Proposition

The spectral sequence of a complex with bounded filtration, def. \ref{BoundedFiltration}, has a limit term, def. \ref{LimitTerm}.

=--

+-- {: .proof}
###### Proof

The spectral sequence of a filtered complex $F_\bullet C_\bullet$ is by def. \ref{ExplicitForm} at $E^r_{p,q}$ a [[quotient]] of a [[subobject]] of $F_p C_{p+q}$. By def. \ref{BoundedFiltration} therefore there are for each $n,r \in \mathbb{Z}$ finitely many non-vanishing terms of the form $E^r_{p,n-p}$. Therefore the spectral sequence is bounded, def. \ref{BoundedSpectralSequence} and hence has a limit term by prop. \ref{BoundedSpectralSequenceHasLimitTerm}.

=--

+-- {: .num_example }
###### Example

If $X \in$ [[Top]] is a [[CW complex]] with cell filtration $X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X$, then the induced filtering 

$$
  F_p C_\bullet(X) \coloneqq C_\bullet(X_n)
$$

on its [[singular chain complex]] $C_\bullet(X)$ yields a first-quadrant spectral sequence, example \ref{QuadrantSpectralSequence}. Therefore it has a limit term.

=--

Before saying that the spectral sequence of a filtered complex converges to the homology of that complex, we need to be careful about what the filtering is on that homology:

+-- {: .num_defn #FilteringOnHomology}
###### Definition

For $F_\bullet C_\bullet$ a [[filtered complex]], write for $p \in \mathbb{Z}$

$$
  F_p H_\bullet(C) 
   \coloneqq
  image( H_\bullet(F_p C_\bullet) \to H_\bullet(C_\bullet) )
  \,.
$$

This defines a filtering $F_\bullet H_\bullet(C)$ of the homology, regarded as a graded object.

=--


+-- {: .num_prop #AbuttingFiltrationConvergesToHomology}
###### Proposition

If the spectral sequence of a filtered complex $F_\bullet C_\bullet$, def. \ref{BoundedFiltration} has a limit term, def. \ref{LimitTerm}, then it converges, def. \ref{Convergence}, to the [[chain homology]] of the complex:

$$
  E^r_{p,q} \Rightarrow H_\bullet(C)
  \,.
$$

Hence for each $p,q$ there is $r(p,q)$ such that

$$
  E^{r \geq r(p,q)}_{p,q} \simeq G_p H_{p+q}(C)
  \,,
$$

with the filtering on the right as in def. \ref{FilteringOnHomology}.


=--

+-- {: .proof}
###### Proof

By assumption, there is for each $p,q$ an $r(p,q)$ such that for all $r \geq r(p,q)$ the $r$-almost cycles and $r$-almost boundaries, def. \ref{AlmostChainsCyclesBoundaries}, in $F_p C_{p+q}$ are the ordinary [[cycles]] and [[boundaries]]. Therefore for $r \geq r(p,q)$ def. \ref{ExplicitForm} gives $E^r_{p,q} \simeq G_p H_{p+q}(C)$.

=--


#### Via exact couples


It is instructive to note that in the $n$th derived [[exact couple]] $\varphi^n D\to E_{(n)} \to \varphi^n D\to{}$, the hidden part $\varphi^n D$ is the [[module|submodule]] $D_{(n)}$ of $\bigoplus_{i} H(F_{i+n})$, as it meets $H(F_{i+n})$ representable by elements of $F_i$; that is, we may sensibly call it
$$F_{i} D_{(n)} = \frac{\ker(d)\cap F_i}{F_i\cap dF_{i+n}}.$$
Separating the grades, the exactness of the couple at $E_{(n)}$ then says 
$$ F_{i} H^j(F_{i+n})\to F_{i+1}H^j(F_{i+n+1}) \to E_{(n)}^{i\dots} \to F_i H^{j+1}(F_{i+n}) \to F_{i+1}H^{j+1}(F_{i+n+1}) $$

One can see this as converging (if it sensibly converges) to either a subquotient of $F_i$ _or_ to a [[module|submodule]] $F_i H^\bullet(C) \lt H^\bullet(C)$.  Taking the latter interpretation, we hope to find in the limiting case exact sequences
$$ F_i H^j(C)\to F_{i+1} H^j(C) \to E_{(\infty)}^{i\dots} \to F_i H^{j+1}(C) \to F_{i+1} H^{j+1}(C).$$
At this stage one can check that the morphisms $F_i H^j(C)\to F_{i+1} H^j(C)$ are indeed definable, and in fact injective, so that whatever $E_{(\infty)}$ should be, the morphism $E_{(\infty)}^{i\dots}\to F_i H^{j+1}$ is null; that is, our long-exact sequence breaks up into the 
[[short exact sequence]]s
$$ 0\to F_i H^j(C) \to F_{i+1} H^j(C)\to E_{(\infty)}^{i\dots} \to 0 .$$

In summary, if the spectral sequence $E_{(n)}$ converges in a sensible way to the correct thing $E_{(\infty)}$, then that correct thing is also the associated graded [[module]] of the [[filtration]] of $H^\bullet(C)$ induced by the [[filtration]] of $C$.


## Examples

### 2-term filtering

The special case where the filtering has just length one  is that where we simply have a sub-complex $C^{(1)}_\bullet \hookrightarrow C_\bullet$ and want to compute the homology of $C_\bullet$ from that of $C^{(1)}_\bullet$ and $C_\bullet/C^{(1)}_\bullet$.

This case is easily solved by elementary means and it serves as an instructive blueprint for the general case.

+-- {: .num_prop}
###### Proposition

Given a [[subobject|sub]]-[[chain complex]] $C^{(1)}_\bullet \hookrightarrow C_\bullet$, consider the following constructions

1. Consider the [[short exact sequence]]

   $$
     0 \to C^{(1)}_\bullet \to C_\bullet \to C_\bullet/C^{(1)}_\bullet \to 0
   $$

1. Its [[long exact sequence in homology]] contains the [[connecting homomorphism]] 

   $$
     \delta 
      : 
     H_\bullet(C_\bullet/C^{(1)}_\bullet)
      \to
     H_{\bullet-1}(C^{(1)}_\bullet)
     \,.
   $$

   Define

   * $G_1 H_\bullet \coloneqq ker \delta$

   * $G_2 H_\bullet \coloneqq coker \delta$.

Then $H_\bullet(C_\bullet)$ is sits in the short exact sequence

$$
  0 \to G_0 H_\bullet \to H_\bullet(C_\bullet) \to G_1 H_\bullet \to 0
  \,.
$$


=--

(...)

### Homology of a tensor product of chain complexes
 {#ExampleHomologyOfTensorProduct}


Consider two chain complexes $C_\bullet, C'_\bullet$ 
of [[vector spaces]] over a [[field]] $k$, both
in non-negative degree.

Their [[tensor product of chain complexes]] is

$$
  C_\bullet \otimes C'_\bullet
  = 
  \oplus_{i+j = k} C_i \otimes C_j
$$

with [[differential]] on homogenous elements

$$
  \partial (\alpha \otimes\beta) = 
  (\partial \alpha)
  \otimes \beta
  +
  (-1)^{deg \alpha} \alpha \otimes \partial \beta
  \,.
$$

We may compute the homology of $C \otimes C'$ by a 
spectral sequence as follows.

Define a filtration on $C \otimes C'$ by

$$
  F_p(C \otimes C')_{k}
  \coloneqq
  \oplus_{i \leq p} C_i \otimes C_{k-i}
  \,.
$$

This means that the [[associated graded object]] is simply

$$
  E^0_{p,q} = G_p (C \otimes C')_{p+q}
  = 
  C_p \otimes C'_q
  \,.
$$

The [[differential]] on this is $\partial_{r = 0} = (-1)^p id_{C} \otimes \partial'$.
Hence the [[universal coefficient theorem]] gives

$$
  E^1_{p,q} = C_p \otimes H_q(C')
  \,.
$$

The next differential is $\partial_1 = \partial \otimes id_{C'}$.
Since $k$ is assumed to be a field we have thus

$$
  E^2_{p,q} = H_p(C_\bullet \otimes H_q(C'_\bullet))
  = 
  H_p(C)\otimes H_q(C')
  \,.
$$

Therefore every element in $E^2_{p,q}$ is represented by 
a tensor product of a $C$-[[cycle]] with a $C'$-cycle and is 
hence itself a $(C \otimes C')$-cycle. Since the differentials
in the spectral sequence all come from the differential on 
$C \otimes C'$, this means that all higher differentials vanish,
and so the sequence collapses on the $E^2$-page. 

The convergence of the spectral sequence to the the homology 
of $C \otimes C'$ thus says that this is given by

$$
  H_{k}(C \otimes C')
  \simeq
  \oplus_{i+j = k} H_i(C) \otimes H_j(C')
  \,.
$$


### Homology of the total complex of a double complex
 {#ExampleHomologyDoubleComplex}


The [[total complex]] of a [[double complex]] is naturally 
[[filtered object|filtered]] either by either row-degree of column-degree. The corresponding filtering spectral sequence converges under good conditions to the homology of the total complex. See at _[[spectral sequence of a double complex]]_. 

### Singular homology of a CW-complex

Let $X \in Top$ be a [[CW-complex]] equipped explicitly with the structure of a [[filtered topological space]] $X^0 \hookrightarrow \cdots \hookrightarrow X^n \hookrightarrow \cdots X$.
This induces on the [[singular homology]] complex $C_\bullet(X)$ the structure of a [[filtered chain complex]] by 

$$
  F_q C_\bullet(X) \coloneqq C_\bullet(X^p)
  \,.
$$

We discuss how the corresponding spectral sequence shows that the [[singular homology]] of $X$ coincides with the [[cellular homology]] of the filtering.


The [[associated graded object]] is

$$
  G_p C_{p+q}(X) = E^0_{p,q} = C_{p+q}(X^p)/C_{p+q}(X^{p-1})
  \,.
$$

+-- {: .num_prop}
###### Proposition


The chain homology of the associated graded chain complex is the [[relative homology]]

$$
  E^1_{p,q} = H_{p+q}(X^p | X^{p-1})
  \,.
$$

=--

Now by assumption that $X^\bullet$ is the cell decomposition of a [[cell complex]] we have

$$
  H_{p+q}(X^p | X^{p+1}) 
  \simeq
  \left\{
    \array{
      \mathbb{Z}[pCells(X)] & q = 0
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

The chain homology of

$$
  \partial \colon 
   H_p(X^p, X^{p-1})
  \to 
  H_{p-1}(X^{p-1}, X^{p-2})
$$

is the cellular chain homology $H^{cell}_p(X)$. 
One finds that

$$
  E^2_{p,q} = 
  \left\{
    \array{
      H_p^{cell}(X) & q = 0
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Since this is concentrated in the $q = 0 $-row all higher-$r$ differentials vanish. 

Hence $H_p(X) \simeq H^{cell}_p(X)$.

+-- {: .num_remark}
###### Remark

The generalization of this argument from [[ordinary homology]] to [[generalized homology]] is given by the [[Atiyah–Hirzebruch spectral sequence]].

=--


### Serre's spectral sequence of a fibration

We indicate the [[Leray-Serre spectral sequence]] of a [[Serre fibration]] as a special case of the filtering spectral sequence. For more discussion see there. Let
$$\begin{matrix} A & \to & X \\
 \downarrow & & \downarrow \\
 * & \to & B \end{matrix} $$
be a [[Serre fibration]] of [[pointed object|pointed]] [[topological spaces]] in which $B$ is a [[connected topological space|connected]] [[CW-complex]].  Then the $k$-[[simplicial skeleton|skeleta]] of $B$ naturally give filtered-space structures to both $B$ and $X$:
$$\begin{matrix} X_{(k)} & \to & X_{(k+1)} & \to & X \\
 \downarrow & & \downarrow & &\downarrow \\
 B_{k} & \to & B_{k+1} & \to & B \end{matrix} $$
and in turn induce filtrations of the singular chain complex of $X$.

The homology [[Serre spectral sequence]] for the fibration is essentially that of this filtered complex.

It is straight-forward to show that the pair $(X_{k+1};X_k)$ is $k$-connected, and in particular the relative homology $H_i(X_{k+1};X_k)$ vanishes for $i\leq k$; this ensures that the spectral sequence is 1st/3rd quadrant (And _nota bene_: this is also a handy way to remember what the bigrading actually is).

There is also an important result about the _second_ page of this spectral sequence


+-- {: .num_theorem }
###### Theorem

*The page $E^{(2)}$ of the homology Serre spectral sequence is given by*
$$ E^{(2)}_{p,q} \simeq H_p(B,\mathcal{H}_q(A|_{b})) $$
*the homology of $B$ with coefficients in the [[local system]] defined by the action of $\Pi_1 (B)$ on $H_q(A|_{b})$.  In the special case that $B$ is simply connected, these local systems are canonically equivalent to $H_q(A)$, the homology of the fiber over the basepoint.

=--


## Related concepts

* [[Cartan-Eilenberg spectral sequence]]

[[!include Lurie spectral sequences -- table]]

## References

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], chapter XV of _Homological algebra_, Princeton Univ. Press (1956)

* {#Kochmann96} [[Stanley Kochman]], section 5.3 of  of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Orlich} Jennifer Orlich, _Spectral sequences and an application_, 1998 ([pdf](http://www.math.osu.edu/~flicker.1/orlich.pdf))


Lecture notes include

* {#Hutchings} [[Michael Hutchings]], _Introduction to spectral sequences_ (2011) ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/ss.pdf))
 

and section 3 of 

* [[Brandon Williams]], _Spectral sequences_ ([pdf](http://www.math.sunysb.edu/~mbw/notes/orals/Spectral%20Sequences.pdf))

For further references see those listed at _[[spectral sequence]]_, 
for instance section 5 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_



[[!redirects spectral sequence of a filtration]]

[[!redirects spectral sequence of a filtered chain complex]]

[[!redirects spectral sequences of filtered complexes]]
