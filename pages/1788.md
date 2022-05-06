
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopical algebra
+--{: .hide}
[[!include Homotopical algebra content]]
=--
#### Category theory
+--{: .hide}
[[!include Category theory content]]
=--
=--
=--

\tableofcontents

##Model structures##

###Definitions###

+-- {: .num_defn #3for2}
###### Definition
We say that a class $\mathcal{W}$  of maps 
in a category $\mathbf{E}$ has the **three-for-two** property 
if for any commutative triangle
\begin{xymatrix}
A \ar[dr]_w \ar[r]^u & B\ar[d]^v\\
 & C
\end{xymatrix}
in which two of the three maps
belong to $\mathcal{W}$, then so is the third.
=--

+-- {: .un_remark #Qmodelstructdef}
######Remark
We call this property *three-for-two* rather than 
*two-for-three* because this is like getting *three apples for
the price of two* in a food store.
=--

+-- {: .num_defn #Qmodelstructdef}
######Definition
We shall say that a triple $(\mathcal{C},\mathcal{W},\mathcal{F})$ 
of classes of maps in finitely bicomplete category $\mathbf{E}$ is a **Quillen model structure**, or just a **model structure**, 
 if the following conditions are satisfied:
* the class $\mathcal{W}$ has the _three-for-two_ property; 
* The pairs $( \mathcal{C}\,\cap \,\mathcal{W},\mathcal{F})$ and 
$(\mathcal{C},\mathcal{F}\,\cap\, \mathcal{W})$ 
are weak factorisation systems.

A  **Quillen model category**, or just a **model category**,
is a category $\mathbf{E}$ equipped with a model structure.
=--


+-- {: .un_remark #Qmodelstructdef2}
######Remark
The definition above is equivalent to the notion of *closed model
structure* introduced by Quillen. The proof of the
equivalence depends on Tierney's lemma \ref{Wclosedunderretracts}
below.
=--


A map in $\mathcal{F}$ is called a **fibration**,
a map in $\mathcal{C}$ a **cofibration**
and a map in $\mathcal{W}$ a **weak equivalence**.
A map in $\mathcal{W}$ is also said to be **acyclic**.
It follows from the axioms that every
map $f:A\to B$ admits a factorisation $f=p u:A\to E\to B$
with $u$ an acyclic cofibration and $p$ a fibration,
and also a factorisation $f=q v:A\to F\to B$
with $v$ a cofibration and $q$ an acyclic fibration.


An object $X\in \mathbf{E}$ is said to be **fibrant**
if the map $X\to \top$ is a fibration, where $\top$
is the terminal object of $\mathbf{E}$. Dually, an object
$A\in \mathbf{E}$ is said to be **cofibrant**
if the map $\bot \to A$ is a cofibration, where $\bot$
is the initial object.
We shall say that an object is **fibrant-cofibrant**
if it is both fibrant and cofibrant.



A model structure is said to be **right proper** if the base change 
of a weak equivalence 
along a fibration is a weak equivalence. 
Dually, a model structure is said to be **left proper** if the cobase change
of a weak equivalence 
along a cofibration is a 
weak equivalence.
A model structure is said to be **proper**
if it is both left and right proper. 



+-- {: .un_example #trivialmodstr}
###### Example
We shall say that a model structure $( \mathcal{C},\mathcal{W},\mathcal{F})$ on a category $\mathbf{E}$ is **trivial**
if $\mathcal{W}$ is the class of isomorphisms,
in which case $\mathcal{C}=\mathbf{E}=\mathcal{F}$.
=--

+-- {: .un_example #coarsemodstr}
###### Example
We shall say that a model structure $( \mathcal{C},\mathcal{W},\mathcal{F})$ on a category $\mathbf{E}$
is **coarse** if $\mathcal{W}$ is the class of all maps,
in which case the pair $(\mathcal{C},\mathcal{F})$
is just an arbitrary weak factorisation system in the category $\mathbf{E}$.
=--

For less trivial examples, see \ref{Kanmodelstructurecat}.



+-- {: .un_prop #Qmodelsdual}
######Duality
If $( \mathcal{C},\mathcal{W},\mathcal{F})$ is a model structure
on a category $\mathbf{E}$, then the triple 
$(\mathcal{F}^o,\mathcal{M}^o,\mathcal{C}^o)$ is a model structure on the opposite category $\mathbf{E}^o$.
=--


If $B$ is an object of a category $\mathbf{E}$
and $\mathcal{M}$ is a class of maps in $\mathbf{E}$, we shall denote
by $\mathcal{M}/B$ the class of maps in $\mathbf{E}/B$
whose underlying map in $\mathbf{E}$ belongs to $\mathcal{M}$.
Dually, we shall denote by $B\backslash \mathcal{M}$ the class of maps in $B\backslash \mathbf{E}$ whose underlying map belongs to $\mathcal{M}$.


+--{: .un_prop #slicewfs}
######Slice and coslice
If $( \mathcal{C},\mathcal{W},\mathcal{F})$  is a model structure
on a category $\mathbf{E}$, then the triple
$(\mathcal{C}/B,\mathcal{W}/B, \mathcal{F}/B)$ is a model structure
in the slice category $\mathbf{E}/B$ for any object
$B\in \mathbf{E}$. Dually, the triple
$(B\backslash \mathcal{C},B\backslash \mathcal{W},B\backslash \mathcal{F})$ is a model structure in the coslice category $B\backslash \mathbf{E}$. 
=--



+-- {: .proof}
###### Proof
This follows from the analogous properties of weak
factorisation systems [here](http://ncatlab.org/joyalscatlab/show/Weak+factorisation+systems#slicewfs).
=--






+-- {: .num_prop #ClosureofleftandrightclassesMDS}
###### Proposition
The classes $\mathcal{C}$, $\mathcal{C}\,\cap \,\mathcal{W}$,
$\mathcal{F}$ and $\mathcal{F}\,\cap \,\mathcal{W}$
are closed under composition and retracts. 
The classes $\mathcal{F}$ and $\mathcal{F}\,\cap \,\mathcal{W}$
are closed under base changes and products.
The classes $\mathcal{C}$ and $\mathcal{C}\,\cap \,\mathcal{W}$
are closed under cobase changes and coproducts.
The intersection $\mathcal{C}\,\cap \,\mathcal{W}\,\cap \, \mathcal{F}$ is the class of isomorphisms. 

=--



+-- {: .proof}
###### Proof
This follows directly from the general properties of 
the classes of a weak factorisation system [here](http://ncatlab.org/joyalscatlab/show/Weak+factorisation+systems#ClosureofleftandrightclassesWFS).
=--



+-- {: .num_corollary #Closurefibrantandcofibrantobjects}
###### Corollary
A retract of a fibrant object is fibrant.
A product of a family of fibrant objects is fibrant.
Dually, a retract of a cofibrant object is cofibrant. 
A coproduct of a family of cofibrant objects is cofibrant.
=--



+-- {: .proof}
###### Proof 
If an object $X$ is a retract of an object $Y$,
then the map $X\to \bot$ is a retract of the map $Y\to \bot$.
If an object $X$ is the product of a family of object $(X_i| i\in I)$,
then the map $X\to bot$ is the product of the family of maps
$(X_i\to \bot| i\in I)$.
=--


+-- {: .num_lemma #Wclosedunderretracts}
###### Lemma
(Myles Tierney)
The class $\mathcal{W}$ is closed under retracts.
=--


+-- {: .proof}
###### Proof
Notice first that the class $\mathcal{F}\,\cap\,\mathcal{W}$ is closed under retracts by Proposition \ref{ClosureofleftandrightclassesMDS}. 
Suppose now that a map $f: A \to B$ is a retract of a map $g: X \to Y$ in  $\mathcal{W}$. We want to show $f \in \mathcal{W}$. We have a commutative diagram
\begin{xymatrix}
 A  \ar[d]_f \ar[r]^{s} & X \ar[d]^g \ar[r]^t & A \ar[d]^f \\
B \ar[r]_u & Y \ar[r]_v & B
\end{xymatrix}
with $t s = 1_A$ and $v u = 1_B$. We suppose first that $f$ is a fibration.
In this case, factor $g$ as $g = q j: X \to Z \to Y$ with 
$j$ an acyclic cofibration and $q$ a fibration. The 
map $q$ is acyclic by three-for-two, since $q$ and $j$
are acyclic. The square
\begin{xymatrix}
 X  \ar[d]_j \ar[rr]^t & & A \ar[d]^f \\
Z \ar[r]_{q} & Y \ar[r]_{v} & B
\end{xymatrix}
has a diagonal filler $d: Z \to A$, since $f$ is a fibration. We get
a commutative diagram
\begin{xymatrix}
 A  \ar[d]_f \ar[r]^{js} & Z \ar[d]^q \ar[r]^d & A \ar[d]^f \\
B \ar[r]_u & Y \ar[r]_v & B
\end{xymatrix}
The map $f$ is a retract of $q$, since $d(j s) = t s =1_A$.
Thus, $f$ is acyclic, since $q$ is an acyclic fibration. 
In the general case, factor
$f$ as $f = p i: A \to E \to B$ with $i$ an acyclic cofibration
and $p$ a fibration. By taking a pushout we obtain a commutative diagram
\begin{xymatrix}
 A  \ar[d]_i \ar[r]^{s} & X \ar[d]^{in_2} \ar[r]^t & A \ar[d]^i \\
E \ar[d]_p  \ar[r]^(0.4){in_1} & E \sqcup_A X \ar[d]^k \ar[r]^(0.6){r} & E \ar[d]^p \\
B \ar[r]_u & Y \ar[r]_v & B
\end{xymatrix}
where $k in_2 =g$ and $r in_1 = 1_E$. The map $in_2$ is a cobase change of $i$, so $ in_2$ is an acyclic cofibration, since $i$ is. Thus, 
$k$ is acyclic by three-for-two, since $g = k in_2$ is acyclic
by assumption. So $p$ is acyclic by the first part, since 
$p$ is a fibration. Finally, $f = p i $ is acyclic, since
$i$ is acyclic. 
=--




The **homotopy category** of a model category $\mathbf{E}$
is defined to be the category of fractions 
$$Ho(\mathbf{ E})=\mathcal{W}^{-1}\mathbf{E}.$$
The canonical functor $H:\mathbf{ E}\to Ho(\mathbf{ E})$
is a [localisation](http://ncatlab.org/joyalscatlab/show/Factorisation+systems#localisationcatFS)
with respects to the maps in $\mathcal{W}$.
Recall that a functor $F:\mathbf{E} \to \mathbf{K}$
is said to *invert* a map $u:A\to B$
if the morphism $F(u):F A\to F B$ is invertible.
The functor $H$ inverts the maps in $\mathcal{W}$
and for any functor $F:\mathbf{E} \to \mathbf{K}$
which inverts the maps in $\mathcal{W}$, there is a unique
functor $F': Ho(\mathbf{ E})\to \mathbf{K}$ such that
$F'H=F$. We shall see in theorem \ref{homotopycategory2}
that a map $u:A\to B$ in the category $\mathbf{E}$
is acyclic _if and only if_ it is inverted by the functor $H$.
We shall see in corollary \ref{homotopycategoryislocallysmall}
that the category $Ho(\mathbf{ E})$
is locally small if the category $\mathbf{ E}$
is locally small.
 

We denote by $\mathbf{E}_f$ (resp. $\mathbf{E}_c$, 
$\mathbf{E}_{f c}$) the full subcategory of $\mathbf{ E}$ spanned by the 
fibrant (resp. cofibrant, fibrant-cofibrant) objects of 
$\mathbf{ E}$. 
If $\mathcal{M}$ is a class of maps in $\mathbf{ E}$, we shall
put
$$\mathcal{M}_f=\mathcal{M} \,\cap\, \mathbf{ E}_f \quad  \quad 
\mathcal{M}_c=\mathcal{M}\,\cap\, \mathbf{ E}_c 
\quad \mathrm{and} \quad  \mathcal{M}_{f c}= \mathcal{M} \,\cap\,
\mathbf{ E}_{f c}. $$


Let us put
$$Ho(\mathbf{ E}_f)=\mathcal{W}_f^{-1}\mathbf{E}_f,
 \quad \quad
Ho(\mathbf{ E}_c)=\mathcal{W}_c^{-1}\mathbf{E}_c,
 \quad \mathrm{and}\quad 
Ho(\mathbf{ E}_{f c})=\mathcal{W}_{f c}^{-1}\mathbf{E}_{f c}.$$
Then the square of inclusions,
\begin{xymatrix}
\mathbf{ E}_{f c} \ar[d] \ar[r] &   \mathbf{ E}_f  \ar[d] \\
 \mathbf{ E}_f \ar[r] &    \mathbf{ E}
\end{xymatrix}
induces a commutative square of categories and canonical functors,
\[
\label{40}
\]
\begin{xymatrix}
\mathrm{Ho}(\mathbf{ E}_{f c})\ar[d]   \ar[r] &  
  \mathrm{Ho}(\mathbf{ E}_f)\ar[d]  \\
\mathrm{Ho}(\mathbf{ E}_c)  \ar[r]& \mathrm{Ho}(\mathbf{ E}).
\end{xymatrix}
We shall see in theorem \ref{homotopycategory2} that the four functors in the square 
are equivalences of categories.


The following result is easy to prove but technically useful:


+-- {: .num_prop #inducedfactsystemmodelcat}
###### Proposition
The pair $( \mathcal{C}_f\,\cap \,\mathcal{W}_f,\mathcal{F}_f)$ and 
the pair $(\mathcal{C}_f,\mathcal{F}_f\,\cap\, \mathcal{W}_f)$ 
are weak factorisation systems in the category $\mathbf{ E}_f$.
The pair $( \mathcal{C}_c\,\cap \,\mathcal{W}_c,\mathcal{F}_c)$ and 
the pair $(\mathcal{C}_c,\mathcal{F}_c\,\cap\, \mathcal{W}_c)$ 
are weak factorisation systems in the category $\mathbf{ E}_c$.
The pair $( \mathcal{C}_{cf}\,\cap \,\mathcal{W}_{cf},\mathcal{F}_{cf})$ and the pair $(\mathcal{C}_{cf},\mathcal{F}_{cf}\,\cap\, \mathcal{W}_{cf})$ 
are weak factorisation systems in the category $\mathbf{ E}_{cf}$.
=--


+-- {: .proof}
###### Proof
Let us how that the pair $( \mathcal{C}_f\,\cap \,\mathcal{W}_f,\mathcal{F}_f)$ is a weak factorisation system in $\mathbf{ E}_f$.
We shall use the characterisation of a weak factorisation system
[here](http://ncatlab.org/joyalscatlab/show/Weak+factorisation+systems#WFS2).
Obviously, we have $u\,\pitchfork\, p$ for every $u\in \mathcal{C}_f\,\cap \,\mathcal{W}_f$ and $p\in  \mathcal{F}_f$.
If $f:X\to Y$ is a map between fibrant objects,
let us choose a factoriation $f=pu:X\to E\to Y$
with $u$ an acyclic cofibration and $p$ a fibration.
The object $E$ is fibrant, since $p$ is a fibration and $Y$ is fibrant.
This shows that $u\in \mathcal{C}_f\,\cap \,\mathcal{W}_f$
and $p\in \mathcal{F}_f$. Finally, the class 
$\mathcal{C}_f\,\cap \,\mathcal{W}_f$ is closed under codomain 
retracts, since a retract of a fibrant object is fibrant.
Similarly, the class $\mathcal{F}_f$ is closed under domain retracts.
=--


###Cylinders and left homotopies###




+-- {: .num_lemma #coproductofcofibrant}
###### Lemma
The inclusion $in_1:A\to A\sqcup B$ is a cofibration
if $B$ is cofibrant, and the inclusion
$in_2:B\to A\sqcup B$ is a cofibration
if $A$ is cofibrant.
=--


+-- {: .proof}
######Proof
The inclusion $in_1:A\to A\sqcup B$ is a cobase change
of the map $\bot \to B$, since
the square
\begin{xymatrix}
\bot  \ar[r]\ar[d] & \ar[d]^{in_2} B \\
A \ar[r]^(0.4){in_1} & A\sqcup B
\end{xymatrix}
is a pushout. Hence the map $in_1$ is a cofibration
if $B$ is cofibrant (since the class of cofibrations 
is closed under cobase changes by 
Proposition \ref{ClosureofleftandrightclassesMDS})
=--





A **cylinder ** for an object $A$
is a quadruple $(I A,d_1,d_0,s)$
obtained by factoring
the codiagonal $\nabla_A=(1_A,1_A):A\sqcup A\to A$ as 
a cofibration $(d_1,d_0):A\sqcup A \to I A$
followed by a weak equivalence $s:I A\to A$.
\begin{xymatrix}
  A \ar[dr]_{d_1}  \ar@/^/[drr]^{1_A}& &   \\
 & I A \ar[r]^{s} & A   \\
A\ar[ru]^{d_0} \ar@/_/[urr]_{1_A}    &     &
\end{xymatrix}


+-- {: .un_remark #remarkinclusionincylinders}
######Remark
The notation $(I A,d_1,d_0,s)$ introduced by Quillen
suggests that a cylinder represents the first two
terms of a cosimplicial object
$$I^* A:\Delta \to \mathbf{A}$$
with $I^0 A =A$ and $I^1 A =I A$.
This is the notion of a
[[Reedy model categories|cosimplicial framing]] of an object $A$.
Beware that if $d_0$ and $d_1$
are the maps $[0]\to [1]$ in the category $\Delta$,
then $d_0(0)=1$ and $d_1(1)=0$.
We may think of a cylinder $(I A,d_1,d_0,s)$ has
an oriented object with two faces,
with the face $d_1:A\to IA$ representing
the *source* of the cylinder
and the face $d_0:A\to IA$ representing the *target*.
=--



The **transpose** of a cylinder $(I A,d_1,d_0,s)$
is the cylinder  $(I A,d_0,d_1,s)$.



+-- {: .num_lemma #inclusionincylinders}
######Lemma
The maps
$d_1:A\to I A$ and $d_0:A\to I A$
are acyclic, and they
are acyclic cofibrations when $A$ is cofibrant.
=--



+-- {: .proof}
######Proof
The map $d_1$ and $d_0$ are acyclic
by three-for-two, since we have
$s d_1=1_A= s d_0$ and $s$ is acyclic.
If $A$ is cofibrant, then
the inclusions $in_1:A\to A\sqcup A$ and $in_2:A\to A\sqcup A$ are 
cofibrations by Lemma \ref{coproductofcofibrant}.
Hence also the composite
$d_1=(d_1,d_0)in_1$ and $d_0=(d_1,d_0)in_2$
(since the class of cofibrations is closed under composition by Proposition \ref{ClosureofleftandrightclassesMDS}).
=--





A **mapping cylinder** of a map $f:A\to B$
is obtained by factoring the map  $(f,1_B):A\sqcup B\to B$
as a cofibration $(i_A,i_B):A\sqcup B\to C(f)$
followed by a weak equivalence $q_B:C(f)\to B$.
We then have $f=q_B i_A$ and $q_B i_B=1_B$.
The factorisation
$$f=q_B i_A:A\to C(f)\to B$$
is called the **mapping cylinder factorisation** of the map $f$.
The map $i_B$ is acyclic 
by three-for-two, since $q_B$ is acyclic and we have
$q_B i_B=1_B$.



+-- {: .num_lemma #inclusioninmappingcylinders}
######Lemma
The maps
$i_A:A\to C(f)$ is a cofibration when $B$ is cofibrant,
and the map $i_B:B\to C(f)$ is a cofibration
when $A$ is cofibrant.
=--





+-- {: .proof}
######Proof
The inclusion $in_1:A\to A\sqcup B$ 
is a cofibration when $B$ is cofibrant by Lemma \ref{coproductofcofibrant}.
Hence also the composite $i_A=(i_A,i_B)in_1$ in this case.
The inclusion $in_2: B\to A\sqcup B$
is a cofibration when $A$ is cofibrant by Lemma \ref{coproductofcofibrant}.
Hence also the composite $i_B=(i_A,i_B)in_2$ in this case.
=--





If $A$ is cofibrant, then a mapping cylinder for a map 
$f:A\to B$ can be constructed from a cylinder 
$(I A,d_1,d_0,s)$
by the following diagram with a pushout square

\[
\label{17}
\]
\begin{xymatrix}
 A\sqcup A \ar[d]_{(d_1,d_0)} \ar[r]^{1_A\sqcup f}   & A\sqcup B \ar[d]_{(i_A,i_B)}   \ar@/^1pc/[ddr]^{(f,1_B) } &  \\
 I A  \ar@/_1pc/[drr]_{f s } \ar[r]^{in}  & 
C(f)\ar[dr]_{q_B}  &  \\
 & & B
\end{xymatrix}
We have $q_B i_A=f$ and $q_B i_B=1_B$ by construction.
The map $(i_A,i_B)$ is a cofibration by
cobase change, since the map $(d_1,d_0)$
is a cofibration.
Let us show that $q_B$ is acyclic. For this, 
it suffices to show that $i_B$ is acyclic by three-for-two, 
since $q_B i_B=1_B$.
The two squares of the following diagram are pushout,
\[
\label{18}
\]
\begin{xymatrix}
  A\ar[d]_{in_2} \ar[r]^{f}   &  B \ar[d]^{in_2}   \\
 A\sqcup A \ar[d]_{(d_1,d_0)} \ar[r]^{1_A\sqcup f}   & A\sqcup B \ar[d]^{(i_A,i_B)}   \\
I A  \ar[r]^{in}  & C(f),
\end{xymatrix}
hence also their composite,
\[
\label{16}
\]
\begin{xymatrix}
 A \ar[d]_{d_0}  \ar[r]^{f}  &  B \ar[d]^{i_B}\\
  I A   \ar[r]^{in}  &  C(f),   &
\end{xymatrix}
by the lemma 
[here](http://ncatlab.org/joyalscatlab/show/Cartesian+squares#cancelcartesian).
This shows that the map $i_B$
is a cobase change of the map $i_1$.
But $i_1$ is an acyclic cofibration 
by Lemma \ref{inclusionincylinders},
since $A$ is cofibrant. 
It follows that $i_B$
is an acyclic cofibration (since the class
of acyclic cofibrations is closed under 
cobase changes by 
Proposition \ref{ClosureofleftandrightclassesMDS}).




+-- {: .num_lemma #Kenbrownorigianl}
###### Lemma
(Ken Brown 1) Let $\mathbf{E}$ be a model category
and let $F:\mathbf{E}_c\to \mathbf{C}$
be a functor defined on the sub-category of cofibrant
objects and taking its values in a category $\mathbf{C}$
equipped with class $\mathcal{W}$
of _weak equivalences_ containing the units
and satisfying three-for-two.
If the functor $F$ takes an acyclic cofibration
to a weak equivalence, then it takes
an acyclic map to a weak equivalence.
=--


+-- {: .proof}
######Proof
If $f:A\to B$ is an acyclic map between 
cofibrant objects, let us choose 
a mapping cylinder factorisation $f=q_B i_A:A\to C(f)\to B$.
The maps $i_A$ and $i_B$ are cofibrations
by Lemma \ref{inclusioninmappingcylinders},
since $A$ and $B$ are cofibrant.
The map $i_B$ is acyclic by three-for-two, since $q_B i_B=1_B$
and $q_B$ is acyclic. Thus, $F(i_B)$ is a weak 
equivalence.
Hence also the map $F(q_B)$
by three-for-two
since we have $F(q_B)F(i_B)=F(q_B i_B)=F(1_B)=1_{F B}$
and $\mathcal{W}$ contains the units.
The map $i_A$ is acyclic by three-for-two,
since $f=q_B i_A$ and $f$ and $q_B$ are acyclic.
Thus, $F(i_A)$ is a weak equivalence,
and it follows by three-for-two that $F(f)$ is a weak equivalence 
since
$F(f)=F(q_B i_A)=F(q_B)F(i_A)$.
=--


Recall that a functor is said to _invert_ a morphism in its domain
if it takes this morphism to an isomorphism.


+-- {: .num_lemma #KenBrownlemma}
######Lemma
(Ken Brown 2) 

* If a functor $F:\mathbf{E}_c\to \mathbf{C}$
inverts acyclic cofibrations, then it inverts
weak equivalences.

* If a functor $F:\mathbf{E}_f\to \mathbf{C}$
inverts acyclic fibrations, then it inverts
weak equivalences.
=--

+-- {: .proof}
######Proof
This follows from Lemma \ref{Kenbrownorigianl},
if $\mathcal{W}$ is 
the class of isomorphisms in $\mathbf{C}$.
=--




+-- {: .un_remark #KenBrownlocaisation}
######Remark
Ken Brown's lemma implies that the inclusion
$\mathcal{C}_c\, \cap\, \mathcal{W}_c \subseteq \mathcal{W}_c$
induces an isomorphism of categories,

$$(\mathcal{C}_c\cap \mathcal{W}_c)^{-1}\mathbf{ E}_c\to Ho(\mathbf{ E}_c).$$
=--




If $(I A,d_1,d_0,s)$ is a cyclinder for $A$, 
then a **left homotopy** $h:f {\rightarrow}_l g$
between two maps $f,g:A\to X$
is a map $h:I A\to X$ such that
and $f= h d_1$ and $g= h d_0$.
We shall say that $h d_1$ is the **source** of the homotopy $h$
and that $h d_0$ is the **target**,
\begin{xymatrix}
  A \ar[dr]_{d_1}  \ar@/^/[drr]^{f}& &   \\
 & I A \ar[r]^{h} & B.   \\
A\ar[ru]^{d_0} \ar@/_/[urr]_{g}    &     &
\end{xymatrix}
The **reverse** of an homotopy $h:f {\rightarrow}_l g$
is the homotopy $g {\rightarrow}_l f$ defined by the same map 
$h:I A\to X$ but on the transpose cylinder $(I A,d_0,d_1,s)$.
The **homotopy unit** $f=_l f$ of a map $f:A\to X$
is defined by the map $f p:I A\to A\to X$.

Two maps $f,g:A\to X$
are **left homotopic**, $f\sim_l g$, if there exists a left
homotopy $h:f\to_l g$ with domain some cylinder object for $A$.


+-- {: .num_lemma #lefthomotopysinglecylinder}
######Lemma
The left homotopy relation between the maps 
$A\to X$ can be defined on a fixed cylinder 
for $A$, when $X$ is fibrant. 
=--



+-- {: .proof}
######Proof
Let us show that if two maps $f,g:A\to X$ are homotopic
by virtue of a homotopy defined on a cylinder $(I A,i_1,i_0,r)$, 
then then they are homotopic by virtue
of a homotopy defined on any another cylinder $(J A,j_1,j_0,s)$.
By assumption, we have $h(i_1,i_0)=(f,g)$ for a map $h: I A\to X$.
Let us choose a factorisation $r=r'u:I A\to I' A\to A$
with $u$ an acyclic cofibration and $r'$ a fibration.
The map $r'$ is acyclic by three-for-two,
since the maps $p$ and $u$ are.
Hence the square
\begin{xymatrix}
A\sqcup A \ar[d]_{(j_1,j_0)}\ar[rr]^{u (i_1,i_0)} \ar[d] & &  I' A \ar[d]^{r'} \\
J A \ar[rr]^s & & A
\end{xymatrix}
has a diagonal filler $k:J A\to I' A$ since the map $(j_1,j_0)$
is a cofibration. But the square
\begin{xymatrix}
I A  \ar[r]^{h} \ar[d]_u &  X  \ar[d] \\
I' A \ar[r] & \top
\end{xymatrix}
has also a diagonal filler $d:I' A\to X$, since $u$ is an acyclic 
cofibration and $X$ is fibrant.
The composite $h'=d k:J A\to X$ is a left homotopy $f\to_l g$.
=--





+-- {: .num_lemma #preservinghomotopies}
######Lemma 
If a functor $F:\mathbf{E}\to \mathbf{K}$
inverts weak equivalences, then 
the implication 
 $$f\sim_l g \quad \Rightarrow \quad F(f)=F(g)$$
is true for any pair of maps $f,g:A\to B$ in $\mathbf{E}$.
The same result is true for a functor
defined on $\mathbf{E}_c$ or on $\mathbf{E}_{f c}$.
=--



+-- {: .proof}
######Proof
If $(I A,d_1,d_0,s)$
is a cylinder for $A$, then the map
$F(s)$ is invertible by the assumption of $F$
since $s$ is acyclic. Hence we have
$F(d_1)=F(d_0)$, since we have
$$F(s) F(d_1)=F(s d_1)=F(1_A)=F(s d_0)=F(s)F(d_0).$$
If $h:I A\to X$ is a homotopy between 
two map $f,g:A\to X$, then
$$F(f)=F(h d_1)=F(h)F(d_1)=F(h)F(d_0)=F(h d_0)=F(g).$$
Let us now consider the case where the domain of the functor 
$F$ is the category $\mathbf{E}_c$. Observe that if $A$ is cofibrant,
then so is the object $I A$ in a cylinder $(I A,d_1,d_0,s)$,
since the map $(d_1,d_0):A\sqcup A \to IA$ is a cofibration
and the object $A\sqcup A$ is cofibrant (since a coproduct of cofibrant
objects is cofibrant by Corollary \ref{Closurefibrantandcofibrantobjects}).
Hence the cylinder $(I A,d_1,d_0,s)$ belongs to the category 
$\mathbf{E}_{c}$ and the proof above can be repeated in this case. 
Let us now consider the case where the domain of the functor $F$ is the category $\mathbf{E}_{f c}$. In this case
the left homotopy relation between the maps $A\to B$
can defined on a fixed cylinder for $A$ 
by Lemma \ref{lefthomotopysinglecylinder},
since $B$ is fibrant.
A cylinder for $A$ can be constructed by factoring the
map $\nabla_A:A\sqcup A\to A$
as an acyclic cofibration $(d_1,d_0):A\sqcup A \to I A$
followed by a fibration $s:I A \to A$.
The object $I A$ is cofibrant, since $A$ is cofibrant.
But $I A$ is also fibrant, since $s$ is a fibration
and $A$ is fibrant.
Hence the cylinder $(I A,d_1,d_0,p)$ 
belongs to the category $\mathbf{E}_{f c}$ 
and the proof above can be repeated. 
=--



The left homotopy relation on the set of maps $A\to X$ is reflexive and symmetric. 
We shall denote by $\pi^l(A,X)$
the quotient of the set $Hom(A,X)$ by
the equivalence relation generated by
the left homotopy relation.
The relation is compatible with composition
on the left: the implication
$$f\sim_l g \quad \Rightarrow \quad p f\sim_l p g$$
is true for every maps $f,g:A\to X$ and $p:X\to X'$.
This defines a functor 
$$\pi^l(A,-):\mathbf{E}\to \mathbf{Set}.$$





+-- {: .num_lemma #lefthomotopyisequiv}
######Lemma
The left homotopy relation between the maps $A\to X$ 
is an equivalence when $A$ is cofibrant.
=--

+-- {: .proof}
######Proof
Cylinders for $A$ can be composed as [[Spans and cospans|cospan]].
More precisely, the composite of a cylinder
$(I A, i_1,i_0,r)$
with a cylinder $(J A,j_1,j_0,s)$
is the cylinder $(K A,k_1,k_0,t)$
defined by the following diagram with a pushout square,
\begin{xymatrix}
  \ar@/_2pc/[ddrr]_{k_1} A \ar[dr]^{i_1}  & &  A \ar[dl]_{i_0}  \ar[dr]^{j_1}  
& & \ar[dl]_{j_0} A \ar@/^2pc/[ddll]^{k_0} \\
 & IA \ar[dr]^{in_1}  & & \ar[dl]_{in_2}  JA  &   \\
 & &  KA   &  &
\end{xymatrix}
The map $t:K A\to A$ is defined by the condition $t in_1=r$ and $t in_2 =s$.
Let us show that $t$ is acyclic.
The map $j_1:A\to J A$ is an acyclic cofibration by Lemma
\ref{inclusionincylinders}, since $A$ is cofibrant.
It follows that $in_1$ is an acyclic cofibration,
since it is a cobase change of $j_1$.
Hence the map $t$ is acyclic by three-for-two, since we have $t in_1=s$
and the maps $in_1$ and $s$ are acyclic.
It remains to show that the map $(k_0,k_1)$
is a cofibration. For this, we can
use the following diagram with a pushout square,
\begin{xymatrix}
  A\sqcup A \sqcup A \sqcup A \ar[d]_{(i_1,i_0)\sqcup (j_1,j_0)} 
\ar[rr]^(0.6){A\sqcup \nabla_A \sqcup A} 
  &  &  A\sqcup A \sqcup A   \ar[d]_k  & & \ar[ll]_(0.4){in_1\sqcup in_3}  A \sqcup A \ar[lld]^{(k_1,k_0)}\\
I A\sqcup J A \ar[rr]^{(in_1,in_2)}   &  & K A. & &
\end{xymatrix}
The map $k$ in this diagram is a cobase change of the map 
$(i_1,i_0)\sqcup (j_1,j_0)$. But the map $(i_1,i_0)\sqcup (j_1,j_0)$
is a cofibration,
since the maps $(i_1,i_0)$ and $(j_1,j_0)$ are cofibrations.
This proves that the map $k$ is a cofibration.
It follows that the composite $(k_1,k_0)=k(in_1\sqcup in_3)$
is a cofibration, since the map $in_1\sqcup in_3$ is a cofibration
by Lemma \ref{coproductofcofibrant}.
We have proved that $(K A,k_1,k_0,r)$ is a cylinder for $A$.
We can now prove that the left homotopy relation on the
set of maps $A\to X$ is transitive.
Let $f_1,f_2$ and $f_3$ be three maps $A\to X$ and suppose that
$h_1:I A\to X$ is a left homotopy $f_1\to_l f_2$,
and $h_2:J A\to X$ is a left homotopy $f_2\to_l f_3$.
There is then a unique map $h_3: K A\to X$
such that $h_3 in_1 =h_1$ and $h_3 in_2 =h_2$,
since $h_1 i_0 =f_2= h_2 j_1$.
This defines a homotopy $h_3:f_1 \to_l f_3$,
since $h_3 k_1= h_3 in_1 i_1 =h_1 i_1=f_1$
and $h_3 k_0 =h_3 in_2 j_0= h_2 j_0 =f_3$.
=--





+-- {: .num_lemma #coveringhomotopy}
######Lemma 
(Covering homotopy theorem) Let $A$ be cofibrant, let $f:X\to Y$ be a fibration, let $a:A\to X$, and let $h: I A\to Y$ be a left homotopy with 
source $f a:A\to Y$. Then there exists a left
homotopy $H: I A\to X$ with source $a$ such that $ f H=h$. 
=--


+-- {: .proof}
######Proof
The square
\begin{xymatrix}
A \ar[d]_{d_1} \ar[r]^a  &  X\ar[d]^{f}  \\
I A \ar[r]^h & Y
\end{xymatrix}
has a diagonal filler $H: I A\to X$, since $d_1$
is an acyclic cofibration by Lemma \ref{inclusionincylinders}
and $f$ is a fibration.
=--




+-- {: .num_lemma #liftinghomotopy}
######Lemma 
(Homotopy lifting lemma) Let $f:X\to Y$ be an acyclic fibration, let $a:A\to X$ and $b:A\to X$, and let 
$h: I A\to Y$ be a left homotopy $f a \to_l f b$. 
Then there exists a map $H: I A\to X$ defining a left homotopy
$a \to_l b$ such that $ f H=h$.
=--


+-- {: .proof}
######Proof
The square
\begin{xymatrix}
A\sqcup A \ar[d]_{(d_1,d_0)} \ar[r]^(0.6){(a,b)}  &  X\ar[d]^{f}  \\
I A \ar[r]^h & Y
\end{xymatrix}
has a diagonal filler $H: I A\to X$, since $(d_1,d_0)$
is a cofibration
and $f$ is an acylic fibration.
=--





+-- {: .num_lemma #lefthomotopyfunctor}
###### Lemma
If $A$ is cofibrant, then
the functor $\pi^l(A,-):\mathbf{E}\to \mathbf{Set}$
inverts acyclic maps between fibrant objects.
=--

+-- {: .proof}
###### Proof
Let us first show that the functor $\pi^l(A,-)$
inverts acyclic fibrations.
If $f:X\to Y$ is an acyclic fibration
and $y:A\to Y$, then the square
\begin{xymatrix}
\bot\ar[d]\ar[r] & X  \ar[d]^{f} \\
A\ar[r]^y & Y
\end{xymatrix}
has a diagonal filler,
since $A$ is cofibrant and $f$ is an acyclic fibration.
Hence there exists a map $x:A\to X$
such that $f x=y$.
This shows that the map $\pi(A,f)$ is surjective.
Let us show that it is injective.
If $a,b:A\to X$ and $f a\sim_l f b$,
then $a\sim_l b$ by the homotopy lifting lemma
\ref{liftinghomotopy}.
We have proved that the map $\pi^l(A,f)$
is bijective.
It then follows from
Ken Brown's lemma \ref{KenBrownlemma}
that that the functor $\pi^l(A,-)$ inverts acyclic maps between fibrant objects.
=--


+-- {: .num_lemma #lefthomotopicweakequiv}
###### Lemma
A map which is left homotopic to an acyclic map is acyclic.
=--

+-- {: .proof}
######Proof
Let $h: I A \to B$
be a left homotopy between two maps $h d_1=u$
and $h d_0=v$. If $v$ is acyclic,
then so is $h$ by three-for-two,
since $d_0$ is acyclic.
Hence the composite $u=h d_1$ is acyclic
by three-for-two, since $d_1$ is acyclic.
=--


###Path objects and right homotopies###



+-- {: .num_lemma #productoffibrant}
###### Lemma*
(Dual to Lemma \ref{coproductofcofibrant})
The projection $pr_1:X\times Y \to X$ is a fibration
if $Y$ is fibrant, and the projection
$pr_2:X\times Y \to Y$ is a fibration
if $X$ is fibrant 
=--



A **path object** for an object $X$
is a quadruple $(P X,\partial_1,\partial_0,\sigma)$
obtained by factoring
the diagonal $\Delta_X=(1_X,1_X):X\to X\times X$ as a weak equivalence
$\sigma:X\to P X$ followed by a fibration 
$(\partial_1,\partial_0):P X\to X\times X$.
\begin{xymatrix}
 & & X\\
X\ar[r]^{\sigma}\ar@/^/[urr]^{1_X} \ar@/_/[drr]_{1_X}  
& P X  \ar[ru]_{\partial_1}\ar[rd]^{\partial_0} & \\
 & & X
\end{xymatrix}


+-- {: .un_remark #remarkprojectionpath}
######Remark
The notation $(P X,\partial_1,\partial_0,\sigma)$ introduced by Quillen
suggests that a path object represents the first two
terms of a simplicial object
$$P_* X:\Delta \to \mathbf{A}$$
with $P_0 X = X$ and $P_1 X= P X$.
This is the notion of [[Reedy model categories|simplicial framing]]
of an object $X$.
Beware that the *source* of a 1-simplex $f$
in a simplicial set $S$ is the vertex $\partial_1(f)\in S_0$,
and that its *target* is the vertex 
$\partial_0(f)\in S_0$.
=--



The **transpose** of a path object $(P X,\partial_1,\partial_0,\sigma)$
is the path object $(P X,\partial_0,\partial_1,\sigma)$.





+-- {: .num_lemma #projectionpathobject}
######Lemma*
(Dual to Lemma \ref{inclusionincylinders})
The maps
$\partial_1:P X \to X$ and $\partial_0:P X\to X$
are acyclic, and they are 
are acyclic fibrations when $X$ is fibrant.
=--



A **mapping path object** of a map $f:X\to Y$
is obtained by factoring the map  
$(1_X,f):X\to X\times Y$
as a weak equivalence $i_X: X\to P(f)$
followed by a fibration $(p_X,p_Y):P(f)\to X\times Y$.
By construction, we have $f=p_Y i_X$ and $p_X i_X=1_X$.
The factorisation
$$f=p_Y i_X:X\to P(f)\to Y$$
is called the **mapping path factorisation** of 
the map $f$.
The map $p_X$ is acyclic 
by three-for-two, since $i_X$ is acyclic and 
$p_X i_X=1_X$. 



+-- {: .num_lemma #projectionmappingpath}
######Lemma*
(Dual to Lemma \ref{inclusioninmappingcylinders})
The maps
$p_X:P X\to X$ and $p_Y: P Y\to Y$
are fibrations when $X$ and $Y$ are fibrant.
=--



If $Y$ is fibrant, then a mapping path object for a map $f:X\to Y$ can be constructed from a path object
$(P Y, \partial_1,\partial_0,\sigma)$ for $Y$
by the following diagram with a pullback square,

\[
\label{27}
\]
\begin{xymatrix}
X\ar@/_1pc/[ddr]_{(1_X,f) } 
\ar@/^1pc/[drr]^{\sigma f }  \ar[dr]^{i_X}&& \\
& P(f)\ar[r]^{pr_2} \ar[d]^{(p_X,p_Y)}  
 &   \ar[d]^{(\partial_1,\partial_0)}   P Y. \\
 &  X\times Y \ar[r]_{f\times Y}   & Y\times Y
\end{xymatrix}
We have $p_X i_X=1_X$ and $p_Y i_X=f$
by construction.
The map $(p_X,p_Y)$ is a fibration by
base change, since the map $(\partial_1,\partial_0)$ is.
Let us show that the map $i_X$ is acyclic.
For this, it suffices to show that $p_X$
is acyclic by three-for-two, since $p_X i_X=1_X$. 
The two squares of the 
following diagram are cartesian,
\[
\label{28}
\]
\begin{xymatrix}
P(f)\ar[r]^{pr_2} \ar[d]_{(p_X,p_Y)}  &  
P Y \ar[d]^{(\partial_1,\partial_0)}\\
   X\times Y\ar[d]_{pr_1}  \ar[r]^{f\times Y}   
& Y\times Y\ar[d]^{pr_1}  \\
  X \ar[r]^{f}   & Y,
\end{xymatrix}
hence also their composite,
\[
\label{16}
\]
\begin{xymatrix}
P(f)\ar[r]^{pr_2} \ar[d]_{p_X}   &   \ar[d]^{\partial_1}   P Y \\
  X \ar[r]^{f}   & Y,
\end{xymatrix}
by the lemma [here](http://ncatlab.org/joyalscatlab/show/Cartesian+squares#cancelcartesian).
Hence the map $p_X$
is a base change of the map $\partial_0$.
But $\partial_1$ is an acyclic fibration 
by Lemma \ref{projectionpathobject},
since $Y$ is fibrant. 
This shows that the map $p_X$
is acyclic (since the base change of an acyclic 
fibration is an acyclic fibration by 
Proposition \ref{ClosureofleftandrightclassesMDS}).



If $(P X,\partial_1,\partial_0,\sigma)$ is a path
object for $X$, then a **right homotopy** $h:f {\rightarrow}_r g$
between two maps $f,g:A\to X$
is defined to be a map $h:A\to PX$ 
such that $f=\partial_1 h$
and $g=\partial_0 h$.
We shall say that $\partial_1 h$ is the **source** of the homotopy $h$
and that $\partial_0 h$ is its **target** .
\begin{xymatrix}
 & & X\\
A\ar[r]^{h}\ar@/^/[urr]^{f} \ar@/_/[drr]_{g}  
& P X  \ar[ru]_{\partial_1}\ar[rd]^{\partial_0} & \\
 & & X
\end{xymatrix}
The **reverse** of $h$ is the homotopy ${}^t h:g {\rightarrow}_r h$ defined by the same map $h: A\to P X$ but on the transpose path object 
$(P X,\partial_0,\partial_1,\sigma)$.
The **unit homotopy** $f=_r f$ of a map $f:A\to X$
is the map $\sigma f : A\to X \to P X$.


Two maps $f,g:A\to X$
are **right homotopic**, $f\sim_r g$, if there exists a right
homotopy $h:f\rightarrow_r g$ with codomain a path object for $X$.




+-- {: .num_lemma #righthomotopyfixedpathobject}
###### Lemma*
(Dual to Lemma \ref{lefthomotopysinglecylinder})
The right homotopy relation between the maps $A\to X$ 
can be defined on a fixed path object for $X$ when $A$ is cofibrant.
=--



We shall denote by $\pi^r(A,X)$
the quotient of $Hom(A,X)$ by
the equivalence relation generated by
the right homotopy relation.
The right homotopy relation is compatible with composition
on the right: 
$$f\sim_r g \quad \Rightarrow \quad f u\sim_r  g u$$
for every map $u:A'\to A$.
We thus obtain a functor 
$$\pi^r(-,X):\mathbf{E}^o\to \mathbf{Set}.$$


+-- {: .num_lemma #righthomotopyisequiv}
###### Lemma*
(Dual to Lemma \ref{lefthomotopyisequiv})
The right homotopy relation between the maps $A\to X$ is an equivalence when $X$ is fibrant.
=--



+-- {: .num_lemma #extensionhomotopy}
######Lemma* 
(Homotopy extension theorem, dual to Lemma \ref{coveringhomotopy}).
Let $X$ be fibrant, let $u:A\to B$ be a cofibration, let $b:B\to X$, and let $h: A \to P X$ be a right homotopy with source $b u:A\to X$.
Then there exists a right homotopy $H: B \to P X$ with source $b $ 
such that $ H u =h$.
=--



+-- {: .num_lemma #prolongationhomotopy}
######Lemma* 
(Homotopy prolongation lemma, dual to Lemma \ref{liftinghomotopy}) 
Let $X$ be fibrant, let $u:A\to B$ be an acyclic cofibration, let $a:B\to X$ and $b:B\to X$, and let  $h: A\to P X$ be a right homotopy $a u\to_r b u$.
Then there exists a map $H: B \to P X$ defining a right
homotopy $a \to_r b $ such that $H u =h$.
=--


+-- {: .num_lemma #righthomotopyfunctor}
###### Lemma*
(Dual to Lemma \ref{lefthomotopyfunctor})
If $X$ is fibrant, then the functor 
$\pi^r(-,X):\mathbf{E}^o\to \mathbf{Set}$
inverts acyclic maps between cofibrant objects.
=--



+-- {: .num_lemma #righthomotopicweakequiv}
###### Lemma*
(Dual to Lemma \ref{lefthomotopicweakequiv})
A map which is right homotopic to an acyclic map is acyclic

=--

###Double homotopies##

If $(I A,d_1,d_0,s)$ is a cylinder object for $A$ and 
$(P X, \partial_1,\partial_0,\sigma)$
is a path object for $X$, then a map $H:I A\to P X$
is *double homotopy* between four maps $A\to X$,
\begin{xymatrix}
\partial_1 H d_1\ar[dd]_{H d_1} \ar[rr]^{\partial_1 H}  \ar@{.>}[ddrr]|{H}  & &\ar[dd]^{H d_0}   \partial_1 H d_0 \\
&  &\\
\partial_0 H d_1 \ar[rr]_{\partial_0 H} &  & \partial_0 H d_0.
\end{xymatrix}


The four corners of the square are representing maps $A\to X$,
the horizontal sides are representing left homotopies,
and the vertical sides are representing right homotopies. 



+-- {: .num_lemma #doublehomotopylem}
###### Lemma
If $X$ is fibrant,
then every open box of three homotopies, opened at the top, 
between four maps $f_{ij}:A\to X$,
\begin{xymatrix}
f_{11}\ar[d]_{v_1} & f_{10}\ar[d]^{v_0}\\
f_{01}  \ar[r]^{h_0}  & f_{00},
\end{xymatrix}
can be filled by a double homotopy $H:I A\to P X$
(ie $\partial_0 H=h_0$, $H d_1=v_1$ and $H d_0=v_0$).
=--

+-- {: .proof}
###### Proof
The square
\begin{xymatrix}
A\sqcup A\ar[d]_{(d_1,d_0)} \ar[rr]^{(v_1,v_0)}  & & P X \ar[d]^{\partial_0}\\
IA  \ar[rr]^{h_0}    & & X
\end{xymatrix}
has a diagonal filler $H:I A \to P X$,
since $(d_1,d_0)$ is a cofibration 
and $\partial_0$ is an acyclic fibration
by Lemma \ref{projectionpathobject}.
=--




+-- {: .num_lemma #leftandrightareequiv}
###### Lemma
If $X$ is fibrant, then the right homotopy relation
on the set of maps $A\to X$
implies the left homotopy relation.
Dually, if $A$ is cofibrant, then the left homotopy
relation implies the right homotopy relation.
Hence the two relations coincide when $A$
is cofibrant and $X$ is fibrant.
=--


+-- {: .proof}
######Proof
Let $h:f\to_r g$ be a right homotopy between two maps $A\to X$.
By Lemma \ref{doublehomotopylem}, the open box of homotopies
\begin{xymatrix}
f\ar[d]_{h} & g \ar@{=}[d]\\
g \ar@{=}[r]    & g
\end{xymatrix}
can be filled by a double homotopy $H:I A \to P X$,
since $X$ is fibrant.
This yields a left homotopy $\partial_1 H :f\to_l g$.
=--


When $A$ is cofibrant and $X$ is fibrant,
then two maps $f,g:A\to X$ 
are said to be **homotopic**
if they are left (or right) homotopic;
we shall denote this relation
by $f\sim g$. We shall denote by $\pi(A,X)$
the quotient of the set $Hom(A,X)$ by
the homotopy relation: 

$$\pi(A,X)=Hom(A,X)/\sim.$$

By definition, $\pi(A,X)=\pi^r(A,X)=\pi^l(A,X).$
This defines a functor

\[
\label{33}
\]
$$\pi:\mathbf{E}_c^o\,\times\, \mathbf{E}_f\to \mathbf{Set},$$

that is, a [[Distributors and barrels|distributor]] 
$\pi:\mathbf{E}_c\Rightarrow \mathbf{E}_f$.

###The homotopy category###





The homotopy relation $\sim$ is compatible with 
the composition law 
$$Hom(Y,Z)\,\times \, Hom(X,Y) \to Hom(X,Z)$$
if $X,Y$ and $Z$ are fibrant-cofibrant objects.
It thus induces a composition law
$$\pi(Y,Z)\,\times \, \pi(X,Y)\to \pi(X,Z)$$
and this defines a category $\pi\mathbf{E}_{f c}$
if we put
$$(\pi\mathbf{E}_{f c})(X,Y)=\pi(X,Y)$$
for $X,Y\in \mathbf{E}_{f c}$.




+-- {: .num_defn #homotopyeqivedef}
###### Definition
We say that a map in $\mathbf{E}_{cf}$
is a **homotopy equivalence** if it is invertible
in the category $\pi\mathbf{E}_{f c}$.
=--


It is obvious from the definition that the
class of homotopy equivalences has the three-for-two
property.

A map $f:X\to Y$ in $\mathbf{E}_{f c}$
is a homotopy equivalence iff there exists a map
$g:Y\to X$ such that $g f\sim 1_X$ and $f g\sim 1_Y$.



Let us denote by
$H:\mathbf{E}\to \mathrm{Ho}(\mathbf{E})$,
$H':\mathbf{E}_{f c}\to \mathrm{Ho}(\mathbf{E}_{f c})$
and $P:\mathbf{E}_{f c}\to \pi(\mathbf{E}_{f c})$,
the canonical functors.
The functor  $H'$ takes homotopic maps $u,v:X\to Y$
to the same morphism by Lemma \ref{preservinghomotopies}.
It follows that there is a unique functor 
$U:\pi\mathbf{E}_{f c}\to \mathrm{Ho}(\mathbf{E}_{f c})$ 
such that the following triangle commutes,
\begin{xymatrix}
\mathbf{E}_{f c} \ar[r]^{P}  \ar[dr]_{H'}   
& \pi\mathbf{E}_{fc} \ar[d]^{U} \\
 & \mathrm{Ho}(\mathbf{E}_{fc}).
\end{xymatrix}


We shall prove in Theorem \ref{weakequivandhomotopy} below that the functor 
$U$ is an isomorphism of categories. We will need a lemma:


+-- {: .num_lemma #localisationaredominant}
###### Lemma
If  $\Sigma$ is a set of morphisms
in a category $\mathbf{A}$, then 
the localisation functor $H:\mathbf{A} \to \Sigma^{-1}\mathbf{A} $
is an epimorphism of category. Moreover, for any category $\mathbf{M}$,
the functor 
$$H^*:\mathbf{[}\Sigma^{-1}\mathbf{A},\mathbf{M}\mathbf{]} \to \mathbf{[}\mathbf{A},\mathbf{M}\mathbf{]}$$
induced by $H$ is fully faithful and it induces
an isomorphism between the category 
$\mathbf{[}\Sigma^{-1}\mathbf{A},\mathbf{M}\mathbf{]}$ and the full subcategory
of $\mathbf{[}\mathbf{A},\mathbf{M}\mathbf{]}$
spanned by the functors $\mathbf{A}\to \mathbf{M}$
inverting the elements of $\Sigma$.
In particular, two functors $Q_0,Q_1:\mathbf{A}\to \mathbf{M}$
are isomorphic iff the functors $Q_0H$ and  $Q_1H$
are isomorphic.
=--

+-- {: .proof}
######Proof
Left to the reader.
=--


+-- {: .num_theorem #weakequivandhomotopy}
###### Theorem
The functor $U:\pi\mathbf{E}_{f c}\to \mathrm{Ho}(\mathbf{E}_{f c})$ 
defined above is an isomorphism of categories. 
A map in $\mathbf{E}_{fc}$
is acyclic iff it is a homotopy equivalence.
=--


+-- {: .proof}
######Proof
 (Mark Hovey) Let us first show that if a map  $f:X\to Y$
in the category $\mathbf{E}_{f c}$ is acyclic,
then it is a homotopy equivalence.
The map $\pi(A,f):\pi(A,X)\to \pi(A,Y)$
is bijective for every cofibrant object $A$
by Lemma \ref{lefthomotopyfunctor}, since $f$ is an
acyclic map between fibrant object.
It follows that $f$ is inverted by the Yoneda functor 
$$\pi\mathbf{E}_{f c}\to [\pi\mathbf{E}_{f c}^o, \mathbf{Sets}].$$
But the Yoneda functor is conservative, since it is fully faithful
by [[Yoneda]]. It follows that $f$ is invertible in the category $\pi\mathbf{E}_{f c}$. This shows that $f$ is a homotopy equivalence.
Let us now prove that the functor $U$ is an isomorphism
of categories. The canonical functor 
$P:\mathbf{E}_{f c}\to \pi(\mathbf{E}_{f c})$
inverts acyclic maps by what we just proved.
Hence there is a unique functor 
$T:\mathrm{Ho}(\mathbf{E}_{f c})\to \pi\mathbf{E}_{f c}$ 
such that the following triangle commutes,
\begin{xymatrix}
\mathbf{E}_{f c} \ar[r]^(0.4){H'}  \ar[dr]_{P}   
& \mathrm{Ho}(\mathbf{E}_{f c})  \ar[d]^{T} \\
 & \pi\mathbf{E}_{f c}.
\end{xymatrix}
Let us show that the functors $U$ and $T$ are mutually inverses.
Let us observe that the functor $P$ is an epimorphism, since 
it is surjective on objects and full. But we have $T U P=T H' =P$.
It follows that we have $T U =Id$, since $P$ is an epimorphism.
On the other hand, the functor $H'$ is an epimorphism by Lemma \ref{localisationaredominant}, since it is a localisation.
It follows that we have $U T=Id$, since we have
$U T H'=U P =H'$.
We have proved that the functor $U$ and $T$ are mutually inverse.
Let us now show that a homotopy equivalence $f:X\to Y$ 
is acyclic. We shall first consider the case where $f$ is a fibration.
There exists a map $g:X\to Y$ such that 
$f g\sim 1_Y$ and $g f\sim 1_X$, since $f$
is a homotopy equivalence by assumption.
There is then a left homotopy $h:f g\to_l 1_Y$
defined on a cylinder $I Y$.
I then follows from the covering homotopy theorem \ref{coveringhomotopy}
that there exists a left homotopy $H:I Y\to X$
such that $H i_0=g$, since $f$ is a fibration.
Let us put $q=H i_1$. Then $f q =1_Y$ and $q\sim g$.
Thus, $q f\sim g f \sim 1_X$, since the homotopy
relation is a congruence. Hence the map $q f$ is acyclic by Lemma
\ref{weakequivandhomotopy}, since $1_X$ is acyclic.
But the map $f:X\to Y$ is retract of the map $q f:X\to X$,
since the following diagram commutes and
we have $f q =1_Y$,
\begin{xymatrix}
X\ar[d]_{f}  \ar[r]^{1_X} & X  \ar[d]^{qf}  \ar[r]^{1_X} & X\ar[d]^f\\
Y \ar[r]^{q}    & X \ar[r]^{f}   &  Y.
\end{xymatrix}
It then follows by Lemma 
\ref{Wclosedunderretracts} that $f$ is a weak equivalence. 
The implication ($\Leftarrow$)
is proved in the case where $f$ is a
fibration. In the general case, let us choose
a factorisation $f=p u:X\to E\to Y$
with $u$ an acyclic cofibration and $p$
a fibration. The map $u$ is a homotopy equivalence
by the first part of the proof,
since it is acyclic.
Thus, $p$ is a homotopy equivalence 
by three-for-two for homotopy equivalences, 
since $f$ is a homotopy equivalence by assumption.
Thus, $p$ is acyclic since it is a fibration. 
Hence the composite $f= p u $ is acyclic by three-for-two.
=--



+-- {: .num_defn #homotopycat1}
###### Definition
A **fibrant replacement** of an object $X$
is a fibrant object $X'$ together with
an acyclic cofibration $X\to X'$.
A **cofibrant replacement** of an object $X$
is a cofibrant object $X'$ together with
an acyclic fibration $X'\to X$.
=--


A fibrant replacement of $X$
is obtained by factoring the map $X\to \top$
as an acyclic cofibration $i_X:X\to R X$
followed by a fibration $R X\to \top$.
If $X$ is fibrant, we can take $R X =X$
and $i_X=1_X$.
Similarly, a cofibrant replacement of $X$
is obtained by factoring the map $\bot \to X$
as a cofibration $\bot \to Q X$ 
followed by an acyclic fibration $q_X:Q X\to X$.
If $X$ is cofibrant, we can take $Q X =X$
and $q_X=1_X$.

A fibrant replacement of a cofibrant 
object is cofibrant; it is thus fibrant-cofibrant.
Dually a cofibrant replacement
of a fibrant object is fibrant-cofibrant. 

The composite $q_X i_X:Q X\to R X$
is acyclic. It can thus be factored
as an acyclic cofibration $j_X:Q X\to W X$
followed by an acyclic fibration $p_X:W X\to R X$,
\[
\label{23}
\]
\begin{xymatrix}
X \ar[r]^{i_X} &  R X\\
Q X \ar[u]^{q_X} \ar[r]_{j_X}   & W X \ar[u]_{p_X}
\end{xymatrix}
The object $W X$ is a **fibrant-cofibrant
replacement** of the object $X$.
If $X$ is cofibrant, we can take $W X=R X$,
and if $X$ is fibrant, we can take $W X =Q X$
(in which case we have $W X =X$, when $X$ is fibrant-cofibrant).




+-- {: .num_lemma #cofibrantreplacement}
###### Lemma
For every map $u:X\to Y$, there exits two maps 
$R(u):R X\to R Y$
and $W(u):W X\to W Y$ fitting in the following 
commutative diagram, 

\[
\label{57}
\]
\begin{xymatrix}
X  \ar[r]^{u}  \ar[d]_{i_X}   &  \ar[d]^{i_Y} Y \\
R X \ar@{.}[r]^{R(u)}    &  R Y \\
W X   \ar@{.}[r]^{W(u)} \ar[u]^{p_X}   &  W Y. \ar[u]_{p_Y}
\end{xymatrix}
The map $R(u)$ is unique up to a right homotopy,
and the map $W(u)$ unique up to homotopy.
The maps $R(u)$ and $W(u)$ are acyclic
if $u$ is acyclic.
If $u:X\to Y$ and $v:Y\to Z$, then 
$R(v u)\sim_r R(v)R(u)$ and $W(v u)\sim W(v)W(u)$.
=--




+-- {: .proof}
######Proof
The map $R(u):R X\to R Y$ 
exists because $R Y$ is fibrant and the map $i_X$ is an acyclic cofibration. After choosing $R(u)$, we can choose the map $W(u):W X\to W Y$, since the object $W X$ is cofibrant and the map $p_Y$ is an acyclic fibration.
The map $R(u)$ is unique up to a right homotopy 
by Lemma \ref{prolongationhomotopy}, since $R Y$ is fibrant. Hence also the composite $R(u)p_X:W X\to R Y$, since the right homotopy relation is compatible
with composition on the right. But this composite
is also unique up to a left homotopy by Lemma \ref{leftandrightareequiv}, since the object $R Y$ is fibrant.  It follows by Lemma \ref{liftinghomotopy} that the map $W(u)$ is unique up to a left homotopy, 
since $p_Y$ is an acyclic fibration.
The first statement is proved.
Let us prove the second statement.
If $u$ is a weak equivalence, then so are the maps 
$R(u)$ and $W(u)$ by three-for-two, since the
vertical sides of the diagram (eq:57) are acyclic.
Let us prove the third statement.
If we compose horizontally the following diagram,
\begin{xymatrix}
X   \ar[d]_{i_X} \ar[r]^{u}  &  \ar[d]^{i_Y} Y \ar[r]^{v}  &  \ar[d]^{i_Z} Z \\
R X \ar[r]^{R(u)}    &  R Y \ar[r]^{R(v)}    &  R Z \\
W X  \ar[u]^{p_X}  \ar[r]^{W(u)}   &  W Y \ar[u]^{p_Y} 
 \ar[r]^{W(v)}   &  W Z, \ar[u]_{p_Z}
\end{xymatrix}
we obtain the  following diagram,
\begin{xymatrix}
X   \ar[d]_{i_X} \ar[rr]^{v u}  &    &  \ar[d]^{i_Z} Z \\
R X \ar[rr]^{R(v)R(u)}     &   &  R Z \\
W X  \ar[u]^{p_X}  \ar[rr]^{W(v)W(u)}   &   &  W Z, \ar[u]_{p_Z}
\end{xymatrix}
which should be compared with the diagram,
\begin{xymatrix}
X   \ar[d]_{i_X} \ar[rr]^{v u}  &    &  \ar[d]^{i_Z} Z \\
R X \ar[rr]^{R(v u)}     &   &  R Z \\
W X  \ar[u]^{p_X}  \ar[rr]^{W(v u)}   &   &  W Z, \ar[u]_{p_Z}
\end{xymatrix}
It then follows from the homotopy uniqueness 
that we have $R(v u)\sim_r R(v)R(u)$ and $W(v u)\sim W(v)W(u)$.
=--


+-- {: .num_theorem #homotopycategory2}
###### Theorem 
The four canonical functors in the following square
are equivalences of categories,
\begin{xymatrix}
\mathrm{Ho}(\mathbf{ E}_{f c})\ar[d]    \ar[r] &  
\mathrm{Ho}(\mathbf{ E}_f)\ar[d]  \\
\mathrm{Ho}(\mathbf{ E}_c)  \ar[r]& \mathrm{Ho}(\mathbf{ E}).
\end{xymatrix}
A map $u:A\to B$ is acyclic iff it is inverted
by the canonical functor $H:\mathbf{ E}\to \mathrm{Ho}(\mathbf{ E})$.
=--


+-- {: .proof}
######Proof
Let us first show that the diagonal functor
$F:\mathrm{Ho}(\mathbf{ E}_{f c}) \to \mathrm{Ho}(\mathbf{ E})$
is an equivalence of categories. 
We shall use the following commutative square of functors,
\[
\label{67}
\]
\begin{xymatrix}
\mathbf{E}_{f c}\ar[d]_{H'}    \ar[r] &  
\mathbf{ E} \ar[d]^{H} \\
 \mathrm{Ho}(\mathbf{ E}_{cf})  \ar[r]^F & 
\mathrm{Ho}(\mathbf{ E}),
\end{xymatrix}
where the top functor is the inclusion
and the vertical functor are the canonical functors.
We have $F(H'(u))=H(u)$ for every map 
$u\in \mathbf{ E}_{f c}$. 
For every map $u:X\to Y$ in $\mathbf{ E}$,
the map $W(u):W X\to W Y$
is well defined up to homotopy
by Lemma \ref{cofibrantreplacement}.
Hence the morphism $H' W(u):W X \to W Y$
is independant of the choice of $W(u)$
by Lemma \ref{preservinghomotopies}.
If $u:X\to Y$ and $v:Y\to Z$,
then $W(v u)\sim W(v)W(u)$ 
by Lemma \ref{cofibrantreplacement}.
Thus, $H' W(v u)= H' W(v) H' W(u)$. 
This defines a functor
$H' W: \mathbf{ E} \to \mathrm{Ho}(\mathbf{ E}_{f c})$.
The functor $H' W$ takes a weak equivalence to 
an isomorphism, since $W$
takes a weak equivalence to a weak equivalence
by Lemma \ref{cofibrantreplacement}.
It follows that there is a unique 
functor  $G: \mathrm{Ho}(\mathbf{ E})\to 
\mathrm{Ho}(\mathbf{ E}_{f c})$ such that the
following square commutes,
\[
\label{67}
\]
\begin{xymatrix}
\mathbf{ E} \ar[d]_{H}    \ar[r]^W &  
\mathbf{ E}_{f c} \ar[d]^{H'} \\
\mathrm{Ho}(\mathbf{ E})  \ar[r]^G & 
\mathrm{Ho}(\mathbf{ E}_{cf}).
\end{xymatrix}
By construction, have $G H(u)=H' W(u)$ for every map $u:X\to Y$. Let us show that the functors $F$ and $G$ are quasi-inverses. 
Observe first that we have $W(u) \sim u$ for a map $u$ in $\mathbf{E}_{f c}$ (we could even suppose that $W(u)=u$); thus $G F H'(u)=G H(u)=H' W(u)=H'(u)$ in this case. This shows that $G F H' =H'$ and it follows that $G F =Id$, since the functor $H'$ is epic by Lemma \ref{localisationaredominant}. Let us now show that the composite $F G$ is isomorphic to the identity of the category $\mathrm{Ho}(\mathbf{E})$. For this, it suffices to show that the functors $F G H$ and $H$ are isomorphic by Lemma \ref{localisationaredominant}, since the functor $H$ is a localisation. We have $F G H(X)= W X$ for every object $X$.
Moreover, for every map $u:X\to Y$, the map $F G H(u):F G H(X)\to F G H(Y)$ is equal to the map $H W(u):W X \to W Y$,
since $F G H(u)= F H' W (u)= H W (u)$. The maps $i_X\to R X $ and $p_X:W X \to R X$ are invertible in the category $\mathrm{Ho}(\mathbf{ E})$ since they are acyclic.
Let us put $\theta_X=H(p_X)^{-1}H(i_X):X\to W X$
in the category $\mathrm{Ho}(\mathbf{ E})$.
This defines a 
natural isomorphim $\theta: H\to F G H$
since the image by $H$ of the commutative diagram
(eq:57) is a commutative diagram 

\[
\label{76}
\]
\begin{xymatrix}
X  \ar[rr]^{H(u)}  \ar[d]^{H(i_X)} \ar@/_3pc/[dd]_{\theta_Y}  & &  
\ar[d]_{H(i_Y)}  Y \ar@/^3pc/[dd]^{\theta_Y}
\\
 R X \ar[rr]^{H R(u)}    &  &   R Y \\
 W X   \ar[rr]^{H W(u)} \ar[u]_{H(p_X)}   & &  
 W Y \ar[u]^{H(p_Y)}
\end{xymatrix}
It then follows from Lemma \ref{localisationaredominant}
that there is a natural isomorphism
$Id \to F G$.
We have proved that the functor $F$
is an equivalence of categories. 
The proof that the canonical functor
$\mathrm{Ho}(\mathbf{ E}_{f}) \to \mathrm{Ho}(\mathbf{ E})$
is an equivalence of categories
is similar except that it uses the fibrant
replacement $R$ instead of the fibrant-cofibrant
replacement $W$.
It then follows by duality that the canonical functor
$\mathrm{Ho}(\mathbf{ E}_{c}) \to \mathrm{Ho}(\mathbf{ E})$
is an equivalence of categories.
Let us now prove that a map 
$u:X\to Y$ is acyclic iff it is inverted
by the canonical functor $H:\mathbf{ E}\to \mathrm{Ho}(\mathbf{ E})$. The implication ($\Rightarrow$) is clear by definition of
the functor $H$. Conversely, if $H(u)$ is invertible,
let us show that $u$ is acyclic. The square (eq:77) shows that the map $H W(u)$ is also invertible since the vertical sides of the square are invertible. But we have $H W(u)=F H' W(u)$.
Hence the map $H' W(u)$ is invertible in the category $\pi\mathbf{ E}_{cf}$, since the functor $F$ is an equivalence.
This shows that $W u$ is a homotopy equivalence.
Thus, $W u$ is acyclic by Theorem \ref{weakequivandhomotopy}.
It then follows by three-for-two that $u$ is acyclic, since the vertical maps in the diagram (eq:57) are acyclic.
=--



+-- {: .num_cor #homotopycategoryislocallysmall}
###### Corollary
If the category $\mathbf{E}$
is locally small, then so is the category 
$\mathrm{Ho}(\mathbf{ E})$
=--


+-- {: .proof}
######Proof
The category $\mathbf{E}_{f c}$ is locally small
since it is a subcategory of $\mathbf{E}$.
Hence the category $\pi\mathbf{E}_{f c}$
is locally small, since it is a quotient
of the category $\mathbf{E}_{f c}$
by a congruence relation.
It follows by Theorem \ref{weakequivandhomotopy}
that the category $\mathrm{Ho}(\mathbf{E}_{f c})$
is locally small. It then follows by Theorem
\ref{homotopycategory2} that the 
category $\mathrm{Ho}(\mathbf{E})$
is locally small.
=-- 




+-- {: .num_cor #corolrighthomotopyfunctor}
###### Corollary
A map between cofibrant objects
$u:A\to B$ is acyclic iff
the map $\pi(u,X):\pi(B,X)\to \pi(A,X)$
is bijective for every fibrant-cofibrant object $X$.
=--

+-- {: .proof}
######Proof
The implication ($\Rightarrow$) 
was proved in Lemma \ref{righthomotopyfunctor}.
Conversely, if the map
$\pi(u,X):\pi(B,X)\to \pi(A,X)$
is bijective for every fibrant-cofibrant object $X$,
let us show that $u$ is acyclic.
For this, let us choose fibrant
replacements $i_A:A\to R A$ and $i_B:B\to R B$ 
of the objects $A$ and $B$,
together with a map $R(u):R A\to R B$
fitting in a commutative square,
\[
\label{97}
\]
\begin{xymatrix}
A  \ar[d]_{u}  \ar[rr]^{i_A}    & &  \ar[d]^{R(u)} R A \\
B   \ar[rr]^{i_B}    &  & R B.
\end{xymatrix}
The horizontal maps of the following square
are bijective by Lemma \ref{righthomotopyfunctor},
since the maps $i_A$ and $i_B$ are acyclic,
\begin{xymatrix}
\pi(A,X)    & &  \ar[ll]_{\pi(i_A,X)}  \pi(R A,X) \\
\pi(B,X) \ar[u]^{\pi(u,X)}      & & 
  \ar[ll]^{\pi(i_B,X)} \pi(R B,X)\ar[u]_{\pi(R(u),X)}.
\end{xymatrix}
It follows that the map $\pi(R(u),X)$ is bijective,
since the map $\pi(u,X)$ is bijective. 
It then follows by using the Yoneda embedding that the 
map $R(u)$ is invertible in the category $\pi\mathbf{E}_{f c}$.
This shows that the map $R(u)$ is a acyclic by Theorem \ref{weakequivandhomotopy}.
It then follows by three-for-two applied to
the square (eq:97) that the map $u$ is acyclic.
=--


###Determination###



+-- {: .num_prop #determination1}
###### Proposition
A model structure $(\mathcal{C},\mathcal{W},\mathcal{F})$
in a category $\mathbf{E}$
is determined by any two of its three classes.
A map $f:X\to Y$ is a weak equivalence iff
it admits a factorisation
$f=p u:X\to E\to Y$ with $u$ an acyclic cofibration
and $p$ an acyclic fibration.
=--

+-- {: .proof}
###### Proof
The class $\mathcal{C}\,\cap\, \mathcal{W}$
determines the class $\mathcal{F}$,
since the pair $( \mathcal{C}\,\cap\, \mathcal{W},\mathcal{F})$
is a weak factorisation system. Hence the pair 
$(\mathcal{C},\mathcal{W})$ determines the class $\mathcal{F}$.
Dually, the pair $(\mathcal{F},\mathcal{W})$ determines the class $\mathcal{C}$. Let us show that the pair $(\mathcal{C},\mathcal{F})$ determines the class $\mathcal{W}$.
Obviously, the pair $(\mathcal{C},\mathcal{F})$
determines the pair 
$(\mathcal{C}\,\cap\, \mathcal{W},\mathcal{F}\,\cap\, \mathcal{W})$
since $\mathcal{C}\,\cap\, \mathcal{W}={}^\pitchfork\mathcal{F}$
and $\mathcal{F}\,\cap\, \mathcal{W}=\mathcal{C}^\pitchfork$.
Hence it suffices to show that a map $f:X\to Y$ is a weak equivalence iff it admits a factorisation
$f=p u:X\to E\to Y$ with $u$ an acyclic cofibration
and $p$ an acyclic fibration. The implication ($\Leftarrow$)
is clear, since the class $\mathcal{W}$ is closed
under composition. Conversely, if $f:X\to Y$
is a weak equivalence, let us choose a factorisation $f=p u$ 
with $u$ an acyclic cofibration and $p$ a fibration.
The map $p$ is acyclic by three-for-two, since the maps $f$ and $u$ are acyclic.
Thus, $p\in \mathcal{F}\,\cap\,\mathcal{W}$.
=--


Let us denote by $M_f$ (resp. $M_c$, $M_{f c}$) the class
of fibrant (resp. cofibrant, fibrant-cofibrant) objects 
of a model structure $M=(\mathcal{C},\mathcal{W},\mathcal{F})$ 
in a category $\mathbf{E}$.


+-- {: .num_prop #determination2}
###### Proposition 
A model structure $M=(\mathcal{C},\mathcal{W},\mathcal{F})$ in a category $\mathbf{E}$ is determined by its class of cofibrations and its class 
$M_{f}$ of fibrant objects (resp. its class $M_{f c}$ of fibrant-cofibrant objects). More precisely, if $M'=(\mathcal{C},\mathcal{W}',\mathcal{F}')$ 
is another model structure with the same cofibrations,
then the four conditions

 $$\mathcal{W}\subseteq \mathcal{W}',
 \quad \quad \quad  M'_{f}\subseteq M_{f}, \quad \quad \quad 
 M'_{f c}\subseteq M_{f c}, \quad \quad \quad 
 \mathcal{W}_c\subseteq \mathcal{W}'_c ,$$

are equivalent.
=--


+-- {: .proof}
######Proof: 
We shall use the equality
$$\mathcal{F}\,\cap\, \mathcal{W}=\mathcal{C}^\pitchfork=\mathcal{F}'\,\cap\, \mathcal{W}'$$
and the inclusion $\mathcal{C}^\pitchfork\subseteq \mathcal{W}\,\cap\, \mathcal{W}'$.
Let us prove the implication (1)$\Rightarrow$(2).
If $\mathcal {W}\subseteq \mathcal {W}'$, then 
$\mathcal{C}\,\cap\,\mathcal{W}\subseteq \mathcal{C}\,\cap\, \mathcal{W}'$.
Thus, $\mathcal {F}'\subseteq \mathcal {F}$,
since $\mathcal{F}=(\mathcal{C}\,\cap\, \mathcal{W})^\pitchfork $
and $\mathcal{F}'=(\mathcal{C}\,\cap\, \mathcal{W}')^\pitchfork $.
It follows that $M'_{f}\subseteq M_{f}$.
The implication (1)$\Rightarrow$(2) is proved. 
The implication (2)$\Rightarrow$(3) is obvious,
since $M_{c}=M'_{c}$. Let us prove the implication (3)$\Rightarrow$(4). If $A$ is cofibrant and $X\in \subseteq M_{f c}$ (resp. $X\in \subseteq M'_{f c}$) let us denote by $\pi(A,X)$ (resp. $\pi'(A,X)$) the set of homotopy classes of maps $A\to X$ with respect to the model structure $M$ (resp. $M'$).
We claim that if $X\in M'_{f c}$, then the left homotopy relation between the maps $A\to X$ only depends on the weak factorisation system $(\mathcal{C},\mathcal{C}^\pitchfork)$. 
To see this, observe that a cylinder object of $A$ can be constructed by factoring the map $\nabla_A:A\sqcup A \to A$ as a cofibration $(d_1,d_0):A\sqcup A\to I A$
followed by a map $s:I A\to A$ in $\mathcal{C}^\pitchfork$.
The left homotopy relation between the maps $A\to X$
can be defined by using this cylinder alone
by Lemma \ref{lefthomotopysinglecylinder}, since the object $X$ is fibrant in both model structures under the assumption that $M'_{f c}\subseteq M_{f c}$. This shows that the left homotopy relation between the maps $A\to X$ only depends on the system 
$(\mathcal{C},\mathcal{C}^\pitchfork)$ if $X\in M'_{f c}$. It follows that we have $\pi'(A,X)=\pi(A,X)$ if $A$ is cofibrant
and $X\in M'_{f c}$. We can now prove that $\mathcal{W}_c\subseteq \mathcal{W}'_c$. If a map $u:A\to B$ belongs to $\mathcal {W}_c$, then the map $\pi(u,X):\pi(B,X)\to \pi(A,X)$ is bijective for every object $X\in M_{f c}$ by Corollary \ref{corolrighthomotopyfunctor},
hence also the map $\pi'(u,X):\pi'(B,X)\to \pi'(A,X)$
for every object $X\in M'_{f c}$.
This shows that $u\in \mathcal {W}'_c$ by the same corollary.
The inclusion $\mathcal{W}_c\subseteq \mathcal{W}'_c$
is proved. Let us now prove the implication (4)$\Rightarrow$(1).
Let $u:A\to B$ be a map in $\mathcal {W}$.
Let us factor the map $\bot \to A$
as a cofibration $\bot \to A'$ followed by a map
$q_A:A'\to A$ in $\mathcal{C}^\pitchfork$,
and then factor the composite $u q_A:A'\to B$
as a cofibration $u':A'\to B'$ followed
by a map $q_B:B'\to B$ in $\mathcal{C}^\pitchfork$.
We obtain a commutative square
\begin{xymatrix}
A'  \ar[d]_{u'}  \ar[r]^{q_A}   &  \ar[d]^u A \\
B'   \ar[r]^{q_B}    & B.
\end{xymatrix}
with $q_A,q_B\in \mathcal{W}\,\cap\, \mathcal{W}'$,
since $\mathcal{C}^\pitchfork\subseteq \mathcal{W}\,\cap\, \mathcal{W}'$. We have $u'\in \mathcal{W}_c$ by three-for-two, since $u\in \mathcal{W}$.
Thus, $u'\in \mathcal{W}'_c$, 
since $\mathcal{W}_c\subseteq \mathcal{W}'_c$ by assumption. 
It  follows by three-for-two that $u\in \mathcal{W}'$.
The implication (4)$\Rightarrow$(1)
is proved. 
=--


+-- {: .num_cor #detemination4}
###### Corollary 
A model structure $(\mathcal{C},\mathcal{W},\mathcal{F})$ in a category $\mathbf{E}$ is determined by its subcategory of fibrant
objects $\mathbf{E}_{f}$ together with one of the classes
$\mathcal{C}$ or $\mathcal{F}\, \cap\, \mathcal{W}.$
Dually, a model structure $(\mathcal{C},\mathcal{W},\mathcal{F})$ 
is determined by its subcategory of cofibrant
objects $\mathbf{E}_{c}$ together with one of the classes
$\mathcal{F}$ or $\mathcal{C}\, \cap\, \mathcal{W}.$
=--


+-- {: .proof}
######Proof: 
The first statement follows from Proposition \ref{determination2}
and by using the fact that $\mathcal{C}={}^\pitchfork(\mathcal{F}\, \cap\, \mathcal{W})$. The rest follows by duality.
=-- 



+-- {: .num_cor #determination3}
###### Corollary 
A model structure $(\mathcal{C},\mathcal{W},\mathcal{F})$ in a category $\mathbf{E}$ is determined by its subcategory of fibrant-cofibrant
objects $\mathbf{E}_{f c}$ together with one of the classes

$$\mathcal{C}, \quad \mathcal{C}\,\cap\, \mathcal{W}, \quad \mathcal{F},
 \quad \mathcal{F}\, \cap\, \mathcal{W}.$$
=--


+-- {: .proof}
######Proof: 
This follows from Proposition \ref{determination2}
in the case of the class $\mathcal{C}$,
and also in the case of the class $\mathcal{F}\, \cap\, \mathcal{W}$,
since we have $\mathcal{C}={}^\pitchfork(\mathcal{F}\, \cap\, \mathcal{W})$.
The rest follows by duality.
=--
 



##Derived functors##



###Definitions###


Let $\Sigma$ be a set of arrows in a category  $\mathbf{A}$,
and let $P:\mathbf{A} \to \Sigma^{-1}\mathbf{A} $
be the localisation functor.
We saw in Lemma \ref{localisationaredominant}
that for any category $\mathbf{M}$, the functor 
$$P^*:[\Sigma^{-1}\mathbf{A},\mathbf{M}] \to [\mathbf{A},\mathbf{M}]$$
induced by $P$ is fully faithful, and that it induces
an isomorphism between the category 
$[\Sigma^{-1}\mathbf{A},\mathbf{M}]$ and the full subcategory
of $[\mathbf{A},\mathbf{M}]$
spanned by the functors $\mathbf{A}\to \mathbf{M}$
which inverts the elements of $\Sigma$. 
We can thus identify these categories, by using the same
notation for a functor $G:\Sigma^{-1}\mathbf{A}\to \mathbf{M}$
and the functor $G P:\mathbf{A}\to \mathbf{B}$.
In which case the category $[\Sigma^{-1}\mathbf{A},\mathbf{M}]$ 
becomes a full subcategory of the
category $[\mathbf{A},\mathbf{M}]$.
The [[Kan extensions|left Kan extension]] of a functor 
$F:\mathbf{A}\to \mathbf{M}$ along the functor $P$
is a functor $F':\Sigma^{-1}\mathbf{A}\to \mathbf{M}$ 
equipped with a natural transformation $\eta:F\to F'$
which _reflects_ $F$ into the full subcategory 
$[\Sigma^{-1}\mathbf{A},\mathbf{M}]$.
More precisely, for any functor
$G:\Sigma^{-1}\mathbf{A}\to \mathbf{M}$ and any natural
transformation $\alpha: F\to G$, there exists a unique
natural transformation $\alpha':F'\to G$
such that $\alpha'\eta=\alpha$,
\begin{xymatrix}
& &  &  &  \\
& & &  & [\Sigma^{-1}\mathbf{A},\mathbf{M}] \\
F \ar[ddrrrr]_(0.45)\alpha \ar[rrr]^{\eta}  && &  F' \ar@{.}[ddd]\ar@{.}[uu]  \ar[ddr]^{\alpha'} & \\  
&&  &  &  \\
&&  &  & G. \\
& &  &  &
\end{xymatrix}
The functor $F'$ can thus be regarded
as the best _right_ approximation of the functor 
$F$ by a functor inverting the elements in $\Sigma$. 

Dually, the [[Kan extensions|right Kan extension]] of a functor 
$F:\mathbf{A}\to \mathbf{M}$ along the functor $P$
is a functor $F':\Sigma^{-1}\mathbf{A}\to \mathbf{M}$ 
equipped with a natural transformation $\epsilon:F'\to F$
which _coreflects_ $F$ into the full subcategory 
$[\Sigma^{-1}\mathbf{A},\mathbf{M}]$.
More precisely, for any functor
$G:\Sigma^{-1}\mathbf{A}\to \mathbf{M}$ and any natural
transformation $\beta: G\to F$, there exists a unique
natural transformation $\alpha':G\to F'$
such that $\epsilon \alpha'=\alpha$,
\begin{xymatrix}
&  &  &   & \\
[\Sigma^{-1}\mathbf{A},\mathbf{M}]  &  &  &   & \\
& F' \ar@{.}[dd]\ar@{.}[uu]  \ar[rrr]^{\epsilon}  &  &   & F   \\  
&  &   & & \\
G\ar[uur]^{\alpha'} \ar[uurrrr]_(0.55)\alpha   &  &    & &
\end{xymatrix}
The functor $F'$ can thus be regarded
as the best _left_ approximation of the functor 
$F$ by a functor inverting the elements in $\Sigma$. 




+-- {: .num_defn #Derivedfunctordef}
###### Definition
Let $\mathbf{E}$ be a category equipped with a class $\mathcal{W}$
of weak equivalences.
The **right derived functor** of a functor 
$F:\mathbf{E}\to \mathbf{M}$ is defined to be the best
dexter approximation $\eta:F\to F^R$ of the functor $F$ 
by a functor $F^R$ inverting weak equivalences. 
Dually, the **left derived functor** of $F$ 
is defined to be the best sinister approximation $\epsilon:F^L\to F$
of the functor $F$ by a functor  $F^L$ inverting weak equivalences. 
=--



We shall say a right derived
functor $\eta:F\to F^R$ is **absolute** if it stays
a right derived functor after postcomposing it with
any functor $U: \mathbf{M}\to  \mathbf{N}$, that is, if 
the natural transformation
$U(\eta):U F\to U F^R$ exibits the functor  $U F^R$
as the the right derived functor $(U F)^R$ of $U F$.
Dually, We shall say a left derived
functor $\epsilon:F^L\to F$ is **absolute** if it stays
a left derived functor after postcomposing it with
any functor $U: \mathbf{M}\to  \mathbf{N}$, that is, if
the natural transformation
$U(\epsilon):U F^L\to U F $ exibits the functor  $U F^L$ 
as the left derived functor $(U F)^L$ of $U F$.






+-- {: .num_prop #Derivedfunctordef}
###### Proposition
Let $\mathbf{E}$ be a model category,
and $F:\mathbf{E}\to \mathbf{M}$ be a functor
which inverts weak equivalences between fibrant 
objects. Then the right derived functor
$\eta:F\to F^R$ exists and
it is absolute.
Moreover, the map $\eta_X:F X\to F^R X$
is an isomorphism when $X$ is fibrant.
=--


+-- {: .proof}
######Proof: 
For each object $X\in \mathbf{E}$, let us choose
a fibrant replacement $i_X:X\to R X$; we shall take $i_X =1_X:X\to X$
when $X$ is fibrant. By Lemma \ref{cofibrantreplacement},
for every map $u:X\to Y$, there exits a map 
$R(u):R X\to R Y$
fitting in the 
commutative square,
\[
\label{100}
\]
\begin{xymatrix}
X  \ar[r]^{u}  \ar[d]_{i_X}   &  \ar[d]^{i_Y} Y \\
R X \ar@{.}[r]^{R(u)}    &  R Y
\end{xymatrix}
The map $R(u)$ is unique up to a right homotopy
by Lemma \ref{cofibrantreplacement}.
Hence the map $F R(u):F R X \to F R Y$ does not 
depends on the choice of $R(u)$ by 
Lemma \ref{preservinghomotopies}.
Moreover, if $u:X\to Y$ and $v:Y\to Z$,
then we have $F R (v u)=F R(v) F R(u)$
by the same lemma. We thus
obtain a functor 
$F^R=F R:\mathbf{E} \to \mathbf{M}$.

The functor $F^R$ inverts weak equivalences,
since $R(u)$ is a weak equivalence between
fibrant objects when $u$ is a weak equivalence
by Lemma \ref{cofibrantreplacement}.
Thus, $F^R:Ho(\mathbf{E}) \to \mathbf{M}$.
Notice that $F^R X =F X$
when $X$ is fibrant.
The image by $F$ of the square (eq:100) is a commutative square,
\begin{xymatrix}
F X  \ar[r]^{F(u)}  \ar[d]_{F(i_X)}   &  \ar[d]^{F(i_Y)} F Y \\
F R X \ar[r]^{F R(u)}    &  F R Y.
\end{xymatrix}
It shows that we can define a natural
transformation $\eta:F\to F^R$ by
putting $\eta_X=F(i_X):F X\to F R X$
for every object $X$.
Notice that we have $\eta_X=1_{F X}$
when $X$ is fibrant.
Let us show that the natural transformation $\eta:F\to F^R$
is _reflecting_ the functor $F$ into the subcategory 
$[Ho(\mathbf{E}),\mathbf{M}]$
of the category $[\mathbf{E},\mathbf{M}]$.
For this we have to prove that for any functor 
$G: Ho(\mathbf{E})\to  \mathbf{M}$ 
and any natural transformation
$\alpha:F\to G$ 
there exists a unique natural transformation 
$\alpha':F^R\to G$ such that $\alpha'\eta =\alpha$,
\begin{xymatrix}
& & &  & [Ho(\mathbf{E}),\mathbf{M}] \\
F \ar[ddrrrr]_(0.45)\alpha \ar[rrr]^{\eta}  && &  F^R \ar@{.}[dd]\ar@{.}[u]  \ar[ddr]^{\alpha'} & \\  
&&  &  &   \\
&&  &  &  G.
\end{xymatrix}
The map $G(i_X):G X\to G R X$ in the following 
square 

\[
\label{99}
\]
\begin{xymatrix}
F X  \ar[r]^{\alpha_X}  \ar[d]_{F(i_X)}   &  
\ar[d]^{G(i_X)} G X \\
F R X \ar[r]^{\alpha_{R X}}    &  G R X.
\end{xymatrix}
is invertible by the assumption on $G$, since $i_X$ is a weak equivalence. We can thus defines a 
map $\alpha'_X:F R X\to G X$ by putting 
$\alpha_X=G(i_X)^{-1}\alpha_{R X}$.
Let us verify that this defines a natural transformation 
$\alpha':F^R\to G$. 
The right hand square of the
following diagram commutes for any map 
$u:X\to Y$ by the functoriality of $G$,
since the square (eq:100) commutes,
\begin{xymatrix}
F R X   \ar@/^3pc/[rr]^{\alpha'_X}  \ar[r]^{\alpha_{R X}}  \ar[d]_{F R(u)}   
&  \ar[d]_{G R(u)} G R X & \ar[l]_(0.42){G(i_X)} G X \ar[d]^{G(u)} \\
F R Y \ar[r]^{\alpha_{R Y}} \ar@/_3pc/[rr]_{\alpha'_Y}  & G R Y &  \ar[l]_(0.42){G(i_Y)} G Y.
\end{xymatrix}
And the left hand square commutes by the naturality of $\alpha$.
The naturality of $\alpha'$ is proved.
Observe that we have
$G(i_X)^{-1} \alpha_{R X} F(i_X)=\alpha_X$
for every object $X$, 
since the square (eq:99) commutes.
This proves that $\alpha'\eta =\alpha$.
It remains to prove the uniqueness of $\alpha'$.
If $\beta:F R\to G$ is a natural
transformation such that $\beta\eta =\alpha$,
let us show that $\beta=\alpha'$.
Notice that $\beta_X=\alpha_X=\alpha'_X$
when $X$ is fibrant, since we have $\eta_X=1_{F X}$
in this case. In general, let us choose a weak
equivalence $w:X\to Y$ with codomain a fibrant object $Y$
(for example, $w=i_X:X\to R X$).
The bottom maps in the following two squares are
equal since $Y$ is fibrant,
\begin{xymatrix}
F R X  \ar[d]_{F R(w)}  \ar[r]^{\alpha'_X}   &  \ar[d]^{G(w)} G X \\
F R Y \ar[r]^{\alpha'_{Y}}    &  G Y.
\end{xymatrix}
Hence also the top maps, since $G(w)$ is invertible by the assumption on $G$. 
Thus, $\beta_X=\alpha'_X$.
We have proved that $F^R$ is the right 
derived functor of $F$. Moreover, the map $\eta_X$ is 
invertible when $X$ is fibrant, since we have 
$\eta_X=1_{F X}$ in this case.
For any functor $U: \mathbf{M}\to  \mathbf{N}$
we have $(U F)^R=(U F)R=U(F R)=U F^R $
and $U(\eta_X)=U F(i_X) $.
This shows that the right
derived functor $F^R $ is absolute. 
=--
 


###Quillen functors###


+-- {: .num_defn #Quillenfunctordef}
###### Definition
We shall say that a functor
$F:\mathbf{U}\to \mathbf{V}$ between two model categories
is a **left Quillen functor**  if it takes
a cofibration to a cofibration and an acyclic
cofibration to an acyclic cofibration. 
Dually, we shall say that $F$
is a **right Quillen functor** if it takes
a fibration to a fibration and an acyclic
fibration to an acyclic fibration.
=--




+-- {: .un_remark #cocontinuousQfunct}
######Remark
Most left Quillen functors that we shall 
consider are cocontinuous and have a right adjoint.
Dually, most right Quillen functors
have a left adjoint.
=--


+-- {: .num_lemma #KenBrownandQfunctor}
######Lemma
A left Quillen functor
takes an acyclic map between cofibrant objects
to an acyclic map. 
A right Quillen functor
takes an acyclic map between fibrant objects
to an acyclic map. 
=--


+-- {: .proof}
######Proof: 
This follows from Ken Brown's lemma \ref{Kenbrownorigianl}.
=--



+-- {: .num_lemma #Quillenpair}
######Lemma
Let $F:\mathbf{U}\leftrightarrow \mathbf{V}:G$
be an adjunction $F\vdash G$ 
between two model categories.
Then the left adjoint $F$
is a left Quillen functor iff the 
right adjoint $G$ is a right Quillen functor.
=--



+-- {: .proof}
######Proof: 
Let us denote by $(\mathcal{C},\mathcal{W},\mathcal{F})$
the model structure on $\mathbf{U}$
and by $(\mathcal{C}',\mathcal{W}',\mathcal{F}')$
the model structure on $\mathbf{V}$.
Then the conditions
$$F(\mathcal{C})\subseteq \mathcal{C}' \quad \mathrm{and} \quad
 G(\mathcal{F}'\,\cap\, \mathcal{W}')\subseteq \mathcal{F}\cap \mathcal{W}$$
are equivalent by the proposition [here](http://ncatlab.org/joyalscatlab/show/Weak+factorisation+system#adjointfunctorandwfs). 
Similarly, the conditions
$$F(\mathcal{C}\,\cap\, \mathcal{W})\subseteq \mathcal{C}'\,\cap\, \mathcal{W}' \quad \mathrm{and} \quad
 G(\mathcal{F}')\subseteq \mathcal{F}$$ 
are equivalent.
=--




+-- {: .num_defn #Quillenadjunctiondef}
###### Definition
We shall say that an adjunction $F\vdash G$
between two model categories is a **Quillen adjunction**
if the left adjoint $F$ is a left Quillen functor, 
or equivalently, if the right adjoint $G$ is a right Quillen functor. 
=--


##Examples of model categories##


+-- {: .num_example #Kanmodelstructurecat}
###### Example
The category of simplicial sets $\mathbf{SSet}$ admits a model structure,
called the [[Kan model structure]], in which the fibrant objects are the Kan complexes and the cofibrations are the monomorphisms. The weak equivalences are the weak homotopy equivalences and the fibrations are the Kan fibrations.
The model structure is cartesian closed and proper.
=--


+-- {: .num_example #naturalmodelstructurecat}
###### Example
The category $\mathbf{Cat}$ admits a model structure, called the
[natural model structure](http://ncatlab.org/joyalscatlab/show/Model+structures+on+Cat)
in which the cofibrations are the functors monic
on objects, the weak equivalences are the equivalences of categories
and the fibrations are the isofibrations.
The model structure is cartesian closed and proper.
=--


+-- {: .num_example #naturalmodelstructurecat}
###### Example
The category of simplicial sets $\mathbf{SSet}$ admits a model structure,
called the 
[[The model structure for quasi-categories|model structure for quasi-categories]],
in which the fibrant objects are the quasi-categories
and the cofibrations are the monomorphisms.
A weak equivalence is called a categorical equivalence
and a fibration is called an isofibration.
The model structure is cartesian closed and left proper.
=--



##Exercises##


+-- {: .num_exercise #duallemma}
###### Exercise
Gives a direct proof (without using the duality) to the lemmata \ref{productoffibrant} 
\ref{projectionpathobject} 
\ref{projectionmappingpath}
\ref{righthomotopyfixedpathobject} 
\ref{righthomotopyisequiv} 
\ref{extensionhomotopy} 
\ref{prolongationhomotopy} 
\ref{righthomotopyfunctor}
\ref{righthomotopicweakequiv}.
=--





+-- {: .num_exercise #fibcofibrantreplacement}
###### Exercise
Recall (from after Definition \ref{homotopycat1}) 
that a fibrant-cofibrant replacement
of an object $X$ is obtained by
factoring the composite $q_X i_X:Q X\to R X$
as an acyclic cofibration $j_X:Q X\to W X$
followed by an acyclic fibration $p_X:W X\to R X$.
Show that for every map $u:X\to Y$, there 
are maps $Q u$, $R u$ and $W u$ 
fitting in a commutative cube:
\begin{xymatrix}
X \ar[rr]  \ar[dr]^u &   & R X  \ar[dr]^{R u}  & \\ 
&  Y \ar[rr] &   & R Y  \\ 
Q X \ar[uu]\ar[dr]^{Q u} \ar '[r] [rr]&  & W X  
 \ar '[u] [uu]\ar[dr]^{W u} &  \\ 
& Q Y  \ar[uu] \ar[rr] &   & W Y. \ar[uu]
\end{xymatrix}
=--

+-- {: .num_exercise #homotopydist}
###### Exercise
Show that the distributor 
$\pi:\mathbf{E} \Rightarrow \mathbf{E}_f$
defined in (eq:33) induces a  distributor 
$\pi':\mathrm{Ho}(\mathbf{E}_c) \Rightarrow \mathrm{Ho}(\mathbf{E}_f)$.
Show that the distributor $\pi'$
is [representable](http://ncatlab.org/joyalscatlab/show/Distributors+and+barrels#defrepresentabledistributor)
by an equivalence of categories
$\mathrm{Ho}(\mathbf{E}_c) \to \mathrm{Ho}(\mathbf{E}_f)$.
=--




+-- {: .num_exercise #determinationnaturalmodelstructurecat}
###### Exercise
Show that the [natural model structure](http://ncatlab.org/joyalscatlab/show/Model+structures+on+Cat)
on $\mathbf{Cat}$ is characterised by each of the 
following four groups of conditions:

* Group 1:

  * the acyclic maps are the equivalences of categories

  * an acyclic map is a fibration iff it is a split epimorphism 

* Group 2:

  * the acyclic maps are the equivalences of categories

  * an acyclic map is a cofibration iff it is a split monomorphism

* Group 3:

  * every object is fibrant.

  * an acyclic map is a fibration iff it is a surjective equivalence

* Group 4:

  * every object is cofibrant.

  * an acyclic map is a cofibration iff it is a monic equivalence

=--









##References##



Papers:

* Dwyer, W.G., Spalinski, J.: _Homotopy Theories and Model Categories_. Handbook of Algebraic Topology. Edited By I.M. James. North Holland (1995). [pdf](http://hopf.math.purdue.edu/cgi-bin/generate?/Dwyer-Spalinski/theories)


* Maltsiniotis, Georges: _Quillen adjunction theorem for derived functors, revisited_. [pdf](http://arxiv.org/abs/math/0611952)



Lecture Notes and Textbooks:

* Dwyer, W.G., Hirschhorn, P.S., Kan, D.M., Smith, J.H.: _Homotopy Limit Functors on Model Categories and Homotopical Categories_. AMS Math. Survey and Monographs Vol 113 (2004)



* [[Peter Gabriel|Gabriel, P.]], Zisman, M.: _Calculus of Fractions and Homotopy Theory_. Ergeb. der Math. undihrer Grenzgebiete, vol 35, Springer-Verlag, New-York  (1967)

* Goerss, P.G., Jardine, J.F.: _Simplicial Homotopy Theory_. Progress in Mathematics vol. 174. Birkhâuser (1999)

* Hirschhorn, Philip S.: _Model Categories and their Localization_. AMS Math. Survey and Monographs Vol 99 (2002)

* Hovey, Mark: _Model Categories_. AMS Math. Survey and Monographs Vol 63 (1999)

* Quillen, Daniel: _Homotopical Algebra_. Lecture Notes in Mathematics, vol. 43. Springer Verlag, Berlin (1967)
