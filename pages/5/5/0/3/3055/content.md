Let $C$ be a [[category]] and $Arr(C)= C^2$ the corresponding [[arrow category]]: the objects in $Arr(C)$ are morphisms in $C$ and the morphisms $(f:x'\to x')\to (g:y\to y')$ in $Arr(C)$ are the commutative squares of the form 

$$\array{
x &\stackrel{v}\to& y\\
\downarrow\mathrlap{f} &&\downarrow\mathrlap{g}\\
x' &\stackrel{u}\to& y'
}$$

with the obvious composition. 

There is a [[functor]] $cod:Arr(C)\to C$ given on objects by the codomain (= target) map, and on morphisms it gives the lower arrow of the commutative square. This functor is in fact a [[Grothendieck fibration|fibered category]] in the sense of Grothendieck, whose inverse image functor $u^*(g)$ amounts to the usual pullback of $g$ along $u$ in $C$. The fiber over an object $c$ in $C$ is the [[overcategory]] $C/c$. This fibered category is called the **codomain fibration** over $C$ (some say the *basic fibration* or the *self-indexing* or the *fundamental fibration* --- anything with so many names must be important!). 

The inverse image functor $u^*$ has a *left* adjoint, namely a postcomposition functor $u_!: f\mapsto u\circ f$. Thus the codomain fibration is in fact a [[bifibration]], though traditionally its fibered aspect is emphasised (and it even motivates the notion of cartesianess for categories over categories).  A right adjoint $u_*$ of $u^*$ exists for every morphism $u$ in $C$ iff C is a [[locally cartesian closed category]].

A categorification in dimension 2 is a codomain 2-fibration, whose main example is $Cat^2$ over $Cat$.

For a dual notion see [[domain cofibration]]. 