

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

**Serre fibration** $\Leftarrow$ [[Hurewicz fibration]] $\Rightarrow$ [[Dold fibration]] $\Leftarrow$ [[shrinkable map]]

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #TopologicalGeneratingAcyclicCofibrations}
###### Definition

Write

$$
  J_{Top}
    \coloneqq
  \left\{
      D^n \stackrel{(id,\delta_0)}{\hookrightarrow} D^n \times I
  \right\}_{n \in \mathbb{N}}
  \;\subset Mor(Top)
$$

for the [[set]] of inclusions of the topological [[n-disks]], into their [[cylinder objects]] (the [[product topological space]] with the [[topological interval]]), along (for definiteness) the left endpoint inclusion.


=--


+-- {: .num_defn #SerreFibration}
###### Definition


A **Serre fibration** is a $J_{Top}$-[[injective morphism]], def. \ref{TopologicalGeneratingAcyclicCofibrations}, hence a [[continuous function]] $f \colon X \longrightarrow Y$ that  has the [[right lifting property]] with respect to all inclusions of the form $(id,0) \colon D^n \hookrightarrow D^n \times I$ that include the standard topological [[n-disk]] into its standard [[cylinder object]].

=--

I.e. $f$ is a Serre fibration if for every [[commuting square]] of [[continuous functions]] of the form

$$
  \array{
    D^n  &\longrightarrow& X
    \\
    {}^{\mathllap{(id,0)}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n \times I &\longrightarrow& Y
  }
$$

then there exists a continuous function $h \colon D^n \times I \to X$ such as to make a [[commuting diagram]] of the form

$$
  \array{
    D^n  &\longrightarrow& X
    \\
    {}^{\mathllap{(id,0)}}\downarrow 
    &{}^h\nearrow& 
    \downarrow^{\mathrlap{f}}
    \\
    D^n \times I &\longrightarrow& Y
  }
$$


+-- {: .num_remark}
###### Remark


The class of Serre fibrations serves as the class of abstract [[fibrations]] in the [[classical model structure on topological spaces]] (whence "Serre-Quillen model structure"). 

=--


## Properties
 {#Properties}

### Closure properties

+-- {: .num_prop #SerreFibrationHasRightLiftingAgainstJTopRelativeCellComplexes}
###### Proposition

A Serre fibration has the [[right lifting property]] against all [[retracts]] of $J_{Top}$-[[relative cell complexes]] (def. \ref{TopologicalGeneratingAcyclicCofibrations}).

=--

+-- {: .proof}
###### Proof

By general closure properties of [[projective and injective morphisms]], see there [this proposition](injective+or+projective+morphism#ClosurePropertiesOfInjectiveAndProjectiveMorphisms) for details.

=--



### Relation to Hurewicz fibrations
 {#RelationToHurewiczFibrations}

+-- {: .num_remark}
###### Remark

The condition in def. \ref{SerreFibration} is part of the condition on a [[Hurewicz fibration]], hence every [[Hurewicz fibration]] is in particular a Serre fibration.

=--

The converse is false:

+-- {: .num_example #SerreFibrationsWhichAreNotHurewiczFibrations}
###### Example
**(Serre fibrations which are not Hurewicz fibrations)**

An example of a generalized [[covering space]] which is a Serre fibration but not a Hurewicz fibration is given by Jeremy Brazas [here](https://mathoverflow.net/a/241597/381).

=--

But under some regularity condition it does becomes true:

+-- {: .num_prop #SerreFibrationsBetweenCWComplexesAreHurewiczFibrations}
###### Proposition
**(Serre fibrations of [[CW-complexes]] are [[Hurewicz fibrations]])**

In the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces|compactly generated]] [[weakly Hausdorff topological spaces]]) a Serre fibration in which the total space and base space are both [[CW complexes]] is a [[Hurewicz fibration]].

(No relationship between the covering map and the CW structures is required.)  

=--

This is due to ([Steinberger-West 84](#SteinbergerWest84)) with the corrected proof due to ([Cauty 92](#Cauty92)) (pointers via [[Peter May]] [here](https://mathoverflow.net/a/241611/381)).  Theorem-page at [[a Serre fibration between CW-complexes is a Hurewicz fibration]].

### Long exact sequences of homotopy groups

Since Serre fibrations are the abstract [[fibrations]] in the Serre-[[classical model structure on topological spaces]], the following statement follows from general [[model category]] theory. But it may also be seen by direct inspection, as follows.

+-- {: .num_lemma #CylinderOverCWComplexIsJTopRelativeCellComplex}
###### Lemma

For $X$ a finite [[CW-complex]], then its inclusion $X \overset{(id, \delta_0)}{\longrightarrow} X \times I$ into its standard [[cylinder object|cylinder]] is a $J_{Top}$-[[relative cell complex]] (def. \ref{TopologicalGeneratingAcyclicCofibrations}).

=--

+-- {: .proof}
###### Proof

First erect a cylinder over all 0-cells

$$ 
  \array{
     \underset{x \in X_0}{\coprod} D^0 &\longrightarrow& X
     \\
     \downarrow &(po)& \downarrow
     \\
     \underset{x\in X_0}{\coprod} D^1 &\longrightarrow& Y_1
  }
  \,.
$$

Assume then that the cylinder over all $n$-cells of $X$ has been erected using attachment from $J_{Top}$. Then the union of any $(n+1)$-cell $\sigma$ of $X$ with the cylinder over its boundary is homeomorphic to $D^{n+1}$ and is like the cylinder over the cell "with end and interior removed". Hence via attaching along $D^{n+1} \to D^{n+1}\times I$ the cylinder over $\sigma$ is erected.

=--

+-- {: .num_prop #SerreFibrationGivesExactSequenceOfHomotopyGroups}
###### Proposition

Let $f\colon X \longrightarrow Y$ be a [[Serre fibration]], def. \ref{SerreFibration}, let $y \colon \ast \to Y$ be any point and write 

$$
  F_y \overset{\iota}{\hookrightarrow} X \overset{f}{\longrightarrow} Y
$$

for the [[fiber]] inclusion over that point. Then for every choice $x \colon \ast \to X$ of lift of the point $y$ through $f$, the induced sequence of [[homotopy groups]]

$$

  \pi_{\bullet}(F_y, x)
    \overset{\iota_\ast}{\longrightarrow}
  \pi_\bullet(X, x)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
$$

is [[exact sequence|exact]], in that the [[kernel]] of $f_\ast$ is canonically identified with the [[image]] of $\iota_\ast$: 

$$
  ker(f_\ast) \simeq im(\iota_\ast)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is clear that the image of $\iota_\ast$ is in the kernel of $f_\ast$ (every sphere in $F_y\hookrightarrow X$ becomes constant on $y$, hence contractible, when sent forward to $Y$).

For the converse, let $[\alpha]\in \pi_{\bullet}(X,x)$ be represented by some $\alpha \colon S^{n-1} \to X$. Assume that $[\alpha]$ is in the kernel of $f_\ast$. This means equivalently that $\alpha$ fits into a [[commuting diagram]] of the form

$$
  \array{
    S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n &\overset{\kappa}{\longrightarrow}& Y
  }
  \,,
$$

where $\kappa$ is the contracting homotopy witnessing that $f_\ast[\alpha] = 0$.

Now since $x$ is a lift of $y$, there exists a [[left homotopy]] 

$$
  \eta  \;\colon\; \kappa \Rightarrow const_y
$$ 

as follows:

$$
  \array{
    && S^{n-1} &\overset{\alpha}{\longrightarrow}& X
    \\
    && {}^{\mathllap{\iota_n}}\downarrow && \downarrow^{\mathrlap{f}}
    \\
    && D^n &\overset{\kappa}{\longrightarrow}& Y
    \\
    && \downarrow^{\mathrlap{(id,1)}} && \downarrow^{\mathrlap{id}}
    \\
    D^n &\overset{(id,0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    \downarrow && &&  \downarrow
    \\
    \ast && \overset{y}{\longrightarrow} && Y
  }
$$

(for instance: regard $D^n$ as embedded in $\mathbb{R}^n$ such that $0 \in \mathbb{R}^n$ is identified with the basepoint on the boundary of $D^n$ and set $\eta(\vec v,t) \coloneqq \kappa(t \vec v)$).

The [[pasting]] of the top two squares that have appeared this way is equivalent to the following commuting square

$$
  \array{
    S^{n-1} &\longrightarrow& &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{(id,1)}}\downarrow 
    &&
    && \downarrow^{\mathrlap{f}}
    \\
    S^{n-1} \times I 
      &\overset{(\iota_n, id)}{\longrightarrow}& 
    D^n \times I 
      &\overset{\eta}{\longrightarrow}& 
    Y
  }
  \,.
$$

Because $f$ is a [[Serre fibration]] and by lemma \ref{CylinderOverCWComplexIsJTopRelativeCellComplex} and prop. \ref{SerreFibrationHasRightLiftingAgainstJTopRelativeCellComplexes}, this has a [[lift]] 

$$
  \tilde \eta \;\colon\; S^{n-1} \times I \longrightarrow X
  \,.
$$


Notice that $\tilde \eta$ is a basepoint preserving [[left homotopy]] from $\alpha = \tilde \eta|_1$ to some $\alpha' \coloneqq \tilde \eta|_0$. Being homotopic, they represent the same element of $\pi_{n-1}(X,x)$:

$$
  [\alpha'] = [\alpha]
  \,.
$$

But the new representative $\alpha'$ has the special property that its image in $Y$ is not just trivializable, but trivialized:
combining $\tilde \eta$ with the previous diagram shows that it sits in the following commuting diagram

$$
  \array{
    \alpha' \colon & S^{n-1} &\overset{(id,0)}{\longrightarrow}& S^{n-1}\times I &\overset{\tilde \eta}{\longrightarrow}& X
    \\
    & \downarrow^{\iota_n} && \downarrow^{\mathrlap{(\iota_n,id)}} && \downarrow^{\mathrlap{f}}
    \\
    & D^n &\overset{(id,0)}{\longrightarrow}& D^n \times I &\overset{\eta}{\longrightarrow}& Y
    \\
    & \downarrow && &&  \downarrow
    \\
    & \ast && \overset{y}{\longrightarrow} && Y
  }
  \,.
$$

The commutativity of the outer square says that $f_\ast \alpha'$ is constant, hence that $\alpha'$ is entirely contained in the fiber $F_y$. Said more abstractly, the [[universal property]] of [[fibers]] gives that $\alpha'$ factors through $F_y\overset{\iota}{\hookrightarrow} X$, hence that $[\alpha'] = [\alpha]$ is in the image of $\iota_\ast$.


=--

(...)

[[long exact sequence of homotopy groups]]

(...)


### Local recognition
 {#LocalRecognition}

+-- {: .num_lemma #MapIsSerreFibrationIfLocallySo}
###### Lemma
**(map is Serre fibration if it is locally so)**

If $p\colon X \to B$ is a [[continuous function]] and $\mathcal{U} = \big\{ U_i \overset{}{\hookrightarrow} B \big\}_{i \in I}$ is an [[open cover]] of its [[codomain]], such that the restriction of $p$ to each $U_i$ (i.e. its [[pullback]] to the cover) is a [[Serre fibration]], then $p$ itself is a Serre fibration:

$$
  \array{
    X_{\vert \mathcal{U}}
    &\longrightarrow&
    X
    \\
    {}^{{}_{\mathllap{
      {Serre}
      \atop
      {fibration}
    }}}
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    {}^{{}_{\mathrlap{
      p
    }}}
    \\
    \underset{i \in I}{\sqcup}
    U_i
    &\underset{  }{\longrightarrow}&
    B
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    X
    \\
    {}^{{}_{\mathllap{
      {Serre}
      \atop
      {fibration}
    }}}
    \big\downarrow
    {}^{{}_{\mathrlap{
      p
    }}}
    \\
    B
  }
$$

=--

See [tom Dieck 08, p. 130, Thm. 6.3.3](#tomDieck2008).

\begin{remark}
  An analogous local recognition holds for [[Hurewicz fibrations]] but with [[numerable open covers]]. See [there](Hurewicz+fibration#LocalRecognition).
\end{remark}




## Examples
 {#Examples}

### Fiber bundles
 {#FiberBundles}


\begin{example}
**([[fiber bundles]] are Serre fibrations)**\linebreak
Every topological [[fiber bundle]] (i.e. [[locally trivial]], meaning that on some [[open cover]] it becomes a [[Cartesian product|product]] [[projection]]) is a Serre fibration.
\end{example}

By Lemma \ref{MapIsSerreFibrationIfLocallySo}.


### Covering spaces

+-- {: .num_example #CoveringSpaceIsSerreFibration}
###### Example
**([[covering space]] projection is Serre fibration)**

Every [[covering space]] projection is a Serre fibration, in fact a [[Hurewicz fibration]] (by [this prop.](covering+space#HomotopyLiftingPropertyOfCoveringSpaces)).

=--

## Related concepts

* [[Serre spectral sequence]]

* [[classical model structure on topological spaces]]

## References

* {#SteinbergerWest84} M. Steinberger and J. West, _Covering homotopy properties of maps between CW complexes or ANRs_, Proc. Amer. Math. Soc. 92 (1984), 573-577.  

* {#Cauty92} R. Cauty, _Sur les ouverts des CW-complexes et les fibr&#233;s de Serre_,  Colloquy Math. 63 (1992), 1--7

* {#tomDieck2008} [[Tammo tom Dieck]],  _Algebraic topology_. European Mathematical Society, Zürich (2008) ([doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86))

For more see at _[[classical model structure on topological spaces]]_.


[[!redirects Serre fibrations]]
[[!redirects Serre fibration of topological spaces]]
[[!redirects Serre fibrations of topological spaces]]