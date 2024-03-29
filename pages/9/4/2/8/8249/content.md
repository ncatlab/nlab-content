

***

This entry discusses the general notion of _[[derived functor]]_ specified to the special context of [[homological algebra]], hence to functors between [[categories of chain complexes]].

In the literature this is often understood to be the default case of derived functors. For more discussion of how the following relates to the more general concepts of derived functors see at _[derived functor -- In homological algebra](derived+functor#InHomologicalAlgebra)_.

***

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

The general concept of [[derived functor]] is in homological algebra usually called the _[[total derived functor|total]] [[hyper-derived functor]]_, with just "derived functor" being reserved for a more restrictive case. In this tradition, we consider the special case first and then generalize it in stages. The relation between all these notions is discussed [below](#Properties).

## Definition

Let $\mathcal{A}$ be an [[abelian category]]. Without essential loss of generality, we may assume that $\mathcal{A} = R Mod$ is the [[category of modules]] over some [[ring]], and we will often speak in terms of this case.

The category $\mathcal{A}$ embeds into its [[nLab:derived category]], the category of degreewise [[nLab:injective object|injective]] [[nLab:cochain complexes]] 

$$
  P : \mathcal{A} \to \mathcal{D}^\bullet(\mathcal{A}) = \mathcal{K}^\bullet(\mathcal{I}_{\mathcal{A}})
$$

or degreewise [[nLab:projective object|projective]] [[nLab:chain complexes]] 

$$
 Q : \mathcal{A} \to \mathcal{D}_\bullet(\mathcal{A}) =  \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}})
$$

modulo [[nLab:chain homotopy]]. This construction of the derived category naturally gives rise to the following notion of [[nLab:derived functors]], which we now discuss.

+-- {: .num_defn #AdditiveFunctor}
###### Definition

For $\mathcal{A}, \mathcal{B}$ two [[nLab:abelian categories]] (e.g. $R$[[nLab:Mod]] and $R'$[[nLab:Mod]]), a [[nLab:functor]]

$$
  F \colon \mathcal{A} \to \mathcal{B}
$$

is called an **[[nLab:additive functor]]** if 

1. $F$ maps [[nLab:generalized the|the]] [[nLab:zero object]] to the zero object, $F(0) \simeq 0 \in \mathcal{B}$; 

1. given any two [[nLab:objects]] $x, y \in \mathcal{A}$, there is an [[nLab:isomorphism]] $F(x \oplus y) \cong F(x) \oplus F(y)$, and this respects the inclusion and projection maps of the [[nLab:direct sum]]:

$$
\array { x &          &            &          & y \\
           & {}_{\mathllap{i_x}}\searrow &            & \swarrow_{\mathrlap{i_y}} \\
           &          & x \oplus y \\
           & {}^{\mathllap{p_x}}\swarrow &            & \searrow^{\mathrlap{p_y}} \\
         x &          &            &          & y }
\quad\quad\stackrel{F}{\mapsto}\quad\quad
\array { F(x) &          &                                      &          & F(y) \\
              & {}_{\mathllap{i_{F(x)}}}\searrow &   & \swarrow_{\mathrlap{i_{F(y)}}} \\
              &          & F(x \oplus y) \cong F(x) \oplus F(y) \\
              & {}^{\mathllap{p_{F(x)}}}\swarrow &                                      & \searrow^{\mathrlap{p_{F(y)}}} \\
         F(x) &          &                                      &          & F(y) }
$$

=--


+-- {: .num_defn #ProlongationOfFunctorToChainComplexes}
###### Definition

Given an [[nLab:additive functor]] $F : \mathcal{A} \to \mathcal{A}'$, it canonically induces a functor 

$$
  Ch_\bullet(F) \colon Ch_\bullet(\mathcal{A}) \to Ch_\bullet(\mathcal{A}')
$$

between [[nLab:categories of chain complexes]] (its "prolongation") by applying it to each [[nLab:chain complex]] and to all the diagrams in the definition of a [[nLab:chain map]]. Similarly it preserves [[nLab:chain homotopies]] and hence it passes to the quotient given by the strong [[nLab:homotopy category of chain complexes]]

$$
  \mathcal{K}(F) \colon \mathcal{K}(\mathcal{A}) \to \mathcal{K}(\mathcal{A}')
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

If $\mathcal{A}$ and $\mathcal{A}'$ have [[nLab:projective object|enough projectives]], then their [[nLab:derived categories]] are

$$
  \mathcal{D}_\bullet(\mathcal{A}) 
   \simeq 
  \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}})
$$

and 

$$
  \mathcal{D}^\bullet(\mathcal{A}) \simeq \mathcal{K}^\bullet(\mathcal{I}_{\mathcal{A}})
$$

etc. One wants to accordingly _derive_ from $F$ a functor $\mathcal{D}_\bullet(\mathcal{A}) \to \mathcal{D}_\bullet(\mathcal{A}')$ between these derived categories. It is immediate to achieve this on the domain category, there we can simply precompose and form

$$
  \mathcal{A}  
    \to 
  \mathcal{D}_\bullet(\mathcal{A})
   \simeq
  \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}}) 
   \hookrightarrow
  \mathcal{K}_\bullet(\mathcal{A})
   \stackrel{\mathcal{K}_\bullet(F)}{\to}
  \mathcal{K}_\bullet(\mathcal{A}')
  \,.
$$

But the resulting composite lands in $\mathcal{K}_\bullet(\mathcal{A}')$ and in general does not factor through the inclusion $\mathcal{D}_\bullet(\mathcal{A}') = \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}'}) \hookrightarrow \mathcal{K}_\bullet(\mathcal{A}')$.

In a more general abstract discussion than we present here, one finds that by applying a projective resolution functor _on chain complexes_, one can enforce this factorization. However, by definition of [[nLab:resolution]], the resulting chain complex is [[nLab:quasi-isomorphism|quasi-isomorphic]] to the one obtained by the above composite. 

This means that if one is only interested in the "weak chain homology type" of the chain complex in the image of a [[nLab:derived functor]], then forming [[nLab:chain homology]] groups of the chain complexes in the images of the above composite gives the desired information. This is what def. \ref{RightDerivedFunctorOfLeftExactFunctor} and def. \ref{LeftDerivedFunctorOfRightExactFunctor} below do.

=--

+-- {: .num_defn #LeftRightExactFunctor}
###### Definition

Let $\mathcal{A}, \mathcal{A}'$ be two [[nLab:abelian categories]], for instance $\mathcal{A} = R $[[nLab:Mod]] and $\mathcal{A}' = R'$[[nLab:Mod]]. Then a [[nLab:functor]] $F \colon \mathcal{A} \to \mathcal{A}'$ 
which preserves [[nLab:direct sums]] (and hence in particular the [[nLab:zero object]]) is called

* a **[[nLab:left exact functor]]** if it preserves [[nLab:kernels]];

* a **[[nLab:right exact functor]]** if it preserves [[nLab:cokernels]];

* an **[[nLab:exact functor]]** if it is both left and right exact.

=--

Here to "preserve kernels" means that for every morphism $X \stackrel{f}{\to} Y$ in $\mathcal{A}$ we have an [[nLab:isomorphism]] on the left of the following [[nLab:commuting diagram]]

$$
  \array{
    F(ker(f)) &\to& F(X) & \stackrel{F(f)}{\to} & F(Y)
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{=}} && \downarrow^{\mathrlap{=}}
    \\
    ker(F(f)) &\to& F(X) &\stackrel{F(f)}{\to}& F(Y)
  }
  \,,
$$

hence that both rows are [[nLab:exact sequence|exact]]. And dually for right exact functors.

We record the following immediate consequence of this definition (which in the literature is often taken to be the definition).

+-- {: .num_prop #LeftRightExactFunctorsCharacterizedByExactSequences}
###### Proposition

If $F$ is a left exact functor, then for every [[nLab:exact sequence]]  of the form

$$
  0 \to A \to B \to C
$$

also 

$$
  0 \to F(A) \to F(B) \to F(C)
$$

is an exact sequence. Dually, if $F$ is a right exact functor, then for every [[nLab:exact sequence]] of the form

$$
  A \to B \to C \to 0
$$

also 

$$
  F(A) \to F(B) \to F(C) \to 0
$$

is an exact sequence.

=--

+-- {: .proof}
###### Proof

If $0 \to A \to B \to C$ is exact then $A \hookrightarrow B$ is a [[monomorphism]].
But then the statement that $A \to B \to C$ is exact at $B$ says 
precisely that $A$ is the [[kernel]] of $B \to C$. 
So if $F$ is left exact then by definition also $F(A) \to F(B)$
is the kernel of $F(B) \to F(C)$ and so is in particular also 
a monomorphism.
Dually for right exact functors.

=--

+-- {: .num_remark }
###### Remark

Proposition \ref{LeftRightExactFunctorsCharacterizedByExactSequences} is
clearly the motivation for the terminology in def. \ref{LeftRightExactFunctor}: a functor is left exact if it preserves short exact sequences to the left, and right exact if it preserves them to the right.

=--

Now we can state the main two definitions of this section.

+-- {: .num_defn #RightDerivedFunctorOfLeftExactFunctor}
###### Definition

Let 

$$
  F : \mathcal{A} \to \mathcal{A}'
$$

be a [[left exact functor]] between [[nLab:abelian categories]] such that $\mathcal{A}$ has [[enough injectives]]. For $n \in \mathbb{N}$ the **$n$th [[right derived functor]]** of $F$ is the composite

$$
  R^n F 
    \;\colon\;
  \mathcal{A}
   \stackrel{P}{\to}
  \mathcal{K}^\bullet(\mathcal{I}_{\mathcal{A}})
   \stackrel{\mathcal{K}^\bullet(F)}{\to}
  \mathcal{K}^\bullet(\mathcal{A}')
    \stackrel{H^n(-)}{\to}
  \mathcal{A}'
  \,,
$$

where

* $P$ is an [[injective resolution]] functor;

* $\mathcal{K}^\bullet(F)$ is a prolongation of $F$ analogous to def. \ref{ProlongationOfFunctorToChainComplexes};

* $H^n(-)$ is the $n$-[[chain homology]] functor. Hence

$$
  (R^n F)(X^\bullet) \coloneqq H^n(F(P(X)^\bullet))
  \,.
$$

=--

Dually:

+-- {: .num_defn #LeftDerivedFunctorOfRightExactFunctor}
###### Definition

Let 

$$
  F \colon \mathcal{A} \to \mathcal{A}'
$$

be a [[right exact functor]] between [[abelian categories]] such that $\mathcal{A}$ has [[enough projectives]]. For $n \in \mathbb{N}$ the **$n$th [[left derived functor]]** of $F$ is the composite

$$
  L_n F 
   \;\colon\;
  \mathcal{A}
   \stackrel{Q}{\to}
  \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}})
   \stackrel{\mathcal{K}_\bullet(F)}{\to}
  \mathcal{K}_\bullet(\mathcal{A}')
    \stackrel{H_n(-)}{\to}
  \mathcal{A}'
  \,,
$$

where

* $Q$ is a [[projective resolution]] functor;

* $\mathcal{K}_\bullet(F)=\mathcal{K}(F)$ is the prolongation of $F$ according to def. \ref{ProlongationOfFunctorToChainComplexes};

* $H_n(-)$ is the $n$-[[chain homology]] functor. Hence

$$
  (L_n F)(X_\bullet) \coloneqq H_n(F(Q(X)_\bullet))
  \,.
$$

=--

## Properties
 {#Properties}

### Basic properties

The following proposition says that in degree 0 these derived functors coincide with the original functors. 

+-- {: .num_prop #BasicPropertiesOfDerivedFunctors}
###### Proposition

Let $F \colon \mathcal{A} \to \mathcal{B}$ a [[left exact functor]], def. \ref{LeftRightExactFunctor} in the presence of [[enough injectives]]. Then for all $X \in \mathcal{A}$ there is a [[nLab:natural isomorphism]]

$$
  R^0F(X) \simeq F(X)
  \,.
$$

Dually, if $F$ is a [[nLab:right exact functor]] in the presence of [[enough projectives]], then 

$$
  L_0 F(X) \simeq F(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is formally dual. 

By [this](/nlab/show/injective+resolution#InjectiveResolutionInComponents) remark an injective resolution $X \stackrel{\simeq_{qi}}{\to} X^\bullet$ is equivalently an [[nLab:exact sequence]] of the form

$$
  0 \to X \hookrightarrow X^0 \to X^1 \to \cdots
  \,.
$$

If $F$ is left exact then it preserves this exact sequence by definition of left exactness, and hence 

$$
  0 \to F(X) \hookrightarrow F(X^0) \to F(X^1) \to \cdots
$$

is an exact sequence. But this means that 

$$
  R^0 F(X) \coloneqq ker(F(X^0) \to F(X^1)) \simeq F(X)
  \,.
$$

=--

The following immediate consequence of the definition is worth recording:

+-- {: .num_prop #LeftDerivedFunctorOnProjectiveVanishes}
###### Proposition

Let $F$ be an [[nLab:additive functor]]. 

* If $F$ is [[nLab:right exact functor|right exact]] and $N \in \mathcal{A}$ is a [[nLab:projective object]], then 

  $$
    L_n F(N) = 0 \;\;\;\; \forall n \geq 1
    \,.
  $$

* If $F$ is [[nLab:left exact functor|left exact]] and $N \in \mathcal{A}$ is a [[nLab:injective object]], then 

  $$
    R^n F(N) = 0 \;\;\;\; \forall n \geq 1
    \,.
  $$

=--

+-- {: .proof}
###### Proof

If $N$ is projective then the chain complex $[\cdots \to 0 \to 0 \to N]$ is already a [[projective resolution]] and hence by definition $L_n F(N) \simeq H_n(0)$ for $n \geq 1$. Dually if $N$ is an injective object.

=--

For proving the basic property of derived functors below in prop. \ref{LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence} which continues these basis statements to higher degree, in a certain way, we need the following technical lemma.

+-- {: .num_lemma #ProjectiveResolutionOfExactSequenceByExactSequence}
###### Lemma

For $0 \to A \stackrel{i}{\to} B \stackrel{p}{\to} C \to 0$ a [[nLab:short exact sequence]]
in an [[nLab:abelian category]] with [[nLab:enough projectives]], 
there exists a [[nLab:commuting diagram]] of [[nLab:chain complexes]]

$$
  \array{
    0 &\to& A_\bullet &\to& B_\bullet &\to& C_\bullet &\to& 0
    \\
      && 
    \downarrow^{\mathrlap{f_\bullet}}
      && 
    \downarrow^{\mathrlap{g_\bullet}}
      && 
    \downarrow^{\mathrlap{h_\bullet}}
    \\
    0 &\to& A &\stackrel{i}{\to}& B &\stackrel{p}{\to}& C &\to& 0
  }
$$

where 

* each vertical morphism is a [[nLab:projective resolution]];

and in addition

* the top row is again a [[nLab:short exact sequence]] of chain complexes.

=--


+-- {: .proof}
###### Proof

By prop. \ref{ExistenceOfInjectiveResolutions} we can choose $f_\bullet$ and $h_\bullet$. The task is now to construct the third resolution $g_\bullet$ such as to obtain a short exact sequence of chain complexes, hence degreewise a short exact sequence, in the two row.

To construct this, let for each $n \in \mathbb{N}$

$$
  B_n \coloneqq A_n \oplus C_n
$$

be the [[nLab:direct sum]] and let the top horizontal morphisms be the canonical inclusion and projection maps of the direct sum.

Let then furthermore (in [[nLab:matrix calculus]] notation)

$$
  g_0 = 
   \left(
     \array{
        (g_0)_A  
        & 
        (g_0)_B
      }
  \right)
 : A_0 \oplus C_0 \to B
$$

be given in the first component by the given composite

$$
 (g_0)_A : A_0 \oplus C_0 \stackrel{}{\to} A_0 \stackrel{f_0}{\to} A \stackrel{i}{\hookrightarrow} B
$$

and in the second component we take

$$
  (g_0)_C : A_0 \oplus C_0 \to C_0 \stackrel{\zeta}{\to} B
$$

to be given by a lift in

$$
  \array{
    && B
    \\
    & {}^{\mathllap{\zeta}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    C_0 &\stackrel{h_0}{\to}& C
  }
  \,,
$$

which exists by the [[nLab:left lifting property]] of the [[nLab:projective object]]
$C_0$ (since $C_\bullet$ is a projective resolution) against the [[nLab:epimorphism]] $p : B \to C$ of the [[nLab:short exact sequence]].

In total this gives in degree 0

$$
  \array{
    A_0 &\hookrightarrow& A_0 \oplus C_0 &\to& C_0
    \\
    {}^{\mathllap{f_0}}\downarrow 
      && 
    {}^{\mathllap{((g_0)_A, (g_0)_C)}}\downarrow &\swarrow_{\zeta}& \downarrow^{\mathrlap{h_0}}
    \\
    A &\stackrel{i}{\hookrightarrow}& B &\stackrel{p}{\to}& C
  }
  \,.
$$

Let then the [[nLab:differentials]] of $B_\bullet$ be given by

$$
  d_k^{B_\bullet} 
    = 
  \left(
    \array{
      d_k^{A_\bullet} & (-1)^k e_k
      \\
      0 & d_k^{C_\bullet}
    }
  \right)
  : 
  A_{k+1} \oplus C_{k+1}
  \to
  A_k \oplus C_k
  \,,
$$

where the $\{e_k\}$ are constructed by [[nLab:induction]] as follows. Let $e_0$ be a lift in 

$$
  \array{   
    & && A_0
    \\
    & & {}^{\mathllap{e_0}}\nearrow & \downarrow^{\mathrlap{f_0}}
    \\
    \zeta \circ d^{C_\bullet}_0 \colon & C_1 &\stackrel{}{\to}& A &\hookrightarrow B&
  }
$$

which exists since $C_1$ is a [[nLab:projective object]] and $A_0 \to A$ is an epimorphism by $A_\bullet$ being a projective resolution. Here we are using that by exactness the bottom morphism indeed factors through $A$ as indicated, because the definition of $\zeta$ and  the chain complex property of $C_\bullet$ gives 

$$
  \begin{aligned}
    p \circ \zeta \circ d^{C_\bullet}_0 
    &= 
    h_0 \circ d^{C_\bullet}_0
    \\
    & = 0 \circ h_1
    \\
    & = 0 
  \end{aligned}
  \,.
$$ 

Now in the induction step, assuming that $e_{n-1}$ has been been found satisfying the chain complex property, let $e_n$ be a lift in

$$
  \array{
    & && A_n
    \\
    & & {}^{\mathllap{e_{n}}}\nearrow & \downarrow^{\mathrlap{d^{A_\bullet}_{n-1}}}
    \\
    e_{n-1}\circ d_n^{C_\bullet} \colon & C_{n+1} &\stackrel{}{\hookrightarrow}& ker(d^{A_\bullet}_{n-2}) = im(d^{A_\bullet}_{n-1})) &\to& A_{n-1}
  }
  \,,
$$


which again exists since $C_{n+1}$ is projective. That the bottom morphism factors as indicated is the chain complex property of $e_{n-1}$ inside $d^{B_\bullet}_{n-1}$.

To see that the $d^{B_\bullet}$ defines this way indeed squares to 0 notice that

$$
  d^{B_\bullet}_{n}
  \circ
  d^{B_\bullet}_{n+1}
  = 
  \left(
    \array{
       0 &  (-1)^{n}\left(e_{n} \circ d^{C_\bullet}_{n+1} - d^{A_\bullet}_n \circ e_{n+1} \right) 
       \\
       0 & 0
     }
  \right)
  \,.
$$

This vanishes by the very commutativity of the above diagram.


This establishes $g_\bullet$ such that the above diagram commutes and the bottom row is degreewise a short exact sequence, in fact a [[nLab:split exact sequence]], by construction. 

To see that $g_\bullet$ is indeed a quasi-isomorphism, consider the [[nLab:homology long exact sequence]] associated to the short exact sequence of cochain complexes $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0$. In positive degrees it implies that the chain homology of $B_\bullet$ indeed vanishes. In degree 0 it gives the short sequence $0 \to A \to H_0(B_\bullet) \to B\to 0$ sitting in a commuting diagram

$$
  \array{
    0 &\to& A &\hookrightarrow& H_0(B_\bullet) &\to& C &\to& 0
    \\
    \downarrow && \downarrow^{\mathrlap{=}} && \downarrow && \downarrow^{\mathrlap{=}} && \downarrow
    \\
    0 &\to& A &\hookrightarrow& B &\to& C &\to& 0 
    \,,
  }
$$

where both rows are exact. That the middle vertical morphism is an [[nLab:isomorphism]] then follows by the [[nLab:five lemma]].

=--


The formally dual statement to lemma \ref{ProjectiveResolutionOfExactSequenceByExactSequence} is the following.

+-- {: .num_lemma #InjectiveResolutionOfExactSequenceByExactSequence}
###### Lemma

For $0 \to A \to B \to C \to 0$ a [[nLab:short exact sequence]]
in an [[abelian category]] with [[injective object|enough injectives]], 
there exists a [[nLab:commuting diagram]] of cochain complexes

$$
  \array{
    0 &\to& A &\to& B &\to& C &\to& 0
    \\
      && 
    \downarrow^{\mathrlap{}}
      && 
    \downarrow^{\mathrlap{}}
      && 
    \downarrow^{\mathrlap{}}
    \\
    0 &\to& A^\bullet &\to& B^\bullet &\to& C^\bullet &\to& 0
  }
$$

where 

* each vertical morphism is an [[nLab:injective resolution]];

and in addition

* the bottom row is again a [[nLab:short exact sequence]] of cochain complexes.

=--

### Long exact sequence of a derived functor
 {#LongExactSequence}


The central general fact about derived functors to be discussed here is now the following.

+-- {: .num_prop #LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence}
###### Proposition

Let $\mathcal{A}, \mathcal{B}$ be [[abelian categories]] and assume that $\mathcal{A}$ has [[injective object|enough injectives]].

Let $F : \mathcal{A} \to \mathcal{B}$ be a [[left exact functor]] and let

$$
  0 \to A \to B \to C \to 0
$$

be a [[short exact sequence]] in $\mathcal{A}$.  

Then there is a [[long exact sequence]] of images of these objects under the right derived functors $R^\bullet F(-)$ of def. \ref{RightDerivedFunctorOfLeftExactFunctor}

$$
  \array{
    0 &\to& R^0F (A)  &\to&  R^0 F(B)  &\to&  R^0 F(C) 
     &\stackrel{\delta_0}{\to}& 
    R^1 F(A) &\to& R^1 F(B) &\to& R^1F(C)
     &\stackrel{\delta_1}{\to}&
    R^2 F(A) &\to& \cdots
    \\
    && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    0 &\to& F(A) &\to& F(B) &\to& F(C)
  }
$$

in $\mathcal{B}$.

=--

+-- {: .proof}
###### Proof

By lemma \ref{InjectiveResolutionOfExactSequenceByExactSequence} we can find an injective resolution

$$
  0 \to A^\bullet \to B^\bullet \to C^\bullet \to 0
$$

of the given exact sequence which is itself again an exact sequence of cochain complexes.

Since $A^n$ is an [[nLab:injective object]] for all $n$, its component sequences $0 \to A^n \to B^n \to C^n \to 0$ are indeed [[nLab:split exact sequences]] (see the discussion there). Splitness is preserved by any functor $F$ (and also since $F$ is [[nLab:additive functor|additive]] it even preserves the [[nLab:direct sum]] structure that is chosen in the proof of lemma \ref{ProjectiveResolutionOfExactSequenceByExactSequence}) and so it follows that

$$
  0 \to F(\tilde A^\bullet) \to F(\tilde B^\bullet) \to F(\tilde C^\bullet) \to 0
$$

is a again short exact sequence of cochain complexes, now in $\mathcal{B}$. Hence we have the corresponding [[nLab:homology long exact sequence]] from prop. \ref{HomologyLongExactSequence}:


$$
  \cdots
   \to
  H^{n-1}(F(A^\bullet)) \to H^{n-1}(F(B^\bullet)) \to H^{n-1}(F(C^\bullet))
    \stackrel{\delta}{\to}
  H^n(F(A^\bullet)) \to H^n(F(B^\bullet)) \to H^n(F(C^\bullet))
    \stackrel{\delta}{\to}
  H^{n+1}(F(A^\bullet)) \to H^{n+1}(F(B^\bullet)) \to H^{n+1}(F(C^\bullet))
   \to
  \cdots
  \,.
$$

By construction of the resolutions and by def. \ref{RightDerivedFunctorOfLeftExactFunctor}, this is equal to

$$
  \cdots
   \to
  R^{n-1}F(A) \to R^{n-1}F(B) \to R^{n-1}F(C) 
   \stackrel{\delta}{\to}
  R^{n}F(A) \to R^{n}F(B) \to R^{n}F(C) 
    \stackrel{\delta}{\to}
  R^{n+1}F(A) \to R^{n+1}F(B) \to R^{n+1}F(C) 
   \to
  \cdots
  \,.
$$

Finally the equivalence of the first three terms with $F(A) \to F(B) \to F(C)$ is given by prop. \ref{BasicPropertiesOfDerivedFunctors}.


=--

+-- {: .num_remark #DerivedFunctorAsObstructionToExactness}
###### Remark

Prop. \ref{LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence} implies that one way to interpret $R^1 F(A)$ is as a "measure for how a [[nLab:left exact functor]] $F$ fails to be an [[nLab:exact functor]]". For, with $A \to B \to C$ any [[nLab:short exact sequence]], this proposition gives the exact sequence

$$
  0 \to F(A) \to F(B) \to F(C) \to R^1 F(A)
$$

and hence $0 \to F(A) \to F(B) \to F(C) \to 0$ is a short exact sequence itself precisely if $R^1 F(A) \simeq 0$.

Dually, if $F$ is [[nLab:right exact functor]], then $L_1 F (C)$ "measures how $F$ fails to be exact" for then 

$$
  L_1F (C) \to F(A) \to F(B) \to F(C) \to 0
$$

is an exact sequence and hence is a short exact sequence precisely if $L_1F(C) \simeq 0$.

=--

Notice that in fact we even have the following statement (following directly from the definition).

+-- {: .num_prop #DerivedFunctorOfExactFunctor}
###### Proposition


Let $F$ be an [[additive functor]] which is an [[exact functor]]. Then its left and right derived functors vanish in positive degree:

$$
  R^{\geq 1} F = 0 
$$

and

$$  
  L_{\geq 1} F = 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because an [[exact functor]] preserves all [[exact sequences]]. If $Y_\bullet \to A$ is a projective resolution then also $F(Y)_\bullet$ is exact in all positive degrees, and hence $L_{n\geq 1} F(A) ) H_{n \geq}(F(Y)) = 0$. Dually for $R^n F$.

=--

Conversely:

+-- {: .num_defn #AcyclicObject}
###### Definition

Let $F \colon \mathcal{A} \to \mathcal{B}$ be a left or right exact additive functor. An object $A \in \mathcal{A}$ is called an $F$-**[[nLab:acyclic object]]** if all positive-degree right/left derived functors of $F$ are zero on $A$. 

=--


### Via acyclic resolutions
 {#ViaAcyclicResolutions}

We now discuss how the derived functor of an additive functor $F$ may also be computed not necessarily with genuine injective/projective resolutions as in def. \ref{RightDerivedFunctorOfLeftExactFunctor}, but with (just) "$F$-injective"/"$F$-projective resolutions".

While projective resolutions in $\mathcal{A}$ are _sufficient_ for computing _every_ [[nLab:left derived functor]] on $Ch_\bullet(\mathcal{A})$ and injective resolutions are sufficient for computing _every_ [[nLab:right derived functor]] on $Ch^\bullet(\mathcal{A})$, if one is interested just in a single functor $F$ then such resolutions may be more than _necessary_. A weaker kind of resolution which is still sufficient is then often more convenient for applications. These _$F$-projective resolutions_ and _$F$-injective resolutions_, respectively, we discuss now. A special case of both are _$F$-[[nLab:acyclic resolutions]]_.

Let $\mathcal{A}, \mathcal{B}$ be [[nLab:abelian categories]] and let $F \colon \mathcal{A} \to \mathcal{B}$ be an [[nLab:additive functor]]. 

+-- {: .num_defn #FInjectives}
###### Definition

Assume that $F$ is [[nLab:left exact functor|left exact]]. An [[nLab:additive category|additive]] [[nLab:full subcategory]] $\mathcal{I} \subset \mathcal{A}$ is called **$F$-injective** (or: consisting of $F$-injective objects) if

1. for every object $A \in \mathcal{A}$ there is a [[nLab:monomorphism]] $A \to \tilde A$ into an object $\tilde A \in \mathcal{I} \subset \mathcal{A}$;

1. for every [[nLab:short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $A, B \in \mathcal{I} \subset \mathcal{A}$ also $C \in \mathcal{I} \subset \mathcal{A}$;

1. for every [[nLab:short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $A\in \mathcal{I} \subset \mathcal{A}$ also $0 \to F(A) \to F(B) \to F(C) \to 0$ is a short exact sequence in $\mathcal{B}$. 

=--

And dually:

+-- {: .num_defn #FProjectives}
###### Definition

Assume that $F$ is [[nLab:right exact functor|right exact]]. An [[nLab:additive category|additive]] [[nLab:full subcategory]] $\mathcal{P} \subset \mathcal{A}$ is called **$F$-projective** (or: consisting of $F$-projective objects) if

1. for every object $A \in \mathcal{A}$ there is an [[nLab:epimorphism]] $\tilde A \to A$ from an object $\tilde A \in \mathcal{P} \subset \mathcal{A}$;

1. for every [[nLab:short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $B, C \in \mathcal{P} \subset \mathcal{A}$ also $A \in \mathcal{P} \subset \mathcal{A}$;

1. for every [[nLab:short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $C\in \mathcal{P} \subset \mathcal{A}$ also $0 \to F(A) \to F(B) \to F(C) \to 0$ is a short exact sequence in $\mathcal{B}$. 

=--

With the $\mathcal{I},\mathcal{P}\subset \mathcal{A}$ as above, we say:

+-- {: .num_defn #FProjectivesResolution}
###### Definition

For $A \in \mathcal{A}$, 

* an **$F$-injective resolution** of $A$ is a [[cochain complex]] $I^\bullet \in Ch^\bullet(\mathcal{I}) \subset Ch^\bullet(\mathcal{A})$ and a [[nLab:quasi-isomorphism]]

  $$
    A \stackrel{\simeq_{qi}}{\to} I^\bullet
  $$ 

* an **$F$-projective resolution** of $A$ is a [[chain complex]] $Q_\bullet \in Ch_\bullet(\mathcal{P}) \subset Ch^\bullet(\mathcal{A})$ and a [[nLab:quasi-isomorphism]]

  $$
    Q_\bullet \stackrel{\simeq_{qi}}{\to} A
    \,.
  $$ 

=--

Let now $\mathcal{A}$ have [[enough projectives]] / [[enough injectives]], respectively.

+-- {: .num_example #FAcyclicObjectsAreFProjectiveObjects}
###### Example

For $F \colon \mathcal{A} \to \mathcal{B}$ an [[nLab:additive functor]],
let $Ac \subset \mathcal{A}$ be the [[nLab:full subcategory]] on the $F$-[[nLab:acyclic objects]], def. \ref{AcyclicObject}. Then

* if $F$ is [[nLab:left exact functor|left exact]], then $\mathcal{I} \coloneqq Ac$ is a subcategory of $F$-injective objects;

* if $F$ is [[nLab:right exact functor|right exact]], then $\mathcal{P} \coloneqq Ac$ is a subcategory of $F$-projective objects.

=--

+-- {: .proof}
###### Proof

Consider the case that $F$ is left exact. The other case works dually.
Then the first condition of def. \ref{FInjectives} is satisfied because every [[nLab:injective object]] is an $F$-[[nLab:acyclic object]] and by assumption there are enough of these. 

For the second and third condition of def. \ref{FInjectives} use that there is the [[nLab:long exact sequence]] of [[nLab:derived functors]] prop. \ref{LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence}

$$
  0 \to F(A) \to F(B) \to F(C) \to R^1 F(A) \to R^1 F(B) \to R^1 F(C) \to R^2 F(A) \to R^2 F(B) \to R^2 F(C) \to \cdot
  \,.
$$

For the second condition, by assumption on $A$ and $B$ and definition of $F$-[[nLab:acyclic object]] we have $R^n F(A) \simeq 0$ and $R^n F(B) \simeq 0$ for $n \geq 1$ and hence short exact sequences

$$
  0 \to 0 \to R^n F(C) \to 0
$$

which imply that $R^n F(C)\simeq 0$ for all $n \geq 1$, hence that $C$ is acyclic. 

Similarly, the third condition is equivalent to $R^1 F(A) \simeq 0$. 

=--

+-- {: .num_example #FAcyclicResolution}
###### Example

The $F$-projective/injective resolutions (def. \ref{FProjectivesResolution}) by [[acyclic objects]] as in example \ref{FAcyclicObjectsAreFProjectiveObjects} are called **$F$-acyclic resolutions**.

=--


Let $\mathcal{A}$ be an [[nLab:abelian category]] with [[nLab:injective object|enough injectives]].
Let $F \colon \mathcal{A} \to \mathcal{B}$ be an [[nLab:additive functor|additive]] [[nLab:left exact functor]] with [[nLab:right derived functor]] $R_\bullet F$, def. \ref{RightDerivedFunctorOfLeftExactFunctor}. Finally let $\mathcal{I} \subset \mathcal{A}$ be a subcategory of $F$-injective objects, def. \ref{FInjectives}.


+-- {: .num_lemma #FPreservesNullnessOfFInjectiveComplexes}
###### Lemma

If a [[nLab:cochain complex]] $X^\bullet \in Ch^\bullet(\mathcal{I}) \subset Ch^\bullet(\mathcal{A})$ is [[nLab:quasi-isomorphism|quasi-isomorphic]] to 0, 

$$
  X^\bullet \stackrel{\simeq_{qi}}{\to} 0
$$

then also $F(X^\bullet) \in Ch^\bullet(\mathcal{B})$ is quasi-isomorphic to 0

$$
  F(X^\bullet) \stackrel{\simeq_{qi}}{\to} 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the following collection of [[nLab:short exact sequences]] obtained from the [[nLab:long exact sequence]] $X^\bullet$:

$$
  0 \to X^0 \stackrel{d^0}{\to} X^1 \stackrel{d^1}{\to} im(d^1) \to 0
$$

$$
  0 \to im(d^1) \to X^2 \stackrel{d^2}{\to} im(d^2) \to 0
$$

$$
  0 \to im(d^2) \to X^3 \stackrel{d^3}{\to} im(d^3) \to 0
$$

and so on. Going by [[nLab:induction]] through this list and using the second condition in def. \ref{FInjectives} we have that all the $im(d^n)$ are in $\mathcal{I}$. Then the third condition in def. \ref{FInjectives} says that all the sequences

$$
  0 \to F(im(d^n)) \to F(X^n+1) \to F(im(d^{n+1})) \to 0
$$

are [[nLab:short exact sequence|exact]]. But this means that 

$$
  0 \to F(X^0)\to F(X^1) \to F(X^2) \to \cdots
$$

is exact, hence that $F(X^\bullet)$ is quasi-isomorphic to 0.


=--


+-- {: .num_theorem #DerivedFFromFInjectiveResolution}
###### Theorem

For $A \in \mathcal{A}$ an object with $F$-injective resolution $A \stackrel{\simeq_{qi}}{\to} I_F^\bullet$, def. \ref{FProjectivesResolution}, we have for each $n \in \mathbb{N}$ an [[nLab:isomorphism]]

$$  
  R^n F(A) \simeq H^n(F(I_F^\bullet))
$$

between the $n$th right derived functor, def. \ref{RightDerivedFunctorOfLeftExactFunctor} of $F$ evaluated on $A$ and the [[nLab:cochain cohomology]] of $F$ applied to the $F$-injective resolution $I_F^\bullet$.

=--

+-- {: .proof}
###### Proof

By [this prop.](https://ncatlab.org/schreiber/show/Introduction+to+Homological+algebra#ExistenceOfInjectiveResolutions) we may also find an injective resolution $A \stackrel{\simeq_{qi}}{\to} I^\bullet$. By [this prop](https://ncatlab.org/schreiber/show/Introduction+to+Homological+algebra#InjectiveResolutionOfCodomainRespectsMorphisms) there is a lift of the identity on $A$ to a [[chain map]] $I^\bullet_F \to I^\bullet$ such that the [[diagram]]

$$
  \array{
     A &\stackrel{\simeq_{qi}}{\to}& I_F^\bullet
     \\
     \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{f}}
     \\
     A &\stackrel{\simeq_{qi}}{\to}& I^\bullet
  }
$$

[[nLab:commuting diagram|commutes]] in $Ch^\bullet(\mathcal{A})$. Therefore by the [[nLab:2-out-of-3]] property of [[nLab:quasi-isomorphisms]] it follows that $f$ is a quasi-isomorphism

Let $Cone(f) \in Ch^\bullet(\mathcal{A})$ be the [[nLab:mapping cone]] of $f$ and let $I^\bullet \to Cone(f)$ be the canonical [[nLab:chain map]] into it. By the explicit formulas for mapping cones, we have that 

1. there is an [[nLab:isomorphism]] $F(Cone(f)) \simeq Cone(F(f))$;

1. $Cone(f) \in Ch^\bullet(\mathcal{I})\subset Ch^\bullet(\mathcal{A})$ (because $F$-injective objects are closed under [[nLab:direct sum]]).

The first implies that we have a [[nLab:homology exact sequence]]

$$
  \cdots \to H^n(I^\bullet) \to H^n(I_F^\bullet) \to H^n(Cone(f)^\bullet)
   \to H^{n+1}(I^\bullet) \to H^{n+1}(I_F^\bullet) \to H^{n+1}(Cone(f)^\bullet) \to \cdots
  \,.
$$

Observe that with $f^\bullet$ a quasi-isomorphism $Cone(f^\bullet)$ is quasi-isomorphic to 0. Therefore 
the second item above implies with lemma \ref{FPreservesNullnessOfFInjectiveComplexes} that also $F(Cone(f))$ is quasi-isomorphic to 0. This finally means that the above homology exact sequences consists of exact pieces of the form

$$
  0 \to (R^n F(A)\coloneqq H^n(I^\bullet) \stackrel{\simeq}{\to} H^n(I_F^\bullet) \to 0
  \,.
$$

=--





### Derived adjoint functors

+-- {: .num_note}
###### Observation

If 

$$
  (F \dashv G) : \mathcal{A}
  \stackrel{\overset{G}{\leftarrow}}{\underset{F}{\to}}
   \mathcal{B}
$$

is a pair of [[additive functor|additive]] [[adjoint functors]], then 

* the [[left adjoint]] $F$ is [[right exact functor|right exact]];

* the [[right adjoint]] $G$ is [[left exact functor|left exact]];

=--


(...)



### Preservation of further limits and colimits

+-- {: .num_prop }
###### Proposition

Let $F \colon \mathcal{A} \to \mathcal{B}$ be an [[additive functor|additive]] [[right exact functor]] with codomain an [[additive and abelian categories|AB5-category]]. 

Then the [[left derived functors]] $L_n F$ preserves [[filtered colimits]] precisely if filtered colimits of [[projective objects]] in $\mathcal{A}$ are $F$-[[acyclic objects]]. 

=--

See [here](http://mathoverflow.net/questions/97658/left-derived-functors-commute-with-filtered-colimits).

## Examples

(...)

## Related concepts

* [[delta-functor]]


## References

A standard textbook introduction is chapter 2 of 

* {#Weibel} [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_.
 

A systematic discussion from the point of view of [[homotopy theory]] and [[derived categories]] is in chapter 7 of

* {#Schapira} [[Pierre Schapira]], _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 
* [[Masaki Kashiwara]], [[Pierre Schapira]], section 13 of _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006)

The above text is taken from

* [[Urs Schreiber]], _[[schreiber:HAI|Introduction to Homological Algebra]]_

[[!redirects derived functors in homological algebra]]

