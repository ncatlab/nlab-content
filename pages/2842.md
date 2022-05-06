
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Hurewicz cofibrations are a kind of [[cofibration]] of [[topological spaces]], hence a kind of [[continuous function]] satisfying certain [[extension]] properties. 

In [[point-set topology]] Hurewicz cofibrations are often just called _cofibrations_. If their [[image]] is a [[closed subspace]] they are called _[[closed cofibrations]]_.

A [[continuous function]] is a _Hurewicz cofibration_ if it satisfies the [[homotopy extension property]] for all spaces and with respect to the standard notion of [[left homotopy]] of topological spaces given by the standard topological [[interval object]]/[[cylinder object]].

More generally, one may speak of morphisms in any [[category with weak equivalences]] having the [[homotopy extension property]] with respect to a chosen [[cylinder object]], one speaks of _h-cofibrations_.


## Definition

+-- {: .num_defn #HurewiczCofibration}
###### Definition

A [[continuous function]] $i \colon A \longrightarrow X$ is a **Hurewicz cofibration** if it satisfies the [[homotopy extension property]] in that:

* for any [[topological space]] $Y$, 

* all continuous functions $ f \colon A\to Y$, there exists $\tilde{f}:X\to Y$ such that $\tilde{f}\circ i=f$ 
   
  $$
    \array{
       A &\stackrel{f}{\to}& Y
       \\
       {}^{\mathllap{i}}\downarrow & \nearrow_{\mathrlap{\tilde f}} 
       \\
       X  
    }
  $$


* and any [[left homotopy]] $F \colon A\times I\to Y$ such that $F(-,0)=f$ 

there is a homotopy $\tilde{F} \colon X\times I\to Y$ such that 
  
* $\tilde{F}\circ(i\times id_I)=F$ 

  $$
    \array{
       A \times I &\overset{F}{\longrightarrow}& Y
       \\
       {}^{\mathllap{i \times id_I}}\downarrow & \nearrow_{\mathrlap{\tilde F}}
       \\
       X \times I
    }
  $$

* and $\tilde{F}(-,0)=\tilde{f}$

  $$
    \array{
       A &\overset{id_A \times const_0}{\longrightarrow}& A \times I &\overset{F}{\longrightarrow}& Y
       \\
       {}^{\mathllap{i \times id_I}}\downarrow
       && {}^{\mathllap{i \times id_I}}\downarrow & \nearrow_{\mathrlap{\tilde F}}
       \\
       X &\underset{id_X \times const_0}{\longrightarrow}& X \times I
    }
    \phantom{AAA}
      =
    \phantom{AAA}
    \array{
    \array{
       A &\stackrel{f}{\to}& Y
       \\
       {}^{\mathllap{i}}\downarrow & \nearrow_{\mathrlap{\tilde f}} 
       \\
       X  
    }
    }
  $$


=--

+-- {: .num_defn #ClosedHurewiczCofibration}
###### Definition

A Hurewicz cofibration $i \colon A\to X$ (def. \ref{HurewiczCofibration}) is called a _[[closed cofibration]]_ if the [[image]] $i(A)$ is a [[closed subspace]] in $X$.

=--

If $A\subset X$ is closed and the inclusion is a cofibration, then the pair $(X,A)$ is called an [[NDR-pair]].

There is also a version of the definition for [[pointed spaces]].

## Properties

### Subspace inclusions
 {#Inclusions}

+-- {: .num_prop}
###### Proposition

A [[topological subspace]] inclusion $A \hookrightarrow X $ is a Hurewicz cofibration precisely if $A \times I \cup X \times \{0\}$ is a [[retract]] of $X\times I$.

=--

+-- {: .num_cor}
###### Corollary

A subcomplex inclusion into a [[CW-complex]] is a closed Hurewicz cofibration.

=--

e.g. Bredon _Topology and Geometry_, p. 431


More generally, every [[retract]] of a [[relative cell complex]] inclusion is a closed Hurewicz cofibration. 

This is part of the statement of the [[Quillen adjunction]] between then [[classical model structure on topological spaces]] and the [[Strøm model structure]] (see [below](#StromModelStructure))

### Closedness
 {#Closedness}


Every Hurewicz cofibration $i$ injective and a [[homeomorphism]] onto its image ([Homotopietheorie](#Homotopietheorie) (1.17)). In the category of [[weakly Hausdorff space|weakly Hausdorff]] [[compactly generated spaces]], $i(A)$ is always closed (the same in the category of all [[Hausdorff spaces]]), but in the category [[Top]] of all topological spaces there are pathological counterexamples. 

The simplest example (see [Homotopietheorie](#Homotopietheorie)) is the following: let $A =\{a\}$ and $X=\{a,b\}$ be the one and two element sets, both with the [[codiscrete topology]] (only $X$ and $\emptyset$ are open in $X$), and $i:A\hookrightarrow X$ is the inclusion $a\mapsto a$. Then $i$ is a non-closed cofibration (useful exercise!). 



### Str&#248;m's model structure
 {#StromModelStructure}

The collections

* [[Hurewicz fibrations]],

* closed Hurewicz cofibrations (def. \ref{HurewiczCofibration}, def. \ref{ClosedHurewiczCofibration}),

* and [[homotopy equivalences]] 

make one of the standard Quillen [[model category]] structures on the category [[Top]] of all topological spaces _[[Strøm's model category]]. 

The identity functor $id \colon Top \to Top$ is [[Quillen adjunction|left Quillen]] from the [[classical model structure on topological spaces]] (or the mixed model structure) to the Str&#248;m model structure, and of course right Quillen in the other direction.  

$$
  Top_{Strom}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  Top_{Quillen}
  \,.
$$

This means in particular that any  [[retract]] of a  [[relative cell complex]] inclusion is a closed Hurewicz cofibration.


### Interaction with pullbacks

+-- {: .num_theorem}
###### Theorem

Let

$$
  \array{
     X_0 &\hookrightarrow & X
     \\
     {}^{\mathllap{p_0}}\downarrow && \downarrow^{\mathrlap{p}}
     \\ 
     B_0 &\hookrightarrow& B
     \\
     \uparrow && \uparrow
     \\
     E_0 &\hookrightarrow& E
  }
$$

be a [[commuting diagram]] of [[topological space]]s such that

* the horizontal morphisms are closed cofibrations;

* the morphisms $p_0$ and $p$ are [[Hurewicz fibration]]s.

Then the induced morphism on [[pullback]]s is also a closed cofibration

$$
  X_0 \times_{B_0} E_0 \hookrightarrow X \times_B E
  \,.
$$ 

=--

This is stated and proven in ([Kieboom](#Kieboom)).

+-- {: .num_cor}
###### Corollary

The [[product]] of two closed cofibrations is a closed cofibration.

=--

## References

* [[Dieter Puppe]], _Bemerkungen &#252;ber die Erweiterung von Homotopien_, Arch. Math. (Basel) 18 1967 81--88; MR0206954 (34 #6770) [doi](http://dx.doi.org/10.1007/BF01899475)

* [[Arne Strøm]], _Note on cofibrations_,  Math. Scand.  19  1966 11--14 [file](http://www.mscand.dk/article.php?id=1782) MR0211403 (35 #2284); _Note on cofibrations II_,  Math. Scand.  22  1968 130--142 (1969) [file](http://www.mscand.dk/article.php?id=1867) MR0243525 (39 #4846) 

* {#Homotopietheorie} [[Tammo tom Dieck]], [[Klaus Heiner Kamps]], and [[Dieter Puppe]]. Homotopietheorie. Vol. 157. Springer-Verlag, 1970.

The fact that morphisms of fibrant pullback diagrams along closed cofibrations induce closed cofibrations is in

* {#Kieboom} [[Rudger Kieboom]], _A pullback theorem for cofibrations_, Manuscripta Math **58** (1987) pp 381–384, doi:[10.1007/BF01165895](https://doi.org/10.1007/BF01165895)


[[!redirects Hurewicz cofibrations]]

[[!redirects closed cofibration]]
[[!redirects closed cofibrations]]

[[!redirects closed Hurewicz cofibration]]
[[!redirects closed Hurewicz cofibrations]]
