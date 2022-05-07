+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contens
{:toc}

## Idea

Given a [[geometric morphism]] $f \colon \mathcal{E} \longrightarrow \mathcal{S}$, we may regard $\mathcal{E}$ as a *[[topos]] [[base topos|over]] $\mathcal{S}$* via $f$.  The geometric morphism $f$ being *bounded* is the "over $\mathcal{S}$" version of $\mathcal{E}$ being a [[Grothendieck topos]].


## Definition

+-- {: .num_defn}
###### Definition

A [[geometric morphism]] $f = (f^*\dashv f_*) \colon \mathcal{E} \longrightarrow \mathcal{S}$ between [[toposes]] is called **bounded**, if any of the following three equivalent condition holds.

* There exists an [[object]]  $B \in \mathcal{E}$ -- called a **bound** of $f$ -- such that every $A \in \mathcal{E}$ 
is a [[subquotient]] of an object of the form $(f^* I) \times B$ for some $I  \in \mathcal{S}$: this means that there exists a diagram

  $$
    \array{
      S &\xrightarrow{\; epi \;}& A
      \\
      {}^{\mathllap{mono}}
      \big\downarrow  
      \\
      (f^* I) \times B
    }
    \,.
  $$

* {#TheGluingFibration} The [[gluing fibration]] $(\mathcal{E}/f^*)\to \mathcal{S}$ has a [fibered separating family](separating+family#fibered).

* The exists a $B\in\mathcal{E}$ such that for every $A\in\mathcal{E}$ the 
composite

  $$
    f^*f_*(\tilde A^B)
      \times 
    B
      \to 
    \tilde A^B\times B\to \tilde A
   $$

   is an [[epimorphism]], where $\tilde A$ is the [[partial map classifier]] of $A$.

=--

+-- {: .proof}
###### Proof of the equivalence.

Lemma B3.1.6 in the [[Elephant]]

=--


If we regard $\mathcal{E}$ as a topos over $\mathcal{S}$ via $f$, then when $f$ is bounded we call $\mathcal{E}$ a **bounded $\mathcal{S}$-topos**.

## Properties

### As relative Grothendieck toposes

If $f \coloneqq \Gamma\colon \mathcal{E}\to Set$ is the [[global section]] geometric morphism of a topos (such a geometric morphism being unique if it exists), then it is bounded if and only if $\mathcal{E}$ is a [[Grothendieck topos]]. As such we can also call Grothendieck toposes "bounded [[Set]]-toposes".

More generally, bounded toposes over $\mathcal{S}$ are precisely the toposes of $\mathcal{S}$-valued [[internal sheaves]] on [[internal sites]] in $\mathcal{S}$ ([Johnstone, Section B3.3](#Johnstone)).

If $f \colon \mathcal{E}\to\mathcal{S}$ is bounded and $\mathcal{S}$ is a [[Grothendieck topos]], then $\mathcal{E}$ is a Grothendieck topos as well. This is a consequence of prop. \ref{StabilityUnderComposition}.

### Stability under composition

+-- {: .num_prop #StabilityUnderComposition}
###### Proposition

Bounded geometric morphisms are stable under [[composition]].

=--

+-- {: .proof}
###### Proof

Assume that $f : \mathcal{F} \to \mathcal{S}$ is bounded by $B\in\mathcal{F}$, and  $g:\mathcal{G}\to\mathcal{F}$ is bounded by $C\in\mathcal{G}$. Let $A\in\mathcal{G}$. Then there exist $J\in \mathcal{F}$ and $I\in\mathcal{S}$, and  subquotient spans
$g^*J\times C\leftarrow\bullet\rightarrow A$ 
and 
$f^*I\times B\leftarrow\bullet\rightarrow J$. 
By applying $g^*(-)\times C$ to the second subquotient and forming a pullback, we get the diagram
$$
\begin{matrix}
\bullet & \to & \bullet & \to A \\
\downarrow && \downarrow \\
\bullet & \rightarrow & g*J\times C \\
\downarrow \\
g^*f^* I\times g^* B \times C
\end{matrix}
$$
where the vertical arrows are monos and the horizontal ones are epis (using the fact that epis are stable under $g^*$, products, and pullbacks), from which we can see that $f g$ is bounded by $g^*B\times C$.

=--

Almost all geometric morphisms in practice are bounded, so that often when people work in the 2-category [[Topos]] of toposes and geometric morphisms, they mean that the geometric morphisms are bounded. See [[unbounded topos]] for the few examples of unbounded geometric morphisms. 

## Related concepts

* [[base topos]]
* [[internal site]]
* [[internal sheaf]]
* [[unbounded topos]]

## References

definition B3.1.7 in

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_


[[!redirects bounded geometric morphisms]]

[[!redirects bounded topos]]
[[!redirects bounded toposes]]
[[!redirects bounded topoi]]