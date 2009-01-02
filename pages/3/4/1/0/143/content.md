#Definition#

Given a [[site]] $(C, J)$, a _sheaf_ over that site is a [[presheaf]] 

$$X: C^{op} \to Set$$ 

such that whenever $i: F \hookrightarrow \hom(-, c)$ is a covering sieve, the map 

$$X(c) \stackrel{Yoneda}{\cong} Set^{C^{op}}(\hom(-, c), X) \stackrel{Set^{C^{op}}(i, X)}{\to} Set^{C^{op}}(F, X)$$ 

is an isomorphism. 


##Remarks##

* The [[vertical categorification|categorifications]] of sheaves are

 * [[stack|stacks]];

 * [[infinity-stack|infinity-stacks]].

* If we read the set $Set^{C^{op}}(F, X)$ as a [[descent and codescent|descent 0-category]] the above isomorphism exhibits the _descent condition_ described at [[infinity-stack]] in a very simple case, namely the case where the $\infty$-stack takes values in "0-categories", namely in [[Set]].

