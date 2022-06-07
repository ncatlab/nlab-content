
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $C$ and $D$ two [[categories]], the **product category** $C \times D$ is the category whose

* [[object]]s are ordered [[pairs]] $(c,d)$ with $c$ an object of $C$ and $d$ an object of $D$;

* [[morphism]]s are ordered pairs $((c \stackrel{f}{\to} c'),(d \stackrel{g}{\to} d'))$,

* composition of morphisms is defined componentwise by composition in $C$ and $D$.

This operation is the [[cartesian product]] in the 1-category [[Cat]].

## In homotopy type theory
 {#InHomotopyTypeTheory}

We discuss cartesian products for [[internal category in homotopy type theory|categories in homotopy type theory]].

Note: [UFP 2013](#UFP13) calls a [[internal category in homotopy type theory|category]] a "precategory" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

### Definition

For categories $A$ and $B$, their **product** $A \times B$ is a category with $(A\times B)_0\equiv A_0 \times B_0$ and

$$hom_{A \times B}\big((a,b),(a',b')\big)\equiv hom_A (a,a')\times hom_B (b,b')$$

Identities are defined by $1_{(a,b)}\equiv (1_a,1_b)$ and composition by

$$(g,g')(f,f') \equiv \big((gf),(g'f')\big)$$

### Properties
 {#InHoTTProperties}

\begin{lemma}\label{Lemma953}
**(Lemma 9.5.3 in [UFP13](#UFP13))**
\linebreak
For [[categories]] $A,B,C$, the following types are [[equivalent]]:

1. Functors $A \times B \to C$
1. Functors $A \to C^B$

\end{lemma}

\begin{proof}
Given $F : A \times B \to C$, for any $a:A$ we obviously have a functor $F_a : B \to C$. This gives a function $A_0 \to (C^B)_0$. Next, for any $f: hom_A(a,a')$, we have for any $b:B$ the morphisms $F_{(a,b),(a',b')}(f,1_b):F_a(b) \to F_{a'}(b)$. 

These are the components of a [[natural transformation]] $F_a \to F_{a'}$. Functoriality in $a$ is easy to check, so we have a functor $\hat{F} : A \to C^B$.

Conversely, suppose given $G:A \to C^B$. Then for any $a:A$ and $b:B$ we have the object $G(a)(b):C$, giving a function $A_0 \times B_0 \to C_0$. And for $f:hom_A(a,a')$ and $g : hom_B(b,b')$, we have the morphism

$$G(a')_{b,b'}(g) \circ G_{a,a'}(f)_b= G_{a,a'}(f)_{b'} \circ G(a)_{b,b'}(g)$$

in $hom_C(G(a)(b),G(a')(b'))$. Functoriality is again easy to check, so we have a functor $\v{G} : A \times B \to C.$ Finally, it is also clear that these operations are inverses. 
\end{proof}

## Related concepts

* [[bifunctor]]

* [[extranatural transformation]]

* [[Yoneda lemma]]

## References ##

Discussion in [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects product categories]]

[[!redirects product of categories]]
