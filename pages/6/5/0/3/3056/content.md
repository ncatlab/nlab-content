# Contents
* toc
{: toc}

## Idea

The notion of _domain opfibration_ is [[duality|dual]] to that of [[codomain fibration]]. See there for more details.

## Definition

Let $C$ be a [[category]] and $Arr(C)= C^2$ the corresponding [[arrow category]]: the objects in $Arr(C)$ are morphisms in $C$ and the morphisms $(f:x'\to x')\to (g:y\to y')$ in $Arr(C)$ are the [[commutative squares]] of the form

$$\array{
x &\stackrel{v}\to& y\\
\downarrow\mathrlap{f} &&\downarrow\mathrlap{g}\\
x' &\stackrel{u}\to& y'
}$$

with the obvious composition. 

There is a [[functor]] $dom:Arr(C)\to C$ given on objects by the domain (= source) map, and on morphisms it gives the lower arrow of the commutative square.  If $C$ has [[pushouts]], then this functor is in fact an [[Grothendieck opfibration|opfibered (cofibered) category]] in the sense of Grothendieck, whose pushforward functor $u_*$ amounts to the usual pushout of $f$ along $u$ in $C$.  The fiber over an object $c$ in $C$ is the [[undercategory]] $c\downarrow C$. This opfibered category is called the **domain opfibration** over $C$ (some say the *basic* opfibration). This notion is dual to the notion of [[codomain fibration]].

## Remarks on notation {#notation}

Although the pushforward functor in an opfibration is usually written $u_!$, in the case of the domain opfibration we usually write it as $u_*$ instead, following the notation of [[algebraic geometry]].  Each such functor also has a [[right adjoint]], given by precomposition (just as in the [[codomain fibration]] the pullback functors have left adjoints given by postcomposition).  Thus, the the domain opfibration is in fact a [[bifibration]], though traditionally its opfibered aspect is emphasised (and it even motivates the notion of cocartesianess for [[categories over categories]]).  And while the right adjoints in a bifibration are usually written as $u^*$, for the domain opfibration we write them as $u^!$, again to conform to usage in algebraic geometry, where the standard string of adjoints is $u_! \dashv u^* \dashv u_* \dashv u^!$.


[[!redirects domain cofibration]]
