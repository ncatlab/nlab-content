# Initiality Project - Partial Interpretation

This page is part of the [[Initiality Project]].

* table of contents
{: toc}

## Overview

Let $C$ be a [[Initiality Project - Semantics|category with families]], with presheaves $Ty$ and $Tm$ of "semantic types" and "semantic terms".  Given a finite set of variables $V \subseteq Var$, we define the **presheaf of environments** for $V$ to be $Tm^V$.  We will define, by structural induction on any term $T$, and any any finite set $V$ of variables, the following [[partial morphisms]] of presheaves.

1. $\llbracket T \rrbracket ^V_{type} : Tm^V \rightharpoonup Ty$.
1. $\llbracket T \rrbracket ^V_{\Rightarrow} : Tm^V \rightharpoonup Tm$.
1. $\llbracket T \rrbracket ^V_{\Leftarrow} : Tm^V \times Ty \rightharpoonup Tm$ such that the composite $Tm^V \times Ty \rightharpoonup Tm \to Ty$ is the second projection.

In fact, the third of these is not actually inductive at all: it is simply a semantic counterpart of the bidirectional mode-switching judgment.  We define $\llbracket T \rrbracket ^V_{\Leftarrow}$ to be the domain restriction of
$$ Tm^V \times Ty \xrightarrow{pr_1} Tm^V \overset{\llbracket T \rrbracket ^V_{\Rightarrow}}{\rightharpoonup} Tm $$
to the equalizer of
$$ Tm^V \times Ty \xrightarrow{pr_1} Tm^V \overset{\llbracket T \rrbracket ^V_{\Rightarrow}}{\rightharpoonup} Tm \to Ty $$
and the restriction of the second projection $Tm^V \times Ty$ to its domain.

The inductive clauses of the definitions of $\llbracket T \rrbracket ^V_{type}$ and $\llbracket T \rrbracket ^V_{\Rightarrow}$ will be given below.  This is an induction over *raw syntax*, but the clauses *should* be defined to precisely mirror the bidirectional rules of our [[Initiality Project - Type Theory|type theory]], using recursive calls to the above three operations as counterparts of the three syntactic judgments $\Gamma \vdash A\,type$, $\Gamma \vdash T\Rightarrow A$, and $\Gamma \vdash T\Leftarrow A$ (and checks for semantic equality as a counterpart of the syntactic equality judgments).  This correspondence will then enable the [[Initiality Project - Totality|proof of totality]] to proceed straightforwardly.

## Inductive Clauses

### Variables

If $T$ is a variable $x$, then:

* $\llbracket x \rrbracket ^V_{type}$ is the empty partial function (this might change with Russell universes).
* If $x\notin V$, then $\llbracket x \rrbracket ^V_{\Rightarrow}$ is the empty partial function.
* If $x\in V$, then $\llbracket x \rrbracket ^V_{\Rightarrow} : Tm^V \rightharpoonup Tm$ is the (total) projection onto the $x^{th}$ factor.

### Constants

TODO

### $\Pi$-types

include [[Initiality Project - Partial Interpretation - Pi-types]]

## Contexts
 {#Contexts}

Now that we have interpreted raw terms as semantic terms and semantic types, we can interpret raw contexts as well.  Suppose $\Gamma$ is a raw context, and let $V$ be the finite (ordered) set of variables occuring in $\Gamma$.  We define a sub-presheaf $\llbracket \Gamma \rrbracket \subseteq Tm^V$ by induction on the length of $\Gamma$ as follows.

* For the empty context $()$, we have $\llbracket () \rrbracket = Tm^0 = 1$, the terminal presheaf.
* For an extended context $(\Gamma, x:A)$, with variables $V \cup \{x\}$ where $x\notin V$, we inductively have $\llbracket \Gamma \rrbracket \subseteq Tm^V$.  We also have (as defined above inductively) $\llbracket A \rrbracket^V_{type} : Tm^V \rightharpoonup Ty$.  Let $U$ be the intersection of $\llbracket \Gamma \rrbracket$ and the domain of $\llbracket A \rrbracket^V_{type}$, and let $\llbracket \Gamma, x:A \rrbracket$ be defined by the following pullback, where the bottom arrow is the composite $U \hookrightarrow Tm^V \overset{\llbracket A \rrbracket^V_{type}}{\rightharpoonup} Ty $.
  $$ \array { \llbracket \Gamma, x:A \rrbracket & \to & Tm \\ \downarrow & & \downarrow \\ U & \to & Ty }$$
  We equip it with the composite $\llbracket \Gamma, x:A \rrbracket \to U \times Tm \to Tm^V \times Tm$, which is a composite of two monomorphisms and hence itself a monomorphism.  Thus $\llbracket \Gamma, x:A \rrbracket$ is indeed a sub-presheaf of $Tm^{V\cup \{x\}} \cong Tm^V \times Tm$ as intended.

category: Initiality Project