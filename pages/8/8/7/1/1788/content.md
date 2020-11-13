[[!redirects categories]]
[[!redirects category]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Basic category theory
+--{: .hide}
[[!include Basic category theory content]]
=--
#### Category theory
+--{: .hide}
[[!include Category theory content]]
=--
=--
=--

\tableofcontents

## Categories

### Definition

A _category_ $\mathbf{C}$ consists of 

* a [[set]] $\mathbf{C}_0$ of _[objects]_;

* for each pair of objects $A,B\in \mathbf{C}_0$, a set $\mathbf{C}(A,B)$ of _[morphisms]_ (or _[arrows]_, or _maps_) $A\to B$ with _[domain]_ $A$ and _[codomain]_ $B$  (or with _[source]_ $A$ and _[target]_ $B$); when the context is clear,  we write $f:A\to B$ or write,
\begin{xymatrix}A\ar[r]^f & B,
\end{xymatrix}
to indicate that $f\in \mathbf{C}(A,B)$;

* for each triples of objects $A,B,C\in \mathbf{C}_0$, a _[composition law]_, $\mathbf{C}(B,C)\times \mathbf{C}(A,B)\to \mathbf{C}(A,C);$  
 when the context is clear, we write $g f:A\to C$ for the composite of  $f:A\to B$ with $g:B\to C$;

* for each object $A\in \mathbf{C}_0$, a morphism  $1_A:A\to A$ called the _[unit morphism]_ or the _[identity morphism]_ of $A$;


* such that the following conditions are satisfied:

  * (*[associativity law]*) $h (g f)=(h g) f$ for every triple of morphisms $f:A\to B$, $g:B\to C$ and $h:C\to D$;

  * (*[the unit law]*) $1_B f=f 1_A =f$ for every morphism $f:A\to B$.
=--

### Notation

The set $\mathbf{C}_0$ of objects of a category $\mathbf{C}$ is often denoted $Ob(\mathbf{C})$. When the context is clear,
we shall often write $A\in \mathbf{C}$ instead of $A\in Ob(\mathbf{C})$; we shall often denote the set 
$\mathbf{C}(A,B)$ by $hom_{\mathbf{C}}(A,B)$, and more simply
by $hom(A,B)$ ($hom(A,B)$ is the set of _homomorphisms_ $A\to B$). 
We often use diagrams in category theory. We say that a triangle
of arrows
\begin{xymatrix}A\ar[r]^{f}\ar[dr]_{h}& B \ar[d]^{g}\\ & C.
\end{xymatrix}
_commutes_ if $h=g f$, and that a square of arrows
\begin{xymatrix}A\ar[r]^{f}\ar[d]_{u}& B \ar[d]^{v}\\ C\ar[r]_{g}& D
\end{xymatrix}
_commutes_ if $g u=v f$.


### Size issues 

The sets involved in the definition of a category can be [[small]] or 
[[large]]. A category $\mathbf{C}$ is said to be _locally small_ if the set 
$\mathbf{C}(A,B)$ is small for every pair of objects $A,B\in \mathbf{C}$. 
A locally small category $\mathbf{C}$ is said to be _[small]_  if 
the $Ob(\mathbf{C})$ is small.
A category which is not small is said to be _large_. 


### Examples

* We shall denote by $\mathbf{Set}$, the category of _small sets_: an object of this category is a small set $S$ and a morphism is a
function $f:S\to T$; the composition law is the usual composition of functions, and the unit
morphisms are the identity functions. The category $\mathbf{Set}$ is large but locally small.


* Let $R$ be a ring. We shall denote by $Mat(R)$ the 
_category of matrices_ with coefficients in $R$; an object of this category is a natural number $n\geq 0$ and a morphism $m\to n$
is a $n\times m$ matrix with coefficients in $R$; the composite of
a matrix $A:m\to n$ with a matrix $B:n\to p$ is their product $B A:m\to p$;
the unit of $n$ is the $n\times n$ unit matrix. The category $Mat(R)$
is small.



* $\mathbf{Grp}$ - [[groups]] as objects, group homomorphisms as morphisms.

* $\mathbf{Ab}$- [[abelian groups]] as objects, group homomorphisms as morphisms.


* $\mathbf{Ring}$ - [[rings]] as objects, ring homomorphisms as morphisms.

* $K\mathbf{Vect}$ - [[K-vector spaces]] as objects, $K$-linear maps as morphisms.

* $\mathbf{Top}$ - [[topological spaces]] as objects, continuous maps as morphisms.

* $\mathbf{SMan}$ - [[smooth manifolds]] as objects, smooth maps as morphisms.
 
These classical examples are the original motivation for the term "category": all of the above categories encapsulate one "kind of mathematical structure".  These are often called "concrete" categories (that term also has a [[concrete category|technical definition]] that these examples all satisfy).  


* **Poset** A [[partial order|poset]] can be thought of as a category with its elements as objects and one morphism in each $hom(x,y)$ if $x$ is less than or equal to $y$, but none otherwise. 


* **Monoid**  A monoid $M$ can be thought of as a category $C$
with a single object $\star$ and with $C(\star,\star)=M$.
It is sometime useful to distinguish between a monoid $M$ and the
associated category with a single object by denoting the latter $\mathbf{B}M$. The category $\mathbf{B}M$ is often called the _classifying category_ of $M$.

* The [[simplicial category]] $\Delta$ has objects the ordered sets
$[n]=\{0,\ldots,n\}$ for $n\geq 0$, and for morphisms the order
preserving maps $[n]\to [m]$.



## Opposite category

* The _opposite_ of a category $\mathbf{C}$ is the category $\mathbf{C}^o$ obtained
by formally reversing the direction of the arrows of $\mathbf{C}$. 
It is sometimes useful to distinguish between the objects
of $\mathbf{C}$ and of $\mathbf{C}^o$ by denoting the object of $\mathbf{C}^o$ which corresponds to an object $A\in \mathbf{C}$ by $A^o\in \mathbf{C}^o$ and by denoting the arrow which corresponds to an arrow $f\in \mathbf{C}(A,B)$ by $f^o\in \mathbf{C}^o(B^o,A^o)$.
If $f\in \mathbf{C}(A,B)$ and $g\in \mathbf{C}(B,C)$, then
the composite of $g^o\in \mathbf{C}^o(C^o,B^o)$ with 
$f^o\in \mathbf{C}^o(B^o,A^o)$ is defined 
by putting $f^o g^o= (g f)^o$,
\begin{xymatrix}A^o & B^o\ar[l]_{f^o} \\ &
\ar[ul]^{f^o g^o} \ar[u]_{g^o} C^o.
\end{xymatrix}
By convention, we shall put $(A^o)^o=A$ and $(f^o)^o=f$ for every object $A\in \mathbf{C}$ and arrow $f\in \mathbf{C}$. This means that we have
 $$(\mathbf{C}^o)^o=\mathbf{C}.$$


The fact that every category has an opposite is the basis of a
fundamental **duality principle** of category theory. To every statement $P(\mathbf{C})$ about the objects and arrows a general category $\mathbf{C}$ corresponds a dual statement 
$P^o(\mathbf{C})\equiv P(\mathbf{C}^o)$ about the objects and arrows of the opposite category. This is analogous to the duality in projective geometrie:
to every statement $P$ about the points and lines of a projective
plane $\Pi$ corresponds a dual statement $P^*$ about the points and lines of the dual projective plane $\Pi^*$.

 


## Special morphisms

### Isomorphisms


* Let $f:A\to B$ and $g:B\to A$ be two morphisms in a category.
If $g f=1_A$ and $f g=1_B$ we say that $g$ is the _inverse_ of $f$. 
The inverse is unique when it exists and we write $g=f^{-1}$.  
A morphism which admits an inverse is said to be _[invertible]_ ,
or to be an _[isomorphism]_.  


* A category $\mathbf{C}$ is said to be a _[[groupoid]]_ if every morphism of $\mathbf{C}$ is invertible.



### Endomorphisms


* An _endomorphism_ of an object $A$ is a morphism $f:A\to A$.
The composition law gives the set of endomorphisms $End(A)=hom(A,A)$ the structure of a monoid, the _monoid of endomorphisms_ of $A$. 


* An _automorphism_ of an object $A$ is an endomorphism of $A$ which is invertible. The composition law gives the set of automorphisms of $A$ the structure of a group, the  _group of automorphisms_ of $A$.

 * An endomorphism $e:A\to A$ is said to be _idempotent_ if $e e=e$. 



### Monomorphisms

* A morphism $f:A\to B$ in a category is said to be _[monic]_ ,
or to be a _[monomorphism]_ if the implication 

 $$f u = f v \Rightarrow u=v$$

 is true for every pair of morphism $u,v:A\to B$.


### Epimorphisms

* A morphism $f:A\to B$ in a category is said to be _epic_ ,
or to be an _epimorphism_ if the implication 

$$u f =v f \Rightarrow u=v$$

is true for every pair of morphism $u,v:B\to C$.
A morphism $f:A\to B$ is epic iff the opposite
morphism $f^o:B^o\to A^o$ is monic.
Hence the notion of epimorphism is *dual* to the
notion of monomorphism.

 
### Sections, retractions

* Let $f:A\to B$ and $g:B\to C$ be two morphisms in a category.
If $g f =1_A$, we say that $g$ is a _left inverse_ of $f$
and that $f$ is a _right inverse_ of $g$. A morphism which admits a left inverse is monic, it is called a *split monomorphism*. A morphism which admits a right inverse is epic, it is called a *split epimorphism*.  The notion of split epimorphism
is dual to the notion of split monomorphism.
A left inverse of a morphism $f$
is sometimes called a _retraction_ of $f$, and a right
inverse a _section_.


* If $f:A\to B$, $g:B\to A$ and $g f=1_A$, then the composite 
$f g:B\to B$ is idempotent.

* An idempotent $e:B\to B$ is said to be _split_ if there exists
an object $A$ together with a pair of morphism $f:A\to B$ and $g:B\to A$ such that $g f=1_A$ and $f g=e$. 

### Examples

* A map $f:S\to T$ in the category of sets $\mathbf{Set}$ is invertible iff it is *bijective*. 

* An isomorphism in the category of topological spaces $\mathbf{Top}$ is said to be a _homeomorphism_.


* An isomorphism in the category of smooth manifolds $\mathbf{SMan}$ is said to be a _diffeomorphism_.

* The isomorphisms in a category $\mathbf{C}$ form a groupoid $Iso(\mathbf{C})$ with the same objects as $\mathbf{C}$. It is the _groupoid of isomorphisms_ of $\mathbf{C}$.


* An automorphism of a set is often called a _permutation_.
The group of permutations of the set ${\underline n}=\{1,\ldots, n\}$ is the [[symmetric group]] $\Sigma_n$ of degree $n$.   

* Let $R$ be a ring. In the category of  $Mat(R)$, the group of automorphisms of the object $n$ is the [[general linear group]] $GL(n,R)$.


* In the category of sets $\mathbf{Set}$, a map is monic iff it is _injective_, and it is epic iff it is surjective.

* In a poset, every morphism is monic and epic.




## Groupoids

* A _[groupoid]_ is a category in which every morphism is invertible.


### Examples


* Every type of mathematical structure carries with it
a notion of isomorphism. Hence the collection of all structures
of a given type form a groupoid. 

* The isomorphisms in a category $\mathbf{C}$ form a groupoid $Iso(\mathbf{C})$ 
having the same objects as $\mathbf{C}$, the 
_groupoid of isomorphisms_ of $\mathbf{C}$.


* A *group* is essentially a groupoid with a single object.
The classifying category of a group $G$ is a groupoid
with a single object $\mathbf{B}G$.
In fact, groupoids are the [[horizontal categorification|many object version]] of groups.


### Isomorphism classes

* Two objects $A$ and $B$ of a category $\mathbf{C}$ are said to be _isomorphic_, $A\simeq B$, if there exists an isomorphism $A\to B$. 
The relation $A\simeq B$ is symmetric, transitive and reflexive.
It is thus an equivalence relation between the objects of $\mathbf{C}$.
An equivalence class for this equivalence relation is said to be
an _isomorphism class_, or an _isomorphism type_.


* In the category of sets $\mathbf{Set}$, two sets $X$ and $Y$ are isomorphic iff they have the same cardinality. In fact, the notion of cardinal number as defined by Cantor is an isomorphism class of sets.

 

* Let us denote by $\mathbf{Ord}$ the category of ordered sets
and order preserving maps. Two ordered sets $X$ and $Y$ are
said to have the same _order type_ if they are isomorphic
in the category $\mathbf{Ord}$. An _ordinal number_ is defined to
be the order type of a well-ordered set.



* Let us denote by $K\mathbf{Vect}$ the category of (left or right) vector spaces over a field $K$. Every $K$-vector space $V$ has a basis,
and any two basis have the same cardinality. 
The dimension of $V$ is defined to be the cardinality of a basis.
Two objects of $K\mathbf{Vect}$  are isomorphic iff they the same dimension.




* Let us denote by $K\mathcal {F}$ the category of algebraically
closed field extensions of a commutative field $K$.
Every algebraically closed field extension $F$ of $K$ has a transcendance basis over $K$, and any two basis have the same cardinality. The transcendance dimension of $F$ over $K$
is defined to be the cardinality of a basis.
Two objects of $K\mathcal {F}$
are isomorphic iff they have the same transcendance dimension
over $K$.

 
 

## Exercises

* Prove that a morphism which is left and right invertible is invertible.

* Prove that the inverse of a morphism is unique when it exists.



* Show that the composite
of two isomorphisms $f: A \to B$ and $g:B \to C$
is an isomorphism and that we have $(g f)^{-1}=f^{-1}g^{-1}$. 



* Show that a category is a groupoid iff every morphism has a left inverse. 

* Show that the composite of two monomorphisms (resp. epimorphisms) is a monomorphism (resp. an epimorphism).

* Show that if the composite $g f$ of two morphisms
$f:A\to B$ and $g:B\to C$ is monic, then then so is $f$.
Dually, show that if $g f$ is epic, then so is $g$. 

* Show that a morphism which is right invertible is epic, and that a morphism which is left invertible is monic.

* Give an example of a morphism in a category which is both monic and epic without been invertible.

* Show that if a monomorphism has a right inverse, then it is invertible.
Dually, show that if an epimorphism has a left inverse, then it is invertible.


* Show that if an idempotent is monic or epic, then it 
is a unit.





