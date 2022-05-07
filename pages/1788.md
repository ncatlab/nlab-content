

*  $\{\bullet\}\lra A$ is in $(\emptyset\longrightarrow \{o\})^{rll}$ iff $A$ is connected

* $Y$ is totally disconnected iff $\{\bullet\}\xra y Y$ is in $(\emptyset\longrightarrow \{o\})^{rllr}$ for each map  $\{\bullet\}\xra y Y$ (or, 
in other words, each point $y\in Y$).



*   a Hausdorff space $K$ is compact iff $K\longrightarrow \{o\}$ is in  $((\{o\}\longrightarrow \{o{ \searrow}c\})^r_{\le5})^{lr}$
*   a  Hausdorff space $K$ is compact iff $K\longrightarrow \{o\}$ is in  $$
     \{\, \{a\leftrightarrow b\}\longrightarrow \{a=b\},\, \{o{ \searrow}c\}\longrightarrow \{o=c\},\,
     \{c\}\longrightarrow \{o{ \searrow}c\},\,\{a{ \swarrow}o{ \searrow}b\}\longrightarrow \{a=o=b\}\,\,\}^{lr}$$

*   a space $D$ is discrete iff $ \emptyset \longrightarrow  D$ is in $   (\emptyset\longrightarrow \{o\})^{rl}      $

*   a space $D$ is antidiscrete iff $  {D} \longrightarrow  \{o\} $ is in  
$(\{a,b\}\longrightarrow \{a=b\})^{rr}= (\{a\leftrightarrow b\}\longrightarrow \{a=b\})^{lr} $ 

*   a space $K$ is connected or empty iff $K\longrightarrow \{o\}$ is in  $(\{a,b\}\longrightarrow \{a=b\})^l $
*   a space $K$ is totally disconnected and non-empty iff $K\longrightarrow \{o\}$ is in  $(\{a,b\}\longrightarrow \{a=b\})^{lr} $

*   a space $K$ is connected and non-empty
 iff
 for some arrow $\{o\}\longrightarrow K$
$\text{ \ \ \ \ \     } \{o\}\longrightarrow K$ is in
            $   (\emptyset\longrightarrow \{o\})^{rll} = (\{a\}\longrightarrow \{a,b\})^l$

*   a space $K$ is non-empty iff $K\longrightarrow \{o\}$ is in $   (\emptyset\longrightarrow \{o\})^l$
*   a space $K$ is empty iff $K \longrightarrow \{o\}$ is in $   (\emptyset\longrightarrow \{o\})^{ll}$
*   a space $K$ is $T_0$ iff $K  \longrightarrow \{o\}$ is in $   (\{a\leftrightarrow b\}\longrightarrow \{a=b\})^r$
*    a space $K$ is $T_1$ iff $K  \longrightarrow \{o\}$ is in $   (\{a{ \searrow}b\}\longrightarrow \{a=b\})^r$
*   a space $X$ is Hausdorff iff for each injective map $\{x,y\} \hookrightarrow  X$
it holds $\{x,y\} \hookrightarrow   {X} \,\rightthreetimes\,  \{  {x} { \searrow}  {o} { \swarrow}  {y} \} \longrightarrow  \{ x=o=y \}$

*   a non-empty space $X$ is regular (T3) iff for each arrow $    \{x\} \longrightarrow  X$ it holds
    $    \{x\} \longrightarrow   {X} \,\rightthreetimes\,  \{x{ \searrow}X{ \swarrow}U{ \searrow}F\} \longrightarrow  \{x=X=U{ \searrow}F\}$
*   a space $X$ is normal (T4) iff $\emptyset \longrightarrow  {X} \,\rightthreetimes\,   \{a{ \swarrow}U{ \searrow}x{ \swarrow}V{ \searrow}b\}\longrightarrow \{a{ \swarrow}U=x=V{ \searrow}b\}$

*   a space $X$ is completely normal iff $\emptyset\longrightarrow  {X} \,\rightthreetimes\,  [0,1]\longrightarrow \{0{ \swarrow}x{ \searrow}1\}$
 where the map $[0,1]\longrightarrow \{0{ \swarrow}x{ \searrow}1\}$ sends $0$ to $0$, $1$ to $1$, and the rest $(0,1)$ to $x$

*  a space $X$ is hereditary normal iff 
$ \emptyset \to X \rightthreetimes 
\{ x \la au \leftrightarrow u' \la u \la uv \ra v \ra v'\leftrightarrow bv \ra x \} 
\longrightarrow
\{ x \la au \leftrightarrow u' = u \la uv \ra v = v'\leftrightarrow bv \ra x \} $


*   a space $X$ is path-connected iff $\{0,1\} \longrightarrow  [0,1] \,\rightthreetimes\,   {X} \longrightarrow  \{o\}$
*   a space $X$ is path-connected iff for each Hausdorff compact space $K$ and each injective map $\{x,y\} \hookrightarrow  K$ it holds
   $\{x,y\} \hookrightarrow   {K} \,\rightthreetimes\,   {X} \longrightarrow  \{o\}$



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

### Lift of morphisms

A **lift** of a morphism $f: Y\to B$ along an [[epimorphism]] (or more general map) $p:X\to B$ is a morphism $\tilde{f}: Y\to X$ such that $f = p\circ\tilde{f}$.

The dual problem is the [[extension]] of a morphism $f: A\to Y$ along a monomorphism $i: A\hookrightarrow X$, which is a morphism $\tilde{f}:X\to Y$ such that $\tilde{f}\circ i = f$. One sometimes extends along more general morphisms than monomorphisms. 

## Idea


The '''lifting property''' is a property of a pair of [[morphism (category theory)|morphism]]s in a [[category (mathematics)|category]]. It is used in [[homotopy theory]] within [[algebraic topology]] to define properties of morphisms starting from an explicitly given class of morphisms. It appears in a prominent way in the theory of [[model categories]], an axiomatic framework for [[homotopy theory]] introduced by [[Daniel Quillen]]. It is also used in the definition of a [[factorization system]], and of a [[weak factorization system]], notions related to but less restrictive than the notion of a model category. A number of elementary notions may also be expressed using the lifting property starting from a list of (counter)examples.

\begin{definition}
A morphism ''i'' in a category has the ''left lifting property'' with respect to a morphism ''p'', and ''p'' also has the ''right lifting property'' with respect to ''i'', sometimes denoted $i\,\,&solb;\,\, p$ or $i\downarrow p$, iff the following implication holds for each morphism ''f'' and ''g'' in the category:

* if the outer square of the following diagram commutes, then there exists ''h'' completing the diagram, i.e. for each $f:A\to X$ and $g:B\to Y$ such that $p\circ f = g \circ i$ there exists $h:B\to X$ such that $h\circ i = f$ and $p\circ h = g$.


\begin{tikzcd}
[
  column sep={between origins, 160pt},
  row sep={between origins, 40pt}
]
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
    "{ \exists }"
  ]
  &&Y
\end{tikzcd}
\end{definition}

This is sometimes also known as the morphism ''i'' being ''weakly orthogonal to'' the morphism ''p''; however, this can also refer to
the stronger property that whenever ''f'' and ''g'' are as above, the diagonal morphism ''h'' exists and is also required to be unique.

For a class ''C'' of morphisms in a category, its ''left weak orthogonal'' or its ''left Quillen negation''
 $C^{&solb; \ell}$ with respect to the lifting property, respectively its ''right weak orthogonal'' and its ''right Quillen negation'' 
$C^{&solb;r}$  is the class of all morphisms which have the left, respectively right, lifting property 
with respect to each morphism in the class ''C''. In notation,

$$
C^{&solb; \ell} := \{ i \mid \forall p\in C, i\,\,&solb;\,\, p\} \,\,\,
C^{&solb; r} := \{ p \mid \forall i\in C, i\,\,&solb;\,\, p\}, \,\,\,
C^{&solb; lr} := (C^{&solb; r})^{&solb; r}  
$$ 

Taking the orthogonal of a class ''C'' is a simple way to define a class of morphisms excluding [[isomorphisms]] from ''C'', in a way which is useful in a [[diagram chasing]] computation.

Thus, in the category '''Set''' of [[Set (mathematics)|sets]], the right orthogonal $\{\emptyset \to \{*\}\}^{&solb;  r}$ of the simplest [[surjective|non-surjection]] $\emptyset\to \{*\},$ is the class of surjections. The left and right orthogonals of $\{x_1,x_2\}\to \{*\},$ the simplest [[Injective|non-injection]], are both precisely the class of injections, 

:$\{\{x_1,x_2\}\to \{*\}\}^{&solb; \ell} = \{\{x_1,x_2\}\to \{*\}\}^{&solb;  r} = \{ f \mid f \text{ is an injection } \}.$

It is clear that $C^{&solb;\ell r} \supset C$ and $C^{&solb; r\ell} \supset C$. The class $C^{&solb;  r}$ is always closed under retracts, [[Pullback (category theory)|pullbacks]], (small) [[Product (category theory)|products]] (whenever they exist in the category) and composition of morphisms, and contains all isomorphisms of C. Meanwhile, $C^{&solb;  \ell}$ is closed under retracts, [[Pushout (category theory)|pushouts]], (small) [[Coproduct (category theory)|coproducts]] and transfinite composition ([[filtered colimit]]s) of morphisms (whenever they exist in the category), and also contains all isomorphisms.

==Examples==
A number of notions can be defined by passing to the left or right orthogonal several times starting from a list of explicit examples, i.e. as $C^{&solb; \ell}, C^{&solb;  r}, C^{&solb; \ell r}, C^{&solb; \ell\ell}$, where $C$ is a class consisting of several explicitly given morphisms. A useful intuition is to think that the property of left-lifting against a class ''C'' is a kind of negation
of the property of being in ''C'', and that right-lifting is also a kind of negation. Hence the classes obtained from ''C'' by taking orthogonals an odd number of times, such as $C^{&solb; \ell}, C^{&solb;  r}, C^{&solb; \ell r\ell}, C^{&solb; \ell\ell\ell}$ etc., represent various kinds of negation of ''C'', so $C^{&solb; \ell}, C^{&solb;  r}, C^{&solb; \ell r\ell}, C^{&solb; \ell\ell\ell}$ each consists of morphisms which are far from having property $C$.

## Examples of lifting properties in algebraic topology
A map $f:U\to B$ has the ''path lifting property'' iff $\{0\}\to [0,1] \,\,&solb;\,\, f$ where $\{0\} \to [0,1]$ is the inclusion of one end point of the closed interval into the interval $[0,1]$.

A map $f:U\to B$ has the [[homotopy lifting property]] iff $X \to X\times [0,1] \,\,&solb;\,\, f$ where $X\to X\times [0,1]$ is the map $x \mapsto (x,0)$.

##Examples of lifting properties coming from model categories

###Fibrations and cofibrations.

* Let '''Top''' be the category of [[topological space]]s, and let $C_0$ be the class of maps $S^n\to D^{n+1}$, [[embedding]]s of the boundary $S^n=\partial D^{n+1}$ of a ball into the ball $D^{n+1}$. Let $WC_0$ be the class of maps embedding the upper semi-sphere into the disk. $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$ are the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations.[Hovey, Model Categories, Def. 2.4.3, Th.2.4.9](https://archive.org/details/arxiv-math9803002)

* Let '''sSet''' be the category of [[simplicial set]]s. Let $C_0$ be the class of boundary inclusions $\partial \Delta[n] \to \Delta[n]$, and let $WC_0$ be the class of horn inclusions $\Lambda^i[n] \to \Delta[n]$. Then the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations are, respectively, $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$.
[Model Categories, Def. 3.2.1, Th.3.6.5](https://archive.org/details/arxiv-math9803002)

* Let '''Ch'''(''R'') be the category of [[chain complex]]es over a [[commutative ring]] ''R''. Let $C_0$ be the class of maps of form
:: $\cdots\to 0\to R \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots,$
: and $WC_0$ be
:: $\cdots \to 0\to 0 \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots.$
:Then $WC_0^{&solb; \ell}, WC_0^{&solb; \ell r}, C_0^{&solb; \ell}, C_0^{&solb; \ell r}$ are the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations.
[Model Categories, Def. 2.3.3, Th.2.3.11](https://archive.org/details/arxiv-math9803002)

# Elementary examples in various categories

## Sets
In '''Set''', 

* $\{\emptyset\to \{*\}\}^{&solb;  r}$ is the class of surjections,

* $(\{a,b\}\to \{*\})^{&solb;  r}=(\{a,b\}\to \{*\})^{&solb; \ell}$ is the class of injections.

## Modules
In the category ''R''-'''Mod''' of [[Module (mathematics)|modules]] over a commutative ring ''R'',

* $\{0\to R\}^{&solb;  r}, \{R\to 0\}^{&solb;  r}$ is the class of surjections, resp. injections,

* A module ''M'' is [[Projective module|projective]], resp. [[Injective module|injective]], iff $0\to M$ is in $\{0\to R\}^{&solb; \ell r}$, resp. $M\to 0$ is in $\{R\to 0\}^{&solb;  rr}$.

## Groups
In the category '''Grp''' of [[Group|groups]], 

* $\{\mathbb{Z} \to 0\}^{&solb;  r}$, resp. $\{0\to \mathbb{Z}\}^{&solb;  r}$, is the class of injections, resp. surjections (where $\mathbb{Z}$ denotes the infinite [[cyclic group]]),

* A group ''F'' is a [[free group]] iff $0\to F$ is in $\{0\to \mathbb{Z} \}^{&solb;  r\ell},$

* A group ''A'' is [[Torsion (algebra)|torsion-free]] iff $0\to A$ is in $\{ n \mathbb{Z} \to \mathbb{Z} : n\ge0 \}^{&solb;  r},$

* A [[subgroup]] ''A'' of ''B'' is [[Pure subgroup|pure]] iff $A \to B$ is in $\{ n\mathbb{Z}\to \mathbb{Z} : n\ge0 \}^{&solb;  r}.$

For a [[finite group]] ''G'', 

* $\{0\to {\mathbb{Z}}/p{\mathbb{Z}}\} \,\,&solb;\,\, G\to 1$ iff the [[Order (group theory)|order]] of ''G'' is prime to ''p'',

* $G\to 1 \in (0\to {\mathbb{Z}}/p{\mathbb{Z}})^{&solb;  rr}$ iff ''G'' is a [[p-group|''p''-group]],

* ''H'' is nilpotent iff the diagonal map $H\to H\times H$ is in $(1\to *)^{&solb; \ell r}$ where $(1\to *)$ denotes the class of maps $\{ 1\to G : G \text{ arbitrary}\},$

* a finite group ''H'' is [[Soluble group|soluble]] iff $1\to H$ is in $\{0\to A : A\text{ abelian}\}^{&solb; \ell r}=\{[G,G]\to G : G\text{ arbitrary } \}^{&solb; \ell r}.$


## [[Uniform spaces]] 

In the category of [[uniform  space]]s or [[metric space]]s with [[uniformly continuous]] maps.

* A space ''X'' is [[Complete metric space|complete]] iff $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}} \,\,&solb;\,\, X\to \{0\}$ where $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}}$ is the obvious inclusion between the two subspaces of the real line with induced metric, and $\{0\}$ is the metric space consisting of a single point,

* A subspace $i:A\to X$ is closed iff $\{1/n\}_{n \in \mathbb{N}} \to \{0\}\cup \{1/n\}_{n \in \mathbb{N}} \,\,&solb;\,\, A\to X.$



# Topological spaces 

Many elementary properties in general topology, such as compactness, being dense or open, 
can be expressed as iterated Quillen negation of morphisms of finite topological spaces
in the category '''Top''' of topological spaces. This leads to a concise, if useless, notation 
for a number of properties. This items uses notation for morphisms of finite topological spaces 
defined in the page on [[separation axioms in terms of lifting properties]].

## Examples of interated Quillen negations defining natural properties

*         $(\emptyset\longrightarrow \{o\})^r$   is the class of surjections
*         $(\emptyset\longrightarrow \{o\})^r$   is the class of maps $A\lra B$ where $A\mathbb{N}eq \emptyset$ or $A=B$
*         $(\emptyset\longrightarrow \{o\})^{rr}$ is the class of subsets, i.e. injective maps $A\hookrightarrow B$ where the topology on $A$ is induced from $B$

*  $(\emptyset\longrightarrow \{o\})^{lr}$ is the class of maps $\emptyset\longrightarrow B$, $B$ arbitrary
*         $(\emptyset\longrightarrow \{o\})^{lrr}$ is the class of maps $A\longrightarrow B$ which admit a section 


*   $(\emptyset\longrightarrow \{o\})^l$ consists of maps $f:A\longrightarrow B$ such that either  $A\mathbb{N}eq \emptyset$ or  $A=B=\emptyset$  



*  $(\emptyset\longrightarrow \{o\})^{rl}$ is the class of maps of form $A\longrightarrow A\sqcup D$ where $D$ is discrete

*  $\{ \{z\llrra x\llrra y\ra c\}\lra\{z=x\llrra y=c\} \}^\lrl  = \{\{c\}\lra \{o\ra c\}\}^\lr$ is the class of closed inclusions $A\subset B$ where $A$ is closed

*  $\{ \{z\llrra x\llrra y\la c\}\lra\{z=x\llrra y=c\} \}^\lrl$ is the class of open inclusions
$A\subset B$ where $A$ is open

*  $\{ \{x\llrra y\ra c\}\lra\{x\llrra y=c\} \}^\lrl $ is the class of closed maps $A\lra B$ 
where the topology on $A$ is pulled back from $B$
*  $\{ \{x\llrra y\la c\}\lra\{x\llrra y=c\} \}^\lrl$ is the class of open maps $A\lra B$ 
where the topology on $A$ is pulled back from $B$


*         $(\{b\}\longrightarrow \{a{\small\searrow}b\})^l$ is the class of maps with dense image
*         $(\{b\}\longrightarrow \{a{\small\searrow}b\})^{lr}$ is the class of closed subsets $A \subset  X$, $A$ a closed subset of $X$
*         $(\{a\}\longrightarrow \{a{\small\searrow}b\})^{lr}$ is the class of subsets $A \subset  X$ such that $A$ is the intersection of open subsets containing $A$
%+       $(\emptyset\longrightarrow \{o\})^l$ is the class of maps $A\longrightarrow B$ such that $A=B=\emptyset$ or $A\mathbb{N}eq\emptyset$, $B$ arbitrary
	%+       $(\emptyset\longrightarrow \{o\})^l$ is the class of maps $A\longrightarrow B$ such that $A=B=\emptyset$ or $A\mathbb{N}eq\emptyset$, $B$ arbitrary

*  $( \{a{\small\searrow}b\}\lra\{a=b\})^l$ is the class of injections
%*  $( \{a{\small\searrow}b\}\lra\{a=b\}$)^{ll}$

*         $((\{a\}\longrightarrow \{a{\small\searrow}b\})^r_{\le5})^{lr}$ is roughly the class of proper maps




