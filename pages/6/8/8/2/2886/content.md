# Measure coalgebras
* tic
{: toc}


## Idea

Measure coalgebras are an [[enriched category|enrichment]] of the category of [[commutative rings]] (or commutative $\mathbb{Z}$-algebras) in the [[cartesian closed category]] of [[cocommutative coalgebra|cocommutative coalgebras]]. 

The starting point is the observation that the category of cocommutative coalgebras $Coalg$ acts on the category of [[commutative algebras]] $Alg$: there is a functor 

$$\{-, -\}: Coalg^{op} \times Alg \to Alg$$ 

where, given a coalgebra $C$ and an algebra $A$, $\{C, A\}$ is the [[abelian group|abelian-group]] [[hom-object|hom]] of additive homomorphisms $f: C \to A$, made into an algebra whose multiplication $f \cdot g$ is given by 

$$C \overset{d}{\to} C \otimes C \overset{f \otimes g}{\to} A \otimes A \overset{m}{\to} A$$ 

where $d$ is the coalgebra comultiplication and $m$ is the algebra multiplication. That this is an "action" here means that there is a natural isomorphism 

$$\{C \otimes D, A\} \cong \{C, \{D, A\}\}$$ 

of algebras; here $Alg$ is sometimes described as an [[actegory]] over $Coalg$. 

## Definition

Given two algebras $A, B$, the **measure coalgebra** $\mu(A, B)$ is by definition the [[representing object]] of the functor 

$$Alg(A, \{-, B\}): Coalg^{op} \to Set$$ 

so that there is an isomorphism, [[natural isomorphism|natural]] for coalgebras $C$, of the form

$$Coalg(C, \mu(A, B)) \cong Alg(A, \{C, B\})$$ 

Assume the existence of equalizers in $Coalg$, and of a right adjoint 

$$Cof: k-Mod \to Coalg$$ 

to the forgetful functor $U: Coalg \to k-Mod$ (cofree cocommutative coalgebra construction). We let 

$$\pi: U \circ Cof \to 1_{k-Mod}$$ 

denote the counit of the adjunction $U \dashv Cof$. 

We construct $\mu(A, B)$ explicitly as the equalizer in $Coalg$ of a pair of maps of the form 

$$Cof(B^A) \overset{\to}{\to} Cof(B^{A \otimes A}) \times Cof(B^k)$$ 

where we denote the internal hom in $k$-$Mod$ by exponentiation (and we recall here that the cartesian product in $Coalg$ is given by tensor product at the level of $k$-$Mod$). The first of these maps is 

$$\langle Cof(B^{m_A}), Cof(B^{u_A}) \rangle: Cof(B^A) \to Cof(B^{A \otimes A}) \times Cof(B^k)$$ 

where $m_A: A \otimes A \to A$ is the multiplication on $A$ and $u_A: k \to A$ is the unit. The second is given by a pair of maps 

$$\langle \Phi, \Psi \rangle$$ 

which we now describe separately. 

The map $\Phi: Cof(B^A) \to Cof(B^{A \otimes A})$ is the unique coalgebra map such that $U \Phi$ lifts the map 

$$U Cof(B^A) \overset{\delta}{\to} U Cof(B^A) \otimes U Cof(B^A) \overset{\pi \otimes \pi}{\to} B^A \otimes B^A \overset{\otimes_1}{\to} (B \otimes B)^{A \otimes A} \overset{m_{B}^{A \otimes A}}{\to} B^{A \otimes A}$$ 

through $\pi: U Cof(B^{A \otimes A}) \to B^{A \otimes A}$. Here $\delta$ denotes the comultiplication (same as the diagonal map as seen in $Coalg$), and $\otimes_1$ indicates the structure of enriched functoriality for $\otimes$. 

The map $\Psi: Cof(B^A) \to Cof(B^k)$ is the unique coalgebra map such that $U \Psi$ lifts the map 

$$U Cof(B^A) \overset{\varepsilon}{\to} k \overset{u_B}{\to} B \cong B^k$$ 

through $\pi: U Cof(B^A) \to B^A$. Here $\varepsilon$ denotes the counit (same as the unique map to the terminal object as seen in $Coalg$). 

## Enrichment of algebras in coalgebras 

The measure coalgebra $\mu(A, B)$ indeed gives an enrichment 

$$\mu(-, -): Alg^{op} \times Alg \to Coalg$$ 

where the composition law in $Coalg$ 

$$\mu(A_0, A_1) \times \mu(A_1, A_2) \to \mu(A_0, A_2)$$ 

(recalling that the [[product]] in $Coalg$ is the [[tensor product]] of the underlying additive groups) is derived by universality from a composition of maps: 

$$\array{ 
Coalg(C, \mu(A_0, A_1) \times \mu(A_1, A_2)) & \cong & Coalg(C, \mu(A_0, A_1)) \times Coalg(C, \mu(A_1, A_2)) & (Coalg(C, -) preserves products)\\
 & \cong & Alg(A_0, \{C, A_1\}) \times Alg(A_1, \{C, A_2\}) & (definition of \mu) \\ 
 & \to & Alg(A_0, \{C, A_1\}) \times Alg(\{C, A_1\}, \{C, \{C, A_2\}\}) & (functoriality of \{C, -\})\\
 & \to & Alg(A_0, \{C, \{C, A_2\}\}) & (composition law)\\ 
 & \cong & Alg(A_0, \{C \otimes C, A_2\}) & (actegory constraint)\\ 
 & \to & Alg(A_0, \{C, A_2\}) & (using d: C \to C \otimes C)\\ 
 & \cong & Coalg(C, \mu(A_0, A_2)) & (definition of \mu)
}$$ 


