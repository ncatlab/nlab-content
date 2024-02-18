
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition 

\begin{definition}
\label{MonoidalMonad}
\linebreak
A **monoidal monad** is a [[monad]] in the [[2-category]] of [[monoidal category|monoidal categories]], [[lax monoidal functor|lax monoidal functors]], and [[monoidal natural transformation|monoidal transformations]]. 
\end{definition}

This notion originates inside the statement of [Kock 1970, Thm. 3.2](#Kock70).


{#InComponents} In components, this means (cf. [Kock 1970, p. 8](#Kock70), review includes [Seal 2012, §1.2](#Seal12)):

Monoidal [[structure]] on a [[monad]]

$
  \mathcal{E} 
  \,\colon\,
  \mathbf{C} \to \mathbf{C}
$

$
  c  \in \mathbf{C}
  \;\;\;\;
   \vdash
  \;\;\;\;
  ret^{\mathcal{E}}_c
  \,\colon\,
  c \to \mathcal{E}(c)
$

$
  c  \in \mathbf{C}
  \;\;\;\;
   \vdash
  \;\;\;\;
  join^{\mathcal{E}}_{c}
  \,\colon\,
  \mathcal{E} \circ \mathcal{E}(c)
  \to 
  \mathcal{E}(c)
$

acting on a [[monoidal category]] $(\mathbf{C}, \otimes, \mathbb{1})$ is:

1. [[lax monoidal functor]]-[[structure]] on $\mathcal{E}$

   $
     c \in \mathbf{C}
     \;\;\;\;
     \vdash
     \;\;\;\;
     \epsilon^{\mathcal{E}}_c
     \,\colon\,
     c \to \mathcal{E}(c)
   $

   $
     c,c' \in \mathbf{C}
     \;\;\;\;
       \vdash
     \;\;\;\;
     \mu^{\mathcal{E}}_{c,c'}
     \,\colon\,
     \mathcal{E}(c) \otimes \mathcal{E}(c')
     \to
     \mathcal{E}(c \otimes c')
   $

1. such that the monad structure transformations $ret^{\mathcal{E}}$ and $join^{\mathcal{E}}$ are [[monoidal transformations]] in that together with the lax monoidal structure transformation $\epsilon^{\mathcal{E}}$ and $\mu^{\mathcal{E}}$ they make the following [[commuting diagram|diagrams commute]]:

First of all, the [[lax monoidal functor|lax monoidal unit]] must coincide with the [[unit of a monad|monad unit]]

\[\label{LaxUnitIsMonadUnit}\]

\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
  & 
  1\!\!1
  \ar[dl, equals]
  \ar[
    dr, 
    "{ 
      \epsilon^{\mathcal{E}}_{1\!\!1} 
    }"
  ]
  \\
  1\!\!1
  \ar[
    rr,
    "{
      \mathrm{ret}^{\mathcal{E}}_{1\!\!1}
    }"{swap}
  ]
  &&
  \mathcal{E}(1\!\!1)
\end{tikzcd}

which already implies the unit diagram for the join operation:

\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
  & 
  1\!\!1
  \ar[
    dl,
    "{
       \epsilon^{\mathcal{E}}_{\mathcal{E}(1\!\!1)}
       \circ
       \epsilon^{\mathcal{E}}_{1\!\!1}
    }"{description}
  ]
  \ar[
    dr,
    "{
      \epsilon^{\mathcal{E}}_{1\!\!1}
    }"
  ]
  \\
  \mathcal{E}\circ\mathcal{E}(1\!\!1)
  \ar[
    rr,
    "{
      \mathrm{join}^{\mathcal{E}}_{1\!\!1}
    }"{swap}
  ]
  &&
  \mathcal{E}(1\!\!1)
\end{tikzcd}

and then the two main conditions:

\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
  c \otimes c'
  \ar[dd, equals]
  \ar[
    rr,
    "{
      \big(\mathrm{ret}^{\mathcal{E}}_c\big)
      \otimes
      \big(\mathrm{ret}^{\mathcal{E}}_{c'}\big)
    }"
  ]
  &&
  \mathcal{E}(c) \otimes \mathcal{E}(c')
  \ar[
    dd,
    "{
      \mu^{\mathcal{E}}_{c,c'}
    }"
  ]
  \\
  \\
  c \otimes c'
  \ar[
    rr,
    "{
      \mathrm{ret}^{\mathcal{E}}_{c \otimes c'}
    }"
  ]
  &&
  \mathcal{E}(c \otimes c')
\end{tikzcd}

and

\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
  \big(\mathcal{E}\circ\mathcal{E}(c)\big)
  \otimes
  \big(\mathcal{E}\circ\mathcal{E}(c')\big)
  \ar[
    d,
    "{
      \mu^{\mathcal{E}}_{\mathcal{E}(c), \mathcal{E}(c')}
    }"
  ]
  \ar[
    rr,
    "{
      \big(
        \mathrm{join}^{\mathcal{E}}_c
      \big)
      \otimes
      \big(
        \mathrm{join}^{\mathcal{E}}_{c'}
      \big)
    }"
  ]
  &&
  \big(\mathcal{E}(c)\big) 
   \otimes
  \big(
    \mathcal{E}(c')
  \big)
  \ar[
    dd,
    "{
      \mu^{\mathcal{E}}_{c,c'}
    }"
  ]
  \\
  \mathcal{E}
  \Big(
  \big(\mathcal{E}(c)\big)
  \otimes
  \big(\mathcal{E}(c')\big)
  \Big)
  \ar[
    d,
    "{
      \mathcal{E}\big(
        \mu^{\mathcal{E}}_{c,c'}
      \big)
    }"
  ]
  \\
  \mathcal{E} \circ \mathcal{E}(c \otimes c')
  \ar[
    rr,
    "{
      \mathrm{join}^{\mathcal{E}}_{c \otimes c'}
    }"{swap}
  ]
  &&
  \mathcal{E}(c \otimes c')
\end{tikzcd}

Moreover, if $\mathbf{C}$ is even a [[symmetric monoidal category]] with [[braiding]] $\sigma$, then a monoidal monad on $\mathbf{C}$ as above is a *symmetric monoidal monad* if the [[underlying]] [[monoidal functor]] is a *[[symmetric monoidal functor]]*.


+-- {: .num_remark}
###### Remark

The notion of monoidal monad is equivalent to the notion of _[[commutative monad]]_. To put it another way: to give a commutative [[strong monad|strength]] for a monad $T$ is to give a monoidal monad whose [[underlying]] monad is $T$. We explore this connection below. 

=--

## Properties

### Relation to commutative strong monads
 {#RelationToCommutativeStrongMonads}

We discuss how monoidal monads [[functor|functorially]] give rise to [[strong monads]].

#### Strength

First to recall the notion of a [[strong monad]]:

Let $V$ be a [[monoidal category]]. We say a [[functor]] $T \colon V \to V$ is **strong** if there are given left and right [[tensorial strength|tensorial strengths]], namely [[natural transformations]] of the form: 


$$
  \tau_{A, B} 
  \;\colon\; 
  A \otimes T(B) 
  \to 
  T(A \otimes B)
$$

$$\,$$ 

$$
  \sigma_{A, B} 
  \;\colon\; 
  T(A) \otimes B 
  \to 
  T(A \otimes B)
  \,,
$$ 

which are suitably compatible with one another: The full set of [[coherence]] conditions may be summarized by saying $T$ preserves the two-sided [[action of a monoidal category|monoidal action]] of $V$ on itself, in an appropriate [[2-category theory|2-categorical]] sense. More precisely: the two-sided action of $V$ on itself is a [[lax functor]] of [[2-categories]]  

$$
  \tilde{V} 
  \colon 
  B V \times (B V)^{op} 
  \to 
  Cat
$$ 

where

* [[Cat]] denotes the 2-category of [[categories]], [[functors]] and [[natural transformations]],

* $B V$ denotes the [[delooping]] one-object 2-category of the monoidal category $V$,

* $(B V)^{op}$ denotes its [[opposite 2-category|1-cell dual]], hence the same 2-category except with [[1-morphism]] [[composition]] (here: [[tensor product]]) in reverse order),

* the two-sided strength means we have a [[structure]] of [[lax natural transformation]] $\tilde{V} \to \tilde{V}$. 


+-- {: .num_remark}
###### Remark

In the setting where $V$ is _[[symmetric monoidal category|symmetric]]_ monoidal, we will assume that the left and right strengths $\tau$ and $\sigma$ are related by the symmetry in the obvious way, by a [[commutative square]] 

$$
  \array{
    A \otimes T(B) 
    & 
    \stackrel
      {\tau_{A, B}}
      {\longrightarrow} 
    & 
    T(A \otimes B) 
    \\
    \mathllap{^c} 
    \big\downarrow 
    & & 
    \big\downarrow
    \mathrlap{^{T(c)}} 
    \\
    T(B) \otimes A 
    & 
    \underset{
      \sigma_{B, A}}
      {\longrightarrow} 
    & T(B \otimes A)
}$$ 

where the $c$'s are instances of the symmetry isomorphism. 

=--



\begin{definition}
\label{StrongMonad}
There is a [[category]] of [[strong functors]] $V \to V$, whose [[morphisms]] are [[natural transformations]] $\lambda \colon S \to T$ which are compatible with the strengths in the obvious sense. Under [[composition]], this is a strict [[monoidal category]]. 

The [[monoid objects]] in this monoidal category are called **[[strong monads]]**. 
\end{definition}



\begin{definition}
\label{CommutativeMonad}
A [[strong monad]] $(T \colon V \to V, m \colon T T \to T, u: 1 \to T)$ (def. \ref{StrongMonad}) is a **[[commutative monad]]** if there is an [[equality]] of [[natural transformations]] $\alpha = \beta$ where 

* $\alpha$ is the composite 

  $$T A \otimes T B \stackrel{\sigma_{A, T B}}{\to} T(A \otimes T B) \stackrel{T(\tau_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B).$$ 

* $\beta$ is the composite 

  $$T A \otimes T B \stackrel{\tau_{T A, B}}{\to} T(T A \otimes B) \stackrel{T(\sigma_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B).$$ 

\end{definition}


#### From monoidal to commutative strong monads 


\begin{definition}
\label{StrengthFromMonoidalness}
**(strength from monoidalness)**
\linebreak
For $(T \colon V \to V, u \colon id \to T, m \colon T T \to T)$  a monoidal monad (Def. \ref{MonoidalMonad}), with the monoidal monad-[[structure]] on the [[underlying]] [[functor]] denoted by 

$$
  \alpha_{A, B} 
  \,\colon\, 
  T(A) \otimes T(B) 
  \to 
  T(A \otimes B), 
  \qquad 
  \iota = u(I) 
  \,:\, I \to T(I)  
  \,,
$$ 

Define [[tensorial strength|strengths]] on both the left and the right by: 

$$
  \tau_{A, B} 
  \;\coloneqq\; 
  \big(
    A \otimes T(B) 
      \overset{u_A \otimes id}{\to} 
    T(A) \otimes T(B) 
      \overset{\alpha_{A, B}}{\to} 
    T(A \otimes B)
  \big)
  \,,
$$ 

$$\,$$ 

$$
  \sigma_{A, B} 
  \;\coloneqq\; 
  \big(
    T(A) \otimes B 
      \overset{id \otimes u_B}{\to} 
    T(A) \otimes T(B) 
      \overset{\alpha_{A, B}}{\to} 
    T(A \otimes B)
  \big)
  \,.
$$ 
\end{definition}

+-- {: .num_prop}
###### Proposition 
The strong monad structures obtained from monoidal monads via Def. \ref{StrengthFromMonoidalness} are [[commutative monads]] (Def. \ref{CommutativeMonad}). 
=-- 

+-- {: .proof} 
###### Proof 
In fact, the two composites 

$$T A \otimes T B \stackrel{\sigma_{A, T B}}{\to} T(A \otimes T B) \stackrel{T(\tau_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B)$$ 

$$\,$$ 

$$T A \otimes T B \stackrel{\tau_{T A, B}}{\to} T(T A \otimes B) \stackrel{T(\sigma_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B)$$

are both equal to $\alpha_{A, B}$. We show this for the second composite; the proof is similar for the first. If $\alpha_T$ denotes the monoidal constraint for $T$ and $\alpha_{T T}$ the constraint for the composite $T T$, then by definition $\alpha_{T T}$ is the composite given by  
$$T T X \otimes T T Y \stackrel{\alpha_T T}{\to} T(T X \otimes T Y) \stackrel{T\alpha_T}{\to} T T(X \otimes Y)$$ 
and so, using the properties of monoidal monads, we have a commutative diagram 

$$\array{
 & & T T X \otimes T Y & \stackrel{\alpha_T}{\to} & T(T X \otimes Y) \\
 & ^\mathllap{u \otimes 1} \nearrow & \downarrow^\mathrlap{1 \otimes T u} & & \downarrow^\mathrlap{T(1 \otimes u)} \\
T X \otimes T Y & \stackrel{u \otimes T u}{\to} & T T X \otimes T T Y & \stackrel{\alpha_T T}{\to} & T(T X \otimes T Y) \\
 & ^\mathllap{1} \searrow & \downarrow^\mathrlap{m \otimes m} & \searrow^\mathrlap{\alpha_{T T}} & \downarrow^\mathrlap{T\alpha_T} \\
 & & T X \otimes T Y & & T T(X \otimes Y) \\
& & & ^\mathllap{\alpha_T} \searrow & \downarrow^\mathrlap{m} \\
 & & & & T(X \otimes Y)
}$$ 

which completes the proof. 
=-- 


This construction is [[functorial]]:

\begin{proposition}
\label{cf}
Given monoidal monads $S$ and $T$ on a [[monoidal category]] $C$, a [[monad#the_bicategory_of_monads|morphism of monads]] $\alpha \colon S\Rightarrow T$ is a [[morphism]] of the induced [[strong monad]] structures (Def. \ref{StrengthFromMonoidalness}) if and only if it is a [[monoidal natural transformation]].
\end{proposition}

(e.g. [FPR (2019), Prop. C.5](#support))

This relation has a converse:

\begin{proposition}
\label{BijectSymmMonoidalMonadsWithCommStrongMonads}
\linebreak
For a [[monad]] $T$ on (the [[underlying]] [[category]] of) a [[symmetric monoidal category|symmetric]] [[closed monoidal category]], there is a [[bijection]] between the [[structure]] on $T$ of:

1. a [[commutative monad|commutative]] [[strong monad]]

1. a [[symmetric monoidal functor|symmetric]] [[monoidal monad]].

\end{proposition}

This is due to [Kock (1972)](#Kock72), Thm. 2.3), a detailed review is in  [GLLN08, §7.3, §A.4](#GLLN08).



### Tensor product of algebras and multimorphisms

See [[commutative monad#tensor_product_of_algebras_and_multimorphisms|here]].


### Monoidal structure on the Kleisli category

The [[Kleisli category]] of a monoidal monad $T$ on $C$ inherits the [[monoidal structure]] from $C$.
In particular, the [[tensor product]] is given

* On objects, by the tensor product $\otimes$ of $C$;
* On morphisms, given $k:X\to TA$ and $h:Y\to TB$, their product is the map $X\otimes Y \to T(A\otimes B)$ obtained by the composition
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
X\otimes Y \ar{r}{f\otimes g} & TA \otimes TB \ar{r}{\nabla} & T(A\otimes B),
\end{tikzcd}
where $\nabla$ is the monoidal multiplication of $T$.

* The associator and unitor are induced by those of $C$.


## Examples

See [[commutative monad#examples|examples of commutative monads]].


## See also

* [[strong monad]], [[tensorial strength]]
* [[monoidal functor]]
* [[commutative monad]], [[commutative algebraic theory]]


## References
 {#References}

The definition originally appears inside statement and proof of Thm. 3.2 in:

* {#Kock70} [[Anders Kock]], *Monads on symmetric monoidal closed categories*, Arch. Math. **21** (1970) 1-10 &lbrack;[doi:10.1007/BF01220868](https://doi.org/10.1007/BF01220868)&rbrack;

establishing right away the relation to [[commutative monads|commutative]] [[strong monads]] (in the case that the underlying [[monoidal category]] is [[symmetric monoidal closed category|symmetric monoidal closed]]) which is further expanded on in:

* {#Kock71} [[Anders Kock]], *Closed categories generated by commutative monads*, Journal of the Australian Mathematical Society **12** 4 (1971) 405-424  &lbrack;[doi:10.1017/S1446788700010272](https://doi.org/10.1017/S1446788700010272), [[KockMonoidalMonads.pdf:file]]&rbrack;

* {#Kock72} [[Anders Kock]], *Strong functors and monoidal monads*, Arch. Math **23** (1972) 113–120 &lbrack;[doi:10.1007/BF01304852](https://doi.org/10.1007/BF01304852), [pdf](http://home.imf.au.dk/kock/SFMM.pdf)&rbrack;

Further discussion:
 
* {#Lindner75} H. Lindner, _Commutative monads_ in: *Deuxi&#233;me colloque sur l'alg&#233;bre des cat&#233;gories* Amiens-1975. R&#233;sum&#233;s des conf&#233;rences, pages 283-288. Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 16, nr. 3 (1975) &lbrack;[numdam:CTGDC_1975__16_3_217_0](http://www.numdam.org/item/CTGDC_1975__16_3_217_0), [pdf](http://www.numdam.org/article/CTGDC_1975__16_3_217_0.pdf)&rbrack;

* {#Keigher78} [[William Keigher]], *Symmetric monoidal closed categories generated by commutative adjoint monads*, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978) 269-293  &lbrack;[numdam:CTGDC_1978__19_3_269_0](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf)&rbrack;

* Kosta Dosen, Zoran Petric, *Coherence for Monoidal Monads and Comonads*, Mathematical Structures in Computer Science , **20** 4 (2010) 545-561  &lbrack;[arXiv:0907.2199](https://arxiv.org/abs/0907.2199), [doi:10.1017/S0960129510000034](https://doi.org/10.1017/S0960129510000034)&rbrack;


* {#Seal12} [[Gavin J. Seal]], *Tensors, monads and actions*, Theory and Applications of Categories **28** 15 (2013) 403-434.  &lbrack;[arXiv:1205.0101](http://arxiv.org/abs/1205.0101), [tac:28-15](http://www.tac.mta.ca/tac/volumes/28/15/28-15abs.html)&rbrack;

  > (on the [[Eilenberg-Moore categories]] of monoidal monads)

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

Discussion in the context of [[monads in computer science]]:

* {#GLLN08} [[Jean Goubault-Larrecq]], [[Slawomir Lasota]], [[David Nowak]], *Logical Relations for Monadic Types*, Mathematical Structures in Computer Science, **18** 6 (2008) 1169-1217 &lbrack;[arXiv:cs/0511006](https://arxiv.org/abs/cs/0511006), [doi:10.1017/S0960129508007172](https://doi.org/10.1017/S0960129508007172)&rbrack;


A statement in the above text is from 

* {#support} [[Tobias Fritz]], [[Paolo Perrone]] and Sharwin Rezagholi, Appendix C of: _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019 ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))


[[!redirects monoidal monads]]

