
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


### Between topological spaces

A [[continuous function]]  $f \colon X \longrightarrow Y$ between [[topological spaces]]  is called __closed__ if the [[image]] of every [[closed subset]] in $X$ is also closed in $Y$.

Recall that $f$ is a __[[continuous map]]__ if the [[preimage]] of every [[closed subspace|closed set]] in $Y$ is closed in $X$.  For defining closed maps typically one restricts attention to closed [[continuous map]]s, although it also makes sense to speak of closed functions that are not continuous.



### Between locales

+-- {: .num_defn #ClosedMapOfLocales}
###### Definition

A map $f : X \to Y$ of [[locales]] is _closed_ iff for any $u \in O(X)$ and $v \in O(Y)$ the [[reciprocity]] relation
$$ f_*(u \vee f^*v) = f_*(u) \vee v $$
holds. ("$\geq$" is trivially always satisfied.) The map $f_* : O(X) \to O(Y)$ is the monotone [[right adjoint]] to $f^* : O(Y) \to O(X)$, explicitly given by
$$ f_*(u) = \sup\{ v \in O(Y) \,|\, f^*(v) \leq u \}. $$

=--

### Between toposes

+-- {: .num_defn}
###### Definition

A [[geometric morphism]] $f \;\colon\; \mathcal{F} \longrightarrow \mathcal{E}$ of [[toposes]] is _closed_ iff for any [[object]] $A \in \mathcal{E}$, the induced [[locale]] [[homomorphism]] 

$$ 
  \mathrm{Sub}_{\mathcal{F}/f^*A}(1) \to \mathrm{Sub}_{\mathcal{E}}(1) 
$$

between the spaces of [[subobjects]] of the corresponding [[terminal objects]] is closed in the sense of def. \ref{ClosedMapOfLocales}.

=--

+-- {: .num_example}
###### Example

Let $A$ be an object of a topos $\mathcal{E}$. Then the canonical [[etale geometric morphism]] $\mathcal{E}/A \to A$ is closed iff $A$ fulfills the following condition, formulated in the [[internal language]]:
$$ \mathcal{E} \models \forall U \subseteq A{:} \forall p \in \Omega{:} \quad A \subseteq (U \cup \{ x \in A \,|\, p \}) \quad\Rightarrow\quad (A \subseteq U) \vee p. $$
Note that this condition is satisfied for any $A$ whatsoever if the [[internal language]] of $\mathcal{E}$ is [[Boolean topos|boolean]].

=--

+-- {: .num_example}
###### Example

Let $f : A \to B$ be a morphism in a topos $\mathcal{E}$. Then the induced geometric morphism $\mathcal{E}/A \to \mathcal{E}/B$ is closed iff, in the internal language of $\mathcal{E}$, the fibers of $f$ fulfill the condition displayed at the previous example.
=--

+-- {: .num_remark}
###### Remark

A [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ is closed iff, in the [[internal language]] of $\mathcal{E}$, the unique locale map $f_* \Omega_{\mathcal{F}} \to \mathrm{pt}$ into the one-point space (given by the frame $\Omega_{\mathcal{E}}$) is closed.
=--

## Related concepts

* [[open morphism]], [[open geometric morphism]]

* [[étale morphism]]

* [[separated morphism]]

* [[covert space]]

## References

Closed maps of locales and toposes are discussed in section C3.2 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_.
 {#Johnstone}


[[!redirects closed morphisms]]

[[!redirects closed map]]
[[!redirects closed maps]]

[[!redirects closed geometric morphism]]
[[!redirects closed geometric morphisms]]
