Definability is most often considered only for a first-order language $L$ (not a theory); a definable set is an equivalence class of formulas which evaluate in the same way in every $L$-structure. It makes sense to do the same for a theory: in that case in the definition of the equivalence relation one restricts to models of $T$. 

Let $L$ be a first-order language and $T$ a theory in $L$. Any formula $\phi(x_1,\ldots,x_n)$, whose only free variables could be among $x_1,\ldots,x_n$, together with a [[model]] $M$ for $T$ evaluates to a truth value on each $a = (a_1,\ldots,a_n)\in  M^n$, hence it determines the subset $\phi(M)\subset M^n$ of all $a$ such that $\phi(a)$. Two formulas $\phi,\psi$ with the same number of free variables are equivalent if $\phi(M) = \psi(M)$ for every model $M$ of $T$. A __definable set__ $X$ in $T$ is an equivalence class of formulas in $L$ under this relation. We can also view definable set for a theory $T$ as a functor from the category of $T$-models and [[elementary monomorphism]]s to the category of sets. 

By $X(M)$ denote the set of all $a\in M$ such that $X(a)$ holds, i.e. $\phi(a)$ is true for any choice of representative $\phi\in X$. 

Given two definable sets $X,Y$ in $T$ a __definable function__ $f: X\to Y$ is a definable subset of the product sort $X\times Y$ such that $f_M\in X(M)\times Y(M)$ is a function (we also write $f_M : X(M)\to Y(M)$) for every model $M$ of $T$. Analogously
a __definable equivalence relation__ is a definable subset $R\subset X\times X$ such that $R(M)$ is an equivalence relation for every model $M$ of $T$. 

We can also consider a _relative_ version of a definable set (definability with parameters). 

Given definable sets $X,Y$, a _fixed_ model $M$ and a _fixed_ set $A\subset X(M)$, we say that an element $b\in Y(M)$ is definable over $A$ if there is $(a_1,\ldots,a_n)\in A^n$ and a $T$-definable function $f:X^n\to Y$ such that $f(a_1,\ldots,a_n)=b$. All elements $b$ definable over $A$ form the subset $Y(A)\subset Y(M)$. A subset $B\subset M$ is __definably closed__ if it is closed under definable functions. Given $A\subset M$, there is the minimal definably closed subset $B$ such that $A\subset B\subset M$, the __definable closure__ $B = dcl(A)$ of $A$.  

For a fixed (multi-sorted) theory $T$, definable sets and definable functions form a category.

One can also study [[ind-object]]s and [[pro-object]]s in the category of definable sets and definable functions. 

* Moshe Kamensky, _Ind- and Pro- definable sets_, [math.LO/0608163](http://arxiv.org/abs/math/0608163)

* Jan Holly, _Definable operations on sets and elimination of imaginaries_, Proc. Amer. Math. Soc. __117__ (1993), no. 4, 1149&#8211;1157, [MR93e:03052](http://www.ams.org/mathscinet-getitem?mr=1116261), [doi](http://dx.doi.org/10.2307/2159546), [pdf](http://www.ams.org/journals/proc/1993-117-04/S0002-9939-1993-1116261-6/S0002-9939-1993-1116261-6.pdf)
* [[David Kazhdan]], Lecture notes in model theory, [pdf](http://www.ma.huji.ac.il/~kazhdan/Notes/motivic/b.pdf)