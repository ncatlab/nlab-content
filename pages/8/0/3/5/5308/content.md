## Definition. ##  
Let $J$ and $C$ be arbitrary categories.  The diagonal
functor $\Delta=\Delta_J\colon C\to C^J$ is the functor sending each
object $c$ to the constant functor $\Delta c$ (the functor having
value $c$ for each object of $J$ and value $1_c$ for each arrow of
$J$), and each arrow $f\colon c\to c'$ of $C$ to the the natural
transformation $\Delta f \colon \Delta c \stackrel{.}{\to} \Delta c'$
which has the same value $f$ at each object $j$ of $J$. 


Since $C$ is $J$-cocomplete ($J$-complete) iff $\Delta$ has a left
(right) adjoint, the general adjoint functor theorem may be
used in some cases to prove cocompleteness (completeness).  For this
to work, $\Delta$ must at least preserve small limits (colimits).

## Proposition. ##
Let $P$ and $C$ be arbitrary categories. Then
$\Delta_P\colon C\to C^P$ preserves _all_ limits that exist in $C$.

Before the proof, recall that limits in functor categories are
calculated pointwise. In some detail, if for an object 
$p\in \mathrm{obj}(P)$
we write $E_p:X^P\to X$ for the ''evaluate at $p$'' functor (with
$E_p(H\colon P\to X)=H(p)$ and $E_p(\sigma\colon
H\stackrel{.}{\to} H')=\sigma_p\colon H(p)\to H'(p)$),
then we have the following fact (Theorem V.3.1 on p. 115 of 
[[Categories Work]]):  If $S\colon
J\to X^P$ is such that for each object $p$ of $P$, $E_p S\colon J\to X$
has a limiting cone $\tau_p\colon L(p)\stackrel{.}{\to} E_p S$,
then there exists a unique functor $L$ with object function 
$p\mapsto L(p)$ such that $\tilde{\tau}=\{\tilde{\tau}_{j,p}\}$ with
$\tilde{\tau}_{j,p}:=\tau_{p,j}$ is a cone
$\tilde{\tau}\colon \Delta_J(L)\stackrel{.}{\to} S$; moreover, this
$\tilde{\tau}$ is a limiting cone from $L\in \mathrm{obj}(X^P)$ to
$S\colon J\to X^P$.

Back to the proof of the proposition, let $F\colon J\to C$ be a
functor with a limiting cone 
$\nu\colon \Delta_J(\ell) \stackrel{.}{\to} F$. We would like to show that $\Delta_P\nu\colon \Delta_P\circ \bigl(\Delta_J(\ell)\bigr) \stackrel{.}{\to} \Delta_P\circ F$ is a
limiting cone. Noting that $\Delta_P\circ \bigl(\Delta_J(\ell)\bigr)=\Delta_J(\Delta_P(\ell))$ (where the first
$\Delta_J$ is $C\to C^J$ and the second is $C^P\to (C^P)^J$), the last
cone may be written as $\Delta_P\nu\colon \Delta_J(\Delta_P(\ell))
\stackrel{.}{\to} \Delta_P\circ F$. 

First, we note that for each object $p$ of $P$,
$E_p\circ(\Delta_P\circ F)$ is just $F$, and therefore has the limiting
cone $\nu\colon\ell \stackrel{.}{\to} F$ by assumption.  Hence, it is
clear that $\Delta_P\circ F$ has a limit, but we must verify that
$\Delta_P\nu$ is a limiting cone.   

One functor $P\to X$ with object function $p\mapsto \ell$ is just
$\Delta_P(\ell)$. For this functor, we have our cone
$\Delta_P\nu\colon \Delta_J(\Delta_P(\ell)) 
\stackrel{.}{\to} \Delta_P\circ F$.  Since for all $j$ and $p$ we
have $(\Delta_P\nu)_{j,p}=\nu_j=j\text{th component of the limiting cone of
}E_p\circ(\Delta_P\circ F)$, we are done by the theorem
on pointwise limits.