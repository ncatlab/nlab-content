Measure coalgebras are an enrichment of the category of commutative rings (or commutative $\mathbb{Z}$-algebras) in the cartesian closed [[category of cocommutative coalgebras]]. 

The starting point is the observation that the category of cocommutative coalgebras $Coalg$ acts on the category of commutative algebras $Alg$: there is a functor 

$$\{-, -\}: Coalg \times Alg \to Alg$$ 

where, given a coalgebra $C$ and an algebra $A$, $\{C, A\}$ is the abelian-group hom of additive homomorphisms $f: C \to A$, made into an algebra whose multiplication $f \cdot g$ is given by 

$$C \overset{d}{\to} C \otimes C \overset{f \otimes g}{\to} A \otimes A \overset{m}{\to} A$$ 

where $d$ is the coalgebra comultiplication and $m$ is the algebra multiplication. "Action" here means that there is a natural isomorphism 

$$\{C \otimes D, A\} \cong \{C, \{D, A\}\}$$ 

of algebras; here $Alg$ is sometimes described as an [[actegory]] over $Coalg$. 

Given two algebras $A$, $B$, the **measure coalgebra** $\mu(A, B)$ is by definition the representing object of the functor 

$$Alg(A, \{-, B\}): Coalg^{op} \to Set$$ 

so that there is an isomorphism, natural for coalgebras $C$, of the form

$$Coalg(C, \mu(A, B)) \cong Alg(A, \{C, B\})$$ 

This indeed gives an enrichment 

$$\mu(-, -): Alg^{op} \times Alg \to Coalg$$ 

where the composition law in $Coalg$ 

$$\mu(A_0, A_1) \times \mu(A_1, A_2) \to \mu(A_0, A_2)$$ 

(noting that the cartesian product in $Coalg$ is the tensor product of the underlying additive groups) is derived by universality from a composition of maps: 

$$\array{ 
Coalg(C, \mu(A_0, A_1) \times \mu(A_1, A_2)) & \cong & Coalg(C, \mu(A_0, A_1)) \times Coalg(C, \mu(A_1, A_2)) & (Coalg(C, -) preserves products)\\
 & \cong & Alg(A_0, \{C, A_1\}) \times Alg(A_1, \{C, A_2\}) & (definition of \mu) \\ 
 & \to & Alg(A_0, \{C, A_1\}) \times Alg(\{C, A_1\}, \{C, \{C, A_2\}\}) & (functoriality of \{C, -\})\\
 & \to & Alg(A_0, \{C, \{C, A_2\}\}) & (composition law)\\ 
 & \cong & Alg(A_0, \{C \otimes C, A_2\}) & (actegory constraint)\\ 
 & \to & Alg(A_0, \{C, A_2\}) & (using d: C \to C \otimes C)\\ 
 & \cong & Coalg(C, \mu(A_0, A_2)) & (definition of \mu)
}$$ 
