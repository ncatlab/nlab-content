
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In [[type theory]]: the the _natural numbers type_ is the [[type]] of [[natural numbers]]. 


## Definition

+-- {: .num_defn #InferenceRules}
###### Definition

The [[type of natural numbers]] $\mathbb{N}$ is the [[inductive type]] defined by the following [[inference rules]].

1. **[[type formation rule]]**:

   $$
     \frac{}{
       \mathclap{\phantom{\vert^{\vert}}}
       \mathbb{N} \,\colon\, Type
     }
   $$

2. **[[term introduction rules]]**:

   $$
     \frac{}{
       \mathclap{\phantom{\vert^{\vert}}}
       0 \,\colon\, \mathbb{N}
     }
     \;\;\;\;\;\;\;\;
     \frac{
       n \,\colon\, \mathbb{N}
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       succ(n) \,\colon\, \mathbb{N}
     }
   $$

3. **[[term elimination rule]]**:

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
         \;\vdash\; 
       P(n) \,\colon\, Type
       \;;
       \;\;\;\;
       \vdash\; 0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,,
       \; 
       p \,\colon\, P(x) 
         \;\vdash\; 
       succ_P(n,\,p) \,\colon\, P\big(succ(n)\big)
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       n \,\colon\, \mathbb{N}
       \;\vdash\;
       ind_{(P, 0_P, succ_P)}(n)
        \,\colon\, 
       P(n)
     }
   $$
   
4. **[[computation rules]]**:

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
        \;\vdash\;  
       P(n) \,\colon\, Type
       \;;
       \;\;\;\;
         \vdash\; 
       0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,, 
       \;
       p \,\colon\, P(x) 
         \;\vdash\; 
       succ_P(n,p) \,\colon\, P\big(succ(n)\big)
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       ind_{(P, 0_P, succ_P)}(0)
        \,=\, 
       0_P 
     }
   $$

   and

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
         \;\vdash\;  
       P(x) \,\colon\, Type
       \;;
       \;\;\;\;
       \vdash\; 0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,, 
       \;
       p \,\colon\, P(x) 
         \;\vdash\; 
       succ_P(x,p) \,\colon\, P(s x)
       \;;
       \;\;\;\;
       \vdash\; n \,\colon\, \mathbb{N}
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       ind_{(P, 0_P, succ_P)}\big(succ(n)\big)
       \,=\, 
       succ_P\big(n,\, ind_{(P, 0_P, succ_P)}(n) \big) 
     }
   $$

(In the last line, "$=$" denotes [[judgemental equality]].)

=--

That this is the right definition (and a special case of the general principle of [[inductive types]]) was clearly understood around [Martin-Löf (1984)](#Martin-Löf84), [pp. 38](/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=44); [Coquand & Paulin (1990, p. 52-53)](#CoquandPaulin90); [Paulin-Mohring (1993, §1.3)](#Paulin-Mohring93); [Dybjer (1994, §3)](#Dybjer94). For review see also, e.g., [Pfenning (2009, §2)](#Pfenning); [UFP (2013, §1.9)](#UFP13); [Söhnen (2018, §2.4.5)](#Söhnen18).

In [[Coq]]-[[syntax]] the [[natural numbers]] are the [[inductive type]] defined &lbrack;cf. [Paulin-Mohring (2014, p. 6)](#Paulin-Mohring14)&rbrack; by:

    Inductive nat : Type :=
     | zero : nat
     | succ : nat -> nat.


In the [[categorical semantics]] (via the [[categorical model of dependent types]], see [below](#CategoricalSemantics))
this is interpreted as the [[initial algebra for an endofunctor|initial algebra]] for the [[endofunctor]] $F$ that sends an object to its [[coproduct]] with the [[terminal object]] 

\[
  \label{TheEndofunctor}
  F(X) \;\coloneqq\; * \sqcup X
  \,,
\]

or in different equivalent notation, which is very suggestive here:

$$
  F(X) \;=\; 1 + X
  \,.
$$

That [[initial algebra for an endofunctor|initial algebra]] is (as also explained [there](#initial+algebra+of+an+endofunctor#NaturalNumbers)) precisely a [[natural number object]] $\mathbb{N}$. The two components of the morphism $F(\mathbb{N}) \to \mathbb{N}$ that defines the algebra structure are the 0-[[generalized element|element]] $0 \,\colon\, * \to \mathbb{N}$ and the [[successor]] [[endomorphism]] $succ \colon \mathbb{N} \to \mathbb{N}$

$$
  (0 ,\, succ) 
  \;\colon\; 
  * \sqcup \mathbb{N} 
  \longrightarrow 
  \mathbb{N}
  \,.
$$

### With typal computation and uniqueness rules

Assuming that [[identification types]], [[function types]] and [[dependent sequence types]] exist in the type theory, the natural numbers type is the [[inductive type]] generated by an element and a [[function]]:

Formation rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}}$$

Introduction rules for the natural numbers type:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash s:\mathbb{N} \to \mathbb{N}}$$

Elimination rules for the natural numbers type:
$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x)) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^C(c_0, c_s, n):C(n)}$$

Computation rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \beta_\mathbb{N}^0(c_0, c_s):\mathrm{Id}_{C(0)}\mathrm{ind}_\mathbb{N}^C(c_0, c_s, 0), c_0)}$$

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x)) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \beta_\mathbb{N}^s(c_0, c_s, n):\mathrm{Id}_{C(s(n))}(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, s(n)), c_s(n)(\mathrm{ind}_\mathbb{N}^C(c_0, c_s, n)))}$$

Uniqueness rules for the natural numbers type:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{x:\mathbb{N}} C(x) \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \eta_\mathbb{N}(c, n):\mathrm{Id}_{C(n)}(\mathrm{ind}_\mathbb{N}^C(c(0), \lambda x:\mathbb{N}.c(s(x)), n), c(n))}$$

The elimination, computation, and uniqueness rules for the natural numbers type state that the natural numbers type satisfy the **dependent universal property of the natural numbers**. If the dependent type theory also has [[dependent sum types]] and [[product types]], allowing one to define the [[uniqueness quantifier]], the dependent universal property of the natural numbers could be simplified to the following rule:

$$\frac{\Gamma, x:\mathbb{N} \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_0:C(0) \quad \Gamma \vdash c_s:\prod_{x:\mathbb{N}} C(x) \to C(s(x))}{\Gamma \vdash \mathrm{up}_\mathbb{N}^C(c_0, c_s):\exists!c:\prod_{x:\mathbb{N}} C(x).\mathrm{Id}_{C(0)}(c(0), c_0) \times \prod_{x:\mathbb{N}} \mathrm{Id}_{C(s(x))}(c(s(x)), c_s(c(x)))}$$

The dependent universal property of the natural numbers is used to characterize the [[dependent product type]] of an type family $C(x)$ dependent on $x:\mathbb{N}$, and states that the [[fibers]] of the function 
$$\lambda c.(c(0), \lambda x.c(s(x))):\prod_{x:\mathbb{N}} C(x) \to \left(C(0) \times \prod_{x:\mathbb{N}} C(x) \to C(s(x))\right)$$
are [[contractible types]]. This is equivalent to saying that the above function is an [[equivalence of types]]:

$$\mathrm{isEquiv}(\lambda c.(c(0), \lambda x.c(s(x))))$$

The non-dependent universal property similarly says that given a type $C$ the function 
$$\lambda c.(c(0), \lambda x.c(s(x))):(\mathbb{N} \to C) \to \left(C \times (\mathbb{N} \to C \to C)\right)$$
is an equivalence of types
$$\mathrm{isEquiv}(\lambda c.(c(0), \lambda x.c(s(x))))$$

### Generalized induction principle

There is also a generalized induction principle (cf. the talk slides in [LumsdaineShulman17](#LumsdaineShulman17)), which uses a type $C$ and a function $f:C \to \mathbb{N}$ instead of a type family $x:\mathbb{N} \vdash P(x)$, and one uses the [[fiber]] $\sum_{z:C} f(z) =_\mathbb{N} n$ to express the generalized induction principle.

Then the induction principle states that given a type $C$ and a function $f:C \to \mathbb{N}$ along with 

* dependent pair

$$c_0:\sum_{z:C} f(z) =_\mathbb{N} 0$$

* dependent function

$$c_s:\prod_{n:\mathbb{N}} \left(\sum_{z:C} f(z) =_\mathbb{N} n\right) \to \left(\sum_{z:C} f(z) =_\mathbb{N} s(n)\right)$$

* and natural number $n:\mathbb{N}$

one could construct the dependent pair

$$\mathrm{ind}_\mathbb{N}^C(f, c_0, c_s, n):\sum_{z:C} f(z) =_\mathbb{N} n$$

such that 

$$\mathrm{ind}_\mathbb{N}^C(f, c_0, c_s, 0) \equiv c_0$$

and for all $n:\mathbb{N}$

$$\mathrm{ind}_\mathbb{N}^C(f, c_0, c_s, s(n)) \equiv c_s(n, \mathrm{ind}(f, c_0, c_s, n))$$

However, by the rules of dependent pair types, one could instead postulate separate elements and identifications instead of an element of a [[fiber type]] throughout the generalized principle. 

Instead of the dependent pair $c_0:\sum_{z:C} f(z) =_\mathbb{N} 0$ we have the element $c_0:C$ and identificaiton $p_0:f(c_0) =_\mathbb{N} 0$, where the original element is given by $(c_0, p_0)$. In addition, given the dependent type 

$$c_s:\prod_{n:\mathbb{N}} \left(\sum_{z:C} f(z) =_\mathbb{N} n\right) \to \left(\sum_{z:C} f(z) =_\mathbb{N} s(n)\right)$$

by currying this is equivalent to

$$c_s:\prod_{n:\mathbb{N}} \prod_{z:C} \left(f(z) =_\mathbb{N} n\right) \to \left(\sum_{z:C} f(z) =_\mathbb{N} s(n)\right)$$

and by the [[type theoretic axiom of choice]] this is equivalent to

$$c_s:\prod_{n:\mathbb{N}} \prod_{y:C} \sum_{g:(f(y) =_\mathbb{N} n) \to C} \prod_{p:f(y) =_\mathbb{N} n} f(g(p)) =_\mathbb{N} s(n)$$

By the rules of dependent pair types, the family of dependent pair types could be split up into 

$$c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C$$

$$p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)$$

where the original dependent funciton is given by 

$$\lambda n:\mathbb{N}.\lambda y:C.(c_s(n, y), p_s(n, y))$$

Then the induction principle of the natural numbers states that given a type $C$ and a function $f:C \to \mathbb{N}$, along with 

* an element $c_0:C$

* an identification $p_0:f(c_0) =_\mathbb{N} 0$

* dependent functions

$$c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C$$

$$p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)$$

we have a function 

$$\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s):\mathbb{N} \to C$$

and a homotopy

$$\mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s):\prod_{n:\mathbb{N}} f(\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n)) =_\mathbb{N} n$$

indicating that $\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s)$ is a [[section]] of $f$, such that

$$\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, 0) \equiv c_0$$

$$\mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, 0) \equiv p_0$$

and for all $n:\mathbb{N}$, 

$$\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, s(n)) \equiv c_s(n, \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n), \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, n))$$

$$\mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, s(n)) \equiv p_s(n, \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n), \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, n))$$

As inference rules these are given by the following:

**elimination rules**:
$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s):\mathbb{N} \to C}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s):\prod_{n:\mathbb{N}} f(\mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n)) =_\mathbb{N} n}$$

**computation rules**:
$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, 0) \equiv c_0}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n)
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, 0) \equiv p_0}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n) \quad \Gamma \vdash n:\mathbb{N}
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, s(n)) \equiv c_s(n, \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n), \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, n))}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:C \to \mathbb{N} \quad \Gamma \vdash c_0:C \quad \Gamma \vdash p_0:f(c_0) =_\mathbb{N} 0 \\
\Gamma \vdash c_s:\prod_{n:\mathbb{N}} \prod_{y:C} (f(y) =_\mathbb{N} n) \to C \quad \Gamma \vdash p_s:\prod_{n:\mathbb{N}} \prod_{y:C} \prod_{p:f(y) =_\mathbb{N} n} f(c_s(n, y, p)) =_\mathbb{N} s(n) \quad \Gamma \vdash n:\mathbb{N}
\end{array}
}{\Gamma \vdash \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, s(n)) \equiv p_s(n, \mathrm{ind}_\mathbb{N}^{C}(f, c_0, p_0, c_s, p_s, n), \mathrm{ind}_\mathbb{N}^{C, \mathrm{sec}}(f, c_0, p_0, c_s, p_s, n))}$$

One gets back the usual induction principle of the natural numbers type when $C \equiv \sum_{n:\mathbb{N}} P(n)$ and $f \equiv \pi_1$ the first projection function of the dependent sum type, and one gets back the recursion principle of the natural numbers type when $C \equiv \mathbb{N} \times X$ and $f \equiv \pi_1$ the first projection function of the product type. 

### Extensionality principle of the natural numbers

First we [[inductive definition|inductively define]] a [[binary function]] into the [[type of booleans]] called [[observational equality]] of the natural numbers: 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Eq}_\mathbb{N}:\mathbb{N} \times \mathbb{N} \to \mathrm{Bit}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \delta^{0, 0}:\mathrm{Id}_\mathrm{Bit}(\mathrm{Eq}_\mathbb{N}(0, 0), 1)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \delta^{0, s}(n):\mathrm{Id}_\mathrm{Bit}(\mathrm{Eq}_\mathbb{N}(0, s(n)), 0)}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, m:\mathbb{N} \vdash \delta^{s, 0}(m):\mathrm{Id}_\mathrm{Bit}(\mathrm{Eq}_\mathbb{N}(s(m), 0), 0)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, m:\mathbb{N}, n:\mathbb{N} \vdash \delta^{s, s}(m, n):\mathrm{Id}_\mathrm{Bit}(\mathrm{Eq}_\mathbb{N}(s(m), s(n)),\mathrm{Eq}_\mathbb{N}(m, n))}$$

The extensionality principle of the natural numbers states that the natural numbers has [[decidable equality]] given by observational equality:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, m:\mathbb{N}, n:\mathbb{N} \vdash \delta(m, n):\mathrm{Id}_\mathbb{N}(m, n) \simeq \mathrm{El}_\mathrm{Bit}(\mathrm{Eq}_\mathbb{N}(m, n))}$$

or equivalently

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, m:\mathbb{N}, n:\mathbb{N} \vdash \delta(m, n):\mathrm{Id}_\mathbb{N}(m, n) \simeq \mathrm{Id}_\mathbb{2}(\mathrm{Eq}_\mathbb{N}(m, n), 1)}$$

### Large recursion principle

In [[dependent type theory]] presented using only a single [[type]] [[judgment]] $A \; \mathrm{type}$, the large recursion principle requires the need for [[dependent type theory with type variables|type variables in the dependent type theory]] (see [Category Theory Zulip](#CTZulip)). This is because the large recursion principle is given by the following: 

Given 

1. a type $T_0 \; \mathrm{type}$

1. a family of types $n:\mathbb{N}, X \; \mathrm{type} \vdash T_s(n, X) \; \mathrm{type}$

one can construct a family of types

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{T_0, T_s}(n) \; \mathrm{type}$$

such that 

$$\mathrm{rec}_\mathbb{N}^{T_0, T_s}(0) \equiv T_0 \; \mathrm{type}$$

and 

$$n:\mathbb{N} \vdash \mathrm{rec}_\mathbb{N}^{T_0, T_s}(s(n)) \equiv T_s(n, \mathrm{rec}_\mathbb{N}^{T_0, T_s}(n) \; \mathrm{type}$$

Without type variables, the second requirement in the large recursion principle that we have a family of types $n:\mathbb{N}, X \; \mathrm{type} \vdash T_s(n, X) \; \mathrm{type}$ will not be possible. 

## Properties

### General

\begin{example}\label{NaturalNumbersAsWType}
**([[natural numbers type]] as a [[W-type|$\mathcal{W}$-type]])**
\linebreak
The [[natural numbers type]] $(\mathbb{N},\, 0,\, succ)$ (Def. \ref{InferenceRules}) is equivalently the [[W-type|$\mathcal{W}$-type]] $\underset{c \colon C}{\mathcal{W}} A(c)$ with:

* $C \,\coloneqq\, \{0, succ\} \,\simeq\, \ast \sqcup \ast$;

* $A_0 \,\coloneqq\, \varnothing$ ([[empty type]]);

  $A_{succ} \,\coloneqq\, \ast$ ([[unit type]])

\end{example}
&lbrack;[Martin-Löf (1984)](#Martin-Löf84), [pp. 45](/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=51), [Dybjer (1997, p. 330, 333)](W-type#Dybjer97)&rbrack;

### Relation to the type of finite types

The natural numbers type is equivalent to the [[set truncation]] of the [[type of finite types]]:

$$\mathbb{N} \simeq [\mathrm{FinType}]_0$$ 

This is the type theoretic analogue of the [[decategorification]] of the [[permutation category]] resulting in the set of [[natural numbers]]. 

This gives us an alternate definition of the natural numbers as the type of finite types

$$\mathbb{N} \coloneqq [\mathrm{FinType}]_0$$ 

One has $[-]_0:\mathrm{FinType} \to [\mathrm{FinType}]_0$ by the introduction rules of set truncation.

The arithmetic operations and order relations on the natural numbers type can be defined by induction on [[set truncation]]:

For all finite types $A:\mathrm{FinType}$ and $B:\mathrm{FinType}$ and finite families $C:A \to \mathrm{FinType}$, we have

$$0 =_\mathbb{N} [\emptyset]_0 \quad 1 =_\mathbb{N} [\mathbb{1}]_0$$
$$[A]_0 + [B]_0 =_\mathbb{N} [A + B]_0$$
$$\sum_{x = 1}^{[A]_0} [C]_0(x) =_\mathbb{N} \left[\sum_{x:A} C(x)\right]_0$$
$$[A]_0 \cdot [B]_0 =_\mathbb{N} [A \times B]_0$$
$$\prod_{x = 1}^{[A]_0} [C]_0(x) =_\mathbb{N} \left[\prod_{x:A} C(x)\right]_0$$
$$[B]_0^{[A]_0} =_\mathbb{N} [A \to B]_0$$

$$[A]_0 =_\mathbb{N} [B]_0 \coloneqq [A \simeq B]_{(-1)} \; \mathrm{or} \; [A =_\mathrm{FinType} B]_{(-1)}$$
$$[A]_0 \leq [B]_0 \coloneqq [A \hookrightarrow B]_{(-1)}$$ 

### Categorical semantics
 {#CategoricalSemantics}

We spell out how under the canonical [[categorical model of dependent types]], the [[categorical semantics]] of the natural numbers types yields a [[natural numbers object]] together with its expected [[recursion]] and [[induction]] principle.

\linebreak

Throughout, we consider an ambient [[category]] $\mathcal{C}$ (e.g. $\mathcal{C} =$ [[Set]]) and write

\[
  \label{CategoryOfFAlgebras}
  F Alg(\mathcal{C}) \xrightarrow{underlying} \mathcal{C}
\]

for the category of [[algebra over an endofunctor|algebras over the endofunctor]] $F$ (eq:TheEndofunctor).


#### Recursion
 {#Recursion}


We spell out how the fact that $\mathbb{N}$ satisfies Def. \ref{InferenceRules} is the classical [[recursion principle]]. 


\linebreak

We begin with a simple special case of recursion (cf. Rem. \ref{NeedForDependentRecursion}), where not only the underlying type but also its successor-map is independent of $\mathbb{N}$ (we come to the general form of recursion further [below](#RecursionGenerally)).

So consider any $F$-algebra $\big(D, (0_D, succ_D)\big) \,\in\, F Alg(\mathcal{C})$ (eq:CategoryOfFAlgebras), hence an [[object]] $D \in \mathcal{C}$ equipped with a morphism

$$
  0_D \colon * \to D
$$

and a morphism

$$
  succ_D \colon D \to D
  \,.
$$

By [[initial object|initiality]] of the $F$-algebra $\mathbb{N}$, there is then a (unique) morphism

$$
  rec \,\colon\, \mathbb{N} \to D
$$

such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    * 
    &\stackrel{0}{\longrightarrow}& 
    \mathbb{N} 
    &\stackrel{succ}{\longrightarrow}& 
    \mathbb{N}
    \\
    \big\downarrow 
    && 
    \big\downarrow\mathrlap{^\mathrlap{rec}} 
    && 
    \big\downarrow\mathrlap{^\mathrlap{rec}}
    \\
    * 
    &\underset{0_D}{\longrightarrow}& 
    D
    &\underset{succ_D}{\longrightarrow}& 
    D
  }
$$

This means precisely that $rec$ is the function [[recursive definition|defined recursively]] by

\[
  rec(0) \;=\; 0_D
\]
and
\[
  \label{FormulaForNonDependentRecursion}
  rec\big(succ(n)\big) 
   \;=\; 
  succ_D\big(rec(n)\big)
  \,.
\]


{#RecursionGenerally} More generally, consider an $F$-algebra in the [[slice category|slice]] over $\big(\mathbb{N}, (0,succ)\big)$, but with the [[underlying]] slice object assumed (dropping also this assumption leads to the fully general notion of induction further [below](#Induction)) to be independent of $\mathbb{N}$, hence of the form

\[
  \label{AssumingUnderlyingScliceObjectToBeIndependent}
  \left[
  \array{
    \mathbb{N} \times D
    \\
    \big\downarrow\mathrlap{^{pr_{\mathbb{N}}}}
    \\
    \mathbb{N}
  }
  \;\;\;
  \right]
  \;\in\;
  \mathcal{C}_{/\mathbb{N}}
  \,,
\]

while the $F$-algebra structure may now depend on $\mathbb{N}$:

\begin{tikzcd}[
  column sep=56pt, 
  row sep=30pt
]
    \ast \,\sqcup\, (\mathbb{N} \times D)
    \ar[
      rr,
      "{
        \big(
          (0, \mathrm{succ} \,\circ\, pr_{\mathbb{N}})
          ,\, 
          (0_D, \mathrm{succ}_D)
        \big)      
      }"
    ]
    \ar[d, "{ \ast \,\sqcup\, \mathrm{pr}_{\mathbb{N}} }"]
    &&
    \mathbb{N} \times D
    \ar[d, "{ \mathrm{pr}_{\mathbb{N}} }"]
    \\
    \ast \,\sqcup\, \mathbb{N}
    \ar[rr, "{(0, \mathrm{succ})}"{swap}]
    &&
    \mathbb{N}
\end{tikzcd}

in that 

$$
  succ_D \;\colon\; \mathbb{N} \times D \to D
$$

may depend on $\mathbb{N}$.

Now, since with $\big(\mathbb{N},(0,\mathrm{succ})\big)$ being the [[initial object]] in $F Alg(\mathcal{C})$, the [[identity morphism]] on $\big(\mathbb{N},(0,\mathrm{succ})\big)$ is the [[initial object]] in the [[slice category]] $F Alg(\mathcal{C})_{/\big(\mathbb{N}, (0,succ)\big)}$ (cf. [there](over+category#InitialAndTerminalObjects)), it follows that from such data is induced a unique morphism $f$ in the following [[commuting diagram]]:

\begin{tikzcd}[
    column sep=34pt,
    row sep=25pt
  ]
    &[+34pt]
    &
    \ast \,\sqcup\, \mathbb{N}
    \ar[
      ddll,
      "{
        (0,\mathrm{succ})
      }"{sloped}
    ]
    \ar[
      dr, 
      equals,
      shorten >=-2pt
     ]
    \ar[
      r,
      dashed,
      shorten=-1pt,
      "{
        \mathrm{id}_\ast
        \,\sqcup\,
        (\mathrm{id}_{\mathbb{N}},\, \mathrm{rec})
      }"
    ]
    &[+16pt]
    \ast \,\sqcup\, (\mathbb{N} \times D)
    \ar[
      d,
      "{
        \mathrm{id}_\ast 
          \,\sqcup\, 
        \mathrm{pr}_{\mathbb{N}}
      }"
    ]
    \\
    &
    &&
    \ast \,\sqcup\, \mathbb{N}
    \ar[
      ddll,
      "{
        (0, \mathrm{succ})
      }"{description, sloped}
    ]
    \\[+10pt]
    \mathbb{N}
    \ar[dr, equals]
    \ar[
      r,
      dashed,
      "{
        (\mathrm{Id}_{\mathbb{N}},\, \mathrm{rec})
      }"{description}
    ]
    &
    \mathbb{N} \times D
    \ar[d]
    \ar[
      from=uurr,
      crossing over,
      "{
        \big(
          (
            0,
            \,
            \mathrm{succ} 
              \,\circ\, 
             \mathrm{pr}_{\mathbb{N}})
          ,\,
          (0_D,\, \mathrm{succ}_D)
        \big)
      }"{description, sloped, pos=.6}
    ]
    \\
    &
    \mathbb{N}
\end{tikzcd}

Here the [[commuting diagram|commutativity]] of the top square means equivalently that

\[
  \mathrm{rec}(0) \,=\, 0_D
\]
and
\[
\label{FormulaForDependentRecursion}
  \mathrm{rec}\big(
    \mathrm{succ}(n)
  \big)
  \;=\;
  \mathrm{succ}_D\big(n,\, \mathrm{rec}(n)\big)
  \,.
\]

\begin{remark}\label{NeedForDependentRecursion}
(**the need for dependent recursion** &lbrack;[cf. Paulin-Mohring (1993, p. 330)](#Paulin-Mohring93)&rbrack;)
\linebreak
  The appearance of the argument "$n$" on the right of (eq:FormulaForDependentRecursion) -- in contrast to formula (eq:FormulaForNonDependentRecursion) for non-dependent recursion -- means (in view of the argument "$succ(n)$" on the left) that the recursor $succ_D$ has access to the *[[predecessor]]* [[partial function]] $pred \,\colon\,succ(n) \,\mapsto\, n$. This is necessary in order to express all computable functions on the natural numbers inductively and hence explains the need for the [[dependent type|dependently typed]] recursion principle (eq:AssumingUnderlyingScliceObjectToBeIndependent) 
\end{remark}


#### Induction
 {#Induction}

Dropping the above constraint (eq:AssumingUnderlyingScliceObjectToBeIndependent) on the dependent $F$-algebra, we spell out in detail how the fact that $\mathbb{N}$ satisfied Def. \ref{InferenceRules} is the classical [[induction principle]]. 

That principle says informally that if a [[proposition]] $P$ depending on the natural numbers is true at $n = 0$ and such that if it is true for some $n$ then it is true for $n+1$, then it is true for all natural numbers.
 
Here is how this is formalized in type theory and then [[categorical semantics|interpreted]] in some suitable ambient category $\mathcal{C}$.

First of all, that $P$ is a proposition depending on the natural numbers means that it is a [[dependent type]]

$$
  n \,\colon\, \mathbb{N} 
  \;\;\vdash\;\; 
  P(n) \,\colon\, Type
  \,.
$$ 

The categorical interpretation of this is by a [[display map]]

\[
  \label{DisplayMapInterpretingNDependentType}
  \array{
     P 
     \\
     \big\downarrow\mathrlap{^{\pi_P}}
     \\
     \mathbb{N}
  }
\]

in the given category $\mathcal{C}$.


{#DiagramInterpretingInductionPrinciple} With this, the [[commuting diagram]] which interprets the induction principle is the following:

\begin{tikzcd}[
    column sep=30pt,
    row sep=25pt
  ]
    &[+34pt]
    &
    \ast \,\sqcup\, \mathbb{N}
    \ar[
      ddll,
      "{
        (0,\mathrm{succ})
      }"{sloped}
    ]
    \ar[
      dr, 
      equals,
      shorten >=-2pt
     ]
    \ar[
      r,
      dashed,
      shorten=-1pt,
      "{
        \mathrm{id}_\ast
        \,\sqcup\,
        \mathrm{ind}
      }"
    ]
    &[+16pt]
    \ast \,\sqcup\, P
    \ar[
      d,
      "{
        \mathrm{id}_\ast 
          \,\sqcup\, 
        \pi_P
      }"
    ]
    \\
    &
    &&
    \ast \,\sqcup\, \mathbb{N}
    \ar[
      ddll,
      "{
        (0, \mathrm{succ})
      }"{description, sloped}
    ]
    \\[+10pt]
    \mathbb{N}
    \ar[dr, equals]
    \ar[
      r,
      dashed,
      "{
        \mathrm{ind}
      }"{description}
    ]
    &
    P
    \ar[
      d,
      "{ \pi_P }"
    ]
    \ar[
      from=uurr,
      crossing over,
      "{
        (0_P,\, \mathrm{succ}_P)
      }"{description, sloped, pos=.6}
    ]
    \\
    &
    \mathbb{N}
\end{tikzcd}

We now unwind again how this comes about and what it all means:

First, the fact that $P$ holds at 0 means that there is a ([[proof]]-)[[term]]

$$
  \vdash \;\; 0_P \,\colon\, P(0)
  \,.
$$

In the [[categorical semantics]] the [[substitution]] of $n$ for 0 that gives $P(0)$ is given by the [[pullback]] of the given display map (eq:DisplayMapInterpretingNDependentType):

$$
  \array{
    0^* P &\longrightarrow& P
    \\
    \big\downarrow && \big\downarrow
    \\
    * &\underset{0}{\longrightarrow}& \mathbb{N}
  }
$$

and the [[term]] $0_P$ is interpreted as a [[section]] of the resulting fibration over the terminal object

$$
  \array{
    * 
    &\overset{p_0}{\longrightarrow}& 
    0^* P 
    & \longrightarrow & 
    P
    \\
    &\searrow& \big\downarrow && \big\downarrow
    \\
    && 
    * 
    &\underset{0}{\longrightarrow}& \mathbb{N}
  }
  \,.
$$

But by the defining [[universal property]] of the [[pullback]], this is equivalently just a [[commuting diagram]]

$$
  \array{
    * &\stackrel{p_0}{\longrightarrow}& P
    \\
    \big\downarrow && \big\downarrow
    \\
    * &\underset{0}{\longrightarrow}& \mathbb{N}
  }
  \,.
$$

Next the induction step. Formally it says that for all $n \in \mathbb{N}$ there is an [[implication]] $succ_P(n) \,\colon\, P(n) \to P(n+1)$

$$
  n \in \mathbb{N} 
  \;\;\;\vdash\;\;\; 
  succ_P(n) \,\colon\, P(n) \to   P(n+1)
  \,.
$$

The [[categorical semantics]] of the [[substitution]] of $n+1$ for $n$ is given by the [[pullback]]

$$
  \array{
     P\big(\ast \sqcup (-)\big) \coloneqq 
     & s^*P &\longrightarrow& P
     \\
     & \big\downarrow && \big\downarrow 
     \\
     & \mathbb{N} &\underset{s}{\longrightarrow}& \mathbb{N}
  }
$$

and the interpretation of the implication term $succ_P(n)$ is as a [[morphism]] $P \to s^* P$ in $\mathcal{C}_{/\mathbb{N}}$

$$
  \array{
     P 
     & \overset{p_s}{\longrightarrow} &  
     s^*P &\longrightarrow& P
     \\
     &\searrow & \big\downarrow && \big\downarrow 
     \\
     && \mathbb{N} &\overset{s}{\longrightarrow}& \mathbb{N}
  }
  \,.
$$

Again by the [[universal property]] of the pullback this is equivalently a [[commuting diagram]]

$$
  \array{
     P &\overset{succ_P}{\longrightarrow}& P
     \\
     \big\downarrow && \big\downarrow 
     \\
     \mathbb{N} 
     &\underset{s}{\longrightarrow}& 
     \mathbb{N}
  }
  \,.
$$

In summary this shows that 

* $P$ being a proposition depending on natural numbers which holds at 0 and which holds at $n+1$ if it holds at $n$ 

is interpreted precisely as an [[algebra for an endofunctor|endofunctor-algebra homomorphism]] 

$$
  \array{
     P
     \\
     \downarrow
     \\
     \mathbb{N}
  }
  \,.
$$

for the [[endofunctor]] $F$ (eq:TheEndofunctor).


The [[induction principle]] is supposed to deduce from this that $P$ holds for every $n$, hence that there is a proof $ind(n) \colon P(n)$ for all $n$:

$$
  n \,\colon\, \mathbb{N} 
  \;\;\;\vdash\;\;\; 
  ind(n) \,\colon\, P(n)
  \,.
$$

The categorical interpretation of this is as a morphism $p \,\colon\, \mathbb{N} \to P$ in $\mathcal{C}_{/\mathbb{N}}$. The existence of this is indeed exactly what the interpretation of the elimination rule (Def. \ref{InferenceRules}) gives exactly what the initiality of the $F$-algebra $\mathbb{N}$ gives.


## Related concepts

* [[natural numbers]], [[natural numbers object]]

* [[decimal numeral representation of the natural numbers]]

* [[dependent sequence type]]

* [[type of finite types]]

* [[dependent type theory with type variables]]

## References

Original articles with emphasis on the nature of $\mathbb{N}$ as an [[inductive type]]:

* {#Martin-Löf84} [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), [pp. 38](/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=44) of: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

* {#CoquandPaulin90} [[Thierry Coquand]], [[Christine Paulin]], p. 52-53 in:  *Inductively defined types*, COLOG-88 Lecture Notes in Computer Science **417**, Springer (1990) 50-66 &lbrack;[doi:10.1007/3-540-52335-9_47](https://doi.org/10.1007/3-540-52335-9_47)&rbrack;

* {#Paulin-Mohring93} [[Christine Paulin-Mohring]], §1.3 in: *Inductive definitions in the system Coq -- Rules and Properties*, in: *Typed Lambda Calculi and Applications* TLCA 1993, Lecture Notes in Computer Science **664** Springer (1993) &lbrack;[doi:10.1007/BFb0037116](https://doi.org/10.1007/BFb0037116)&rbrack;

* {#Dybjer94} [[Peter Dybjer]], §3 in: *Inductive families*, Formal Aspects of Computing **6** (1994) 440–465 $[$[doi:10.1007/BF01211308](https://doi.org/10.1007/BF01211308), [doi:10.1007/BF01211308](https://doi.org/10.1007/BF01211308), [pdf](http://www.cse.chalmers.se/~peterd/papers/Inductive_Families.pdf)$]$

The syntax in [[Coq]]:

* {#Paulin-Mohring14} [[Christine Paulin-Mohring]], p. 6 in: *Introduction to the Calculus of Inductive Constructions*, contribution to: *Vienna Summer of Logic* (2014) &lbrack;[hal:01094195](https://hal.inria.fr/hal-01094195), [pdf](https://hal.inria.fr/hal-01094195/document), [pdf slides](https://easychair.org/smart-program/VSL2014/APPA-invited-slides-6.pdf)&rbrack;


See also:

* {#Pfenning} [[Frank Pfenning]], _Lecture notes on natural numbers_ (2009) &lbrack;[pdf](http://www.cs.cmu.edu/~fp/courses/15317-f09/lectures/06-nat.pdf), [[Pfenning-NaturalNumbersType.pdf:file]]&rbrack;


  
Discussion in a context of [[homotopy type theory]] and in view of [[higher inductive types]]:

* {#UFP13} [[Univalent Foundations Project]], §1.9 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Egbert Rijke]], §3 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#Söhnen18} Kajetan Söhnen, §2.4.5 in: *Higher Inductive Types in Homotopy Type Theory*, Munich (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Soehnen.pdf), [[Soehnen-HigherInductiveTypes.pdf:file]]&rbrack;

* {#LumsdaineShulman17} [[Peter LeFanu Lumsdaine]], [[Mike Shulman]], *Semantics of higher inductive types*, Math. Proc. Camb. Phil. Soc. **169** (2020) 159-208 &lbrack;[arXiv:1705.07088](https://arxiv.org/abs/1705.07088), talk slides [pdf](http://home.sandiego.edu/~shulman/papers/cellcxs.pdf), [doi:10.1017/S030500411900015X](https://doi.org/10.1017/S030500411900015X)&rbrack;

Equivalence to binary presentations:

* [[Nicolas Magaud]], [[Yves Bertot]], *Changing Data Structures in Type Theory: A Study of Natural Numbers*, in *Types for Proofs and Programs. TYPES 2000*, Lecture Notes in Computer Science **2277** &lbrack;[doi:10.1007/3-540-45842-5_12](https://doi.org/10.1007/3-540-45842-5_12), [pdf](https://dpt-info.u-strasbg.fr/~magaud/papers/types2000-nmagaud.pdf)&rbrack;

* [[Nicolas Magaud]], *Changing Data Representation within the Coq*, in *Theorem Proving in Higher Order Logics. TPHOLs 2003*, Lecture Notes in Computer Science **2758** &lbrack;[doi:10.1007/10930755_6](https://doi.org/10.1007/10930755_6)&rbrack;

Some discussion about the large recursion principle of the natural numbers type in [[dependent type theory with type variables]] occurs in:

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

That one can construct the [[natural numbers type]] from the integers type can be found in:

* [[Christian Sattler]], *Natural numbers from integers* ([pdf](https://www.cse.chalmers.se/~sattler/docs/naturals.pdf))

[[!redirects natural number type]]
[[!redirects natural-number type]]
[[!redirects natural numbers type]]
[[!redirects natural-numbers type]]
[[!redirects type of natural numbers]]

[[!redirects universal property of the natural numbers type]]
[[!redirects dependent universal property of the natural numbers type]]

[[!redirects universal property of the natural numbers]]
[[!redirects dependent universal property of the natural numbers]]
