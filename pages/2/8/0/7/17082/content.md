
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _lifting property_ is a property of a pair of [[morphism]]s in a [[category]]. It is used in [[homotopy theory]] within [[algebraic topology]] to define properties of morphisms starting from an explicitly given class of morphisms. It appears in a prominent way in the theory of [[model categories]], an axiomatic framework for [[homotopy theory]] introduced by [[Daniel Quillen]]. It is also used in the definition of a [[factorization system]], and of a [[weak factorization system]], notions related to but less restrictive than the notion of a model category. 
A number of elementary notions may also be expressed using the lifting property starting from a list of (counter)examples.

{#AsQualitativeNegation} Often it is useful to think of lifting properties as a expressing a kind of qualitative negation ("[[Quillen negation]]"): The morphisms with the left/right lifting property against those in a class $P$ tend to be characterized by properties opposite of those in $P$.
For example, a morphism in [[Sets]] is [[surjective]] iff it has the right lifting property against the archetypical non-surjective map $\varnothing \to \{*\}$, and [[injective]] iff it has either left or right lifting property against the archetypical non-injective map  $\{x_1,x_2\}\to \{*\}$. (For more such examples see at *[[separation axioms in terms of lifting properties]]*.) 

## Definition

\begin{definition}\label{LiftingPropertiesOfMorphisms}
**(lifting properties of morphisms)**
\linebreak
A morphism $i$ in a category has the *left lifting property* with respect to a morphism $p$, and $p$ also has the *right lifting property* with respect to $i$, sometimes denoted $i\,\,&solb;\,\, p$ or $i\downarrow p$, iff the following implication holds for each morphism $f$ and $g$ in the category:

* if the outer square of the following diagram commutes, then there exists $h$ completing the diagram, i.e. for each $f:A\to X$ and $g:B\to Y$ such that $p\circ f = g \circ i$ there exists $h:B\to X$ such that $h\circ i = f$ and $p\circ h = g$.

\begin{tikzcd}
  A
  \ar[dd, "i"]
  \ar[rr, "f"]
  && X\ar[dd,"p"]
  \\
  \\
  B
  \ar[
    rr,"g"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"{description}
  ]
  &&Y
\end{tikzcd}
\end{definition}

This is sometimes also known as the morphism $i$ being ''weakly orthogonal to'' the morphism $p$; however, ''orthogonal to'' will refer to the stronger property that whenever $f$ and $g$ are as above, the diagonal morphism $h$ exists and is also required to be unique.

\begin{remark} \label{LiftingForObjects}
**(lifting properties of objects)**
\linebreak
One also speaks of *[[objects]]* having left or right lifting properties (for instance in the definition of [[projective objects]] and [[injective objects]], respectively, or in the characterization of [[cofibrant objects]] and [[fibrant objects]], respectively), by which one then means, respectively:
\end{remark}

* that the corresponding unique morphisms $\varnothing \longrightarrow B$ (from the [[initial object]]) has the left lifting property in the sense of Def. \ref{LiftingPropertiesOfMorphisms} (against the given morphism $p$):

\begin{tikzcd}
  \color{lightgray}
  \varnothing
  \ar[dd, "\exists !", lightgray]
  \ar[rr, "\exists !", lightgray]
  && 
  X \ar[dd,"p"]
  \\
  \\
  B
  \ar[
    rr,"g"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"{description}
  ]
  &&
  Y
  \mathrlap{\,,}
\end{tikzcd}

* that the unique morphism $X \longrightarrow \ast$ (to the [[terminal object]]) has the right lifting property (against the given morphism $i$):

\begin{tikzcd}
  A
  \ar[dd, "i"]
  \ar[rr, "f"]
  && 
  X\ar[dd,"\exists !", lightgray]
  \\
  \\
  B
  \ar[
    rr, "\exists !", lightgray
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"{description}
  ]
  &&
  \color{lightgray}
  \ast
  \mathrlap{\,,}
\end{tikzcd}




\begin{definition}
\label{QuillenNegation}
**([[orthogonal class]]/[[Quillen negation]])**
\linebreak
Given a [[class]] $M \;\subset\; Mor(\mathcal{C})$ of [[morphisms]] in a [[category]] $\mathcal{C}$, its 

* *left weak orthogonal class* or *left [[Quillen negation]]*
 $\multiscripts{^&solb;}{M}{}$ 

or 

* *right weak orthogonal class* or *right [[Quillen negation]]*  $\multiscripts{}{M}{^&solb;}$  

is the class of all morphisms which have the left, respectively right, lifting property (in the sense of Def. \ref{LiftingPropertiesOfMorphisms}) with respect to each morphism in the class $M$:

$$
  M^{&solb;} 
  \;\coloneqq\;
  \Big\{ 
    p \,\in\, Mor(\mathcal{C})
    \;\big\vert\; 
   \underset{i \in M}{\forall}
   \; i \,&solb;\, p
  \Big\}, 
  \;\;\;\;\;
  {}^{&solb;}M 
  \;\coloneqq\;
  \Big\{ 
    i \,\in\, Mor(\mathcal{C})
    \;\big\vert\; 
   \underset{p \in M}{\forall}
   \; i \,&solb;\, p
  \Big\}
  \,.
$$ 

\end{definition}


## Examples of lifting properties
 {#ExamplesOfLiftingProperties}

Decyphering notation in most of the examples below leads to standard definitions or reformulations. The intuition behind most examples below 
is that the class of morphisms consists of simple or archetypal examples
related to the property defined. 

We use the notation of Def. \ref{QuillenNegation}.

### Elementary examples 

#### Sets

In _[[Set]]_, 

* $
    \big\{
      \varnothing \to \{*\}\big
    \}^{&solb;}
    \;\;\;
    =
    \;\;\;
    Srjctv
  $ 

  is the class of [[surjective functions]],

* $
    \big( \{a,b\}\to \{*\} \big)^{&solb;}
    \;\;\;
    =
    \;\;\;
    Injctv
  $ 

  is the class of [[injective functions]].


#### Modules
 {#ExamplesModules}

In the category *[[RMod]]* of [[module|modules]] over a [[commutative ring]] $R$ (recalling that we use the notation of Def. \ref{QuillenNegation}):

The [[surjection|surjective]] [[homomorphisms]] are those with the [[right lifting property]] against the [[initial object|initial]] [[homomorphism]] from the [[zero]] [[module]] into the [[ground ring]]:


\[
  \label{SurjectiveModuleMapsAsRightOrthClass}
  \{ 0 \to R \}^{&solb;} 
  \;\;\;=\;\;\; 
  Srjctv
  \,.
\]

The [[injection|injective]] [[homomorphisms]] are those with the [[right lifting property]] against the [[terminal object|terminal]] [[homomorphism]] from the [[ground ring]] 
into the [[zero]] [[module]]:

\[
  \label{InjectiveModuleMapsAsRightOrthClass}
  \{ R \to 0 \}^{&solb;}
  \;\;\;=\;\;\;
  Injctv
  \,.
\]


An $R$-[[module]] $M$ is [[projective module|projective]] iff (by direct unwinding of the definitions of [[projective objects]] and lifts) the [[initial object|initial morphism]] $0 \to R$ (out of the [[zero]] [[module]] into the [[ground ring]]) has the [[left lifting property]] against all surjective homomorphisms.

With the notation of Def. \ref{QuillenNegation} this reads as follows:

  $$
    M\;\text{projective}
    \;\;\;\;\;
      \Leftrightarrow
    \;\;\;\;\;
    \{ 0 \to M \}
    \;&solb;\;
    Srjctv
    \;\;\;\;\;
      \overset{
        \text{(eq:SurjectiveModuleMapsAsRightOrthClass)}
      }{
      \Leftrightarrow
      }
    \;\;\;\;\;
    \{ 0 \to M \}
    \;&solb;\;
    \Big(
      \{ 0 \to R \}^{&solb;}
    \Big)
    \;\;\;\;\;
      \Leftrightarrow
    \;\;\;\;\;
    \{ 0 \to M \}
    \;\in\;
    \multiscripts{^{&solb;}}
    {
    \Big(
      \{ 0 \to R \}^{^&solb;}
    \Big)
    }{}
  $$



#### Groups

In the category _[[Grp]]_ of [[Group|groups]], 

* $\{\mathbb{Z} \to 0\}^{&solb;  r}$, resp. $\{0\to \mathbb{Z}\}^{&solb;  r}$, is the class of injections, resp. surjections (where $\mathbb{Z}$ denotes the infinite [[cyclic group]]),

* A group $F$ is a [[free group]] iff $0\to F$ is in $\{0\to \mathbb{Z} \}^{&solb;  r\ell},$

* A group $A$ is [[torsion|torsion-free]] iff $0\to A$ is in $\{ n \mathbb{Z} \to \mathbb{Z} : n\ge0 \}^{&solb;  r},$

* A [[subgroup]] $A$ of $B$ is [[pure subgroup|pure]] iff $A \to B$ is in $\{ n\mathbb{Z}\to \mathbb{Z} : n\ge0 \}^{&solb;  r}.$


* $(*\to 1)^{&solb; l}$ is the class of retracts
*  $(1\to *)^{&solb; r}$ is the class of split homomorphisms

* $(0\longrightarrow \mathbb{Z})^{&solb; r}$ is the class of surjections
* $(\mathbb{Z}\to 1)^{&solb; r}$ is the class of injections
*     a group $F$ is free iff
 $1\to F$ is in  $(0\longrightarrow \mathbb{Z})^{&solb;rl}$ 

* a group $A$ is Abelian iff $A\to 1$ is in $( \mathbb{F}_2 \to \mathbb{Z}\times\mathbb{Z})^{&solb; r}$

* group $G$ can be obtained from $H$ by adding commutation relations, i.e.~the kernel of $H\to G$ is generated by commutators $[h_1,h_2]$, $h_1,h_2\in H$,
iff 
 $H\to G$ is in $( \mathbb{F}_2 \to \mathbb{Z}\times\mathbb{Z})^{&solb;rl}$


* subgroup $H$ of $G$ is the normal span of substitutions in words $w_1,..,w_i$ of the free group $\mathbb{F}_n$ iff 
$G \to G/H$ is in $( \mathbb{F}_n \to \mathbb{F}_n/\le\!w_1,...,w_i\!\ge)^{&solb;rl}$


* $\{0\to A : A\,\,\text{ abelian}\}^{&solb; \ell l}$ is the class 
of homomorphisms whose kernel is perfect

For a [[finite group]] $G$, in the category of finite groups, 

* $\{0\to {\mathbb{Z}}/p{\mathbb{Z}}\} \,\,&solb;\,\, G\to 1$ iff the [[order]] of $G$ is prime to $p$,

* $G\to 1 \in (0\to {\mathbb{Z}}/p{\mathbb{Z}})^{&solb;  rr}$ iff $G$ is a [[p-group|$p$-group]],

* $H$ is nilpotent iff the diagonal map $H\to H\times H$ is in $(1\to *)^{&solb; \ell r}$ where $(1\to *)$ denotes the class of maps $\{ 1\to G : G \text{ arbitrary}\},$

* a finite group $H$ is [[soluble]] iff $1\to H$ is in $\{0\to A : A\,\,\text{ abelian}\}^{&solb; \ell r}=\{[G,G]\to G : G\,\,\text{ arbitrary } \}^{&solb; \ell r}.$

Moreover, 

* $\{0\to G : G\,\,\text{ arbitrary}\}^{&solb; \ell r}$ is the class of subnormal subgroups

*  $\{0\to A : A\,\,\text{ abelian}\}^{&solb; \ell r}=\{[G,G]\to G : G\,\,\text{ arbitrary } \}^{&solb; \ell r}$,
 and is the class of subgroups $H\leq G$ such that there is a chain of subnormal subgroups 
$H=G_0 \vartriangleleft G_1  \vartriangleleft \ldots  \vartriangleleft G_n =G$ such that $G_{i+1}/G_{i}$ is Abelian, for $i=0,...,n-1$.

* $\{1 \to S\}^{&solb; \ell r}$ is the class of subgroups $H\leq G$ such that there is a chain of subnormal subgroups
$H=G_0 \vartriangleleft G_1  \vartriangleleft \ldots  \vartriangleleft G_n =G$ such that $G_{i+1}/G_{i}$ embeds into $S$, for $i=0,...,n-1$. 

*  $(\mathbb{Z}/p\mathbb{Z}\longrightarrow 0)^{&solb;r}$ is the class of homomorphisms whose kernel has no elements of order $p$
*  $(\mathbb{Z}/p\mathbb{Z}\longrightarrow 0)^{&solb;rr}$ is the class of surjective homomorphisms whose kernel is a $p$-group 



### In algebraic topology and in model categories

Lifting properties are paramount in [[homotopy theory]] and [[algebraic topology]]. In "abstract homotopy theory" lifting properties are encoded in the structures of [[model categories]], whose defintion revolves all around compatible classes of [[weak factorization systems]]. In particular:

* the [[cofibrations]] in a model category are precisely the class with the left lifting property against the [[acyclic fibrations]],

* the [[fibrations]] in a model category are precisely the class with the right lifting property against the [[acyclic cofibrations]],

#### Serre fibrations of topological spaces

The [[classical model structure on topological spaces]] $Top_{Qu}$ is controlled by the following lifting properties:

consider let $C_0$ be the class of maps $S^n\to D^{n+1}$, [[embeddings]] of the boundary $S^n=\partial D^{n+1}$ of a ball into the ball $D^{n+1}$. Let $WC_0$ be the class of maps embedding the upper semi-sphere into the disk. $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$ are the classes of [[Serre fibrations]], acyclic cofibrations, acyclic fibrations, and cofibrations. [Hovey, Model Categories, Def. 2.4.3, Th.2.4.9](https://archive.org/details/arxiv-math9803002)

#### Hurewicz fibrations of topological spaces


A map $f:U\to B$ has the ''path lifting property'' iff $\{0\}\to [0,1] \,\,&solb;\,\, f$ where $\{0\} \to [0,1]$ is the inclusion of one end point of the closed interval into the interval $[0,1]$.

A map $f:U\to B$ has the [[homotopy lifting property]] iff $X \to X\times [0,1] \,\,&solb;\,\, f$ where $X\to X\times [0,1]$ is the map $x \mapsto (x,0)$.



#### Kan fibrations of simplicial sets

The [[classical model structure on simplicial sets]] $sSet_{Qu}$ is controlled by the following lifting properties:

Let $C_0$ be the class of boundary inclusions $\partial \Delta[n] \to \Delta[n]$, and let $WC_0$ be the class of horn inclusions $\Lambda^i[n] \to \Delta[n]$. Then the classes of [[Kan fibrations]], acyclic cofibrations, acyclic fibrations, and cofibrations are, respectively, $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$.
[(Model Categories, Def. 3.2.1, Th.3.6.5)](https://archive.org/details/arxiv-math9803002)

#### Degreewise surjections of chain complexes

A [[model structure on chain complexes]] is controlled by the following lifting properties:

* Let _Ch_($R$) be the category of [[chain complexes]] over a [[commutative ring]] $R$. Let $C_0$ be the class of maps of form
$\cdots\to 0\to R \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots,$
and $WC_0$ be
 $\cdots \to 0\to 0 \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots.$
Then $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$ are the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations.
 [(Model Categories, Def. 2.3.3, Th.2.3.11)](https://archive.org/details/arxiv-math9803002)





### Topology

Many elementary properties in [[general topology]], such as compactness, being dense or open, 
can be expressed as iterated Quillen negation of morphisms of finite topological spaces
in the category _Top_ of topological spaces. This leads to a concise, if useless, notation 
for a number of properties. Items below use notation for morphisms of finite topological spaces 
defined in the page on [[separation axioms in terms of lifting properties]],
and some examples are explained there in detail.


#### Uniform spaces 

In the category of [[uniform  spaces]] or [[metric spaces]] with [[uniformly continuous]] maps.

* A space $X$ is [[complete]] iff $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}} \,\,&solb;\,\, X\to \{0\}$ where $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}}$ is the obvious inclusion between the two subspaces of the real line with induced metric, and $\{0\}$ is the metric space consisting of a single point,

* A subspace $i:A\to X$ is closed iff $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}} \,\,&solb;\,\, A\to X.$



#### In topological spaces 

The following lifting properties are calculated in the category of (all) topological spaces. Below
we use notation defined in 
[[separation axioms in terms of lifting properties#NotationForFiniteTopologicalSpaces|the page on lifting properties]]

#### Iterated lifting properties

*         $(\emptyset\longrightarrow \{o\})^{&solb;r}$   is the class of surjections
*         $(\emptyset\longrightarrow \{o\})^{&solb;r}$   is the class of maps $A\longrightarrow B$ where $A\neq \emptyset$ or $A=B$
*         $(\emptyset\longrightarrow \{o\})^{&solb;rr}=\{\{x\leftrightarrow y\rightarrow c\}\longrightarrow\{x=y=c\}\}^{&solb;l}=\{\{x\leftrightarrow y\leftarrow c\}\longrightarrow\{x=y=c\}\}^{&solb;l}$ is the class of subsets, i.e. injective maps $A\hookrightarrow B$ where the topology on $A$ is induced from $B$

*  $(\emptyset\longrightarrow \{o\})^{&solb;lr}$ is the class of maps $\emptyset\longrightarrow B$, $B$ arbitrary
*         $(\emptyset\longrightarrow \{o\})^{&solb;lrr}$ is the class of maps $A\longrightarrow B$ which admit a section 


*   $(\emptyset\longrightarrow \{o\})^{&solb;l}$ consists of maps $f:A\longrightarrow B$ such that either  $A\neq \emptyset$ or  $A=B=\emptyset$  



*  $(\emptyset\longrightarrow \{o\})^{&solb;rl}$ is the class of maps of form $A\longrightarrow A\sqcup D$ where $D$ is discrete

*  $(\emptyset\longrightarrow \{o\})^{&solb;rll}$ is the class of maps 
$A\to B$ such that each connected subset of $B$ intersects the image of $A$; for "nice" spaces it means that the map $\pi_0(A)\to \pi_0(B)$ is surjective, where "nice" means that connected componets are both open and closed. 

*  $(\emptyset\longrightarrow \{o\})^{&solb;rllr}$ is the class of maps 
of form $A\to A\sqcup B$ where $A\sqcup B$ denotes the disjoint union of $A$ and $B$. 


*  $\{ \{z\leftrightarrow  x\leftrightarrow  y\rightarrow c\}\longrightarrow\{z=x\leftrightarrow  y=c\} \}^{&solb;l}  = \{\{c\}\longrightarrow \{o\rightarrow c\}\}^{&solb;lr}$ is the class of closed inclusions $A\subset B$ where $A$ is closed

*  $\{ \{z\leftrightarrow  x\leftrightarrow  y\leftarrow c\}\longrightarrow\{z=x\leftrightarrow  y=c\} \}^{&solb;l}$ is the class of open inclusions
$A\subset B$ where $A$ is open

*  $\{ \{x\leftrightarrow  y\rightarrow c\}\longrightarrow\{x\leftrightarrow  y=c\} \}^{&solb;l} $ is the class of closed maps $A\longrightarrow B$ 
where the topology on $A$ is pulled back from $B$
*  $\{ \{x\leftrightarrow  y\leftarrow c\}\longrightarrow\{x\leftrightarrow  y=c\} \}^{&solb;l}$ is the class of open maps $A\longrightarrow B$ 
where the topology on $A$ is pulled back from $B$


*         $(\{b\}\longrightarrow \{a{ \searrow}b\})^{&solb;l}$ is the class of maps with dense image
*         $(\{b\}\longrightarrow \{a{ \searrow}b\})^{&solb;lr}=\{ \{z\leftrightarrow x \leftrightarrow y\rightarrow c\}\longleftarrow\{z=x\leftrightarrow y=c\} \}^{&solb;l}$ is the class of closed subsets $A \subset  X$, $A$ a closed subset of $X$

*         $\{ \{z\leftrightarrow x \leftrightarrow y\leftarrow c\}\longleftarrow\{z=x\leftrightarrow y=c\} \}^{&solb;l}$ is the class of open subsets $A \subset  X$, $A$ a open subset of $X$


*         $(\{a\}\longrightarrow \{a{ \searrow}b\})^{&solb;lr}$ is the class of subsets $A \subset  X$ such that $A$ is the intersection of open subsets containing $A$

*         $((\{a\}\longrightarrow \{a \searrow b\})^{&solb;r}_{\le 4})^{&solb;lr}$ is roughly the class of proper maps



#### Separation axioms

Here follows a list of examples of well-known properties defined by 
iterated Quillen negation starting from maps between [[finite topological spaces]], often with less than 5 elements.  See at *[[separation axioms in terms of lifting properties]]*  for more on the following.


*   a space $K$ is non-empty iff $K\longrightarrow \{o\}$ is in $   (\emptyset\longrightarrow \{o\})^{&solb;l}$
*   a space $K$ is empty iff $K \longrightarrow \{o\}$ is in $   (\emptyset\longrightarrow \{o\})^{&solb;ll}$
*   a space $K$ is $T_0$ iff $K  \longrightarrow \{o\}$ is in $   (\{a\leftrightarrow b\}\longrightarrow \{a=b\})^{&solb;r}$
*    a space $K$ is $T_1$ iff $K  \longrightarrow \{o\}$ is in $   (\{a{ \searrow}b\}\longrightarrow \{a=b\})^{&solb;r}$
*   a space $X$ is Hausdorff iff for each injective map $\{x,y\} \hookrightarrow  X$
it holds $\{x,y\} \hookrightarrow   {X} \,&solb;\,  \{  {x} { \searrow}  {o} { \swarrow}  {y} \} \longrightarrow  \{ x=o=y \}$

*   a non-empty space $X$ is regular (T3) iff for each arrow $    \{x\} \longrightarrow  X$ it holds
    $    \{x\} \longrightarrow   {X} \,&solb;\,  \{x{ \searrow}X{ \swarrow}U{ \searrow}F\} \longrightarrow  \{x=X=U{ \searrow}F\}$
*   a space $X$ is normal (T4) iff $\emptyset \longrightarrow  {X} \,&solb;\,   \{a{ \swarrow}U{ \searrow}x{ \swarrow}V{ \searrow}b\}\longrightarrow \{a{ \swarrow}U=x=V{ \searrow}b\}$

*   a space $X$ is completely normal iff $\emptyset\longrightarrow  {X} \,&solb;\,  [0,1]\longrightarrow \{0{ \swarrow}x{ \searrow}1\}$
 where the map $[0,1]\longrightarrow \{0{ \swarrow}x{ \searrow}1\}$ sends $0$ to $0$, $1$ to $1$, and the rest $(0,1)$ to $x$

*  a space $X$ is hereditary normal iff 
$ \emptyset \to X &solb; 
\{ x \leftarrow au \leftrightarrow u' \leftarrow u \leftarrow uv \rightarrow v \rightarrow v'\leftrightarrow bv \rightarrow x \} 
\longrightarrow
\{ x \leftarrow au \leftrightarrow u' = u \leftarrow uv \rightarrow v = v'\leftrightarrow bv \rightarrow x \} $


*   a space $X$ is path-connected iff $\{0,1\} \longrightarrow  [0,1] \,&solb;\,   {X} \longrightarrow  \{o\}$
*   a space $X$ is path-connected iff for each Hausdorff compact space $K$ and each injective map $\{x,y\} \hookrightarrow  K$ it holds
   $\{x,y\} \hookrightarrow   {K} \,&solb;\,   {X} \longrightarrow  \{o\}$

* A map $X\longrightarrow Y$ is a quotient iff $X\to Y \,\,&solb;\,\, \{o \rightarrow c\}\longrightarrow \{o\leftrightarrow c\}$
* For every pair of disjoint closed subsets of $X$, the closures of their images  of $Y$ do not intersect, if
$X\to Y \,\,&solb;\,\,  \{x\leftarrow o\rightarrow y\}\longrightarrow \{x=o=y\}$

* A topological space $X$ is extremally disconnected iff 
$\emptyset\to X \,\,&solb;\,\, \{u\rightarrow a,b\leftarrow v\}\longrightarrow \{u\rightarrow a=b\leftarrow v\}$

* A topological space $X$ is zero-dimensional iff 
$\emptyset\to X \,\,&solb;\,\, \{a\leftarrow u,v\rightarrow b\}\longrightarrow \{a\leftarrow u=v\rightarrow b\}$

* A topological space $X$ is ultranormal iff 
$\emptyset\to X \,\,&solb;\,\, \{u\rightarrow a,b\leftarrow v\}\longrightarrow \{a\leftarrow u=v\rightarrow v\}$

*  $\{\bullet\}\longrightarrow A$ is in $(\emptyset\longrightarrow \{o\})^{&solb;rll}$ iff $A$ is connected

*  $Y$ is totally disconnected iff $\{\bullet\}\xrightarrow y Y$ is in $(\emptyset\longrightarrow \{o\})^{&solb;rllr}$ for each map  $\{\bullet\}\xrightarrow y Y$ (or, 
in other words, each point $y\in Y$).



*   a Hausdorff space $K$ is compact iff $K\longrightarrow \{o\}$ is in  $((\{o\}\longrightarrow \{o{ \searrow}c\})^{&solb;r}_{\le5})^{&solb;lr}$
*   a  Hausdorff space $K$ is compact iff $K\longrightarrow \{o\}$ is in  $$
     \{\, \{a\leftrightarrow b\}\longrightarrow \{a=b\},\, \{o{ \searrow}c\}\longrightarrow \{o=c\},\,
     \{c\}\longrightarrow \{o{ \searrow}c\},\,\{a{ \swarrow}o{ \searrow}b\}\longrightarrow \{a=o=b\}\,\,\}^{&solb;lr}$$

* a topological space $X$ is compactly generated iff 
$\varnothing\longrightarrow X$ is in  $\big(\{\{0 \leftrightarrow 1\}\to\{0=1\}\}\cup\{\varnothing \to K \,\,:\,\, K\,\, \text{ compact}\}\big)^{&solb;rl}$

*   a space $D$ is discrete iff $ \emptyset \longrightarrow  D$ is in $   (\emptyset\longrightarrow \{o\})^{&solb;rl}      $

*   a space $D$ is codiscrete iff $  {D} \longrightarrow  \{o\} $ is in  
$(\{a,b\}\longrightarrow \{a=b\})^{&solb;rr}= (\{a\leftrightarrow b\}\longrightarrow \{a=b\})^{&solb;lr} $ 

*   a space $K$ is connected or empty iff $K\longrightarrow \{o\}$ is in  $(\{a,b\}\longrightarrow \{a=b\})^{&solb;l} $
*   a space $K$ is totally disconnected and non-empty iff $K\longrightarrow \{o\}$ is in  $(\{a,b\}\longrightarrow \{a=b\})^{&solb;lr} $

*   a space $K$ is connected and non-empty
 iff
 for some arrow $\{o\}\longrightarrow K$
it holds that $\{o\}\longrightarrow K$ is in
            $   (\emptyset\longrightarrow \{o\})^{&solb;rll} = (\{a\}\longrightarrow \{a,b\})^{&solb;l}$


* A topological space $X$ has Lebesgue dimension at most $n$  iff 
for each finite set $I$
$\emptyset\to X \,\,&solb;\,\, 
\{ (F,J): 1\leq |F|\leq n+1, F\subset J\subset I\}\longrightarrow
\{ J: 1\leq |J|, J\subset I\} 
$
where the order on the domain 
$\{ (F,J): 1\leq |F|\leq n+1, F\subset J\subset I\}$ is given by
$(F,J)\to (F',J')$ iff $F\subset F'$ and $J\subset J'$.

* A topological space $X$ has Lebesgue dimension at most $n$  iff 
for each closed subset $A$ of $X$ $
A\to X \,\,&solb;\,\, \mathbb{S}^n\to \{o\}$
where $\mathbb{S}^n$ denotes the $n$-sphere.

#### Homotopy theory

A finite CW complex $X$ is contractible iff  $X  \longrightarrow  {\{\bullet\}} \in \{   \{a{ \swarrow}U{ \searrow}x{ \swarrow}V{ \searrow}b\}\longrightarrow \{a{ \swarrow}U=x=V{ \searrow}b\}\}^{&solb;rl}$

The map defining Separation Axiom $T_4$ above 
is a trivial Serre fibration, hence their ${}^{&solb;rl}$-orthogonals are classes of trivial fibrations.


\begin{conjecture} If $f$ is a "nice" map, then 
$f$ is a trivial fibration iff 
$$f\in\{  \{a{ \swarrow}U{ \searrow}x{ \swarrow}V{ \searrow}b\}\longrightarrow \{a{ \swarrow}U=x=V{ \searrow}b\}
\}^{&solb;rl}$$
\end{conjecture}

One can make the same conjecture for the map
defining Separation Axiom $T_6$ (hereditary normal) since it is also a trivial Serre fibration.



### Model theory 

In model theory, 
a number of the Shelah's divining lines,
namely  $NOP, NSOP, NSOP_i, NTP, NTP_i$, and $NATP$
are [[situs|expressed as Quillen lifting properties of form]] 
$$A_\bullet \to B_\bullet \rightthreetimes M_\bullet\to\top$$  
where $\top$ is the terminal object, and 
$M$ is a situs associated with a model and a formula,
and $A$ and $B$ are objects of combinatorial nature,
in the category of simplicial objects in the [[category of filters]]. 









## Related concepts

* [[factorization system]], [[weak factorization system]]

* [[homotopy lifting property]]

* [[Kan lift]]

* [[Joyal-Tierney calculus]]

* [[lifts and extensions]]

* [Tychonoff theorem -- Proof via lifting properties](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties)

* [covering space lifting properties](covering+space#LiftingProperties)


[[!redirects lifts]]

[[!redirects lifting]]
[[!redirects liftings]]

[[!redirects lifting property]]
[[!redirects lifting properties]]

[[!redirects right lifting property]]
[[!redirects left lifting property]]
[[!redirects right lifting properties]]
[[!redirects left lifting properties]]


[[!redirects lifting problem]]
[[!redirects lifting problems]]


