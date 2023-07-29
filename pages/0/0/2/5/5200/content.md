
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}

## Idea

The flavor of (classical) _[[modal logic]]_ called $S4$ is (classical) [[propositional logic]] equipped with a single [[modality]] usually written "$\Box$" subject to the rules that for all [[propositions]] $p, q \colon Prop$ we have

1. $\Box K \colon \Box(p \to q) \to (\Box p \to \Box q)$ ([[K modal logic]])

1. $\Box T \colon \Box p \to p$ ([[T modal logic]])

1. $\Box 4 \colon \Box p \to \Box \Box p$. (S4 modal logic)

1. (in addition in [[S5 modal logic]] one adds: $\lozenge p \to \Box \lozenge p$).


Traditionally the canonical interpretation of the Box operator is that $\Box p$ is the statement that "$p$ is _[[necessity|necessarily]]_ true." (The [[de Morgan duality|de Morgan dual]] to the necessity modality is the "[[possibility]]" modality.) Then the interpretation of $\Box $ is that "If $p$ is necessarily true then it is necessarily necessarily true."
S4 modal logic appears in many [[temporal logics]].


If instead of a single Box operator one considers $n \in \mathbb{N}$ box operators $\Box_i$ of this form, the resulting modal logic is denoted $S4(n)$. Here $\Box_i p$ is sometimes interpreted as "the $i$th agent knows $p$."

In intuitionistic (or constructive) Modal Logic, one does not expect the possibility modality to be dual to the necessity modality, necessarily. [[Alex Simpson]] has written in his thesis the most used constructive modal logic system, but other systems exist.

## Properties

### Relation to Kripke frames

The [[models]] for [[T modal logic]] corresponded to [[Kripke frames]] where each [[relation]] $R_i$ is [[reflexive relation|reflexive]].  
For $S4$ modal logic they are furthermore [[transitive relation|transitive]].

+-- {: .un_theorem}
###### Theorem (Soundness of $S4_{(m)}$)

$S4_{(m)}\vdash \phi \Rightarrow \mathcal{S}4(m)\models \phi.$
=--

+-- {: .proof}
###### Proof

(We show this for $m = 1$.)

Suppose that $\mathfrak{M}= ((W,R),V)$ where $R$ is a reflexive transitive relation on $W$.  We have to check that $\mathfrak{M}\models (4)$.

Suppose $\mathfrak{M},w\models K p$, then, for every  $t$ with $R w t$, we have $\mathfrak{M},t\models p$.  Now suppose we seek to check that $\mathfrak{M},w\models K K p$ so we have $t$ with $R w t$ and want $\mathfrak{M},t\models K p$, so we look at all $u$ with $R t u$ and have to see if $\mathfrak{M},u\models p$, but as $R w t$ and $R t u$ hold then $R w u$ holds, since $R$ is transitive, and we then _know_ that $\mathfrak{M},u\models p$.
=--

## Related concepts

* [[modal logic]], [[S5 modal logic]]

* [[epistemic modal logic]], [[necessity and possibility]]

* [[K modal logic]]
  
* [[T modal logic]]

* [[Kripke frame]]

* [[Löb's axiom]]


## References

The terminology "S4" in modal logic originates with:

* [[Clarence I. Lewis]], [[Cooper H. Langford]], App. II, p 501 of: *Symbolic Logic* (1932), Dover (2000) &lbrack;App. II [pdf](https://www.hist-analytic.com/Lewisstrict.pdf)&rbrack;

The "[[possible worlds]]" [[Kripke semantics]] of S4 originates with:

* {#Kripke63} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic I. Normal Modal Propositional Calculi*, Mathematical Logic Quaterly **9** 5-6 (1963) 67-96 &lbrack;[doi:10.1002/malq.19630090502](https://doi.org/10.1002/malq.19630090502)&rbrack;

See also:

* {#Kripke80} [[Saul Kripke]], _[[Naming and Necessity]]_ (1980)


A [[natural deduction]]-formulation and making explicit the [[modal operator]] as a [[comonad]]:

* {#BiermanDePaiva96} [[Gavin M. Bierman]], [[Valeria de Paiva]], *Intuitionistic necessity revisited*, School of Computer Science research reports-University of Birmingham CSR (1996) &lbrack;[researchgate](https://www.researchgate.net/publication/2810611_Intuitionistic_Necessity_Revisited), [[Bierman-dePaiva-NecessityRevisited.pdf:file]]&rbrack;

* [[Gavin M. Bierman]], [[Valeria de Paiva]], _On an Intuitionistic Modal Logic_ Studia Logica **65** (2000) 383–416 &lbrack;[doi:10.1023/A:1005291931660](https://doi.org/10.1023/A:1005291931660), [pdf] (https://www.researchgate.net/profile/Valeria-De-Paiva/publication/226515897_On_An_Intuitionistic_Modal_Logic/links/00b4951ed416906ccc000000/On-An-Intuitionistic-Modal-Logic.pdf)&rbrack;

* {#Kobayashi97} [[Satoshi Kobayashi]], *Monad as modality*, Theoretical Computer Science **175** 1 (1997) 29-74 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(96)00169-7">doi:10.1016/S0304-3975(96)00169-7</a>&rbrack;

* Natasha Alechina, Michael Mendler, [[Valeria de Paiva]], Eike Ritter: *Categorical and Kripke Semantics for Constructive S4 Modal Logic*, in *Computer Science Logic. CSL 2001* Lecture Notes in Computer Science **2142**, Springer (2001) 292 &lbrack;[doi:10.1007/3-540-44802-0_21](https://doi.org/10.1007/3-540-44802-0_21)&rbrack;

See also:

* [[Alex Simpson]], _The proof theory and semantics of intuitionistic modal logic_ (1994) &lbrack;[pdf] (https://era.ed.ac.uk/handle/1842/407), [handle:1842/407](http://hdl.handle.net/1842/407)&rbrack;

More on $S4$, $S5_{(m)}$ and their applications in Artificial Intelligence can be found in

* J.- J. Ch. Meyer and W. Van der Hoek, _Epistemic logic for AI and Computer Science_, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995.


General books on modal logics which treat  these logics thoroughly in the general context include 

* [[Patrick Blackburn]], M. de Rijke and [[Yde Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.


[[!redirects the logic S4(m)]]
[[!redirects S4(m)]]
[[!redirects S4 modal logic]]

[[!redirects S4]]

