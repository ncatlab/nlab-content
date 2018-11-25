 A _category of interest_, $\mathbb{X}$, is a [[variety of algebras|variety]] of [[universal algebras]] whose theory contains 

* a set, $\Omega$, of finitary operations with $\Omega =  \Omega_0\cup \Omega_1\cup \Omega_2,$ $\Omega_i$ being the set of $i$-ary operations, so $\Omega_0$ is the set of constants, 

and

* a set, $\mathbb{E}$, of identities / equational axioms, 

such that the forgetful functor from $\mathbb{X}$ to $\mathsf{Set}$ factors through the category of groups and the forgetful functor on that, (so the objects of $\mathbb{X}$ are groups with (possibly) extra operations and $\mathbb{E}$ includes the group laws) and such that the following conditions hold:  

1.  the group operations (here written additively, as $+, -$, and $0$, although the group is not assumed to be abelian) are elements of $\Omega_2$, $\Omega_1$ and $\Omega_0$ respectively, and we write $\Omega_2^\prime=\Omega_2\setminus \{+\}$, $\Omega_1^\prime=\Omega_1\setminus \{-\}$, and $\Omega_0= \{0\}$.  Further it is assumed that, for any binary operation, $*\in \Omega^\prime_2$, its opposite, $*^\circ$, given by  $x*^\circ y=y* x$ is also in  $\Omega_2^\prime$;

2. for any $*\in  \Omega_2^\prime$, $\mathbb{E}$ includes the identity, $x*(y+z)=x*y+x*z$, (so each $*$ distributes over the group operation, $+$);

3. for any $\omega\in\Omega_1^\prime$ and $*\in  \Omega_2^\prime$, $\mathbb{E}$ includes the identities:$\omega(x+y) = \omega(x)+\omega(y)$ \quad and \quad $\omega(x)*y=\omega(x*y)$$

4. for $*\in  \Omega_2^\prime$, $x_1 + (x_2*x_3) = (x_2*x_3)+x_1$ for all $x_1$, $x_2$, $x_3$;

5.  for any $*, \overline{*} \in \Omega_2^\prime$, there is a word, $W$ such that 

$(x_1*x_2)\overline{*}x_3 = W(x_1(x_2x_3), x_1(x_3x_2), (x_2x_3)x_1, (x_3x_2)x_1,x_2(x_1x_3),x_2(x_3x_1),(x_1x_3)x_2,x_3x_1)x_2),$
 
where  each juxtaposition represents an operation in $\Omega_2^\prime$.


## Remark

Any category of interest is a variety of $\Omega$-groups (in the sense of Higgins) and so is automatically a [[semi-abelian category]].



##References

* Grace Orzech, _Obstruction theory in algebraic categories I, II_, J. Pure Appl. Algebra __2__ (1972) 287-340, 315 - 340. 
