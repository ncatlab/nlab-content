
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

_Exact couples_ are a way to encode data that makes a [[spectral sequence]], specially adapted to the case that the underlying filtering along which the spectral sequence proceeds is induced from a tower of [[homotopy fibers]], such as a [[Postnikov tower]] or [[Adams tower]] (see also at _[[Adams spectral sequence]]_).
 
## Definition

### Exact couples

+-- {: .num_defn}
###### Definition


Given an [[abelian category]] $\mathcal{C}$, an **[[exact couple]]** in $\mathcal{C}$ is a cyclic [[long exact sequence]] of three [[morphisms]] among two [[objects]] of the form

$$ 
  \cdots \stackrel{k}{\longrightarrow} E \overset{j}{\to} D \overset{\varphi}{\longrightarrow} D \overset{k}{\to} E \overset{j}{\longrightarrow} \cdots 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This being cyclic, it is usually depicted as a triangle

$$
  \array{
    D && \stackrel{\varphi}{\longrightarrow} && D
    \\
    & {}_{\mathllap{j}}\nwarrow && \swarrow_{\mathrlap{k}}
    \\
    && 
    E
  }
$$

=--

The archetypical example from which this and the following definition draw their meaning is example \ref{ExactCoupleOfATower} below.


### Spectral sequences from exact couples
 {#SpectralSequencesFromExactCouples}

+-- {: .num_defn #CohomologySpectralSequence}
###### Definition

A _cohomology [[spectral sequence]]_ $\{E_r^{p,q}, d_r\}$ is

1. a sequence $\{E_r^{\bullet,\bullet}\}$ $r \in \mathbb{Z}$, $r \geq 2$ of [[bigraded object|bigraded]] [[abelian groups]];

1. a sequence of [[differentials]] $\{d_r \colon E_r^{\bullet,\bullet} \longrightarrow E_r^{\bullet+r, \bullet-r+1}\}$

such that 

* $H_{r+1}^{\bullet,\bullet}$ is the [[cochain cohomology]] of $d_r$:, i.e. $E_{r+1}^{\bullet, \bullet} = H(E_r^{\bullet,\bullet},d_r)$.

Given a $\mathbb{Z}$-[[graded abelian group]]_ $C^\bullet$ equipped with a decreasing [[filtration]]

$$
  C^\bullet \supset \cdots \supset F^s C^\bullet \supset F^{s+1} C^\bullet \supset \cdots \supset 0$$

such that

$$
  C^\bullet = \underset{s}{\cup} F^s C^\bullet \;\;\;\; and \;\;\;\; 0 = \underset{s}{\cap} F^s C^\bullet
$$

then the spectral sequence is said to _converge_ to  $C^\bullet$, denoted, 

$$
  E_2^{\bullet,\bullet} \Rightarrow C^\bullet
$$

if

1.  in each bidegree $(s,t)$ the sequence $\{E_r^{s,t}\}_r$ eventually becomes constant on a group 

    $E_\infty^{s,t} \coloneqq E_{\gg 1}^{s,t}$;

1. $E_\infty^{\bullet,\bullet}$ is the [[associated graded]] of the filtered $C^\bullet$ in that

   $E_\infty^{s,t} \simeq F^s C^{s+t} / F^{s+1}C^{s+t}$.


The converging spectral sequence is called _multiplicative_ if 

1. $\{E_2^{\bullet,\bullet}\}$ is equipped with the structure of a [[bigraded object]] [[associative algebra|algebra]];

1. $F^\bullet C^\bullet$ is equipped with the structure of a filtered [[graded algebra]] ($F^p C^k \cdot F^q C^l \subset F^{p+q} C^{k+l}$);

such that

1. each $d_{r}$ is a [[derivation]] with respect to the (induced) algebra structure on ${E_r^{\bullet,\bullet}}$, graded of degree 1 with respect to total degree;

1. the multiplication on $E_\infty^{\bullet,\bullet}$ is compatible with that on $C^\bullet$.

=--

+-- {: .num_defn #ExactCoupleAndDerivedExactCouple}
###### Definition
**(derived exact couples)**

An _[[exact couple]]_ is three [[homomorphisms]] of [[abelian groups]] of the form

$$
  \array{
    D && \stackrel{g}{\longrightarrow} && D
    \\
    & {}_{\mathllap{f}}\nwarrow && \swarrow_{\mathrlap{h}}
    \\
    && E
  }
$$

such that the [[image]] of one is the [[kernel]] of the next.

$$
  im(h) = ker(f)\,,\;\;\; im(f) = ker(g)\,, \;\;\; im(g) = ker(h)
  \,.
$$

Given an exact couple, then its _derived exact couple_ is

$$
  \array{
    im(g) && \stackrel{g}{\longrightarrow} && im(g)
    \\
    & {}_{\mathllap{f}}\nwarrow && \swarrow_{\mathrlap{h \circ g^{-1}}}
    \\
    && H(E, h \circ f)
  }
  \,.
$$

=--

Here and in the following we write $g^{-1}$ etc. for the operation of choosing a [[preimage]] under a given function $g$. In each case it is left implicit that the given expression is independent of which choice is made.

+-- {: .num_prop #CohomologicalSpectralSequenceOfAnExactCouple}
###### Proposition
**(cohomological spectral sequence of an exact couple)**

Given an exact couple, def. \ref{ExactCoupleAndDerivedExactCouple}, 

$$
  \array{
    D_1 && \stackrel{g_1}{\longrightarrow} && D_1
    \\
    & {}_{\mathllap{f_1}}\nwarrow && \swarrow_{\mathrlap{h_1}}
    \\
    && E_1
  }
$$

its derived exact couple 

$$
  \array{
    D_2 && \stackrel{g_2}{\longrightarrow} && D_2
    \\
    & {}_{\mathllap{f_2}}\nwarrow && \swarrow_{\mathrlap{h_2}}
    \\
    && E_2
  }
$$

is itself an exact couple. Accordingly there is induced a sequence of exact couples 

$$
  \array{
    D_r && \stackrel{g_r}{\longrightarrow} && D_r
    \\
    & {}_{\mathllap{f_r}}\nwarrow && \swarrow_{\mathrlap{h_r}}
    \\
    && E_r
  }
  \,.
$$

If the abelian groups $D$ and $E$ are equipped with [[bigraded object|bigrading]] such that

$$
  deg(f) = (0,0)\,,\;\;\;\; deg(g) = (-1,1)\,,\;\;\; deg(h) = (1,0)
$$

then $\{E_r^{\bullet,\bullet}, d_r\}$ with

$$
  \begin{aligned}
    d_r & \coloneqq h_r \circ f_r
     \\
     & = h \circ g^{-r+1} \circ f
  \end{aligned}
$$

is a cohomological spectral sequence, def. \ref{CohomologySpectralSequence}. 

(As before in prop. \ref{CohomologicalSpectralSequenceOfAnExactCouple}, the notation $g^{-n}$ with $n \in \mathbb{N}$ denotes the function given by choosing, on representatives, a [[preimage]] under $g^n = \underset{n\;times}{\underbrace{g \circ \cdots \circ g \circ g}}$, with the implicit claim that all possible choices represent the same equivalence class.)

If for every bidegree $(s,t)$ there exists $R_{s,t} \gg 1$ such that for all $r \geq R_{s,t}$ 

1. $g \colon D^{s+R,t-R} \stackrel {\simeq}{\longrightarrow} D^{s+R -1, t-R-1}$;

1. $g\colon D^{s-R+1, t+R-2} \stackrel{0}{\longrightarrow} D^{s-R,t+R-1}$ 

then this spectral sequence converges to the [[inverse limit]] group

$$
  G^\bullet \coloneqq \underset{}{\lim}
  \left(
    \cdots \stackrel{g}{\to} D^{s,\bullet-s} \stackrel{g}{\longrightarrow} D^{s-1, \bullet - s + 1}
   \stackrel{g}{\to}
   \cdots
  \right)
$$

filtered by 

$$
  F^p G^\bullet \coloneqq ker(G^\bullet \to D^{p-1, \bullet - p+1})
  \,.
$$

=--

(e.g. [Kochmann 96, lemma 2.6.2](#Kochmann96))

+-- {: .proof}
###### Proof

We check the claimed form of the $E_\infty$-page:

Since $ker(h) = im(g)$ in the exact couple, the kernel

$$
  ker(d_{r-1}) \coloneqq ker(h \circ g^{-r+2} \circ f)
$$

consists of those elements $x$ such that $g^{-r+2} (f(x)) = g(y)$, for some $y$, hence 

$$
  ker(d_{r-1})^{s,t} \simeq f^{-1}(g^{r-1}(D^{s+r-1,t-r+1}))
  \,.
$$

By assumption there is for each $(s,t)$ an $R_{s,t}$ such that for all $r \geq R_{s,t}$ then $ker(d_{r-1})^{s,t}$ is independent of $r$. 

Moreover, $im(d_{r-1})$ consists of the image under $h$ of those $x \in D^{s-1,t}$ such that $g^{r-2}(x)$ is in the image of $f$, hence (since $im(f) = ker(g)$ by exactness of the exact couple) such that $g^{r-2}(x)$ is in the kernel of $g$, hence such that $x$ is in the kernel of $g^{r-1}$. If $r \gt R$ then by assumption $g^{r-1}|_{D^{s-1,t}} = 0$ and so then $im(d_{r-1}) = im(h)$.

(Beware this subtlety: while $g^{R_{s,t}}|_{D^{s-1,t}}$ vanishes by the convergence assumption, the expression $g^{R_{s,t}}|_{D^{s+r-1,t-r+1}}$ need not vanish yet. Only the higher power $g^{R_{s,t}+ R_{s+1,t+2}+2}|_{D^{s+r-1,t-r+1}}$ is again guaranteed to vanish. ) 

{#InfinityPage} It follows that

$$
  \begin{aligned}
    E_\infty^{p,n-p}
    & =
    ker(d_R)/im(d_R)
    \\
    &
    \simeq
    f^{-1}(im(g^{R-1}))/im(h)
    \\
    &
    \simeq
    f^{-1}(im(g^{R-1}))/ker(f)
    \\
    &
    \underoverset{\simeq}{f}{\longrightarrow}
    im(g^{R-1}) \cap im(f)
    \\
    & 
    \simeq
    im(g^{R-1}) \cap ker(g)
  \end{aligned}
$$

where in last two steps we used once more the exactness of the exact couple.

{#InfinityPageIsSubgroupOfImageOfFirstPageUnderf}(Notice that the above equation means in particular that the $E_\infty$-page is a sub-group of the image of the $E_1$-page under $f$.)

The last group above is that of elements $x \in G^n$ which map to zero in $D^{p-1,n-p+1}$ and where two such are identified if they agree in $D^{p,n-p}$, hence indeed 

$$
  E_\infty^{p,n-p} \simeq F^p G^n / F^{p+1} G^n
  \,.
$$


=--

## Examples

### Exact couple of a tower of (co)-fibrations
 {#ExactCoupleOfATowerOfFibrations}

...[[spectral sequence of a tower of fibrations]]...

+-- {: .num_defn #FilteredSpectrum}
###### Definition

A [[filtered spectrum]] is a [[spectrum]] $X$ equipped with a sequence $X_\bullet \colon (\mathbb{N}, \gt) \longrightarrow Spectra$  of spectra of the form

$$
  \cdots 
   \longrightarrow
  X_3
    \stackrel{f_2}{\longrightarrow} 
  X_2 
    \stackrel{f_1}{\longrightarrow} 
  X_1 \stackrel{f_0}{\longrightarrow} X_0 = X 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

More generally a [[filtered object in an (infinity,1)-category|filtering]] on an object $X$ in (stable or not) [[homotopy theory]] is a $\mathbb{Z}$-graded sequence $X_\bullet $ such that $X$ is the [[homotopy colimit]]  $X\simeq \underset{\longrightarrow}{\lim} X_\bullet$. But for the present purpose we stick with the simpler special case of def. \ref{FilteredSpectrum}.

=--


+-- {: .num_remark}
###### Remark

There is _no_ condition on the [[morphisms]] in def. \ref{FilteredSpectrum}. In particular, they are _not_ required to be [[n-monomorphisms]] or [[n-epimorphisms]] for any $n$. 

On the other hand, while they are also not explicitly required to have a presentation by [[cofibrations]] or [[fibrations]], this follows automatically: by the existence of [[model structures for spectra]], every filtering on a spectrum is equivalent to one in which all morphisms are represented by [[cofibrations]] or by [[fibrations]]. 

This means that we may think of a filtration on a spectrum $X$ in the sense of def. \ref{FilteredSpectrum} as equivalently being a [[tower of fibrations]] over $X$.

=--

The following remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} unravels the structure encoded in a filtration on a spectrum, and motivates the concepts of [[exact couples]] and their [[spectral sequences]] from these.


+-- {: .num_remark #UnrolledExactCoupleOfAFiltrationOnASpectrum}
###### Remark

Given a [[filtered spectrum]] as in def. \ref{FilteredSpectrum},
write $A_k$ for the [[homotopy cofiber]] of its $k$th stage, such as to obtain the diagram

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   X_3 
     &\stackrel{f_2}{\longrightarrow}& 
   X_2 
     &\stackrel{f_2}{\longrightarrow} & 
   X_1 
     &\stackrel{f_1}{\longrightarrow}& 
   X
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

where each stage

$$
 \array{
   X_{k+1} &\stackrel{f_k}{\longrightarrow}& X_k   
   \\
   && \downarrow^{\mathrlap{cofib(f_k)}}
   \\
   && A_k
 }
$$

is a [[homotopy fiber sequence]]. 

To break this down into invariants, apply the [[stable homotopy groups]]-[[functor]]. This yields a diagram of $\mathbb{Z}$-[[graded abelian groups]] of the form

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   \pi_\bullet(X_3) 
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}& 
   \pi_\bullet(X_2) 
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow} & 
   \pi_\bullet(X_1) 
     &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}& 
   \pi_\bullet(X_0)
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && \pi_\bullet(A_3) && \pi_\bullet(A_2) && \pi_\bullet(A_1) && \pi_\bullet(A_0)
  }
  \,.
$$

Here each hook at stage $k$ extends to a [[long exact sequence of homotopy groups]] via [[connecting homomorphisms]] $\delta_\bullet^k$

$$
  \cdots
    \to
  \pi_{\bullet+1}(A_k)
    \stackrel{\delta_{\bullet+1}^k}{\longrightarrow}
  \pi_\bullet(X_{k+1})
    \stackrel{\pi_\bullet(f_k)}{\longrightarrow}
  \pi_\bullet(X_k)
    \stackrel{}{\longrightarrow}
  \pi_\bullet(A_k)
   \stackrel{\delta_\bullet^k}{\longrightarrow}
  \pi_{\bullet-1}(X_{k+1})
  \to 
  \cdots
  \,.
$$

If we understand the [[connecting homomorphism]]

$$
  \delta_k \colon \pi_\bullet(A_k) \longrightarrow \pi_\bullet(X_{k+1})
$$

as a morphism of degree -1, then all this information fits into one diagram of the form

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   \pi_\bullet(X_3) 
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}& 
   \pi_\bullet(X_2) 
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow} & 
   \pi_\bullet(X_1) 
     &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}& 
   \pi_\bullet(X_0)
   \\
   && 
   \downarrow &{}_{\mathllap{\delta_2}}\nwarrow & 
   \downarrow &{}_{\mathllap{\delta_1}}\nwarrow &
   \downarrow &{}_{\mathllap{\delta_0}}\nwarrow
   & \downarrow
   \\
   && \pi_\bullet(A_3) && \pi_\bullet(A_2) && \pi_\bullet(A_1) && \pi_\bullet(A_0)
  }
  \,,
$$

where each triangle is a rolled-up incarnation of a [[long exact sequence of homotopy groups]] (and in particular is _not_ a commuting diagram!).

If we furthermore consider the [[bigraded object|bigraded]] [[abelian groups]] $\pi_\bullet(X_\bullet)$ and $\pi_\bullet(A_\bullet)$, then this information may further be rolled-up to a single diagram of the form

$$
  \array{
     \pi_\bullet(X_\bullet)
       & \stackrel{\pi_\bullet(f_\bullet)}{\longrightarrow} &
     \pi_\bullet(X_\bullet)
     \\
       & {}_{\mathllap{\delta}}\nwarrow 
       & \downarrow^{\mathrlap{\pi_\bullet(cofib(f_\bullet))}}
     \\
     && 
     \pi_\bullet(A_\bullet)
  }
$$

where the morphisms $\pi_\bullet(f_\bullet)$, $\pi_\bullet(cofib(f_\bullet))$ and $\delta$ have bi-degree $(0,-1)$, $(0,0)$ and $(-1,1)$, respectively.

Here it is convenient to shift the bigrading, equivalently, by setting

$$
  \mathcal{D}^{s,t} \coloneqq \pi_{t-s}(X_s)
$$

$$
  \mathcal{E}^{s,t} \coloneqq \pi_{t-s}(A_s)
  \,,
$$

because then $t$ counts the cycles of going around the triangles:

$$
  \cdots
   \to 
  \mathcal{D}^{s+1,t+1}
    \stackrel{\pi_{t-s}(f_s)}{\longrightarrow}
  \mathcal{D}^{s,t}
    \stackrel{\pi_{t-s}(cofib(f_s))}{\longrightarrow}
  \mathcal{E}^{s,t}
    \stackrel{\delta_s}{\longrightarrow}
  \mathcal{D}^{s+1,t}
    \to
  \cdots
$$

Data of this form is called an _[[exact couple]]_, def. \ref{ExactCouple} below. 


=--


+-- {: .num_defn #UnrolledExactCouple}
###### Definition

An _unrolled [[exact couple]]_ (of Adams-type) is a diagram of [[abelian groups]] of the form

$$
  \array{
     \cdots 
       &\stackrel{}{\longrightarrow}& 
     \mathcal{D}^{3,\bullet} 
       &\stackrel{i_2}{\longrightarrow}& 
     \mathcal{D}^{2,\bullet} 
       &\stackrel{i_1}{\longrightarrow} & 
     \mathcal{D}^{1,\bullet} 
       &\stackrel{i_0}{\longrightarrow}& 
     \mathcal{D}^{0,\bullet}
     \\
     && 
     \downarrow^{\mathrlap{}}  &{}_{\mathllap{k_2}}\nwarrow & 
     {}^{\mathllap{j_2}}\downarrow &{}_{\mathllap{k_1}}\nwarrow &
     {}^{\mathllap{j_1}}\downarrow &{}_{\mathllap{k_0}}\nwarrow
     & {}_{\mathllap{j_0}}\downarrow
     \\
     && \mathcal{E}^{3,\bullet} && \mathcal{E}^{2,\bullet} 
     && \mathcal{E}^{1,\bullet} && \mathcal{E}^{0,\bullet}
   }
$$

such that each triangle is a rolled-up [[long exact sequence]] of [[abelian groups]] of the form

$$
  \cdots
   \to 
  \mathcal{D}^{s+1,t+1}
    \stackrel{i_s}{\longrightarrow}
  \mathcal{D}^{s,t}
    \stackrel{j_s}{\longrightarrow}
  \mathcal{E}^{s,t}
    \stackrel{k_s}{\longrightarrow}
  \mathcal{D}^{s+1,t}
    \to
  \cdots
  \,.
$$


=--

The collection of this "un-rolled" data into a single diagram of [[abelian groups]] is called the corresponding _[[exact couple]]_.


+-- {: .num_defn #ExactCouple}
###### Definition

An _[[exact couple]]_ is a [[diagram]] (non-commuting) of [[abelian groups]] of the form

$$
  \array{
    \mathcal{D}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \,,
$$

such that this is [[exact sequence]] exact in each position, hence such that the [[kernel]] of every [[morphism]] is the [[image]] of the preceding one.

=--


The concept of exact couple so far just collects the sequences of long exact sequences given by a filtration. Next we turn to extracting information from this sequence of sequences.

+-- {: .num_remark #Observingd1}
###### Remark

The sequence of long exact sequences in remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} is inter-locking, in that every $\pi_{t-s}(X_s)$ appears _twice_:

$$
  \array{
    && & \searrow && \nearrow
    \\
    && && \pi_{t-s-1}(X_{s+1})
    \\
    && & {}^{\mathllap{\delta_{t-s}^s}}\nearrow 
    && \searrow^{\mathrlap{\pi_{t-s-1}(cofib(f_{s+1}))}}
    && && && \nearrow
    \\
    && \pi_{t-s}(A_s) && \underset{def: \;\;d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
    && \stackrel{def: \; d_1^{s+1,t}}{\longrightarrow} && \pi_{t-s-2}(A_{s+2})
    \\
    & \nearrow && && && {}_{\mathllap{\delta_{t-s-1}^{s+1}}}\searrow 
    && \nearrow_{\mathrlap{\pi_{t-s-2}(cofib(f_{s+2}))}}
    \\
    && && && && \pi_{t-s-2}(X_{s+2})
    \\
    && && && & \nearrow && \searrow
  }
$$

This gives rise to the horizontal composites $d_1^{s,t}$, as show above, and by the fact that the diagonal sequences are long exact, these are differentials: $d_1^2 = 0$, hence give a [[chain complex]]:

$$
  \array{
    \cdots & \stackrel{}{\longrightarrow}
    && \pi_{t-s}(A_s) && \overset{d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
    && \stackrel{d_1^{s+1,t}}{\longrightarrow} && \pi_{t-s-2}(A_{s+2})
    &&\longrightarrow & \cdots
  }
  \,.
$$

We read off from the interlocking long exact sequences what these differentials _mean_: an element $c \in \pi_{t-s}(A_s)$ lifts to an element $\hat c \in \pi_{t-s-1}(X_{s+2})$ precisely if $d_1 c = 0$:

$$
  \array{
    &\hat c \in & \pi_{t-s-1}(X_{s+2})
    \\
    && & \searrow^{\mathrlap{\pi_{t-s-1}(f_{s+1})}} 
    \\
    && && \pi_{t-s-1}(X_{s+1})
    \\
    && & {}^{\mathllap{\delta_{t-s}^s}}\nearrow 
    && \searrow^{\mathrlap{\pi_{t-s-1}(cofib(f_{s+1}))}}
    \\
    & c \in  & \pi_{t-s}(A_s) && \underset{d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
  }
$$

This means that the [[cochain cohomology]] of the complex $(\pi_{\bullet}(A_\bullet), d_1)$ produces elements of $\pi_\bullet(X_\bullet)$ and hence of $\pi_\bullet(X)$.

In order to organize this observation, notice that in terms of the exact couple of remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}, the differential 

$$
  d_1^{s,t}  \;\coloneqq \; \pi_{t-s-1}(cofib(f_{s+1})) \circ \delta_{t-s}^s
$$

is a component of the composite 

$$
  d \coloneqq j \circ k
  \,.
$$


=--

Some terminology:

+-- {: .num_defn #PageOfAnExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple}, 

$$
  \array{
    \mathcal{D}^{\bullet,\bullet}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}^{\bullet,\bullet}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}^{\bullet,\bullet}
  }
$$

its _page_ is the [[chain complex]]

$$
  (E^{\bullet,\bullet}, d \coloneqq j \circ  k)
  \,.
$$

=--

+-- {: .num_defn #DerivedExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple}, then the induced _derived exact couple_ is the diagram

$$
  \array{
    \widetilde {\mathcal{D}}
    &\stackrel{\tilde i}{\longrightarrow}&
    \widetilde {\mathcal{D}}
    \\
    & {}_{\mathllap{\tilde k}}\nwarrow & \downarrow^{\mathrlap{\tilde j}}
    \\
    && \widetilde{\mathcal{E}}
  }
$$

with 

1. $\tilde{\mathcal{E}} \coloneqq ker(d)/im(d)$;

1. $\tilde {\mathcal{D}} \coloneqq im(i)$;

1. $\tilde i \coloneqq i|_{im(i)}$;

1. $\tilde j \coloneqq j \circ (im(i))^{-1}$;

1. $\tilde k \coloneqq k|_{ker(d)}$.


=--

+-- {: .num_prop #DerivedExactCoupleIsExactCouple}
###### Proposition

A derived exact couple, def. \ref{DerivedExactCouple}, 
is again an exact couple, def. \ref{ExactCouple}.

=--

+-- {: .num_defn}
###### Definition

Given an exact couple, def. \ref{ExactCouple},
then the induced [[spectral sequence]], def. \ref{SpectralSequence}, is the sequence of pages, def. \ref{PageOfAnExactCouple}, of the induced sequence of derived exact couples, def. \ref{DerivedExactCouple}, prop. \ref{DerivedExactCoupleIsExactCouple}.

=--


+-- {: .num_example #AdamsTypeSpectralSequenceOfATower}
###### Example

Consider a [[filtered spectrum]], def. \ref{FilteredSpectrum},

$$
  \array{
   \cdots 
     &\stackrel{}{\longrightarrow}& 
   X_3 
     &\stackrel{f_2}{\longrightarrow}& 
   X_2 
     &\stackrel{f_2}{\longrightarrow} & 
   X_1 
     &\stackrel{f_1}{\longrightarrow}& 
   X
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

and its induced [[exact couple]] of [[stable homotopy groups]], from remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}

$$
  \array{
    \mathcal{D} &\stackrel{i}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{k}}\nwarrow& \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \;\;\;\;\;\,\;\;\;\;\;\;
  \array{
    \mathcal{D} &\stackrel{(-1,-1)}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{(1,0)}}\nwarrow& \downarrow^{\mathrlap{(0,0)}}
    \\
    && \mathcal{E}
  }
$$

with bigrading as shown on the right.

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/adamstypedifferentials.jpg" width="360" > 
</div>

As we pass to derived exact couples, by def. \ref{DerivedExactCouple}, 
the bidegree of $i$ and $k$ is preserved, but that of $j$ increases by $(1,1)$ in each step, since

$$
  deg(\tilde j) = deg( j \circ im(i)^{-1}) = deg(j) + (1,1)
  \,.
$$


Therefore the induced [[spectral sequence]] has differentials of the form

$$
  d_r \;\colon\; \mathcal{E}_r^{s,t} \longrightarrow \mathcal{E}_r^{s+r, t+r-1}
  \,.
$$

=--

## References

The original article is

*  [[W. S. Massey]], _Exact Couples in Algebraic Topology (Parts I and II)_, Annals of Mathematics, Second Series, Vol. 56, No. 2 (Sep., 1952), pp. 363-396 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/massey6.pdf))

also

* [[Beno Eckmann]], [[Peter Hilton]], _Exact couples in an abelian category_, Journal of Algebra Volume 3, Issue 1, January 1966, Pages 38-87 ([jorunal](http://www.sciencedirect.com/science/article/pii/0021869366900196))

A class of examples leading to what later came to be known as the [[Atiyah-Hirzebruch spectral sequence]] is discussed in section XV.7 of 

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press (1956)

Textbook accounts include

* [[Frank Adams]], part III, section 7 of _[[Stable homotopy and generalised homology]]_, 1974
 
* {#Kochmann96} [[Stanley Kochmann]], section 2.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#McCleary01} [[John McCleary]], section 2.2 (from p. 37 on) in _[A user's guide to spectral sequences](https://pages.vassar.edu/mccleary/books/users-guide-to-spectral-sequences/)_, Cambridge University Press, 2001 

* [[Charles Weibel]], section 5.9 _[[An Introduction to Homological Algebra]]_

Another review with an eye towards application to the [[Adams spectral sequence]] is in 

* [[Doug Ravenel]], chapter 2, section 1 of _[[Complex cobordism and stable homotopy groups of spheres]]_

[[!redirects exact couples]]

[[!redirects spectral sequence of an exact couple]]
[[!redirects spectral sequences of exact couples]]
