
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

+-- {: .num_defn #InterpretationOfTheRules}
###### Definition

The [[type of natural numbers]] $\mathbb{N}$ is the [[inductive type]] defined as follows.

1. **[[type formation rule]]**

   $$
     \frac{}{\mathbb{N} : Type}
   $$

2. **[[term introduction rules]]**

   $$
     \frac{}{0 : \mathbb{N}}
   $$
   and
   $$
     \frac{n : \mathbb{N}}{s n : \mathbb{N}}
   $$

3. **[[term elimination rule]]**

   $$
     \frac{
       x : \mathbb{N} \vdash P(x) : Type;
       \;\;
       \vdash p_0 : P(0);
       \;\;
       x : \mathbb{N}, p : P(x) \vdash p_s(x,p) : P(s x);
       \;\;
       \vdash n : \mathbb{N}
     }{
       rec^n_P(p_0,p_s) : P(n)
     }
   $$
   
4. **[[computation rules]]**

   $$
     \frac{
       x : \mathbb{N} \vdash  P(x) : Type;
       \;\;
       \vdash p_0 : P(0);
       \;\;
       x : \mathbb{N}, p : P(x) \vdash p_s(x,p) : P(s x)
     }{
       rec^0_P(p_0,p_s) = p_0 : P(0)
     }
   $$
   and
   $$
     \frac{
       x : \mathbb{N} \vdash  P(x) : Type;
       \;\;
       \vdash p_0 : P(0);
       \;\;
       x : \mathbb{N}, p : P(x) \vdash p_s(x,p) : P(s x);
       \;\;
       \vdash n : \mathbb{N}
     }{
       rec^{s n}_P(p_0,p_s) = p_s(n,rec^n_P(p_0,p_s)) : P(s n)
     }
   $$
=--

See for instance ([Pfenning, section 2](#Pfenning)).

In [[Coq]]-[[syntax]] the [[natural numbers]] are the inductive type defined by

    Inductive nat : Type :=
     | zero : nat
     | succ : nat -> nat.

In the [[categorical semantics]]
this is interpreted as the [[initial algebra for an endofunctor|initial algebra]] for the endofunctor $F$ that sends an object to its [[coproduct]] with the [[terminal object]] 

$$
  F(X) = * \coprod X
  \,,
$$

or in different equivalent notation, which is very suggestive here:

$$
  F(X) = 1 + X
  \,.
$$

That [[initial algebra for an endofunctor|initial algebra]] is (as explained there) precisely a [[natural number object]] $\mathbb{N}$. The two components of the morphism $F(\mathbb{N}) \to \mathbb{N}$ that defines the algebra structure are the 0-[[generalized element|element]] $zero : * \to \mathbb{N}$ and the successor [[endomorphism]] $successor : \mathbb{N} \to \mathbb{N}$

$$
  (zero,successor) : * \coprod \mathbb{N} \to \mathbb{N}
  \,.
$$

In the following we write of course for short $0 : * \to \mathbb{N}$ and $s : \mathbb{N} \to \mathbb{N}$.


## Properties

### Induction

+-- {: .num_example}
###### Example

We spell out in detail how the fact that $\mathbb{N}$ satisfied def. \ref{InterpretationOfTheRules} is the classical [[induction principle]]. 

That principle says informally that if a [[proposition]] $P$ depending on the natural numbers is true at $n = 0$ and such that if it is true for some $n$ then it is true for $n+1$, then it is true for all natural numbers.
 
Here is how this is formalized in type theory and then [[categorical semantics|interpreted]] in some suitable ambient category $\mathcal{C}$.

First of all, that $P$ is a proposition depending on the natural numbers means that it is a [[dependent type]]

$$
  n \in \mathbb{N} \vdash P(n) : Type
  \,.
$$ 

The categorical interpretation of this is by a [[display map]]

$$
  \array{
     P 
     \\
     \downarrow
     \\
     \mathbb{N}
  }
$$

in the given category $\mathcal{C}$.

Next, the fact that $P$ holds at 0 means that there is a ([[proof]]-)[[term]]

$$
  \vdash p_0 \in P(0)
  \,.
$$

In the categorical semantics the [[substitution]] of $n$ for 0 that gives $P(0)$ is given by the [[pullback]] of the above fibration

$$
  \array{
    0^* P &\to& P
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{0}{\to}& \mathbb{N}
  }
$$

and the [[term]] $p_0$ is interpreted as a [[section]] of the resulting fibration over the terminal object

$$
  \array{
    * &\stackrel{p_0}{\to}& 0^* P &\to& P
    \\
    &\searrow& \downarrow && \downarrow
    \\
    && * &\stackrel{0}{\to}& \mathbb{N}
  }
  \,.
$$

But by the defining [[universal property]] of the pullback, this is equivalently just a [[commuting diagram]]

$$
  \array{
    * &\stackrel{p_0}{\to}& P
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{0}{\to}& \mathbb{N}
  }
  \,.
$$

Next the induction step. Formally it says that for all $n \in \mathbb{N}$ there is an [[implication]] $p_s(n) : P(n) \to P(n+1)$

$$
  n \in \mathbb{N} \vdash p_s(n)  : P(n) \to   P(n+1)
$$

The categorical semantics of the [[substitution]] of $n+1$ for $n$ is now given by the [[pullback]]

$$
  \array{
     P((-)+1) \coloneqq & s^*P &\to& P
     \\
     & \downarrow && \downarrow 
     \\
     & \mathbb{N} &\stackrel{s}{\to}& \mathbb{N}
  }
$$

and the interpretation of the implication term $p_s(n)$ is as a morphism $P \to s^* P$ in $\mathcal{C}_{/\mathbb{N}}$

$$
  \array{
     P & \stackrel{p_s}{\to} &  s^*P &\to& P
     \\
     &\searrow & \downarrow && \downarrow 
     \\
     && \mathbb{N} &\stackrel{s}{\to}& \mathbb{N}
  }
  \,.
$$

Again by the [[universal property]] of the pullback this is the same as a [[commuting diagram]]

$$
  \array{
     P &\stackrel{p_s}{\to}& P
     \\
     \downarrow && \downarrow 
     \\
     \mathbb{N} &\stackrel{s}{\to}& \mathbb{N}
  }
  \,.
$$

In summary this shows that the fact that $P$ is a proposition depending on natural numbers which holds at 0 and which holds at $n+1$ if it holds at $n$ is interpreted precisely as an $F$-[[algebra for an endofunctor|algebra homomorphism]]

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

The [[induction principle]] is supposed to deduce from this that $P$ holds for every $n$, hence that there is a proof $p_n : P(n)$ for all $n$:

$$
  n \in \mathbb{N} \vdash p(n) : P(n)
  \,.
$$

The categorical interpretation of this is as a morphism $p : \mathbb{N} \to P$ in $\mathcal{C}_{/\mathbb{N}}$. The existence of this is indeed exactly what the interpretation of the elimination rule, def. \ref{InterpretationOfTheRules}, gives, or (equivalently by prop. \ref{BothFormulationsOfInitialityAreEquivalent}) exactly what the initiality of the $F$-algebra $\mathbb{N}$ gives.
=--


### Recursion

+-- {: .num_example}
###### Example

We spell out how the fact that $\mathbb{N}$ satisfies def. \ref{InterpretationOfTheSimpleRules} is the classical [[recursion principle]]. 


So let $A$ be an $F$-algebra object, hence equipped with a morphism

$$
  a_0 : * \to A
$$

and a morphism

$$
  h : A \to A
  \,.
$$

By [[initial object|initiality]] of the $F$-algebra $\mathbb{N}$, there is then a (unique) morphism

$$
  f : \mathbb{N} \to A
$$

such that the diagram 

$$
  \array{
    * &\stackrel{0}{\to}& \mathbb{N} &\stackrel{(-)+1}{\to}& \mathbb{N}
    \\
    \downarrow && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f}}
    \\
    * &\stackrel{a_0}{\to}& A &\stackrel{h}{\to}& A
  }
$$

commutes. This means precisely that $f$ is the function defined recursively by

1. $f(0) = a_0$;

1. $f(n+1) = h(f(n))$.

=--


## Related concepts

* [[natural numbers]], [[natural numbers object]]
* [[decimal representation of the natural numbers]]

## References

* Frank Pfenning, _Lecture notes on natural numbers_ (2009) ([pdf](http://www.cs.cmu.edu/~fp/courses/15317-f09/lectures/06-nat.pdf))
  {#Pfenning}


[[!redirects natural number type]]
[[!redirects natural-number type]]
[[!redirects natural numbers type]]
[[!redirects natural-numbers type]]
[[!redirects type of natural numbers]]
