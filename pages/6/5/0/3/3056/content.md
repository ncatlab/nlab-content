[[!redirects domain cofibration]]
Let $C$ be a [[category]] and $Arr(C)= C^2$ the corresponding [[arrow category]]: the objects in $Arr(C)$ are morphisms in $C$ and the morphisms $(f:x'\to x')\to (g:y\to y')$ in $Arr(C)$ are the commutative squares of the form

$$\array{
x &\stackrel{v}\to& y\\
\downarrow\mathrlap{f} &&\downarrow\mathrlap{g}\\
x' &\stackrel{u}\to& y'
}$$

with the obvious composition. 

There is a [[functor]] $dom:Arr(C)\to C$ given on objects by the domain (= source) map, and on morphisms it gives the lower arrow of the commutative square.  If $C$ has [[pushouts]], then this functor is in fact an [[Grothendieck opfibration|opfibered (cofibered) category]] in the sense of Grothendieck, whose pushforward functor $u_*$ amounts to the usual pushout of $f$ along $u$ in $C$.  The fiber over an object $c$ in $C$ is the [[undercategory]] $c\downarrow C$. This opfibered category is called the **domain opfibration** over $C$ (some say the *basic* opfibration). This notion is dual to the notion of [[codomain fibration]].

The direct image functor $u_*$ has a *right* adjoint, namely a precomposition functor $u^!: f\mapsto g\circ u$. Thus the domain opfibration is in fact a [[bifibration]], though traditionally its opfibered aspect is emphasised (and it even motivates the notion of cocartesianess for categories over categories). 

[[!redirects domain cofibration]]