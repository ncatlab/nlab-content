

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of [[adjoint triples]] generalized form [[adjoint functors]] to [[Quillen adjunctions]].

## Definition

+-- {: .num_defn #QuillenAdjointTriple}
###### Definition

Let $\mathcal{C}_1, \mathcal{C}_2, \mathcal{D}$ be [[model categories]], where $\mathcal{C}_1$ and $\mathcal{C}_2$ share the same underlying [[category]] $\mathcal{C}$, and such that the [[identity functor]] on $\mathcal{C}$ constitutes a [[Quillen equivalence]]

\[
  \label{EquivForQuillenAdjointTriple}
  \mathcal{C}_2 
    \underoverset
      {\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}}
      {\overset{ \phantom{AA}id\phantom{AA} }{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{C}_1
\]

Then 

1. a [[Quillen adjoint triple]] of the form

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
         \\
         \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
         \\
       }
     \mathcal{D}
   $$ 

   is a diagram in the [[double category of model categories]] of the form

   $$
     \array{
       && 
       \mathcal{C}_1
       &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_2
       \\
       && 
       {}^{\mathllap{ L }}\Big\downarrow 
       &{}^{\mathllap{\eta}}\swArrow&
       \Big\downarrow{}^{\mathrlap{id}}
       \\
       \mathcal{C}_2    
        &\overset{ \phantom{A}R\phantom{A} }{\longrightarrow}&
       \mathcal{D}
        &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{ id }}\Big\downarrow
       & {}^{\mathllap{\epsilon}}\swArrow &
       {}^{\mathllap{C}}
       \Big\downarrow
         &\swArrow_{\mathrlap{id}}& 
       \Big\downarrow{}^{ \mathrlap{ id } }
       \\
       \mathcal{C}_2
       &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}&
       \mathcal{C}_2
       &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
       \mathcal{C}_2
     }
   $$

   such that $\eta$ is the [[unit of an adjunction]] and $\epsilon$ the [[counit of an adjunction]], thus exhibiting [[Quillen adjunctions]] 

   $$
     \array{
       \mathcal{C}_1
         \underoverset
           {\underset{C}{\longleftarrow}}
           {\overset{L}{\longrightarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
       \\
       \\
       \mathcal{C}_2
         \underoverset
           {\underset{R}{\longrightarrow}}
           {\overset{C}{\longleftarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
     }
   $$

   and such that the [[derived natural transformation]] $Ho(id)$ of the bottom right square ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is invertible (a [[natural isomorphism]]);
   

1. a [[Quillen adjoint triple]] of the form

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
         \\
         \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
         \\
       }
     \mathcal{D}
   $$ 

   is a diagram in the [[double category of model categories]] of the form

   $$
     \array{
       \mathcal{C}_2
       &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
       \mathcal{C}_1   
       &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{id}}
       \Big\downarrow
         &{}^{ \mathllap{ id } }\swArrow& 
       \Big\downarrow{}^{ \mathrlap{ C } }
        & {}^{ \mathllap{\epsilon} }\swArrow &  
       \Big\downarrow{}^{\mathrlap{id}}
       \\
       \mathcal{C}_2
       &\underset{ \phantom{A}C\phantom{A} }{\longrightarrow}&
       \mathcal{D}
       &\underset{R}{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{id}}\Big\downarrow 
         &{}^{\mathllap{ \epsilon }}\swArrow& 
       \Big\downarrow{}^{\mathrlap{L}}
       \\
       \mathcal{C}_2
       &\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_2
     }
   $$

   such that $\eta$ is the [[unit of an adjunction]] and $\epsilon$ the [[counit of an adjunction]], thus exhibiting [[Quillen adjunctions]] 

   $$
     \array{
       \mathcal{C}_2
         \underoverset
           {\underset{C}{\longrightarrow}}
           {\overset{L}{\longleftarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
       \\
       \\
       \mathcal{C}_1
         \underoverset
           {\underset{R}{\longleftarrow}}
           {\overset{C}{\longrightarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
     }
   $$

   and such that the [[derived natural transformation]] $Ho(id)$ of the top left square square ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is invertible (a [[natural isomorphism]]).


If a Quillen adjoint triple of the first kind overlaps with one of the second kind

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L_1 \phantom{= A_a}}{\longrightarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C_1 = L_2}{\longleftarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{R_1 = C_2}{\longrightarrow}
         \\
         \overset{\phantom{A_a = } R_2}{\longleftarrow}
         \\
       }
     \mathcal{D}
   $$ 

we speak of a _Quillen [[adjoint quadruple]]_, and so forth.

=--

## Properties

### Derived adjoint triple

+-- {: .num_prop #QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}
###### Proposition
**([[Quillen adjoint triple]] induces [[adjoint triple]] of [[derived functors]] on [[homotopy category of a model category|homotopy categories]])**

Given a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}), the induced [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] form an ordinary [[adjoint triple]]:

$$
  \mathcal{C}_{1/2}
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAAA}
  Ho(\mathcal{C})
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}C \simeq \mathbb{R}C}{\longleftarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}
      \\
    }
  Ho(\mathcal{D})
$$ 

$\,$

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAAA}
  Ho(\mathcal{C})
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}C \simeq \mathbb{R}C}{\longleftarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}
      \\
    }
  Ho(\mathcal{D})
$$ 

=--

+-- {: .proof}
###### Proof

This follows immediately from the fact that passing to [[homotopy categories of model categories]] is a [[double pseudofunctor]] from the [[double category of model categories]] to the [[double category of squares]] in [[Cat]] ([this Prop.](double+category+of+model+categories#HomotopyDoublePseudofunctor)).

=--


### Derived adjoint modality
 {#DerivedAdjointModality}

We discuss how the [[derived functors]] of a [[simplicial Quillen adjunction|simplicial]] [[Quillen adjoint triple]] combine to a pair of derived modal operators (Prop. \ref{DerivedModalityFromQuillenAdjointTriple} below) which are adjoint in the sense of [[adjoint (∞,1)-functors]] (Prop. \ref{DerivedModalityFromQuillenAdjointTriple} below). Moreover, on suitably [[fibrant and cofibrant objects]] these derived modal operators are represented by the ordinary [[modal operators]] associated with the orinary [[adjoint triple]] (Lemma \ref{CompositeDerivedFunctorsOfQuillenAdjointTriple} and Lemma \ref{AltCompositeDerivedFunctorsOfQuillenAdjointTriple} below).



+-- {: .num_lemma #CompositeDerivedFunctorsOfQuillenAdjointTriple}
###### Lemma
**(composite [[derived functors]] of [[Quillen adjoint triple]])**

Consider a [[Quillen adjoint triple]]

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
    }
  \mathcal{D}
  \phantom{AA}\text{or}\phantom{AA}
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
    }
  \mathcal{D}
$$ 

and assume that $C$ is a left and right Quillen functor for both model structures $\mathcal{C}_1$, $\mathcal{C}_2$.

Then 

1. the composite [[derived functor]]

   $$
     \bigcirc_L
     \;\coloneqq\;
     \mathbb{R}C \circ \mathbb{L} L
   $$

   is equivalent to $\mathbb{L}(C \circ L)$, and under this identification the [[derived adjunction unit]] is given by the plain [[adjunction unit]] on [[cofibrant objects]];

1. the composite [[derived functor]]

   $$
     \Box_R 
     \;\coloneqq\;
     \mathbb{L} C\circ \mathbb{R} R
   $$

   is equivalent to $\mathbb{R}(C \circ R)$, and under this identification the [[derived adjunction counit]] is given by the plain [[adjunction counit]] on [[fibrant objects]]l;

1. on [[cofibrant objects]] the composite [[derived functor]] 

   $$
     \Box_L 
     \;\coloneqq\;
     \mathbb{L} L \circ \mathbb{R} C
   $$

   is equivalent to $\mathbb{R}(L \circ C)$, and under this identification the [[derived adjunction counit]] is given by the plain [[adjunction counit]] on [[cofibrant objects]];

1. on [[fibrant objects]] the composite [[derived functor]] 

   $$
     \bigcirc_R
       \;\coloneqq\; 
     \mathbb{R}_2 R \circ \mathbb{L}_2 C
     \;\;
   $$ 
   
   is equivalent to $\mathbb{L}_2( R \circ C )$, and under this identification the [[derived adjunction unit]] is given by the plain [[adjunction unit]] on [[fibrant objects]].

=--


+-- {: .proof}
###### Proof

In the first two cases, the assumption on $C$ means that it takes the resolution weak equivalence to a weak equivalence, so that it may be omitted, up to isomorphism in the [[homotopy category of a model category|homotopy category]].

In the second two cases, the assumption on $C$ implies that the result of applying $C$ is already (co-)fibrant in the relevant model structure, so that the following resolution morphism may be taken to be the identity morphism.

In the following we make this proof more explicit. We will denote [[cofibrant resolutions]] by

$$
  \emptyset 
    \underoverset{\phantom{A}\in Cof\phantom{A}}{i_X}{\longrightarrow} 
  Q X 
    \underoverset{\in W \cap Fib}{p_X}{\longrightarrow} 
  X
$$ 

and [[fibrant resolutions]] by 

$$
  X 
    \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} 
  P X 
    \underoverset{\phantom{A} \in Fib \phantom{A}}{q_X}{\longrightarrow} 
  \ast
$$ 

(as in [this Def.](geometry+of+physics+--+categories+and+toposes#FibrantCofibrantReplacementFunctorToHomotopyCategory)).

Consider the first claim, for the situation on the left.

A priori, the full derived functor is given by

$$
  \mathbb{R} C \circ \mathbb{L}_1L (c)
  \;=\;
  C P L Q_1 (c)
$$

The comparison morphism is

$$
  C L Q_1(c) \overset{ C (j_{L Q(c)}) }{\longrightarrow} C P L Q_1(c)
$$

where $j_{L Q(c)}$ exhibits [[fibrant resolution]] in $\mathcal{D}$ and hence is an [[acyclic cofibration]] in $\mathcal{D}$.

Therefore, since $C$ is also a left Quillen functor with respect to $\mathcal{C}_1$, the comparison morphism $C\left(j_{L Q(c)}\right)$ is an acyclic cofibration in $\mathcal{C}_1$, hence in particular a [[weak equivalence]] in $\mathcal{C}_1$. 

Since the [[derived adjunction unit]] on $Q_1(c)$ is the composition of the plain [[adjunction unit]] with this comparison morphism the claim follows.

For the second claim, for the situation on the left:

A priori, the full derived functor is given by

$$
  \mathbb{L}_2 C\circ \mathbb{R}_2 R (c)
  \;\simeq\;
  C Q R P_2 (c)
  \,.
$$

The comparison morphism is 

$$
  C Q R P_2 (c)
    \overset{ C\left( p_{R P_2(c)}  \right) }{\longrightarrow}
  C R P_2 (c)
$$

Here $p_{R P_2(c)}$ is an [[acyclic fibration]]  in $\mathcal{D}$. Since $C$ is also a [[right Quillen functor]] with respect to $\mathcal{C}_2$, the comparison morphism $C\left( p_{R P_2(c)} \right)$ is an [[acyclic fibration]] in $\mathcal{C}_1$, hence in particular a [[weak equivalence]] in $\mathcal{C}_2$. 

Since the [[derived adjunction counit]] on $P_2(c)$ is the composition of the plain [[adjunction counit]] with this comparison morphism the claim follows.

Consider the third claim, for the situation on the left:

A priori, the composite derived functor is

$$
  \mathbb{L} L \circ \mathbb{R} C (d)
  \;\simeq\;
  L Q_1  C P (d)
  \,.
$$

The comparison morphism is of the form

$$
  L Q_1  C P (d)  
    \overset{ L((p_1)_{C P (d)}) }{\longrightarrow}
  L C P (d)  
  \,.
$$

But since $d$ is assumed to be cofibrant, so is $P(d)$ and since $C$ is assumed to be left Quillen for $\mathcal{C}_1$, also $C P(d)$ is cofibrant in $\mathcal{C}_1$. Therefore the comparison morphism may be taken to be the identity.

Consider the fourth claim, for the situation on the left:

A priori, the composite derived functor is

$$
  \mathbb{R} R\circ \mathbb{L} C (d)
  \;\simeq\;
  R P_2 C Q (d)
$$

The comparison morphism is

$$
  R C Q (d)
    \overset{ R\left( (j_2)_{C Q (d)} \right) }{\longrightarrow}
  R P_2 C Q (d)
  \,.
$$

But since $d$ is assumed to be fibrant, and since $C$ is assumed to be right Quillen with respect to $\mathbb{C}_2$, also $C Q (d)$ is fibrant in $\mathcal{C}_2$, and hence we may take the comparison morphism to be the identity.

Consider the first claim, for the siuation on the right:

A priori, the composite derived functor is

$$
  \mathbb{R}C  \circ \mathbb{L}L (d)
  \;\simeq\;
  C P_2 L Q(d)
  \,.
$$

The comparison morphism is

$$
  C L Q(d)
    \overset{ C\left( (j_2)_{L Q(d)} \right) }{\longrightarrow}
  C P_2 L Q(d)
$$

where $(j_2)_{L Q(d)}$ is an [[acyclic cofibration]] in $\mathcal{C}_2$. But since $C$ is assumed to be a left Quillen functor with respect to $\mathcal{C}_2$, also the comparison morphism is an acyclic cofibration in $\mathcal{C}_2$, hence in particular a weak equivalence.

And so forth.

=--



+-- {: .num_prop #DerivedModalityFromQuillenAdjointTriple}
###### Proposition
**(derived modality from Quillen adjoint triple)**


Consider a [[simplicial Quillen adjunction|simplicial]] [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAA}
  \text{or}
  \phantom{AA}
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
      \\
    }
  \mathcal{D}
$$ 

such that the functor $C$ is left and right Quillen with respect to both $\mathcal{C}_1$ and $\mathcal{C}_2$.

1. If $C$ is a [[fully faithful functor]], consider the composite [[derived functors]]

   $$
     \bigcirc_L \;\coloneqq\;
     \mathbb{R} C \circ \mathbb{L} L
     \phantom{AAA}
     \Box_R \;\coloneqq\;
     \mathbb{L} C \circ \mathbb{R} R
   $$

   Then for every [[fibrant and cofibrant object]] $Y$ we have: 

   1. the map on [[derived hom-spaces]] given by precomposition with the [[derived adjunction unit]]

      $$
        \mathbb{R}hom(\bigcirc_L X, C Y)
        \longrightarrow 
        \mathbb{R}hom( X, C Y ) 
      $$

      is a [[weak equivalence]] in the [[classical model structure on simplicial sets]] $sSet_{Qu}$;


   1. the map on [[derived hom-functors]] given by postcomposition with the [[derived adjunction counit]]

      $$
        \mathbb{R}hom( C Y, X ) 
         \longrightarrow
        \mathbb{R}hom(C Y, \Box_R X)
      $$

      is a [[weak equivalence]] in the [[classical model structure on simplicial sets]] $sSet_{Qu}$.

1. If $L$ and $R$ are [[fully faithful functors]] write


   $$
     \Box_L \;\coloneqq\;
     \mathbb{L} L\circ \mathbb{R} C
     \phantom{AAA}
     \bigcirc_R \;\coloneqq\;
     \mathbb{R} R \circ \mathbb{L} C
   $$

   for the composite derived functors

   Then for every [[fibrant and cofibrant object]] $Y$ we have: 

   1. the map on [[derived hom-spaces]] given by precomposition with the [[derived adjunction unit]]

      $$
        \mathbb{R}hom(\bigcirc_R X, C Y)
        \longrightarrow 
        \mathbb{R}hom( X, C Y) 
      $$

      is a [[weak equivalence]] in the [[classical model structure on simplicial sets]] $sSet_{Qu}$;


   1. the map on [[derived hom-spaces]] given by postcomposition with the [[derived adjunction counit]]

      $$
        \mathbb{R}hom( C Y, X ) 
         \longrightarrow
        \mathbb{R}hom(C Y, \Box_L X)
      $$

      is a [[weak equivalence]] in the [[classical model structure on simplicial sets]] $sSet_{Qu}$.


=--

+-- {: .proof}
###### Proof


By Lemma \ref{CompositeDerivedFunctorsOfQuillenAdjointTriple}, the [[derived adjunction unit|derived adjunction (co-)unit]] in each case is the plain [[adjunction unit|adjunction (co-)unit]], up to weak equivalence. Hence the statement follows with the corresponding statement for (co-)reflective subcategories.

=--

+-- {: .num_prop}
###### Proposition
**(derived adjoint modality from Quillen adjoint triple)**

Given [[simplicial model category|simplicial]] [[Quillen adjoint triples]]

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAA}\text{or}\phantom{AAA}
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
      \\
    }
  \mathcal{D}
$$ 

such that $C$ is a left and right Quillen functor with respect to both model category structures $\mathcal{C}_{1,2}$, then
the composite [[derived functors]] 

$$
  \bigcirc \;\coloneqq\;
  \mathbb{R}_1 C \circ \mathbb{L}_1 L
  \phantom{AAA}
  \Box \;\coloneqq\;
  \mathbb{L}_2 C \circ \mathbb{R}_2 R
$$

satisfy the hom-equivalence of a pair of [[adjoint (∞,1)-functors]] $\bigcirc \dashv \Box$ with respect to the [[derived hom-functor]], in that for all $X,Y$ in the [[homotopy category of a model category|homotopy category]] there is a [[weak equivalence]]

$$
  \mathbb{R}hom( \bigcirc X, Y )
  \overset{\in W}{\longrightarrow}
  \mathbb{R}hom( X, \Box Y )
  \,.
$$

Similarly, for a [[Quillen adjoint triple]] of the form

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
      \\
    }
  \mathcal{D}
$$

the composite [[derived functors]] from Prop. \ref{DerivedModalityFromQuillenAdjointTriple} 

satisfy

$$
  \mathbb{R}hom( \Box_L X, Y )
  \overset{\in W}{\longrightarrow}
  \mathbb{R}hom( X, \bigcirc_R Y )
  \,,
  \phantom{AAAA}
  \,.
  \mathbb{R}hom( \bigcirc_L X, Y )
  \overset{\in W}{\longrightarrow}
  \mathbb{R}hom( X, \Box_R Y )
  \,.
$$

=--

+-- {: .proof}
###### Proof

In the cases where $X$ and $Y$ are objects of $Ho(\mathcal{D})$ choose [[fibrant and cofibrant objects|fibrant and cofibrant]] representatives in $\mathcal{D}$, which we denote by the same symbols. 

In the cases where $X,Y$ are objects of $\mathcal{C}$, choose $X$ to be a [[fibrant and cofibrant object]] with respect to $\mathcal{C}_1$ and $Y$ a [[fibrant and cofibrant object]] with respect to $\mathcal{C}_2$.

Then by Lemma \ref{CompositeDerivedFunctorsOfQuillenAdjointTriple}, in each case the derived [[modal operators]] are represented on these objects by the ordinary modal operators.

We discuss the first case, with the Quillen adjoint triple on the left. The other cases are directly analogous.

Let $X$ be a [[fibrant and cofibrant object|fibrant and cofibrant]] representative in $\mathcal{C}_1$ and $Y$ be [[fibrant and cofibrant object|
fibrant and cofibrant]] representative in $\mathcal{C}_2$. By lemma \ref{CompositeDerivedFunctorsOfQuillenAdjointTriple}, on these the derived modal operators are represented by the plain [[modal operators]]

$$
  \bigcirc X \simeq C L X
  \,,
  \phantom{AA}
  \Box Y \simeq C R Y
  \;\;\in\;
  Ho(\mathcal{C})
  \,.
$$

Moreover,

1. $C L X$ is cofibrant in $\mathcal{C}_1$, and hence also in $\mathcal{C}_2$;

1. $C R Y$ is fibrant in $\mathcal{C}_2$ and hence in $\mathcal{C}_1$ 

where we used (eq:EquivForQuillenAdjointTriple).

This means that the [[derived hom-functor]], computed either with respect to $\mathcal{C}_1$ or $\mathcal{C}_2$, is given on these objects, up to weak equivalence, by the ordinary [[sSet]]-[[enriched hom-functor]] 

$$
  \mathcal{C}(-,-)
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow
  sSet
$$

Hence using the adjunction hom-isomorphisms for the ordinart [[enriched adjunctions]] $(L \dashv C \dashv R)$ we obtain the following sequences of [[weak homotopy equivalences]]:

$$
  \begin{aligned}
    \mathbb{R}hom( \bigcirc X, Y )
    & \simeq_W
    \mathcal{C}( C L X, Y )
    \\
    & \simeq_{\phantom{W}}
    \mathcal{C}( X, C R Y )
    \\
    & \simeq_W
    \mathbb{R}hom(X, \Box Y)
  \end{aligned}
$$

=--


## Examples 

### Homotopy (co-)limits

+-- {: .num_example #HomotopyLimitQuillenAdjointTriple}
###### Example
**([[Quillen adjoint triple]] of [[homotopy limits]]/[[homotopy colimits|colimits]] of [[simplicial sets]])**

Let $\mathcal{C}$ be a [[small category]], and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$ for the projective/injective [[model structure on simplicial presheaves]] over $\mathcal{C}$, which participate in a [[Quillen equivalence]] of the form 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$

(by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModelCategoriesOfSimplicialPresheaves)).

Moreover, the [[constant functor|constant diagram]]-assigning functor

$$
  [\mathcal{C}^{op}, sSet] \overset{const}{\longleftarrow} sSet
$$

is clearly a [[left Quillen functor]] for the injective model structure, and a [[right Quillen functor]] for the projective model structure.

Together this means that in the [[double category of model categories]] we have a [[2-morphism]] of the form

$$
  \array{
    sSet_{Qu}
      &\overset{const}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{const}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

Moreover, the [[derived natural transformation]] $Ho(id)$ of this square is invertible, if for every [[Kan complex]] $X$

$$
  Q const X
    \overset{}{\longrightarrow}
  const X
    \longrightarrow
  P const X  
$$ 

is a [[weak homotopy equivalence]] (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)), which here is trivially the case.

Therefore we have a Quillen adjoint triple of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\underset{\longrightarrow}{\lim}}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{const}{\longleftarrow}
      \\
      \overset{\underset{\longleftarrow}{\lim}}{\longrightarrow}
      \\
    }
  sSet_{Qu}
$$ 

witnessed by the following diagram in the [[double category of model categories]]

$$
  \array{
    && 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}    
    \\
    && 
    {}^{\mathllap{ \underset{\longrightarrow}{\lim} }}\Big\downarrow 
    &{}^{\mathllap{\eta}}\swArrow&
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}    
     &\overset{ \phantom{A}\underset{\longleftarrow}{\lim}\phantom{A} }{\longrightarrow}&
    sSet_{Qu}
      &\overset{\phantom{A}const\phantom{A}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{ id }}\Big\downarrow
    & {}^{\mathllap{\epsilon}}\swArrow &
    {}^{\mathllap{const}}
    \big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

The induced [[adjoint triple]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) is the [[homotopy colimit]]/[[homotopy limit]] adjoint triple

$$
  Ho([\mathcal{C}^{op}, sSet])
  \;
    \array{
       \overset{\phantom{AA}\mathbb{L}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
       \\
       \overset{\phantom{AA}const\phantom{AA}}{\longleftarrow}
       \\
       \overset{\phantom{AA}\mathbb{R}\underset{\longleftarrow}{\lim}\phantom{AA}}{\longrightarrow}
    }
  \;
  Ho(sSet)
$$ 

=--


+-- {: .num_example #QuillenAdjointQuadrupleOverSiteWithTerminalObject}
###### Example
**([[homotopy limit|limit]]/[[homotopy colimit|colimit]] [[Quillen adjoint quadruple]] over [[site]] with [[terminal object]])**

If $\mathcal{C}$ has a [[terminal object]] $\ast \in \mathcal{C}$, then 

$$
  \underset{\longleftarrow}{\lim}
  = \Gamma
  \;\colon\;
  [\mathcal{C}^{op}, sSet]
  \longrightarrow
  sSet
$$

is given by evaluation on that terminal object

$$
  \Gamma(\mathbf{X}) \coloneqq \mathbf{X}(\ast)  
$$

and this operation has a further [[right adjoint]]

$$
  coconst \;\colon\; sSet \longrightarrow [\mathcal{C}^{op}, sSet]
$$

given by [[right Kan extension]] along the terminal object inclusion.

Hence in this case $\underset{\longleftarrow}{\lim} =\Gamma$ is also a [[left Quillen functor]] on the projective model structure (using that $id : [\mathcal{C}^{op}, sSet_{Qu}]_{proj} \to [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$ is also left Quillen, as above) and hence we get a further Quillen adjoint triple

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj/proj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{const}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\underset{\longleftarrow}{\lim}=\Gamma}{\longrightarrow}
      \\
      \overset{coconst}{\longleftarrow}
      \\
    }
  sSet_{Qu}
$$ 
 
witnessed by the following diagram in the [[double category of model categories]]


$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}   
    &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{id}}
    \Big\downarrow
      &{}^{ \mathllap{ id } }\swArrow& 
    \Big\downarrow{}^{ \mathrlap{ \underset{\longleftarrow}{\lim}=\Gamma } }
      & {}^{ \mathllap{\epsilon} }\swArrow &
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{A}\underset{\longleftarrow}{\lim}=\Gamma\phantom{A} }{\longrightarrow}&
    sSet_{Qu}
    &\underset{coconst}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{id}}\Big\downarrow 
      &{}^{\mathllap{ \epsilon }}\swArrow& 
    \Big\downarrow{}^{\mathrlap{const}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$


Moreover, the [[derived natural transformation]] $Ho(id)$ of the top left square is invertible, if for every injectively fibrant simplicial presheaf $\mathbf{X}$ the composite

$$
  \Gamma Q_{inj} \mathbf{X}
    \overset{}{\longrightarrow}
  \Gamma \mathbf{X}
    \longrightarrow
  \Gamma P_{proj} \mathbf{X}  
$$ 

is a [[weak equivalence]] (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)), which here is trivially the case.


Hence in this case we have a [[Quillen adjoint quadruple]]


$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\phantom{AA}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\phantom{AA}const\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{ \phantom{AA}\underset{\longleftarrow}{\lim}\phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{A}coconst\phantom{A} }{\longleftarrow}
      \\
    }
  sSet_{Qu}
$$ 

witnessing the [[model topos]] over a [[site]] with [[terminal object]] as being [[cohesive (infinity,1)-topos|cohesive]].

=--

### Homotopy Kan extension

More generally:

+-- {: .num_example #QuillenAdjointTripleHomotopyKanExtension}
###### Example
**([[Quillen adjoint triple]] of [[homotopy Kan extension]] of [[simplicial presheaves]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]], and let 

$$
  \mathcal{C}
    \overset{\phantom{AA}F\phantom{AA}}{\longrightarrow}
  \mathcal{D}
$$

be a [[functor]] between them. By [[Kan extension]] this induces an [[adjoint triple]] between [[categories of simplicial presheaves]]:

$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot}{ \phantom{AA}F_!\phantom{AA}  }{\longrightarrow}
      \\
      \underoverset{\bot}{ \phantom{AA}F^\ast\phantom{AA}  }{\longleftarrow}
      \\
      \overset{ \phantom{AA}F_\ast\phantom{AA}  }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

where 

$$
  F^\ast \mathbf{X}
  \;\coloneqq\;
  \mathbf{X}(F(-))
$$

is the operation of precomposition with $F$. This means that $F^\ast$ preserves all objectwise cofibrations/fibrations/weak equivalences. Hence it is 

1. a [[right Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$;

1. a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$;

and since $[\mathcal{D}^{op}, sSet]_{proj} \overset{id}{\to} [\mathcal{D}^{op}, sSet]_{inj}$ is also a left Quillen functor, the second point implies that $F^\ast$ is also 

* a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$.

In summary this means that we have a [[2-morphism]] in the [[double category of model categories]] of the following form:

$$
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
      &\overset{\phantom{AA}F^\ast\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{F^\ast}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

To check that the corresponding [[derived natural transformation]] $Ho(id)$ is a [[natural isomorphism]], we need to check (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)) that the composites


$$
  Q_{inj} F^\ast \mathbf{X}
    \overset{ p_{F^\ast \mathbf{X}} }{\longrightarrow}
  F^\ast \mathbf{X}
    \overset{ j_{F^\ast \mathbf{X}} }{\longrightarrow}
  P_{proj} F^\ast \mathbf{X}  
$$ 

are invertible in the [[homotopy category of a model category|homotopy category]] $Ho([\mathcal{C}^{op}, sSet_{Qu}]_{inj})$, for all projectively fibrant-cofibrant simplicial presheaves $\mathbf{X}$. But this is immediate, since the two factors are weak equivalences, by definition of [[fibrant resolution|fibrant/cofibrant resolution]].

Hence we have a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$

The corresponding derived [[adjoint triple]] on [[homotopy category of a model category|homotopy categories]] (Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}) is that of _[[homotopy Kan extension]]_:


$$
  Ho([\mathcal{C}^{op}, sSet])
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ \phantom{A}\mathbb{L}F_! \phantom{\simeq A_a}\phantom{A}  }{\longrightarrow}
      \\
      \underoverset{\phantom{\simeq A_a} \bot}{ \phantom{A}\mathbb{R}F^\ast \simeq \mathbb{L}F^\ast\phantom{A}  }{\longleftarrow}
      \\
      \overset{ \phantom{A} \phantom{A_a \simeq} \mathbb{R}F_\ast\phantom{A}  }{\longrightarrow}
    }
  Ho([\mathcal{D}^{op}, sSet])
$$

=--

+-- {: .num_example #QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair}
###### Example
**([[Quillen adjoint quadruple]] of [[homotopy Kan extension]] of [[simplicial presheaves]] along [[adjoint pair]])**

Now let 

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA}R\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longrightarrow}}
      {\bot}
  \mathcal{D}
$$

be a [[adjoint pair|pair]] of [[adjoint functors]]. By [[Kan extension]] this induces an [[adjoint quadruple]] between [[categories of simplicial presheaves]]

$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ L_! \phantom{\simeq A_a} }{\longrightarrow}
      \\
      \underoverset{\bot \phantom{\simeq} \bot }{ L^\ast \simeq R_! }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot}{ L_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq } R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

By the previous example the top three of these form a [[Quillen adjoint triple]]. To see that the bottom three form another, compatible [[Quillen adjoint triple]], we need to show that the following is a [[2-morphism]] in the [[double category of model categories]]:

$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}   
    \\
    {}^{\mathllap{id}}
    \Big\downarrow
      &{}^{ \mathllap{ id } }\swArrow& 
    \Big\downarrow{}^{ R^\ast }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{AA}R^\ast\phantom{AA} }{\longrightarrow}&
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  }
$$

But since $R^\ast \mathbf{X} = \mathbf{X}(R(-))$ is given by precomposition, this functor preserves all object-wise cofibrations/fibrations weak equivalences, and hence is

1. a [[left Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{inj}$;

1. a [[right Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{proj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{proj}$;

But since also $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{id}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$ is a right Quillen functor, the second point implies that $R^\ast$ is also 

1. a [[right Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{proj}$.

This demonstrates the above square.

Finally to check its [[derived natural transformation]] $Ho(id)$ is 
invertible: By [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos) this is equivalent, in the present situation, to the condition that for each simplical presheaf $\mathbf{X}$ that is both fibrant and cofibrant, the composite

$$
  R^\ast Q \mathbf{X}
    \overset{ R^\ast p_{\mathbf{X}} }{\longrightarrow}
  R^\ast \mathbf{X}
    \overset{ R^\ast j_{\mathbf{X}} }{\longrightarrow}
  R^\ast P \mathbf{X} 
$$ 

is a weak equivalence. But we have already seen that $R^\ast$ preserves all weak equivalences, hence this is the case. (In fact, since $\mathbf{X}$ is already fibrant and cofibrant, both the [[fibrant resolution]] morphism $j_{\mathbf{X}}$ as well as the [[cofibrant resolution]] morphism $p_{\mathbf{X}}$ may be taken to be [[identity morphisms]].)


Hence, in conclusion, we have a [[Quillen adjoint quadruple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ L_! \phantom{\simeq A_a} }{\longrightarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ L^\ast \simeq R_! }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ L_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq } R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]_{proj}
$$

Notice that the bottom adjoint triple $R_! \dashv R^\ast \dashv R_{\ast}$ is now realized differently by [[Quillen functors]] than in what results by applying Example \ref{QuillenAdjointTripleHomotopyKanExtension} to $R$: Here $R_!$ is regarded, in particular, as a [[right Quillen functor]] between the projective model structures, while in the second case it is regarded as a [[left Quillen functor]] between the projective model structures.
But by [this Example](double+category+of+model+categories#DerivedFunctorOfLeftRightQuillenFunctor) this does not affect the [[derived functor]] of $R_!$, up to [[natural isomorphism]]:

$$
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
      &\overset{\phantom{A}R_! \simeq L^\ast\phantom{A}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{R_! \simeq L^\ast}}\Big\downarrow 
      &{}^{id}\swArrow& 
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
      &\underset{\phantom{A}id\phantom{A}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
  }
  \phantom{AAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAA}
  \mathbb{R}_{proj,proj}R_! \simeq \mathbb{L}_{proj,proj} R_!
$$

Hence by essential uniqueness of adjoints ([this prop](adjoint}functor#UniquenessOfAdjoints)) also the derived functors of $R^\ast$ and of $R_\ast$ agree, up to natural isomorphism, for both ways of regarding it. 

=--

## Related concepts

* [[adjoint triple]]

* [[adjoint quadruple]]

[[!redirects Quillen adjoint triples]]

[[!redirects Quillen adjoint quadruple]]
[[!redirects Quillen adjoint quadruples]]

