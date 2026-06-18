> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***


## Idea

In [[topology]], the *Bolzano-Weierstrass theorem* states that every [[bounded set|bounded]] [[sequence]] in a [[finite number|finite]]-[[dimension of a manifold|dimensional]] [[Euclidean space]] contains a [[convergence of a sequence|convergent]] [[subsequence]].

## References

Named after:

* [[Bernard Bolzano]]: *Rein analytischer Beweis des Lehrsatzes, dass zwischen je zwey Werthen, die ein entgegengesetztes Resultat gewähren, wenigstens eine reelle Wurzel der Gleichung liege*, Gottlieb Haase, Prague (1817) \[<a href="https://eudml.org/doc/202403">eudml:202403</a>, [dml.cz:400016](https://dml.cz/handle/10338.dmlcz/400016), [pdf](https://dml.cz/bitstream/handle/10338.dmlcz/400016/Bolzano_24-1817-1_1.pdf), [[Bolzano-1817.pdf|pdf:file]]\]
  > (Where the BW-theorem is introduced as a [[lemma]] to prove the [[intermediate value theorem]].)

Textbook account:

* {#Rudin64} [[Walter Rudin]]; Thms. 3.6(b) and 2.42 in: _Principles of Mathematical Analysis_, McGraw-Hill (1964, 1976) &lbrack;[pdf](https://david92jackson.neocities.org/images/Principles_of_Mathematical_Analysis-Rudin.pdf)&rbrack;

See also: 

* Wikipedia: *[Bolzano-Weierstrass theorem](https://en.wikipedia.org/wiki/Bolzano%E2%80%93Weierstrass_theorem)*

* [[eom]]: *[Bolzano-Weierstrass theorem](https://encyclopediaofmath.org/index.php?title=Bolzano-Weierstrass_theorem)*

Discussion in [[constructive mathematics]] relating to the [[limited principle of omniscience]]:

* {#Mandelkern88} [[Mark Mandelkern]]: *Limited Omniscience and the Bolzano-Weierstrass Principle*, Bulletin of the London Mathematical Society **20** 4 (1988) 319--320, &lbrack;[doi:10.1112/blms/20.4.319](https://doi.org/10.1112/blms/20.4.319), [pdf](https://www.zianet.com/mandelkern/mandelkern_bwp.pdf)&rbrack;



$\alpha$

\begin{proof}
Let $f : \mathbb{N} \to \mathbb{2}$ be a sequence of booleans.

First to recall what we need to prove:

By assumption, the fully-truncated $\mathrm{LPO}_\mathbb{N}$ gives the inclusive disjunction:
$$
  \left[ 
    \left( \exists n:\mathbb{N}. f(n) = 1 \right) 
     + 
    \left( \textstyle{\prod_{n:\mathbb{N}}} f(n) = 0 \right)   
  \right]
  \mathrlap{\,,}
$$
which is the propositional truncation of the sum type. 

Abbreviating

$$
  \begin{aligned}
    P & \coloneqq \exists n:\mathbb{N}. f(n) = 1
    \\
    Q & \coloneqq \textstyle{\prod_{n:\mathbb{N}}} f(n) = 0
    \mathrlap{\,,}
  \end{aligned}
$$
our premise is therefore an element of the truncated type $[P + Q]$.

And to prove the claim, need to construct an element of the disjunction-untruncated type, which is the bare sum type:
$$
  \left( 
    \exists n \colon \mathbb{N}. f(n) = 1 
  \right) 
     + 
  \left( 
    \textstyle{\prod_{n \colon \mathbb{N}}} f(n) = 0 
  \right)
  \mathrlap{\,,}
$$
hence to construct a term of $P + Q$. Hence we need to construct a map
$$
  [P + A] \longrightarrow (P + Q)
  \mathrlap{\,.}
$$

Now to establish that:

First, by the definition of the existential quantifier $\exists$ as the propositional truncation of the dependent sum, $P$ is a [[mere proposition]]: $\mathrm{isProp}(P)$ holds. 
Assuming [[weak function extensionality]], the [[dependent product]] of a family of mere propositions is a mere proposition. Since equality in the [[boolean domain]] $\mathbb{2}$ is a mere proposition, it follows that $\mathrm{isProp}(Q)$ holds.

Second, we establish that $P$ and $Q$ are [[mutually exclusive propositions|mutually exclusive]] by constructing a [[function type|function]] 
$$
  P \times Q \to \varnothing
  \mathrlap{\,.}
$$ 
Namely, suppose we have an element of $Q$, meaning $\prod_{n \colon\mathbb{N}} f(n) = 0$. We wish to map $P$ to $\varnothing$. Because $\varnothing$ is a mere proposition, we may apply the [[universal property]] of [[propositional truncation]] to eliminate out of $P = \big[\textstyle{\sum_{n \colon \mathbb{N}}} f(n) = 1\big]$. This means we may legitimately assume we have a specific pair $(n, p)$ where $p \colon f(n) = 1$. 
Applying our element of $Q$ to $n$ yields a proof that $f(n) = 0$. Consequently, we have $1 = 0$ in the boolean domain $\mathbb{2}$, which is a contradiction yielding an element of the empty type $\emptyset$. 

Now we must show that any pair of elements $x, y : P + Q$ are equal. We proceed by case analysis:

1. the case $x = \mathrm{inl}(p_1), y = \mathrm{inl}(p_2)$:

   Since $\mathrm{isProp}(P)$ is established, $p_1 = p_2$, which implies $x = y$.

2. the case $x = \mathrm{inr}(q_1), y = \mathrm{inr}(q_2)$:

   Since $\mathrm{isProp}(Q)$ is established, $q_1 = q_2$, which implies $x = y$.

3. the case $x = \mathrm{inl}(p), y = \mathrm{inr}(q)$: 

   We have terms of both $P$ and $Q$. By the second step above, this yields an element of $\emptyset$. By the principle of *ex falso quodlibet*, any equality can be extracted from a contradiction, so $x = y$ holds vacuously.

4. the case $x = \mathrm{inr}(q), y = \mathrm{inl}(p)$: 

   An identical contradiction is reached, and $x = y$ holds vacuously.

Because all branches evaluate to equality, $\mathrm{isProp}(P + Q)$ holds.

To conclude:
Because $P + Q$ is a mere proposition, the canonical map $(P + Q) \to [P + Q]$ is an equivalence. This gives us a well-defined inverse map:
$$
  [P + Q] \to (P + Q)
  \mathrlap{\,.}
$$
By applying this inverse map to our premise (the element of $[P + Q]$ provided by the standard $\mathrm{LPO}_\mathbb{N}$), we extract a valid element of $P + Q$. 

This establishes the claimed disjunction-untruncated $\mathrm{LPO}_\mathbb{N}$.
\end{proof}



The mechanism relies heavily on the functional freedom inherent in the [F-term](https://en.wikipedia.org/wiki/F-term) scalar potential:

$$
  V 
   \;=\; 
  e^K \left( 
    K^{i\bar{j}} D_i W \overline{D_j W} 
     - 
    3{|W|}^2  
  \right)
$$

By making judicious choices of the target-space geometry via the [[Kähler potential]] $K$ and the holomorphic [[superpotential]] $W$, one can engineer the scalar potential $V$ to satisfy the required slow-roll conditions. Specifically, the $\alpha$-attractor models of Kallosh & Linde et al. (typically formulated on hyperbolic Kähler manifolds mapping to the Poincaré disk) naturally yield predictions for the spectral index $n_s$ and the tensor-to-scalar ratio $r$ that sit squarely within the empirical sweet spot of the [[cosmic microwave background]] observations. 

Furthermore, the persistent challenge posed by the negative $-3|W|^2$ term, which leads to [[anti de Sitter spacetime|anti-de Sitter]] vacua, is circumvented by introducing nilpotent chiral superfields. This non-linear realization of supersymmetry (effectively incorporating the [Volkov-Akulov theory](supergravity#VolkovAkulov1972)) provides a phenomenologically controllable uplift to a metastable [[de Sitter spacetime|de Sitter]] vacuum, thus accommodating the observed [[dark energy]].


(...)


[[AlgebraicTopologySection1BAllenHatcher.jpg:pic]]