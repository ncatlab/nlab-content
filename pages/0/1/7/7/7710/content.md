

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[definable set]] of an $\mathcal{L}$-theory $T$ in a [[first-order language]] is an [[equivalence class]] of [[formulas]] which evaluate the same way in every model of $T$. (In the case that $T$ is empty, $\mathbf{Mod}(T)$ is just the class of $\mathcal{L}$-structures.)

## Definition

Let $L$ be a first-order language and $T$ a theory in $L$. Any formula $\phi(x_1,\ldots,x_n)$, whose only free variables could be among $x_1,\ldots,x_n$, together with a [[model]] $M$ for $T$ evaluates to a truth value on each $a = (a_1,\ldots,a_n)\in  M^n$, hence it determines the subset $\phi(M)\subset M^n$ of all $a$ such that $\phi(a)$. Two formulas $\phi,\psi$ with the same number of free variables are equivalent if $\phi(M) = \psi(M)$ for every model $M$ of $T$. A __definable set__ $X$ in $T$ is an equivalence class of formulas in $L$ under this relation. Consider the category $\mathcal{M}_{el}(L)$ of $L$-[[structure in model theory|structures]] and [[elementary embedding|elementary embeddings]] and its full subcategory $\mathcal{M}_{el}(T)$ whose objects are the models of $T$. We can also view a __definable set__ for a theory $T$ as a [[functor]] $\mathcal{M}_{el}(T)\to Set$ which is of the form $M\mapsto\phi(M)$ for some $L$-formula $\phi$. 

By $X(M)$ denote the set of all $a\in M$ such that $X(a)$ holds, i.e. $\phi(a)$ is true for any choice of representative $\phi\in X$. 

Given two definable sets $X,Y$ in $T$ a __definable function__ $f: X\to Y$ is a definable subset of the product sort $X\times Y$ such that $f_M\in X(M)\times Y(M)$ is a function (we also write $f_M : X(M)\to Y(M)$) for every model $M$ of $T$. Analogously
a __definable equivalence relation__ is a definable subset $R\subset X\times X$ such that $R(M)$ is an equivalence relation for every model $M$ of $T$. 

## Properties

__Proposition.__ Given a small category $\mathcal{M}$ and two functors $F,G:\mathcal{M}\to Set$ the natural transformations $\alpha : F\to G$ are in 1-1 correspondence with
functors $\tilde\alpha : \mathcal{M}\to Set$ such that $\tilde\alpha(A) \subset  F(A)\times G(A)$ and such that $\tilde\alpha(A)$ is a functional relation. 

Proof. If $\alpha:F\to G$ is an $Ob(\mathcal{M})$-indexed family with components $\alpha_A: F(A)\to G(A)$ viewed as functional relations $\tilde\alpha_A\subset F(A)\times G(A)$, then the extension to a functor means  
that there is a (automatically unique) dotted arrow $\tilde\alpha_f$
$$\array{
\tilde\alpha_A & \stackrel{\tilde\alpha_f}\hookrightarrow & \tilde\alpha_B\\
\downarrow && \downarrow \\
F(A)\times G(A)&\stackrel{F(f)\times G(f)}\longrightarrow & F(B)\times G(B)
}$$
making the diagram commutative (once the existence of $\tilde\alpha_f$ is known, the functoriality of $\tilde\alpha_{f\circ g} = \tilde\alpha_f\circ\tilde\alpha_g$ comes by uniqueness of $\tilde\alpha_f$ and the functoriality of $F\times G$ which it restricts from). That means that for every $x\in F(A)$ 
$(x,\alpha_A(x))$ should be sent to $(F(f)(x), G(f)(\alpha_A(x)))$ by $\tilde\alpha_f$, what is a restriction of $F(f)\times G(f)$, but by $\alpha_B$ being _functional_ relation this must be the same as $(F(f)(x), \alpha_B(F(f)(x)))$, i.e. that $G(f)(\alpha_A(x))=\alpha_B(F(f)(x))$. Q.E.D.

In other words, functoriality of $\tilde\alpha$ is the same as $\alpha$ being natural. 

__Corollary.__ Definable functions for $L$ (for $T$) are in 1-1 correspondence with natural transformations of __definable sets__ as functors $\mathcal{M}_{el}(L)\to Set$ (resp. $\mathcal{M}_{el}(T)\to Set$). 

For a fixed (multi-sorted, first-order) theory $T$, definable sets and definable functions form a category $Def(T)$. This category (or any equivalent category) is the [[syntactic category]] of the theory. Models of $T$ can be recovered as left exact 
functors $Def(T)\to Set$. Notice that definable sets are functors from models to sets, and models are functors from definable sets to sets; just the latter are the "evaluation functionals" among all functors. 

See also [[definable groupoid]].

An $\infty$-definable set is an intersection of definable sets. 

We can also consider a _relative_ version of a definable set (definability with parameters). 

Given definable sets $X,Y$, a _fixed_ model $M$ and a _fixed_ set $A\subset X(M)$, we say that an element $b\in Y(M)$ is definable over $A$ if there is $(a_1,\ldots,a_n)\in A^n$ and a $T$-definable function $f:X^n\to Y$ such that $f(a_1,\ldots,a_n)=b$. All elements $b$ definable over $A$ form the subset $Y(A)\subset Y(M)$. A subset $B\subset M$ is __definably closed__ if it is closed under definable functions. Given $A\subset M$, there is the minimal definably closed subset $B$ such that $A\subset B\subset M$, the __definable closure__ $B = dcl(A)$ of $A$.  

If we extend the language by the constants from $A$ we get a new language $L_A$. The definable sets in language $L$ over $A$ are the definable sets in language $L_A$ over $\emptyset$.

## Ind- and pro-definable sets

One can also study [[ind-object]]s and [[pro-object]]s in the category of definable sets and definable functions. 

+-- {: .num_defn #type-definable-set}

###### Definition

An important special case of a pro-definable set that shows up in model theory are **type-definable sets**, which are just infinite conjunctions of definable sets. (There is no restriction that the formulas representing these definable sets all sit inside a finite product of [[type|sorts]].)

=--

## Related concepts

* [[constructible set]]

* [[recursive subset]]

* [[computable set]]

* [[definable groupoid]]


## References

* Moshe Kamensky, _Ind- and Pro- definable sets_, [math.LO/0608163](http://arxiv.org/abs/math/0608163)

* Jan Holly, _Definable operations on sets and elimination of imaginaries_, Proc. Amer. Math. Soc. __117__ (1993), no. 4, 1149&#8211;1157, [MR93e:03052](http://www.ams.org/mathscinet-getitem?mr=1116261), [doi](http://dx.doi.org/10.2307/2159546), [pdf](http://www.ams.org/journals/proc/1993-117-04/S0002-9939-1993-1116261-6/S0002-9939-1993-1116261-6.pdf)
* [[David Kazhdan]], Lecture notes in model theory, [pdf](http://www.ma.huji.ac.il/~kazhdan/Notes/motivic/b.pdf)
* D. Haskell, E. Hrushovski, H.D.Macpherson, _Definable sets in algebraically closed valued fields: elimination of imaginaries_, J. reine und angewandte Mathematik __597__ (2006), [MR2007i:03040](http://www.ams.org/mathscinet-getitem?mr=2264318), [doi](http://dx.doi.org/10.1515)/CRELLE.2006.066)

[[!redirects definable sets]]
[[!redirects pro-definable set]]
[[!redirects pro-definable sets]]
[[!redirects ind-definable set]]
[[!redirects ind-definable sets]]
[[!redirects type-definable set]]
[[!redirects type-definable sets]]
[[!redirects definable subset]]
[[!redirects definable subsets]]
