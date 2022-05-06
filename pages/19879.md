# Initiality Project - Totality

This page is part of the [[Initiality Project]].

* table of contents
{: toc}

## Overview

We now prove that the [[Initiality Project - Partial Interpretation|partial interpretations]] of types, terms, and contexts satisfy the following "local" totality properties, for any raw context $\Gamma$ with variables $V$.

1. If $\Gamma \vdash A\, type$ is derivable, then the domain of $\llbracket A \rrbracket^V_{type} : Tm^V \rightharpoonup Ty$ contains $\llbracket\Gamma\rrbracket$.
1. If $\Gamma \vdash T \Rightarrow A$ is derivable, then the domain of $\llbracket T \rrbracket^V_{\Rightarrow} : Tm^V \rightharpoonup Tm$ contains $\llbracket\Gamma\rrbracket$, and the composite $Tm^V \overset{\llbracket T \rrbracket^V_{\Rightarrow}}{\rightharpoonup} Tm \to Ty$ agrees with $\llbracket A \rrbracket^V_{type}$ on $\llbracket\Gamma\rrbracket$.
1. If $\Gamma \vdash T \Leftarrow A$ is derivable, then the domain of $\llbracket T \rrbracket^V_{\Leftarrow} : Tm^V \times Ty \rightharpoonup Tm$ contains the subobject defined by $\llbracket\Gamma\rrbracket \hookrightarrow Tm^V \overset{(id,\llbracket A \rrbracket^V_{type})}{\rightharpoonup} Tm^V \times Ty$.
1. If $\Gamma \vdash A \equiv B \, type$ is derivable, then $\llbracket A \rrbracket^V_{type}$ and $\llbracket B \rrbracket^V_{type}$ agree on $\llbracket\Gamma\rrbracket$.
1. If $\Gamma \vdash S \equiv T : A$ is derivable, then $\llbracket S \rrbracket^V_{\Leftarrow}$ and $\llbracket T \rrbracket^V_{\Leftarrow}$ agree on the subobject $\llbracket\Gamma\rrbracket \hookrightarrow Tm^V \times Ty$ defined in (3) above.

The proof is by mutual induction on these mutually defined inductive judgments; thus we have one clause for each primitive rule in our [[Initiality Project - Type Theory|type theory]].

## Inductive clauses

### Variables

### Mode-switching

### Equality

### Constants

### $\Pi$-types

include [[Initiality Project - Totality - Pi-types]]

## Valid Contexts

The above totality theorem is called "local" because it only says the interpretations are defined on the interpretation of the context; if the context is invalid then the latter interpretation could be empty.  However, with the local totality theorem in hand, we can deduce a *global* totality theorem for valid contexts.  Note that this parallels how the notion of valid context was defined after giving the inductive definition of the judgments, and also how the partial interpretation of contexts was defined after giving the partial interpretations of types and terms.

The global totality theorem is:

+-- {: .un_theorem}
###### Theorem
If $\Gamma$ is a valid context, then $\llbracket \Gamma \rrbracket$ is a [[representable presheaf]].
=--
+-- {: .proof}
###### Proof
By induction on the length of $\Gamma$.  If it is empty, then $\llbracket () \rrbracket = 1$, the terminal presheaf, which is representable as our CwF $C$ has a terminal object.

For a context extension $(\Gamma,x:A)$, by induction we have $\llbracket \Gamma \rrbracket$ representable.  [[Initiality Project - Partial Interpretation|Recall]] that $\llbracket\Gamma,x:A\rrbracket$ is defined as a pullback
$$ \array { \llbracket \Gamma, x:A \rrbracket & \to & Tm \\ \downarrow & & \downarrow \\ U & \to & Ty. }$$
Since $Tm\to Ty$ is, by our definition of CwF, a [[representable morphism]], it will therefore suffice to show that $U$ is a representable object.

Now $U$ is by definition the intersection of $\llbracket\Gamma\rrbracket$ with the domain of $\llbracket A \rrbracket^V_{type}$.  But since $(\Gamma,x:A)$ is valid, $\Gamma \vdash A \, type$ is derivable, so by the local totality theorem, the domain of $\llbracket A \rrbracket^V_{type}$ *contains* $\llbracket \Gamma \rrbracket$.  Thus, $U = \llbracket \Gamma \rrbracket$, which is representable by the inductive hypothesis.
=--

Furthermore, since $Tm\to Ty$ is *algebraically* represented, at each step we obtain a specified representing object for $\llbracket\Gamma\rrbracket$.  We henceforth abusively denote this object of $C$ also by $\llbracket\Gamma\rrbracket$.

Combining this with the local totality theorem, we can extract more traditional-looking interpretations of derivable judgments with valid contexts that are "purely inside $C$" rather than phrased in terms of presheaves.

* If $\Gamma$ is valid and $\Gamma \vdash A\,type$ is derivable, we have (by local totality) a total morphism $\llbracket \Gamma \rrbracket \xrightarrow{\llbracket A \rrbracket^V_{type}} Ty$, hence (by the Yoneda lemma) an element of the set $Ty(\llbracket \Gamma\rrbracket)$, which we may denote $\llbracket A \rrbracket^\Gamma_{type}$.
* If $\Gamma$ is valid and $\Gamma \vdash T \Rightarrow A$ is derivable, we have a total morphism $\llbracket \Gamma \rrbracket \xrightarrow{\llbracket A \rrbracket^V_{\Rightarrow}} Tm$, hence an element of the set $Tm(\llbracket \Gamma\rrbracket)$ which we may denote $\llbracket T \rrbracket^\Gamma_{\Rightarrow}$.  By the rest of the local totality theorem for type synthesis, the underlying semantic type of this semantic term is $\llbracket A \rrbracket^\Gamma_{type}$.
* If $\Gamma$ is valid and $\Gamma \vdash T \Leftarrow A$ is derivable, we similarly obtain an element $\llbracket T \rrbracket^\Gamma_{\Leftarrow A}$ of $Tm(\llbracket \Gamma\rrbracket)$, whose underlying semantic type is $\llbracket A \rrbracket^\Gamma_{type}$.
