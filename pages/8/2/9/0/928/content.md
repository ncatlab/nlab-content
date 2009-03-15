#Idea# 
In his development of an '[[algebraic homotopy]]' theory,
Baues uses interacting structures, one of Quillen type (or rather of
K. Brown's version of half of Quillen's theory) and the other of cylinder
functor type.  The two structures are called [[cofibration category|cofibration categories]] and 
_$I$-categories_.

# Definition

An **$I$-category** has various data specified: $(C, \mathit{cof}, I, \emptyset)$.

 Here $C$ is a category, $\mathit{cof}$ is a class of 'cofibrations', $\emptyset$ is an [[initial object]] of $C$, and $I$ is a [[cylinder functor]] (written as a functor, so $I(X)$ is the cylinder on object $X$).


These are required to satisfy: 

I 1)  $I$ is a cylinder functor;

I 2)  Pushout axiom (almost as in the first part of C2 of [[cofibration category]], but $I$ is also
to preserve pushouts, and $I(\emptyset) = \emptyset$ so in fact $I$ preserves all finite colimits);

I 3) Cofibration axiom:

* $\iso \subset \mathit{cof}$ (where $\iso$ is the class of [[isomorphism]]s in $C$);
* $\emptyset \rightarrow X$ is always in $\mathit{cof}$; 
* a composition of cofibrations is a cofibration and all morphisms in $\mathit{cof}$ satisfy the [[homotopy
extension property]].

I 4)  Relative cylinder axiom:

If $i : B \rightarrow A$ is a cofibration and one forms the pushout
$A \cup_B I(B)\cup_B A$,
then the natural map 
$$A \cup_B I(B)\cup_B A \rightarrow A\times I$$ 
is a cofibration;


I 5) The 'interchange' axiom.

For all objects $X$, there is a map
$$T : I^2(X) \rightarrow I^2(X)$$
interchanging the two copies of $I$,
i.e. 
$$T \circ e_i(I(X)) = I(e_i(X)), \quad T \circ I(e_i(X)) = e_i(I(X))$$
for $i = 0,1$.

(This corresponds to exchanging the first and second $I$-coordinates of
$X\times \mathbf{I} \times \mathbf{I}$ (where $I(X)$ is thought of as $X \times \mathbf{I}$), that is 
$$(x,s,t) \rightarrow (x,t,s).$$





