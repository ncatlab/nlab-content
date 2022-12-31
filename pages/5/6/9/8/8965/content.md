
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

See for instance [Pfenning (2009, §2)](#Pfenning), [Söhnen (2018, §2.4.5)](#Söhnen18).

In [[Coq]]-[[syntax]] the [[natural numbers]] are the inductive type defined by

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

That [[initial algebra for an endofunctor|initial algebra]] is (as also explained [there](#initial+algebra+of+an+endofunctor#NaturalNumbers)) precisely a [[natural number object]] $\mathbb{N}$. The two components of the morphism $F(\mathbb{N}) \to \mathbb{N}$ that defines the algebra structure are the 0-[[generalized element|element]] $0 \colo * \to \mathbb{N}$ and the [[successor]] [[endomorphism]] $succ \colon \mathbb{N} \to \mathbb{N}$

$$
  (0 ,\, succ) 
  \;\colon\; 
  * \sqcup \mathbb{N} 
  \longrightarrow 
  \mathbb{N}
  \,.
$$


## Properties

### Categorical semantics
 {#CategoricalSemantics}

We spell out how under the canonical [[categorical model of dependent types]], the [[categorical semantics]] of the natural numbers types yields a [[natural numbers object]] together with its expected [[recursion]] and [[induction]] principle.

\linebreak

Throughout, we consider an ambient [[category]] $\mathcal{C}$ (e.g. $\mathcal{C} =$ [[Set]]) and write

$$
  F Alg(\mathcal{C}) \xrightarrow{underlying} \mathcal{C}
$$

for the category of [[algebra over an endofunctor|algebras over the endofunctor]] $F$ (eq:TheEndofunctor).


#### Recursion
 {#Recursion}


We spell out how the fact that $\mathbb{N}$ satisfies Def. \ref{InterpretationOfTheSimpleRules} is the classical [[recursion principle]]. 


\linebreak

Consider then any $F$-algebra $\big(D, (0_D, succ_D)\big) \,\in\, F Alg(\mathcal{C})$, hence an [[object]] $D \in \mathcal{C}$ equipped with a morphism

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
  f \colon \mathbb{N} \to D
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
    \big\downarrow\mathrlap{^\mathrlap{f}} 
    && 
    \big\downarrow\mathrlap{^\mathrlap{f}}
    \\
    * 
    &\underset{0_D}{\longrightarrow}& 
    D
    &\underset{succ_D}{\longrightarrow}& 
    D
  }
$$

This means precisely that $f$ is the function defined recursively by

1. $f(0) \;=\; 0_D$;

1. $f\big(succ(n)\big) \;=\; succ_D\big(f(n)\big)$.


{#RecursionGenerally} More generally, consider an $F$-algebra in the [[slice category|slice]] over $\big(\mathbb{N}, (0,succ)\big)$, but with the [[underlying]] slice object assumed to be independent of $\mathbb{N}$, hence of the form

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
        (\mathrm{id}_{\mathbb{N}},\, f)
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
        (\mathrm{Id}_{\mathbb{N}},\, f)
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

$$
  f(0) \,=\, 0_D
  \;\;\;\;\text{and}\;\;\;\;\;
  f\big(
    \mathrm{succ}(n)
  \big)
  \;=\;
  \mathrm{succ}_D\big(n,\, f(n)\big)
  \,.
$$


#### Induction
 {#Induction}

Dropping the above constraint (eq:AssumingUnderlyingScliceObjectToBeIndependent) on the dependent $F$-algebra, we spell out in detail how the fact that $\mathbb{N}$ satisfied def. \ref{InterpretationOfTheRules} is the classical [[induction principle]]. 

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
  \vdash \;\; p_0 \,\colon\, P(0)
  \,.
$$

In the [[categorical semantics]] the [[substitution]] of $n$ for 0 that gives $P(0)$ is given by the [[pullback]] of the above fibration

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
  n \in \mathbb{N} 
  \;\;\;\vdash\;\;\; 
  p_s(n) \,\colon\, P(n) \to   P(n+1)
  \,.
$$

The [[categorical semantics]] of the [[substitution]] of $n+1$ for $n$ is given by the [[pullback]]

$$
  \array{
     P\big((-)+1\big) \coloneqq & s^*P &\to& P
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


The [[induction principle]] is supposed to deduce from this that $P$ holds for every $n$, hence that there is a proof $p_n : P(n)$ for all $n$:

$$
  n \,\colon\, \mathbb{N} 
  \;\;\;\vdash\;\;\; 
  p(n) \,\colon\, P(n)
  \,.
$$

The categorical interpretation of this is as a morphism $p : \mathbb{N} \to P$ in $\mathcal{C}_{/\mathbb{N}}$. The existence of this is indeed exactly what the interpretation of the elimination rule, def. \ref{InterpretationOfTheRules}, gives, or (equivalently by prop. \ref{BothFormulationsOfInitialityAreEquivalent}) exactly what the initiality of the $F$-algebra $\mathbb{N}$ gives.


## Related concepts

* [[natural numbers]], [[natural numbers object]]

* [[decimal numeral representation of the natural numbers]]


## References

* {#Pfenning} [[Frank Pfenning]], _Lecture notes on natural numbers_ (2009) &lbrack;[pdf](http://www.cs.cmu.edu/~fp/courses/15317-f09/lectures/06-nat.pdf), [[Pfenning-NaturalNumbersType.pdf:file]]&rbrack;
  
Discussion in a context of [[homotopy type theory]] and in view of [[higher inductive types]]:

* [[Univalent Foundations Project]], §1.9 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


* {#Söhnen18} Kajetan Söhnen, §2.4.5 in: *Higher Inductive Types in Homotopy Type Theory*, Munich (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Soehnen.pdf), [[Soehnen-HigherInductiveTypes.pdf:file]]&rbrack;




[[!redirects natural number type]]
[[!redirects natural-number type]]
[[!redirects natural numbers type]]
[[!redirects natural-numbers type]]
[[!redirects type of natural numbers]]
