
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


The _model structure on [[reduced simplicial sets]]_ is a [[presentable (infinity,1)-category|presentation]] of the full [[sub-(∞,1)-category]] 

[[∞Grpd]]${}^{*/}_{\geq 1} \hookrightarrow$ [[∞Grpd]]${}^{*/}$ $\simeq$ [[Top]]${}^{*/}$ 

of [[pointed object|pointed]] [[∞-groupoids]] on those that are [[connected]]. 

By the [[looping and delooping]]-equivalence, this is [[equivalence of (∞,1)-categories|equivalent]] to the [[(∞,1)-category]] of [[∞-groups]] and this equivalence is presented by a [[Quillen equivalence]] to the [[model structure on simplicial groups]].


## Definition


+-- {: .num_defn #ReducedSimplicialSet}
###### Definition

A _[[reduced simplicial set]]_ is a [[simplicial set]] $S$ with a single vertex, hence with $X_0$ [[generalized the|the]] [[singleton set]]

$$
  S_0 \;=\; \ast
  \,.
$$

Write $sSet_0 \subset $ [[sSet]] for the [[full subcategory]] of the category of [[simplicial sets]] on those that are reduced.

=--


+-- {: .num_prop #TheModelStructure}
###### Proposition

There is a [[model category]] structure on $sSet_0$ (def. \ref{ReducedSimplicialSet}) whose

* weak equivalences 

* and cofibrations

are those in the [[classical model structure on simplicial sets]] (i.e. the [[weak homotopy equivalences]] and the [[monomorphisms]], respectively.)

=--

This appears as ([Goerss & Jardine, Ch V, Prop. 6.2](#GoerssJardine)).


## Properties

### Relation to ordinary simplicial sets
 {#RelationToOrdinarySimplicialSets}

+-- {: .num_prop #FibrationsInTermsOfKanFibrations}
###### Proposition

Under the [[forgetful functor]] $U \colon sSet_0 \hookrightarrow sSet$ 

* a fibration $f : X \to Y$ with respect to the reduced model structure (prop. \ref{TheModelStructure}) maps to a fibration in the [[classical model structure on simplicial sets]] (a [[Kan fibration]]) precisely if it has the [[right lifting property]] against $* \to S^1 \coloneqq \Delta[1]/ \partial \Delta[1]$;

In particular

* every [[fibrant object]] maps to a fibrant object.

=--

+-- {: .proof}
###### Proof

The first statment appears as ([Goerss & Jardine, Ch. V, Lemma 6.6.](#GoerssJardine)). The second is an immediate consequence. It appears as ([Goerss & Jardine, Ch. V, Corollary 6.8](#GoerssJardine)).

=--

\begin{corollary}\label{KanFibrationBetweenReducedKanComplexesAsReducedFibration}
  Let $f \colon X \longrightarrow Y$ be a [[fibration]]
  in the model structure on reduced simplicial sets 
  (Prop. \ref{TheModelStructure}) such that both $X$ and $Y$ are 
  [[Kan complexes]].
  Then $f$ is a [[Kan fibration]]
  precisely if it induces a [[surjection]] on 
  the first [[simplicial homotopy group]]
  $\pi_1(f) \colon \pi_1(X) \twoheadrightarrow \pi_1(Y)$. 
\end{corollary}

([Goerss & Jardine, Ch. V, Cor. 6.9](#GoerssJardine))

As an example:

\begin{proposition}\label{DeloopedKanFibrationOfHomomorphismOfSimplicialGroups}
  Let $\mathcal{G}_1 \xrightarrow{\phi} \mathcal{G}_2$ be a [[homomorphism]] of [[simplicial groups]] which is a [[Kan fibration]].
Then the induced morphism of [[simplicial classifying spaces]]
$\overline{W}\mathcal{G}_1 \xrightarrow{ \overline{W}(\phi)} \overline{W}\mathcal{G}_2$ is a [[Kan fibration]] if and only if $\phi$ is a [[surjection]] on [[connected components]]: $\pi_0(\phi) \colon \pi_0(\mathcal{G}_1) \twoheadrightarrow{\;} \pi_0(\mathcal{G}_1)$.
\end{proposition}
([Goerss & Jardine, Ch. V, Cor. 6.9](#GoerssJardine))
\begin{proof}
  Since $\overline{W}(-)$ is a [[right Quillen functor]] to the model structure on reduced simplicial sets (Prop. \ref{QuillenAdjunctionWithSimplicialGroups}) it follows that $\overline{W}(\phi)$ is in any case a fibration in that model structure. Hence Cor. \ref{KanFibrationBetweenReducedKanComplexesAsReducedFibration} implies that $\overline{W}(\phi)$ is a Kan fibration precisely of $\pi_1 \circ \overline{W}(\phi)$ is surjective. But $\pi_1 \circ \overline{W} = \pi_0$, by [this Prop](simplicial+classifying+space#HomotopyGroupsOfBarWG).
\end{proof}


### Relation to pointed simplicial sets
 {#RelationToPointedSimplicialSets}

+-- {: .num_prop #CoreflectiveQuillenAdjunctionToPointedSimplicialSets}
###### Proposition

The [[coreflective embedding]]

$$
  sSet^{\ast/}
   \underoverset
     {\underset{cn}{\longrightarrow}}
     {\overset{i}{\longleftarrow}}
     {\bot}
  sSet_{0}
$$

into [[pointed simplicial sets]] (where $i$ the obvious inclusion, and $cn$ forms the 1st [[Eilenberg subcomplex]] over the basepoint) is a [[Quillen adjunction]] 
(with respect to the reduced model structure from prop. \ref{TheModelStructure} and the [[coslice model structure]] under the point of the [[classical model structure on simplicial sets]]).

=--

+-- {: .proof}
###### Proof

By prop. \ref{TheModelStructure} the left adjoint preserves cofibrations and acyclic cofibrations (in fact all weak equivalences).

=--



+-- {: .num_prop #SuspensionQuillenAdjunctionWithReducedSimplicialSets}
###### Proposition

The operation of [[reduced suspension]] $\Sigma_\ast$ ([[smash product]] with the simplicial circle $S^1 \coloneqq \Delta[1]/\partial \Delta[1]$) and forming [[loop space]] $\Omega_\ast$ ([[pointed mapping space]] out of the circle) constitute a [[Quillen adjunction]] 


$$
  sSet_0
    \underoverset
      {\underset{\Omega_\bullet}{\longrightarrow}}
      {\overset{\Sigma_\ast}{\longleftarrow}}
      {\bot}
  sSet^{\ast/}
$$

=--

+-- {: .proof}
###### Proof

By the [[internal hom]] construction we have the [[adjunction]]

$$
  sSet^{\ast/}
    \underoverset
      {\underset{\Omega_\bullet}{\longrightarrow}}
      {\overset{\Sigma_\ast}{\longleftarrow}}
      {\bot}
  sSet^{\ast/}
$$


But by the formula at [[smash product]] the [[reduced suspension]] clearly lands in [[reduced simplicial sets]], so that we do have the restricted adjunction as claimed. Now by the fact that the [[classical model structure on simplicial sets]] is a [[simplicial model category]], the above is a [[Quillen adjunction]] and $\Sigma_\ast$ preserves cofibrations and acyclic cofibrations. Hence, by prop. \ref{TheModelStructure}, so does its factorization through the model structure on reduced simplicial sets. 

=--

+-- {: .num_cor #LoopingSuspensionQuillenAdjunction}
###### Corollary

The operations of [[reduced suspension]] and [[loop space]] (co-)restrict to a [[Quillen adjunction]] on the reduced model structure (prop. \ref{TheModelStructure}) itself, by [[composition]] of the Quillen adjunctions from prop. \ref{CoreflectiveQuillenAdjunctionToPointedSimplicialSets} and prop. \ref{SuspensionQuillenAdjunctionWithReducedSimplicialSets}.

$$
  sSet_0
    \underoverset
      {\underset{\Omega_\bullet}{\longrightarrow}}
      {\overset{\Sigma_\ast}{\longleftarrow}}
      {\bot}
  sSet^{\ast/}
   \underoverset
     {\underset{cn}{\longrightarrow}}
     {\overset{i}{\longleftarrow}}
     {\bot}
  sSet_{0}
$$


=--



### Relation to simplicial groups
 {#RelationToSimplicialGroups}

+-- {: .num_prop #QuillenAdjunctionWithSimplicialGroups}
###### Proposition
**([[Quillen equivalence between simplicial groups and reduced simplicial sets]])**

The [[simplicial loop space]] functor $G$ and the [[simplicial classifying space]]-construction $\overline{W}(-)$ constitute a [[Quillen equivalence]]

$$
  (G \dashv \overline{W}) \colon 
    sGr 
      \underoverset
        {\underset{\overline{W}}{\longrightarrow}}
        {\overset{G}{\longleftarrow}}
        {\;\;\;\;\;\;\;\;\bot\;\;\;\;\;\;\;\;}
    sSet_0
$$

between the model structure on reduced simplicial sets from prop. \ref{TheModelStructure} and [[model structure on simplicial groups]].

=--

This appears as ([Goerss-Jardine, ch. V prop. 6.3](#GoerssJardine)).


## Related concepts

* [[model structure on simplicial groups]]

* **model structure on reduced simplicial sets**

* [[groupoid object in an (∞,1)-category]], [[∞-group]], [[looping and delooping]]

## References

Textbook account:


* {#GoerssJardine} [[Paul Goerss]], [[J. F. Jardine]], Chapter V in: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

