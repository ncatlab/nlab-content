# Initiality Project - Substitution

This page is part of the [[Initiality Project]].

* table of contents
{:toc}

## Statements

Based on the definition of the [[Initiality Project - Partial Interpretation|partial interpretation functions]], we now prove the following substitution properties by mutual induction over raw terms and types.

### Weakening, exchange, and contraction

Let $V_1,V_2 \subseteq Var$ be finite, and suppose $\theta : V_1\to V_2$ is a function.  Then:

* For any raw type $A$, the composite partial morphism $Tm^{V_2} \xrightarrow{Tm^\theta} Tm^{V_1} \overset{\llbracket A \rrbracket^{V_1}_{type}}\rightharpoonup Ty$ is contained in the partial morphism  $Tm^{V_2} \overset{\llbracket A[\theta] \rrbracket^{V_2}_{type}}\rightharpoonup Ty$.
* For any raw term $T$, the composite partial morphism $Tm^{V_2} \xrightarrow{Tm^\theta} Tm^{V_1} \overset{\llbracket T \rrbracket^{V_1}_{\Rightarrow}}\rightharpoonup Tm$ is contained in the partial morphism  $Tm^{V_2} \overset{\llbracket T[\theta] \rrbracket^{V_2}_{\Rightarrow}}\rightharpoonup Tm$.
* For any raw term $T$, the composite partial morphism $Tm^{V_2}\times Ty \xrightarrow{Tm^\theta} Tm^{V_1} \times Ty \overset{\llbracket T \rrbracket^{V_1}_{\Leftarrow}}\rightharpoonup Tm$ is contained in the partial morphism  $Tm^{V_2}\times Ty \overset{\llbracket T[\theta] \rrbracket^{V_2}_{\Leftarrow}}\rightharpoonup Tm$.

Here $A[\theta]$ and $T[\theta]$ denote simultaneous capture-avoiding substitution of $\theta(x)$ for each variable $x\in V_1$.  When $\theta$ is a bijection, this asserts invariance under renaming of free variables.  When $\theta$ is an inclusion, it asserts weakening, and when $\theta$ is surjective it is contraction.  Note that in general these containments can be strict, e.g. if some variable in $V_2 \setminus \theta(V_1)$ appears freely in $A$ or $T$, then the composites may have empty domain while the morphisms they are being compared to might not.

### Substitution

Let $V\subseteq Var$ be finite and $x\in Var\setminus V$, while $N$ is a raw term.  Then:

* For any raw type $A$, the composite partial morphism $Tm^V \overset{(id,\llbracket N \rrbracket^V_{\Rightarrow})}{\rightharpoonup} Tm^{V\cup \{x\}} \overset{\llbracket A \rrbracket^{V\cup \{x\}}_{type}}{\rightharpoonup} Ty$ is contained in the partial morphism $Tm^V \overset{\llbracket A[N/x] \rrbracket^V_{type}}{\rightharpoonup} Ty$.
* For any raw term $T$, the composite partial morphism $Tm^V \overset{(id,\llbracket N \rrbracket^V_{\Rightarrow})}{\rightharpoonup} Tm^{V\cup \{x\}} \overset{\llbracket T \rrbracket^{V\cup \{x\}}_{\Rightarrow}}{\rightharpoonup} Tm$ is contained in the partial morphism $Tm^V \overset{\llbracket T[N/x] \rrbracket^V_{\Rightarrow}}{\rightharpoonup} Tm$.
* For any raw term $T$, the composite partial morphism $Tm^V\times Ty \overset{(id,\llbracket N \rrbracket^V_{\Rightarrow},id)}{\rightharpoonup} Tm^{V\cup \{x\}}\times Ty \overset{\llbracket T \rrbracket^{V\cup \{x\}}_{\Leftarrow}}{\rightharpoonup} Tm$ is contained in the partial morphism $Tm^V \times Ty\overset{\llbracket T[N/x] \rrbracket^V_{\Leftarrow}}{\rightharpoonup} Tm$.

## Inductive clauses

TODO.
