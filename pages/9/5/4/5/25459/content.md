
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[type theory]], the *binomial types* or *binomial sets* are the [[categorification]] of the [[binomial coefficients]] and then the further generalization from [[family of finite types|finite types]]/[[finite sets]] to arbitrary [[types]] or [[sets]]. 

## Definition

Given [[types]] $A$ and $B$, the **binomial type** of $A$ and $B$ is defined as

$$
  \left(
    \begin{array}{c}
    A 
    \\ 
    B
   \end{array}
\right) 
  \;\coloneqq\;
  \sum_{
   f \colon 
   A \to \mathbb{2}
   } 
  \left[
    B \simeq 
    \left(
    \sum_{a \colon A} 
      f(a) 
      =_\mathbb{2} 
      1
    \right)
  \right]
  \,,
$$

where 

* $\sum_{(-)} (-)$ denotes the [[dependent pair type]]-formation;

* $(-)\to(-)$ denotes [[function type]]-formation;

* $\mathbb{2}$ denotes the finite type with two elements "$0$" and "$1$";

* $(-) =_\mathbb{2} (-)$ denotes its [[identification type]]; 

* $[-]$ denotes [[propositional truncation]] ([[bracket types]]).

Since $A \simeq B$ is defined as the [[dependent pair type]] $\sum_{f:A \to B} \mathrm{isEquiv}(f)$, the above definition is the same as 

$$
  \left(
    \begin{array}{c}
    A 
    \\ 
    B
   \end{array}
\right) 
  \;\coloneqq\;
  \sum_{
   f \colon 
   A \to \mathbb{2}
   } 
  \exists g:B \to \left(
    \sum_{a \colon A} 
      f(a) 
      =_\mathbb{2} 
      1
    \right).\mathrm{isEquiv}(g)
  \,,
$$

where given a type family $x:A \vdash B(x)$ the [[existential quantifier]] is defined as the propositional truncation of the dependent pair type

$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$

This definition can be translated directly into [[set theory]] notation as follows: 

$$
  \left(
    \begin{array}{c}
    A 
    \\ 
    B
   \end{array}
\right) 
  \;\coloneqq\;
  \{f \in \mathbb{2}^A \vert \exists g \in \{a \in A \vert f(a) =_\mathbb{2} 1\}^B.\mathrm{isBijection}(g)\}
  \,,
$$

where $B^A$ is the [[function set]] with [[domain]] $A$ and [[codomain]] $B$ and $\mathbb{2}$ is the [[type of booleans]], and the predicate $\mathrm{isBijection}(f)$ on the function set $f \in B^A$ is defined as 
$$\mathrm{isBijection}(f) \coloneqq \forall y \in B.\exists!x \in A.f(x) = y$$

This results in **binomial sets**. 

### Locally small binomial types

There is an alternative way to express the second definition, by use of a [[univalent universe]], but the resulting type is only locally small relative to the universe. 

We define the type of decidable embeddings as the type of functions whose fibers are decidable:
$$A \hookrightarrow_d B \coloneqq \sum_{f:A \to B} \prod_{b:B} \left(\sum_{a:A} f(a) =_B b\right) \vee \neg \left(\sum_{a:A} f(a) =_B b\right)$$ 

Let $(U, \mathrm{El})$ be a [[univalent Tarski universe]], and given type $A$, let us define $U_A$ to be the type of all types in $U$ which are merely equivalent to $A$:
$$U_A \coloneqq \sum_{X:U} \left[A \simeq \mathrm{El}(X)\right]$$
Then given [[essentially small type|essentially $U$-small types]] $A$ and $B$, the locally $U$-small binomial type is defined as 
$$\left(\begin{array}{c}A \\ B\end{array}\right)_U \coloneqq \sum_{X:U_B} \left[\mathrm{El}(X) \hookrightarrow_d A\right]$$

One could also translate the above definition into [[set theory]]: 

Given a [[universe]] $U$ of [[small sets]], the set $U_A$ is defined to be the set of all small sets in $U$ which are in bijection with $A$:

$$U_A \coloneqq \{X \in U \vert \exists i \in X^A.\forall x \in X.\exists!a \in A.a \in i^*(x)\}$$

where $i^*(x)$ is the [[preimage]] or [[fiber]] of $i$ at $x$. 

Then given small sets $A$ and $B$, the locally $U$-small **binomial set** of $A$ and $B$ is defined as the set of all $X \in U_B$ such that there exists a [[decidable injection]] from $X$ to $A$:

$$\left(\begin{array}{c}A \\ B\end{array}\right)_U \coloneqq \{X \in U_B \vert \exists i \in A^X.\forall x \in X.(\exists!a \in A.a \in i^*(x)) \vee (\neg \exists a \in A.a \in i^*(x))\}$$

## See also

* [[binomial theorem]]

* [[categorification]]

## References

The above definitions of binomial types can be found, respectively, in remark 17.6.7 and definition 17.6.7 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&lbrack;

[[!redirects binomial type]]
[[!redirects binomial types]]

[[!redirects binomial set]]
[[!redirects binomial sets]]