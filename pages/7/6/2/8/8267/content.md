
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _salamander lemma_ is a fundamental [[lemma]] in [[homological algebra]] providing information on the relation between [[homology groups]] at different positions in a [[double complex]]. 

By a simple consequence illustrated in remark \ref{ExtramuralMapsAsDiagonals} below, all the standard [[diagram chasing lemmas]] of [[homological algebra]] are direct and transparent consequences of the salamander lemma, such as the [[3x3 lemma]], the [[four lemma]], hence the [[five lemma]], the [[snake lemma]], and also the [[long exact sequence in cohomology]] corresponding to a [[short exact sequence]].

These lemmas are all classical, but their traditional [[proofs]] are, while elementary, not very illuminating. The Salamander lemma serves to make the mechanism behind these lemmas more transparent and also to make evident a host of further lemmas of this kind not traditionally considered, such as an [nxn lemma](#nxnLemma) for all $n \in \mathbb{N}$.


## The Salamander lemma
 {#TheSalamanderLemma}

The Salamander lemma, prop. \ref{SalamanderLemma} below, is a statement about the [[exact sequence|exactness]] of a sequence naturally associated with any [[morphism]] in a [[double complex]]. In the _[Preliminaries](#Preliminaries)_ we first introduce this sequence itself.


### Preliminaries
 {#Preliminaries}


+-- {: .num_remark}
###### Remark
**(general assumption/convention)**

As always in [[homological algebra]], when we consider _[[elements]]_ of [[objects]] in the ambient [[abelian category]] $\mathcal{A}$ it is either assumed that $\mathcal{A}$ is of the form $R$[[Mod]] for some [[ring]] $R$, or that one of the _[embedding theorems](abelian+category#EmbeddingTheorems)_ has been used to embed it into such, by a [[faithful functor|faithful]] and [[exact functor]], so that these elements are actual elements of the [[sets]] underlying these [[modules]].

In the following, many of the [[proofs]] are spelled out in terms of elements this way, and we will not always repeat this assumption. This should help to amplify how utterly elementary the salamander lemma is. But explicitly element-free/general abstract proofs can of course be given without much more effort, too, see [Wise](#Wise).

=--

+-- {: .num_defn #DonorReceptor}
###### Definition

Let  $A_{\bullet \bullet}$ be a [[double complex]] in some [[abelian category]] $\mathcal{A}$, hence a [[chain complex]] of chain complexes $A_{\bullet, \bullet} \in Ch_\bullet(Ch_\bullet(\mathcal{A}))$, hence a [[diagram]] of the form

$$
  \array{
   && \vdots && \vdots
   \\
   & & \downarrow^{\mathrlap{\partial^{vert}}} && \downarrow^{\mathrlap{\partial^{vert}}}
   \\
    \cdots &\to & 
    A_{n,m} &\stackrel{\partial^{hor}}{\to}& A_{n-1,m}
    & \to & \cdots
   \\
   & & \downarrow^{\mathrlap{\partial^{vert}}} && \downarrow^{\mathrlap{\partial^{vert}}}
   \\
    \cdots &\to & 
    A_{n,m-1} &\stackrel{\partial^{hor}}{\to}& A_{n-1,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{\mathrlap{\partial^{vert}}} && \downarrow^{\mathrlap{\partial^{vert}}}
   \\
   && \vdots && \vdots
  }
$$

where $\partial^{hor} \circ \partial^{hor} = 0$, where $\partial^{vert} \circ \partial^{vert} = 0$ and where all squares [[commuting diagram|commute]], $\partial^{hor} \circ \partial^{vert} = \partial^{vert} \circ \partial^{hor}$.

Let $A \coloneqq A_{k l}$ be any [[object]] in the double complex at any position $(k,l)$. This is the [[source]] and [[target]] of horizontal, vertical and diagonal (unique composite of a horizontal and a vertical) [[morphisms]] to be denoted as follows:

$$
  \array{
     ^\mathllap{\partial_{in}^{diag}} \searrow
     & \downarrow^{\mathrlap{\partial_{in}^{vert}}}
     \\
     \stackrel{\partial_{in}^{hor}}{\to} & A &
     \stackrel{\partial_{out}^{hor}}{\to} 
     \\
     & ^\mathllap{\partial_{out}^{vert}} \downarrow
     &
     \searrow^{\mathrlap{\partial_{out}^{diag}}}
  }
  \,.
$$

Define

* $A^{hor} \coloneqq ker (\partial^{hor}_{out}) / im (\partial^{hor}_{in}) \in \mathcal{A}$ -- the horizontal [[chain homology]] at $X$;

* $A^{vert} \coloneqq ker (\partial^{vert}_{out}) / im (\partial^{vert}_{in}) \in \mathcal{A}$ -- the vertical [[chain homology]] at $X$;

* ${}^{\Box}A \coloneqq \frac{ker (\partial^{hor}_{out}) \cap ker(\partial^{vert}_{out})}{im(\partial^{diag}_{in})} \in \mathcal{A}$ -- the "receptor" at $A$;

* $A_{\Box}\coloneqq \frac{ker (\partial^{diag}_{out}) }{ im(\partial^{hor}_{in}) + im(\partial^{vert}_{in})}$ -- the "donor" at $A$;

where 

* $ker(-)$ denotes the [[kernel]] of a map, 

* $im(-)$ the [[image]] of a map, 

* $\frac{N_1}{N_2}$ the [[quotient module]] of the module $N_1$ by a [[submodule]] $N_2 \hookrightarrow N_1$,

*  $N_1 + N_2$ the sum of two submodules (i.e., their [[join]] in the [[lattice]] of submodules under inclusion). 

=--

+-- {: .num_lemma #Intramural}
###### Lemma

The [[identity]] on representatives in $A$ induces a [[commuting diagram]] of [[homomorphisms]] from the donor of $A$ to the receptor of $A$, def. \ref{DonorReceptor}, via the horizontal and vertical [[homology groups]] at $A$:

$$
  \array{
    && {}^\Box A
    \\
    & \swarrow && \searrow
    \\
    A^{vert} &&&& A^{hor}
    \\
    & \searrow && \swarrow
    \\
    && A_\Box
    \,.
  }
$$

These morphisms are to be called the **intramural maps** of $A$.

=--

This is immediate, here is one way to make it fully explicit:

+-- {: .proof}
###### Proof

The statement that the top two morphisms exist and are given by the identity on representatives is that if $[a] \in {}^\Box A$ is represented by $a \in A$, then $a$ also represents an element in $A^{hor}$ and $A^{vert}$.
But this is the very definition of ${}^\Box A$: being a [[quotient module]] of $ker(\partial^{vert}_{out}) \cap ker(\partial^{hor}_{out})$ means that its elements are represented by elements of $A$ that are annihiliated by both $\partial^{vert}_{out}$ and $\partial^{hor}_{out}$. Moreover if $[a] \in {}^\Box A$ is 0 then $a$ also represents the 0-element in $A^{hor}$ and in $A^{vert}$, because by definition of ${}^\Box A$ it is then in the [[image]] of $\partial^{hor} \circ \partial^{vert} = \partial^{vert} \circ \partial^{hor}$. Moreover it is clear that everything respects addition of module elements and the [[action]] by the ring $R$, hence the top morphisms are well defined [[module]] [[homomorphisms]].

Similarily the bottom two morphisms exist and are given by the identity on representatives by the very definition of $A_{\Box}$: this being a quotient of the kernel of $\partial^{vert} \partial^{hor} = \partial^{hor} \partial^{vert}$ it contains in particular the elements that are represented in $A$ by elements in the kernel of $\partial^{hor}$ and in the kernel of of $\partial^{vert}$ separately. And if $[a]$ is the 0-element in $A^{hor}$ or $A^{vert}$ then $a$ is in the image of $\partial^{hor}$ or of $\partial^{vert}$, respectively, and since these two images are quotiented out to obtain $A_{\Box}$, such $a$ also represent the 0-element there.

=--

+-- {: .num_remark }
###### Remark


In lemma \ref{Intramural} "intramural" is meant to allude to the fact that these morphisms go between objects that all come from $A$ and hence remain "in the context of $A$". The "extramural" maps to follow in lemma \ref{Extramural} below instead go from objects associated to some $A$ to objects associated to some $B$, so they go "out of the context of $A$".

=--

+-- {: .num_lemma #Extramural}
###### Lemma

Any vertical or horizontal morphism $\partial : A \to B$ in the double complex induces a homomorphism

$$
  A_\Box \to {}^\Box B
$$

from the donor of $A$ to the receptor of $B$, def. \ref{DonorReceptor}, called the **extramural map** associated with $\partial$. 


=--

Again this is immediate, here is one way to make it explicit:

+-- {: .proof}
###### Proof

We discuss the case that $\partial = \partial^{hor}$ is a horizontal [[differential]]. The other case works verbatim the same way, only with the roles of $\partial^{hor}$ and $\partial^{vert}$ interchanged.

By definition \ref{DonorReceptor}, an $[a] \in A_{\Box}$ is represented by an $a \in A$ for which $\partial^{vert}\partial^{hor} a = 0$. The claim is that $\partial^{hor} a$ then represents an element in ${}^{\Box}B$ such that this is a module homomorphism.

*  We have $\partial^{vert} (\partial^{hor} a) = 0$ by assumption on $a$ and $\partial^{hor} (\partial^{hor} a) = 0$ by the chain complex property. Hence $\partial^{hor} a$ represents an element in ${}^{\Box} B$.

* If $[a] = 0$ then there is $c$ such that $a = \partial^{hor} c$ or $d$ such that $a = \partial^{vert} d$. In the first case the chain complex property gives that $\partial^{hor}a = \partial^{hor}\partial^{hor}c = 0$ and hence $[\partial^{hor} a] = 0$ in ${}^\Box B$, in the second $\partial^{hor}a = \partial^{hor}\partial^{vert} d$ which is also 0 in ${}^\Box B$ since this is the quotient by $im(\partial^{hor} \partial^{vert})$. 

=--

+-- {: .num_remark #ExtramuralMapsAsDiagonals}
###### Remark
**(central idea on diagram chasing)**

It is useful in computations, such as those shown below in _[Implications - The diagram chasing lemmas](#Implications)_, to draw the extramural morphisms of lemma \ref{Extramural} as follows.

1. For a horizontal $\partial^{hor} \colon A \to B$ we draw the induced extramural map as

   $$   
     \array{   
        &&& \Box
        \\
        A && \nearrow & & B
        \\
        & \Box
     }
     \,.
   $$

1. For a vertical $\partial^{vert} \colon A \to B$ we draw the induced extramural map as

   $$
     \array{
       & A
       \\
       && \Box
       \\
       & \swarrow
       \\
       \Box
       \\
       & B
     }
   $$

This notation makes it manifest that in every [[double complex]] $X_{\bullet, \bullet}$ the extramural maps form long diagonal [[zigzags]] between donors and receptors

$$   
  \array{   
     && &&&&&&&& \udots
     \\
     && &&&&& X_{k, l+1} && \nearrow
     \\
     && &&&&&& \Box
     \\
     && &&&&& \swarrow
     \\
     && &&&& \Box
     \\
     && &X_{k+1,l} && \nearrow & & X_{k,l}
     \\
     && && \Box
     \\
     && &\swarrow
     \\
     && \Box
     \\
     & \nearrow & & X_{k+1, l-1}
     \\
     \udots
  }
  \,.
$$

But moreover, the intramural maps relate the donors and receptors in particular at the far end of these zigzags back to the actual homology groups of interest:

$$   
  \array{   
     && && && &&&&&&&& & \Box
     \\
     && && && &&&&&            &&           & \udots && B
     \\
     && && && &&&&& X_{k, l+1} && \nearrow  &        &&    & \searrow
     \\
     && && && &&&&&            & \Box      &&        &&    & & B^{hor}
     \\
     && & & && &&&&& \swarrow
     \\
     && & & && &&&& \Box
     \\
     && & & && &X_{k+1,l} && \nearrow & & X_{k,l}
     \\
     && & & && && \Box
     \\
     && & & && &\swarrow
     \\
     A^{hor} && & & && \Box
     \\
     &\searrow & & & & \nearrow & & X_{k+1, l-1}
     \\
     && A & & \udots
     \\
     && & \Box
  }
  \,.
$$

This means that in order to get "far diagonal identifications" of homology groups in a double complex, all one needs is sufficient conditions that all the intramural and extramural maps in a "long salamander" like this are [[isomorphisms]].

These turn out to be certain exactness conditions to be checked/imposed locally at each of the positions involved in a long salamander like this discussed in  _[Intramural and extramural isomorphism](#IntraExtramuralIsomorphisms)_ below. 
All the long diagonal identifications of the standard [[diagram chasing lemmas]] follows by piecing together such long salamanders. This is discussed in the  _[Implications](#Implications)_ below.


=--

+-- {: .num_remark #OmittingIntramuralMaps}
###### Remark

Moreover, it is useful to combine the extramural notation of remark \ref{ExtramuralMapsAsDiagonals} with the evident diagonal notation for the intramural maps, lemma \ref{Intramural}, which allow extramural maps to "enter at the receptor" and "exit at the donor" of a given entry in the double complex. Together these two notations yield for every piece of a [[double complex]] of the form

$$
  \array{
    C 
    \\
    \downarrow^{\mathrlap{\partial^{vert}}}
    \\
    A &\stackrel{\partial^{hor}}{\to}& B
    \\
    && \downarrow^{\mathrlap{\partial^{vert}}}
    \\
    && D
  }
$$

the **salamander**-shaped diagrams of mural maps

$$
  \array{
      & C
      \\
      && \Box
      \\
      & \swarrow
      \\
      \Box &&& & \Box
      \\
      & A && \nearrow & & B
      \\
      && \Box & && & \Box
      \\
      &&&&& \swarrow
      \\
      &&&& \Box
      \\
      &&&&& D
  }
  \,.
$$

These give the salamander lemma, prop. \ref{SalamanderLemma} below, its name. 

=--

+-- {: .num_lemma}
###### Lemma

For $\partial^{hor} : A \to B$ any horizontal morphism in the double complex, the canonically induced morphism $A^{vert} \to B^{vert}$ on vertical homology is the composite of the above intramural and extramural maps:

$$
  A^{vert} \to A_{\Box} \to {}^\Box B \to B^{vert}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the above, on representatives the first map is the identity, the second is $\partial^{hor}$ and the third again the identity. Hence the total map is given on representative by $\partial^{hor}$. 

=--


### Statement 

+-- {: .num_prop #SalamanderLemma}
###### Proposition
**(Salamander lemma)**

If a [[diagram]]

$$
  \array{
    C 
    \\
    \downarrow^{\mathrlap{\partial^{vert}}}
    \\
    A &\stackrel{\partial^{hor}}{\to}& B
    \\
    && \downarrow^{\mathrlap{\partial^{vert}}}
    \\
    && D
  }
$$

is part of a [[double complex]] in an [[abelian category]], then there is a **6-term [[long exact sequence]]** running horizontally in

$$
  \array{
    &&  {}^\Box A
    \\
   & \nearrow && \searrow
    \\
    C_\Box &&\to&& A^{hor} &\to& A_{\Box} &\to& {}^{\Box} B &\to& B^{hor} 
   &&\to&& {}^{\Box}D 
   \\
    && && && && && & \searrow && \nearrow
   \\
    && && && && && && B_{\Box}
  }
  \,,
$$

where all the elementary morphisms are the unique intramural maps from lemma \ref{Intramural} and the extramural maps from lemma \ref{Extramural} -- they are the morphisms of the _salamander diagram_ of remark \ref{OmittingIntramuralMaps}.

Similarly, if a diagram

$$
  \array{
    C &\stackrel{\partial^{hor}}{\to}& A
    \\
    && \downarrow^{\mathrlap{\partial^{vert}}}
    \\
    && B &\stackrel{\partial^{hor}}{\to}& D
  }
$$

is part of a double complex, then there is a 6-term [[long exact sequence]] running horizontally in 

$$
  \array{
    && {}^\Box A
    \\
    & \nearrow & & \searrow
    \\
    C_\Box &&\to&& A^{vert} &\to& A_{\Box} &\to& {}^\Box B &\to&
    B^{vert}
    &&\to&&
    {}^\Box D
    \\
    && && && && && & \searrow && \nearrow
    \\
    && && && && && && B_\Box
  }
  \,
$$

=--

This is [Bergman, lemma 1.7](#Bergman).

+-- {: .proof}
###### Proof

We spell out the proof of the first case. That of the second case is verbatim the same, only with the roles of $\partial^{hor}$ and $\partial^{vert}$ interchanged.

By lemmas \ref{Intramural} and \ref{Extramural}, all the maps are given on representatives either by identities or by the [[differentials]] of the double complex themselves. Using this we may check exactness at each position explicitly:

1. exactness at $C_\Box \to A^{hor} \to A_\Box$.

   An element $[a] \in A^{hor}$ is in the kernel of $A^{hor} \to A_{\Box}$ if there is $c$ and $d$ such that $a = \partial^{vert}c + \partial^{hor} d$. 
The $c$ that satisfy this equation hence satisfy $\partial^{hor}\partial^{vert} c = 0$, hence represent elements in $C_\Box$ and so the map $\partial^{hor} : C_\Box \to A^{hor}$ hits all of the kernel of $A^{hor}\to A_\Box$. Also it clearly hits at most this kernel. 

1. exactness at $A^{hor} \to A_\Box \to {}^\Box B$.

   Suppose $[a] \in A_\Box$ is in the kernel of $A_\Box \to {}^\Box B$. This means that there is $c$ such that $\partial^{hor}a = \partial^{hor} \partial^{vert}c$, hence that $\partial^{hor} (a-\partial^{vert} c) = 0$. But $[a] = [a - \partial^{vert}c] \in A_{\Box}$ and so this says that $[a]$ is the image under $A^{hor} \to A_{\Box}$ of the element represented there by $a - \partial^{vert} c$. Conversely, clearly everything in that image is in the kernel of $A_\Box \to {}^\Box B$.

1. exactness at $A_\Box \to {}^\Box B \to B^{hor}$

   An element $[b] \in {}^\Box B$ is in the kernel of ${}^\Box B \to B^{hor}$ if there is $a$ such that $\partial^{hor} a = b$. But since the representative $b$ of $[b] \in {}^\Box B$ has to satisfy in particular $\partial^{vert} b = 0$ it follows that $\partial^{hor} \partial^{vert}a  = 0$ and hence that $a$ represents an element in $A_{\Box}$, hence that $[b]$ is in the image of $A_{\Box} \to {}^{\Box }B$. Conversely, clearly every element in that image is in the kernel of ${}^\Box B \to B^{hor}$.

1. exactness at ${}^\Box B \to B^{hor} \to {}^\Box D$

   An element $[b] \in B^{hor}$ is in the kernel of $B^{hor} \to {}^\Box D$ if there is $a$ with $\partial^{vert} b = \partial^{vert} \partial^{hor} a$, hence $\partial^{vert}(b - \partial^{hor}a) = 0$ Since in addition $\partial^{hor}(b - \partial^{hor}a) = 0$ by assumption on $b$ and the chain complex property, this says that $[b] = [b - \partial^{hor} a]$ is in the image of ${}^\Box B \to B^{hor}$. Moreover, clearly everything in this image is in the kernel of $B^{hor} \to {}^\Box D$.

=--

### Intramural and extramural isomorphisms
 {#IntraExtramuralIsomorphisms}

The following two statements are direct consequences (special cases) of the salamander lemma, prop. \ref{SalamanderLemma}. They give sufficient conditions for the intramural and the extramural maps, lemma \ref{Intramural} and lemma \ref{Extramural}, to be [[isomorphisms]]. All of the standard [[diagram chasing lemmas]] in [[homological algebra]] follow in a natural way from combining these _intramural isomorphisms_ with long [[zigzags]] of these _extramural isomorphisms_. This is discussed below in _[The basic diagram chasing lemmas](#Implications)_.

+-- {: .num_cor #ExtramuralIso}
###### Corollary
**(extramural isomorphisms)**

If the rows of a double complex are exact at the domain and codomain of a horizontal morphism $\partial^{hor} : A \to B$, i.e. if  $A^{hor} = 0$ and $B^{hor} = 0$, then the extramural map of lemma \ref{Extramural}

$$
  A_{\Box} \to {}^\Box B
$$ 

is an [[isomorphism]].

Similarly if for a vertical morphism $\partial : A \to B$ we have $A^{vert} = 0$ and $B^{vert} = 0$, the induced extramural map 

$$
  \array{
    A_\Box
    \\
    \downarrow
    \\
    {}^\Box B
  }
$$

is an isomorphism.

=--

This appears as [Bergman, cor. 2.1](#Bergman).

It is straightforward to check this directly on elements:

+-- {: .proof}
###### Proof

It is sufficient to show that under the given assumptions both the [[kernel]] and the [[cokernel]] of the given map are trivial.
We discuss the horizontal case. The proof of the vertical case is verbatim the same, only with the roles of $\partial^{vert}$ and $\partial^{hor}$ exchanged.

  Suppose an element $[a] \in A_{\Box}$ is in the kernel of $\partial^{hor} : A_{\Box} \to {}^\Box B$. By definition of ${}^\Box B$ this means that there is $c$ such that  $\partial^{hor} \partial^{vert} c = \partial^{hor} a$, hence such that $\partial^{hor}(a- \partial^{vert} c) = 0$. By assumption that  $A^{hor} = 0$ this means that there is $d$ such that  $a - \partial^{vert} c = \partial^{hor} d$. But this means that $a \in im(\partial^{hor}) + im(\partial^{vert})$ and hence $[a] = 0$ in $A_\Box$.

  Conversely, consider $[b] \in {}^\Box B$. This means that $\partial^{vert}b = 0$ and $\partial^{hor} b = 0$. By $B^{hor} = 0$ the second condition means that there is $a$ such that $b = \partial^{hor} a$. 
Moreover, this $a$ satisfies $\partial^{vert}\partial^{hor} a = \partial^{vert} b = 0$ by the first condition. Therefore $[a] \in A_{\Box}$ and $[b]$ is its image.

=--

Alternatively, this statement is a direct consequence of the salamander lemma already proven above:

+-- {: .proof}
###### Proof

Under the given assumptions the exact sequence of prop. \ref{SalamanderLemma} involves the exact sequence

$$
  0 \to A_{\Box} \to {}^\Box B \to 0
  \,.
$$

This being exact says that the map in the middle has vanishing [[kernel]] and [[cokernel]] and is hence an [[isomorphism]].

=--

+-- {: .num_cor #IntramuralIsos}
###### Corollary
**(intramural isomorphisms)**

In each of the situations in a double complex shown below, if the direction _perpendicular_ to $\partial : A \to B$ or $\partial : B \to A$ is [[exact sequence|exact]] at $B$ as indicated in the following, then the two intramural maps from lemma \ref{Intramural},  shown in each case on the right, are [[isomorphisms]]:

1. $$
     \array{
       && \vdots && \vdots
       \\
       && \downarrow && \downarrow
       \\
       0 &\to& A &\to& &\to& \cdots
       \\
       && \downarrow^{\mathrlap{\partial}} && \downarrow
       \\
       0 &\to& B &\stackrel{ker = 0}{\to}& &\to& \cdots
       \\
       && \downarrow && \downarrow
       \\
       && \vdots && \vdots
     }
     \;\;\;\;\;\;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;\;\;\;\;\;
     \array{
       {}^\Box A &\stackrel{\simeq}{\to}& A^{hor}
       \\
       A^{vert} & \stackrel{\simeq}{\to}&  A_{\Box}
     }
   $$

1. $$
     \array{
       && 0 && 0
       \\
       && \downarrow && \downarrow
       \\
       \cdots &\to& A &\stackrel{\partial}{\to}& B &\to& \cdots
       \\
       && \downarrow && \downarrow^{\mathrlap{ker = 0}}
       \\
       \cdots &\to& &\to& &\to& \cdots
       \\
       && \vdots && \vdots
     }
     \;\;\;\;\;\;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;\;\;\;\;\;
     \array{
       {}^\Box A &\stackrel{\simeq}{\to}& A^{vert}
       \\
       A^{hor} & \stackrel{\simeq}{\to}&  A_{\Box}
     }  
   $$

1. $$
     \array{
       && \vdots && \vdots
       \\
       && \downarrow && \downarrow
       \\
       \cdots &\to& &\stackrel{im = B}{\to}& B &\to& 0
       \\
       && \downarrow && \downarrow^{\mathrlap{\partial}}
       \\
       \cdots &\to& &\to& A &\to& 0
       \\
       && \downarrow && \downarrow
       \\
       && \vdots && \vdots
     }
     \;\;\;\;\;\;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;\;\;\;\;\;
     \array{
        A^{hor} &\stackrel{\simeq}{\to}& A_{\Box}
        \\
        {}^\Box A &\stackrel{\simeq}{\to}& A^{vert}
     }
   $$

1. $$
     \array{
       && \vdots && \vdots
       \\
       \cdots &\to& &\to& &\to& \cdots
       \\
       && \downarrow^{\mathrlap{im = B}} && \downarrow
       \\
       \cdots &\to& B &\stackrel{\partial}{\to}& A &\to& \cdots
       \\
       && \downarrow && \downarrow
       \\
       && 0 && 0
     }
     \;\;\;\;\;\;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;\;\;\;\;\;
     \array{
       A^{vert} &\stackrel{\simeq}{\to}& A_{\Box}
       \\
       {}^\Box A &\stackrel{\simeq}{\to}& A^{hor}
     }
   $$


=--

This appears as [Bergman, cor. 2.2](#Bergman).

+-- {: .proof}
###### Proof

We spell out the proof of the first item. The others work
analogously.

Applying cor. \ref{ExtramuralIso} to $0 \to B$ yields ${}^\Box B \simeq 0_\Box = 0$. Therefore the exact sequence of the Salamander lemma \ref{SalamanderLemma} corresponding to 

$$
  \array{
    \bullet 
    \\
    \downarrow
    \\
    0 &\to& A 
    \\
    && \downarrow
    \\
    && B
  }
$$

ends with 

$$
  \cdots \to 0 \to {}^\Box  A\to A^{hor} \to 0
  \,,
$$

which implies the first isomorphism. Analogously, the salamander exact sequence associated with 

$$
  \array{
    0 &\to& A
    \\
    && \downarrow
    \\
    && B &\to& \bullet
  }
$$

begins as

$$
  0 \to A^{vert} \to A_{\Box} \to 0 \to \cdots
  \,.
$$

which gives the second isomorphism.

=--


## Implications: The basic diagram-chasing lemmas
 {#Implications}

We derive the basic [[diagram chasing lemmas - contents|diagram chasing lemmas]] from the salamander lemma, or in fact just from repeated application of the [intramural/extramural isomorphisms](#IntraExtramuralIsomorphisms).

### The $3 \times 3$ lemma
 {#3x3Lemmas}

We derive the [[sharp 3x3 lemma]] from the salamander lemma.

+-- {: .num_prop #ShortSharp3x3}
###### Proposition

If in a [[diagram]] of the form

$$
  \array{
    && 0 && 0 && 0
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A' &\to& B' &\to& C'
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A &\to& B &\to& C
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A'' &\to& B'' &\to& C''
  }
$$

all columns and the second and third row are [[exact sequence|exact]], 
then also the first row is exact.

=--

The following proof is that given in [Bergman, lemma 2.3](#Bergman).

+-- {: .proof}
###### Proof

First of all one notices that the diagram is a [[double complex]]: by column-exactness the first row includes as [[subobjects]] into the second, so the horizontal maps of the first row are restrictions of the [[differentials]] of the second and so at least the first row is a [[chain complex]].

We need to show that ${A'}^{hor}\simeq 0$ and ${B'}^{hor} \simeq 0$.

First consider exactness at $A'$. The intramural iso, cor. \ref{IntramuralIsos} item 1, of

$$
  \array{
    A'  
    \\
    \downarrow^{\mathrlap{\partial}}
    \\
    A &\stackrel{ker = 0}{\to}& B
  }
$$

is ${}^\Box A' \simeq {A'}^{hor}$, and the one of 

$$
  \array{
    A' &\stackrel{\partial}{\to}& B'
    \\
    && \downarrow^{\mathrlap{ker = 0}}
    \\
    && B
  }
$$

according to cor. \ref{IntramuralIsos} item 2
is ${}^\Box A' \simeq {A'}^{vert}$. Together this gives the desired exactness from the assumption that ${A'}^{vert} = 0$ (since all the columns are exact by assumption):

$$
  {A'}^{hor} \simeq A'_\Box \simeq {A'}^{vert} = 0
  \,.
$$

To apply an analogous argument for ${B'}^{hor}$, we combine this kind of identification with the [[zigzag]] of extramural maps along the diagonal

$$
  \array{
    &&&& B'
    \\
    &&&&& \Box
    \\
    &&&& \swarrow
    \\
    &&& \Box
    \\
    A && \nearrow && B
    \\
    & \Box
  }
  \,,
$$

which are isos by cor \ref{ExtramuralIso}. These appear now in the 
middle of the following chain of isomorphisms


$$
  {B'}^{hor} \simeq \left({B'}_{\Box}\simeq {}^{\Box}B \simeq A_{\Box}\right) \simeq \left(A^{vert} \simeq 0\right)\,,
$$

where the first and the last are intramural isos obtained from cor. \ref{IntramuralIsos}.

=--

+-- {: .num_remark}
###### Remark

From this argument it is clear that by directly analogous reasoning we obtain "$n \times n$-lemmas" for arbitrary $n$, see prop. \ref{nxn} below. 

=--

In particular we have the following _[[sharp 3x3 lemma]]_.


+-- {: .num_prop #Sharp3x3}
###### Proposition

If in a [[diagram]] of the form

$$
  \array{
    && 0 && 0 && 0
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A' &\to& B' &\to& C' &\to& 0
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A &\to& B &\to& C &\to& 0
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& A'' &\to& B'' &\to& C'' 
    \\
    && \downarrow
    \\
    && 0
  }
$$

all columns and the second and third row are [[exact sequence|exact]], 
then also the first row is exact.

=--

+-- {: .proof}
###### Proof

We can extend the middle and right columns by adding the cokernel of $B \to B''$ below $B''$, and $C'' \to 0$ below C''.  It's straightforward to check that the resulting diagram is still a complex, and we now have vertical exactness at $B''$.  Note that we may not have vertical exactness at $C''$, nor exactness in the bottom row containing the cokernel, but we don't need those.

Exactness in $A'$ and $B'$ is as in prop. \ref{ShortSharp3x3}.
For exactness in $C'$ we now use the long [[zigzag]] of 
extramural isomorphisms, cor \ref{ExtramuralIso}. 

$$
  \array{  
    &&&&&&&& C'
    \\
    &&&&&&&& & \Box
    \\
    &&&&&&&& \swarrow
    \\ 
    &&&&&&& \Box
    \\
    &&&& B && \nearrow && C
    \\
    &&&&& \Box
    \\
    &&&& \swarrow
    \\
    &&& \Box
    \\
    A'' && \nearrow && B''
    \\
    & \Box
  }
  \,,
$$

So ${C'}^{hor} \simeq C_{\Box}$ by the intramural iso, then $\dots \simeq A''_\Box$ by this zigzag of extramural isos (this is where we need vertical exactness at $B''$), and finally $\cdots \simeq {A''}^{hor} \simeq 0$ by another intramural iso and by assumption.

=--

### The $n \times n$ lemma
 {#nxnLemma}

The proofs of the $3 \times 3$-lemmas [above](#3x3Lemmas) via long diagonal zigzags of extramural isomorphism clearly generalize from double complexes of size $3 \times 3$ to those of arbitrary finite size.

+-- {: .num_prop #nxn}
###### Proposition

If in a diagram of the form

$$
  \array{
    && 0 && 0 && 0 && 0 &&
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& X_{n,n} &\to& X_{n-1,n} &\to& X_{n-2,n} &\to& X_{n-3,n} &\to& \cdots
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& X_{n,n-1} &\to& X_{n-1,n-1} &\to& X_{n-2,n-1} &\to& X_{n-3,n-1} &\to& \cdots
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& X_{n,n-2} &\to& X_{n-1,n-2} &\to& X_{n-2,n-2} &\to& X_{n-3,n-2} &\to& \cdots
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& X_{n,n-3} &\to& X_{n-1,n-3} &\to& X_{n-2,n-3} &\to& X_{n-3,n-3} &\to& \cdots
    \\
    && \downarrow && \downarrow && \downarrow && \downarrow
  }
$$

all rows except possibly the first $X_{\bullet, n}$ as well as all columns except possibly the first $X_{n,\bullet}$ are [[exact sequence|exact]], then the homology groups of the first row equal those of the first column in that

$$
  \forall k : X_{k,n}^{hor} \simeq X_{n,k}^{vert}
  \,.
$$

=--

This appears as [Bergman, lemma 2.6](#Bergman).

+-- {: .proof}
###### Proof

The proof proceeds in direct generalization of the proofs of the 
3x3 lemma [above](#3x3Lemmas): the isomorphism for each $k$ is given by the composite of two extramural isomorphisms that identify the given homology group with a donor or receptor group, respectively, with a long zigzag of extramural isomorphisms.

=--

### The four lemma
 {#FourLemma}

We prove the  _strong [[four lemma]]_ from the salamander lemma. 

+-- {: .num_prop}
###### Proposition

Consider a [[commuting diagram]] in $\mathcal{A}$ of the form

$$
  \array{
    A &\to& B &\stackrel{\xi}{\to}& C &\to& D
    \\
    \downarrow^{\mathrlap{\tau}}
    &&
    \downarrow^{\mathrlap{f}}
    &&
    \downarrow^{\mathrlap{g}}
    &&
    \downarrow^{\mathrlap{\nu}}
    \\
    A' &\to& B' &\stackrel{\eta}{\to}& C' &\to& D'
  }
$$

where 

1. the rows are [[exact sequences]],

1. $\tau$ is an [[epimorphism]],

1. $\nu$ is a [[monomorphism]].

Then 

1. $\xi(ker(f)) = ker(g)$

1. $im(f) = \eta^{-1}(im(g))$

and so in particular

1. if $f$ is a [[monomorphism]] then so is $g$;

1. if $g$ is an [[epimorphism]] then so is $f$.

=--

+-- {: .proof}
###### Proof

By assumption on $\tau$ and $\nu$ we can complete the diagram 
to a [[double complex]] of the form

$$
  \array{
    && 0 && 0
    \\
    && \downarrow && \downarrow
    \\
    && ker(f) &\stackrel{\xi|_{ker(f)}}{\to}& ker(g) &\to& 0
    \\
    && \downarrow && \downarrow && \downarrow
    \\
    A &\to& B &\stackrel{\xi}{\to}& C &\to& D
    \\
    \downarrow^{\mathrlap{\tau}}
    &&
    \downarrow^{\mathrlap{f}}
    &&
    \downarrow^{\mathrlap{g}}
    &&
    \downarrow^{\mathrlap{\nu}}
    \\
    A' &\to& B' &\stackrel{\eta}{\to}& C' &\to& D'
    \\
    \downarrow && \downarrow && \downarrow
    \\
    0 &\to& B'/im(f) &\to& C'/im(g)
    \\
     && \downarrow && \downarrow
    \\
    && 0 && 0
  }
$$

such that

1. all columns are [[exact sequence|exact]];

1. the middle two rows are exact.

For the first statement it is now sufficient to show that $ker(g)^{hor} \simeq 0$, for that is immediately equivalent to $\xi(ker(f)) = ker(g)$.

To see this we use the intramural isomorphism, 
cor. \ref{IntramuralIsos} item 2, to deduce that

$$
  ker(g)^{hor} \simeq ker(g)_{\Box}
  \,.
$$

Then the long [[zigzag]] of extramural isomorphisms, cor. \ref{ExtramuralIso}, shows that this is isomorphic to the 
${}^\Box 0 \simeq 0$ in the bottom left corner of the diagram.

The second statement follows dually: it is implied by
$(B'/im(f))^{hor} \simeq 0$ for that directly implies that 
$\eta^{-1}(im(g))\simeq im(f)$.

Here the intramural ismorphism to use is

$$
  (B'/im(f))^{hor} \simeq {}^{\Box}(B'/im(f))
$$

and then the long sequence of zigzags of extramural isomorphisms identifies this with the $0_\Box \simeq 0$ in the top right corner.

=--

+-- {: .num_remark}
###### Remark

The [[four lemma]], in turn, directly implies what is 
known as the [[five lemma]].

=--


### The snake lemma
 {#TheSnakeLemma}

We discuss a proof of the [[snake lemma]] from the salamander lemma.

+-- {: .num_prop #Snake}
###### Proposition

If in a commuting diagram of the form

$$
  \array{
    && X_1 &\to& X_2 &\to& X_3 &\to& 0
    \\
    && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{h}}
    \\
    0 &\to& Y_1 &\to& Y_2 &\to& Y_3
  }
$$

both rows are [[exact sequence|exact]], then there is a [[long exact sequence]]

$$
  ker(f) \to ker(g) \to ker(h) 
   \stackrel{\delta}{\to}
  coker(f) \to coker(g) \to coker(h)
$$

starting with the [[kernels]] of the three vertical maps and ending with their [[cokernels]] (with the middle morphism $\delta$ called the "[[connecting homomorphism]]").

=--

+-- {: .proof}
###### Proof

Consider the completion of the given diagram to a [[double complex]]:

$$
  \array{
     &&  ker(f) &\to& ker(g) &\to& ker(h) &\to& 0
    \\
     && \downarrow && \downarrow && \downarrow && \downarrow
    \\
    ker(l) &\to& X_1 &\stackrel{l}{\to}& X_2 &\to& X_3 &\to& 0
    \\
    \downarrow && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{h}} && \downarrow
    \\
    0 &\to& Y_1 &\to& Y_2 &\stackrel{r}{\to}& Y_3 &\to& coker(r)
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    0 &\to& coker(f) &\to& coker(g) &\to& coker(h) && 
  }
  \,.
$$

By assumption and construction, here all columns are exact and the rows are exact at the $X_i$ and at the $Y_i$, and the squares involving $ker(l)$ and $coker(r)$ commute.

Now horizontal exactness at $ker(g)$ follows from the intramural isomorphism
$ker(g)^{hor} \simeq ker(g)_{\Box}$, cor. \ref{IntramuralIsos}, combined with the [[zigzag]] of extramural isomorphisms, cor. \ref{ExtramuralIso},

$$
  \array{
     &&&&&&& ker(g)
     \\
     &&&&&&&& \Box
     \\
     &&&&&&& \swarrow
     \\
     & &&&&& \Box
     \\
     & X_1 &&&& \nearrow & & X_2
     \\
     && \Box
     \\
     & \swarrow
     \\
     \Box
     \\
     & Y_1
  }
$$

which give $\cdots \simeq {}^\Box Y_1$, and then the extramural isomorphism
$\cdots \simeq 0_{\Box} = 0$.

Exactness at $coker(g)$ is shown analogously.

Finally, building the [[connecting homomorphism]] $ker(h) \to coker(f)$ is the same as giving an  [[isomorphism]] from $coker(ker(g) \to ker(h)) \simeq ker(h)^{hor}$ to 
$ker(coker(f) \to coker(g)) = coker(f)^{hor}$. This is in turn given by the intramural isomorphisms $ker(h)^{hor} \simeq ker(h)_{\Box}$ and ${}^\Box coker(f) \simeq coker(f)^{hor}$, cor. \ref{IntramuralIsos} connected by the [[zigzag]] of extramural isomorphisms, cor. \ref{ExtramuralIso}

$$
  \array{
    &&&&&&&&& ker(h)
    \\
    &&&&&&&&&& \Box
    \\
    &&&&&&&&& \swarrow
    \\
    &&&&& && & \Box
    \\
    &&&&& X_2 && \nearrow && X_3
    \\
    &&&&&& \Box
    \\
    &&&&& \swarrow
    \\
    &&&& \Box
    \\
    & Y_1 && \nearrow & & Y_2
    \\
    && \Box
    \\
    & \swarrow
    \\
    \Box
    \\
    & coker(f)
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

From the [[snake lemma]] one obtains in turn the 
[[connecting homomorphism]] between homology groups that leads to the long exact sequence of homology; see there for details.

=--

## References
 {#References}

The salamander lemma is due to 

* {#Bergman12} [[George Bergman]], _On diagram-chasing in double complexes_, Theory and Applications of Categories **26** (2012) 60-96 &lbrack;[arXiv:1108.0958](http://arxiv.org/abs/1108.0958), [tac:26-03](http://www.tac.mta.ca/tac/volumes/26/3/26-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/26/3/26-03.pdf)&rbrack;

based on an earlier unpublished preprint which was circulated  since 2007 ([pdf](http://sbseminar.files.wordpress.com/2007/11/diagramchasingbergman.pdf)).

Exposition:

* [[Anton Geraschenko]], _The Salamander lemma_ (2007) &lbrack;[blog post](http://sbseminar.wordpress.com/2007/11/13/anton-geraschenko-the-salamander-lemma/)&rbrack;

An alternative proof (also of the [[snake lemma]]) "without elements", using only [[universal properties]]:

* {#Wise} [[Jonathan Wise]], §4 in: *A non-elementary proof of the snake lemma* (2011, 2023) &lbrack;[pdf](https://math.colorado.edu/%7Ejonathan.wise/papers/snake.pdf), [[Wise-SnakeLemma.pdf:file]], [MO:a/7531](https://mathoverflow.net/a/7531/381)&rbrack;



[[!redirects Salamander lemma]]
