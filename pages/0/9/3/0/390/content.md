
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{: toc}


##Definition
 {#Definition}

### Orthogonal factorization systems

+-- {: .num_defn }
###### Definition

Let $C$ be a [[category]] and let $(E,M)$ be two [[classes]] of [[morphisms]] in 
$C$. We say that $(E,M)$ is an **orthogonal factorization system** if $(E,M)$ is a [[weak factorization system]] in which solutions to lifting problems are unique.  

=--

We spell out several equivalent explicit formulation of what this means.

+-- {: .num_defn #EquivalentDefinitions}
###### Definition

$(E,M)$ is an **orthogonal factorization system** if
every morphism $f$ in $C$ factors $f = r\circ \ell$ as a morphism $\ell \in E$ followed by a morphism $r \in M$; and the following equivalent conditions hold

1. We have:
 
   1. $E$ is precisely the class of morphisms that are left [[orthogonality|orthogonal]] to every morphism in $M$;

   1. $M$ is precisely the class of morphisms that are right [[orthogonality|orthogonal]] to every morphism in $E$.

1. We have:

   1. The factorization is unique up to unique [[isomorphism]].

   1. $E$ and $M$ both contain all [[isomorphisms]] and are closed under composition.

1. We have:

   1. $E$ and $M$ are [[replete subcategories]] of the [[arrow category]] $C^I$.

   1. Every morphism in $E$ is left [[orthogonality|orthogonal]] to every morphism in $M$.

=--

OFS's are traditionally called just **factorization systems**.
See the _[[joyalscatlab:Factorization systems|Catlab]]_ for more of the theory.

An orthogonal factorization system is called **proper** if every morphism in $E$ is an [[epimorphism]] and every morphism in $M$ is a [[monomorphism]].


### Prefactorization systems

For any class $E$ of morphisms in $C$, we write $E^\perp$ for the class of all morphisms that are right orthogonal to every morphism in $E$.  Dually, given $M$ we write ${}^\perp M$ for the class of all morphisms that are  left orthogonal to every morphism in $M$.  The second condition in the definition of an OFS then says that $E= {}^\perp M$ and $M= E^\perp$.

In general, $(-)^\perp$ and ${}^\perp(-)$ form a [[Galois connection]] on the [[poset]] of classes of morphisms in $C$.  A pair $(E,M)$ such that $E= {}^\perp M$ and $M= E^\perp$ is sometimes called a **prefactorization system**.  Note that by generalities about Galois connections, for any class $A$ of maps we have prefactorization systems $({}^\perp(A^\perp),A^\perp)$ and $({}^\perp A, ({}^\perp A)^\perp)$.  We call these *generated* and *cogenerated* by $A$, respectively.

## Properties
 {#Properties}

### General

+-- {: .num_prop}
###### Proposition

The different characterization in def. \ref{EquivalentDefinitions} 
are indeed all equivalent.

=--

+-- {: .proof}
###### Proof

(...)

For the moment see ([Joyal](#Joyal)).

(...)

=--

+-- {: .num_prop}
###### Proposition

A [[weak factorization system]] $(L,R)$ is an orthogonal factorization system precisely if $L \perp R$.

=--

+-- {: .proof}
###### Proof

(...)

For the moment see ([Joyal](#Joyal)).

(...)

=--

+-- {: .num_prop #IsomorphismsAreIntersection}
###### Proposition

For $(L,R)$ an orthogonal factorization system
in a category $C$, the intersection $L \cap R$ is precisely the class of [[isomorphisms]] in $C$.

=--

+-- {: .proof}
###### Proof

If is clear that every isomorphism is in $L \cap R$.
Conversely, let $f : A \to B$ be a morphism in $L \cap R$. This implies that the two trivial factorizations

$$
  f = A \stackrel{id_A}{\to} A \stackrel{f}{\to} B
$$

and

$$
  f = A \stackrel{f}{\to} B \stackrel{id_B}{\to} B
$$

are both $(L,R)$-factorization. Therefore there is a unique morphism $\tilde f$ in the [[commuting diagram]]

$$
  \array{
    A &\stackrel{id_A}{\to}& A
    \\
    \downarrow^{\mathrlap{f}}
     &\nearrow_{\bar f}&
    \downarrow^{\mathrlap{f}}
    \\
    B &\stackrel{id_B}{\to}& B
  }
  \,.
$$

This says precisely that $\bar f$ is a left and right [[inverse]] of $f$.

=--

### Closure properties

A prefactorization system $(E,M)$ (and hence, also, a factorization system) satisfies the following closure properties.  We state them  for $M$, but $E$ of course satisfies the dual property.

* $M$ contains the isomorphisms and is closed under composition and [[pullback]] (insofar as pullbacks exist in $C$).
* If a composite $f g$ is in $M$, and $f$ is either in $M$ or a [[monomorphism]], then $g$ is in $M$.
* $M$ is closed under all [[limits]] in the [[arrow category]] $Arr(C)$.

If $C$ is a [[locally presentable category]], then for any *small set* of maps $A$, the prefactorization system $({}^\perp(A^\perp),A^\perp)$ is actually a factorization system.  The argument is by a transfinite construction similar to the [[small object argument]].

On the other hand, if $(E,M)$ is any prefactorization system for which $M$ consists of monomorphisms and $C$ is [[complete category|complete]] and [[well-powered category|well-powered]], then $(E,M)$ is actually a factorization system.  (Of course, there is a dual statement as well.)  In fact something slightly more general is true; see [[M-complete category]] for this and other related ways to construct factorization systems.




### Cancellation properties
 {#CancellationProperties}


+-- {: .num_prop}
###### Proposition

For $(L,R)$ an orthogonal factorization system. Let

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    X
    &&
    \stackrel{g \circ f}{\to}
    &&
    Z
  }
$$

be two composable morphisms. Then

* If $f$ and $g \circ f$ are in $L$, then so is $g$.

* If $g$ and $g\circ f$ are in $R$, then so is $f$.

=--

+-- {: .proof}
###### Proof

Consider the first case. The second is directly analogous.

Choose an $(L,R)$-factorization of $g$

$$
  g : Y \stackrel{\ell}{\to} I \stackrel{r}{\to} Z
  \,.
$$

With this we have lifting diagrams of the form

$$
  \array{
    X &\stackrel{g \circ f}{\to}& Z
    \\
    \downarrow^{\mathrlap{f}} &&  \downarrow^{id_Z}
    \\
    Y & \nearrow_r&
    \\
    \downarrow^{\mathrlap{\ell}} && \downarrow^{id_Z}
    \\
    I &\stackrel{r}{\to}& Z
  }
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \array{
    X &\stackrel{f}{\to}& Y &\stackrel{\ell}{\to}& I
    \\
    {}^{\mathllap{g \circ f}}\downarrow
     & & \nearrow_{r^{-1}}& &
    \downarrow^{\mathrlap{r}}
    \\
    Z &\underset{id_Z}{\to}& &\underset{id_Z}{\to}& Z 
  }
$$

exhibiting an inverse of $r$. Therefore $r$ is an isomorphism, hence is in $L$, by prop. \ref{IsomorphismsAreIntersection}, hence so is the composite $f = r \circ \ell$.

=--

## Examples 
 {#Examples}

Several classical examples of OFS $(E,M)$:

* in any [[topos]] or [[pretopos]], $E$ = class of all epis, $M$ = class of all monos: the [[(epi, mono) factorization system]];

* more generally, in any [[regular category]], $E$ = class of all [[regular epimorphisms]], $M$ = class of all monos

* in any [[quasitopos]], $E$ = all epimorphisms, $M$ = all [[strong monomorphisms]]

* In [[Cat]], $E$ = [[bo functors]], $M$ = [[fully faithful functors]]: the [[bo-ff factorization system]]

* In [[Cat]], [[(eso, fully faithful) factorization system]]

* In [[Cat]], [[(eso+full, faithful) factorization system]]

* (Street) in [[Cat]], $E$ = 0-[[final functors]], $M$ = [[discrete fibrations]] 

* (Street) in $\mathrm{Cat}$,  $M$ = 0-[[initial functors]], $M$ = [[discrete opfibration]]s

* in $\mathrm{Cat}$, $M$ = [[conservative functor]]s, $E$ = left orthogonal of $M$ ("iterated strict localizations" after A. Joyal)

* in the category of small categories where morphisms are functors which are [[exact functor|left exact]] and have [[right adjoint]]s, $E$ = class of all such functors which are also localizations, $M$ = class of all such functors which are also conservative

* if $F\to C$ is a [[fibered category]] in the sense of Grothendieck, then $F$ admits a factorization system $(E,M)$ where $E$ = arrows whose projection to $C$ is invertible, $M$ = cartesian arrows in $F$


* See the ([Joyal](#Joyal)) for more examples. 

## Related concepts

* [[factorization system]]

  * [[weak factorization system]]

  * **orthogonal factorization system**

  * [[reflective factorization system]]

  * [[stable factorization system]]

* [[factorization system in a 2-category]]

* [[factorization system in an (∞,1)-category]]

  * [[orthogonal factorization system in an (∞,1)-category]]

* [[factorization structure for sinks]]


## References

* [[André Joyal]] _[[joyalscatlab:Factorization systems]]_
 {#Joyal}


[[!redirects orthogonal factorization system]]
[[!redirects orthogonal factorization systems]]
[[!redirects orthogonal factorisation system]]
[[!redirects orthogonal factorisation systems]]
[[!redirects unique factorization system]]
[[!redirects unique factorization systems]]
[[!redirects unique factorisation system]]
[[!redirects unique factorisation systems]]
[[!redirects prefactorization system]]
[[!redirects prefactorization systems]]
