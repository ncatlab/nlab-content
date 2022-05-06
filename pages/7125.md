
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

**Artin gluing** is a fundamental construction in [[locale]] theory and [[topos]] theory. The original example is the way in which a [[topological space]] or locale $X$ may be glued together from an [[open subspace]] $i \colon U \hookrightarrow X$ and its [[closed subspace|closed]] complement $j \colon K \hookrightarrow X$. The analogous construction for toposes gives the [[sheaf topos]] $Sh(X)$ via a gluing together of $Sh(U)$ and $Sh(K)$, and applies more generally to give a sense of how to put two toposes together so that one becomes an [[open geometric morphism|open]] [[subtopos]] and the other a [[closed subtopos]] of the gluing. 

## The topological case 

Let us consider first the case of topological spaces. Let $X$ be a [[topological space]], $i \colon U \hookrightarrow X$ an open subspace, and $j \colon K \hookrightarrow X$ the complementary closed subspace. Let $O(X)$ denote the topology of $X$. There is an injective map 

$$\langle i^\ast, j^\ast \rangle \colon O(X) \to O(U) \times O(K)$$ 

$$V \mapsto (U \cap V, K \cap V)$$ 

that is a map of [[frame|frames]]. The general problem is to characterize the [[image]] of this map: in terms of structure pertaining to $O(U)$ and $O(K)$, which pairs $(W, W')$ of relatively open sets in $U$ and $K$ "glue together" to form an open set $W \cup W'$ in $X$? 

Let $int_X: P(X) \to P(X)$ denote the [[interior]] operation, assigning to a subset of $X$ its interior; this is a [[left exact functor|left exact]] [[comonad]] on $P(X)$. (Indeed, topologies on the set $X$ are in natural bijection with left exact comonads on $P(X)$.) Our problem is to understand when the inclusion 

$$W \cup W' \hookrightarrow int_X(W \cup W')$$ 

obtains. Since $W \in O(U)$ is already open when considered as a subset of $X$, this condition boils down to the condition that 

$$W' \hookrightarrow int_X(W \cup W'). \qquad (1) $$ 

+-- {: .un_thm}
######Proposition 
A necessary and sufficient condition for (1) is that the inclusion $W' \hookrightarrow int_X(W \cup K)$ obtains. 
=-- 

+-- {: .proof}
######Proof 
The necessity is clear since $W' \subseteq K$. The sufficiency is equivalent to having an inclusion 

$$W' \cap int_X(W \cup K) \hookrightarrow int_X(W \cup W').$$ 

Since $W'$ is relatively open in the subspace $K$, we may write $W' = K \cap V$ for some $V \in O(X)$, and so we must check that there is an inclusion 
$$(K \cap V) \cap int_X(W \cup K) \hookrightarrow int_X(W \cup (K \cap V))$$ 

or in other words, using distributivity and the fact that $int_X$ preserves intersections, an inclusion 

$$K \cap V \cap int_X(W \cup K) \hookrightarrow int_X(W \cup K) \cap int_X(W \cup V).$$ 

But this is clear, since we have 

$$K \cap V \cap int_X(W \cup K) \hookrightarrow int_X(W \cup K)$$ 

and 

$$K \cap V \cap int_X(W \cup K) \hookrightarrow V \hookrightarrow W \cup V = int_X(W \cup V)$$ 

where to derive the last equation, we use the fact that $W \in O(U)$ and $V$ are open in $X$. 
=-- 

+-- {: .un_thm} 
######Proposition 
The operation 
$$O(U) \ni W \mapsto int_X(W \cup K) = int_X(W \cup \neg U) \in O(X)$$ 
is the right adjoint $i_\ast$ to $i^\ast: O(X) \to O(U)$. 
=-- 

+-- {: .proof} 
######Proof 
This is well-known. Indeed, for $V \in O(X)$ we have 

$$\frac{V \subseteq int_X(W \cup \neg U) \qquad \text{in} \: O(X)}{V \subseteq W \cup \neg U \qquad \text{in} \: P(X)}$$ 

but the last condition is equivalent to having $U \cap V \subseteq W$ in $P(X)$, or to $i^\ast(V) = U \cap V \subseteq W$ in $O(X)$. 
=-- 

Summarizing, the gluing condition (1) above (for $W' \in O(K)$, $W \in O(U)$) translates into saying that there is an inclusion 

$$W' \hookrightarrow j^\ast i_\ast W.$$ 

where $i^\ast, j^\ast$ are restriction maps and $i^\ast \dashv i_\ast$. For future reference, observe that the operator $j^\ast i_\ast: O(U) \to O(K)$ is left exact. 

We can turn all this around. Suppose $U$ and $K$ are topological spaces, and suppose $f: O(U) \to O(K)$ is left exact. Then we can manufacture a space $X$ which contains $U$ as an open subspace and $K$ as its closed complement, and (letting $i$, $j$ being the inclusions as above) such that $f = j^\ast i_\ast$. The open sets of $X$ may be identified with pairs $(W, W') \in O(U) \times O(K)$ such that $W' \subseteq f(W)$; here we are thinking of $(W, W')$ as a stand-in for $W \cup W'$. In particular, open sets $W$ of $U$ give open sets $(W, \emptyset)$ of $X$, while open sets $W'$ of $K$ also give open sets $U \cup W'$ of $X$. 

## The localic case

The development given above generalizes readily to the context of [[locales]]. 
Thus, let $X$ be a locale, with corresponding [[frame]] denoted by $O(X)$. Each element $U \in O(X)$ gives rise to two distinct frames: 

* The frame whose elements are [[algebra for a monad|algebras]] ([[fixed point|fixed points]]) of the left exact [[idempotent monad]] $U \vee - \colon O(X) \to O(X)$. The corresponding locale is the [[closed sublocale]] $\neg U$ (more exactly, the frame surjection $O(X) \to Alg(U \vee -)$ is identified with a sublocale $\neg U \to X$). 

* The frame whose elements are algebras of the left exact idempotent monad $U \Rightarrow - \colon O(X) \to O(X)$. (NB: for topological spaces, this is $U \Rightarrow V = int_X(V \cup \neg U)$.  This is isomorphic as a frame (but not as a subset of $O(X)$) to the [[principal ideal]] of $O(X)$ generated by $U$, which is more obviously the topology of $U$.) The sublocale corresponding to the frame surjection $O(X) \to Alg(U \Rightarrow -)$ is the [[open sublocale]] corresponding to $U$. 

Put $K = \neg U$, and let $i^\ast: O(X) \to O(U)$, $j^\ast: O(X) \to O(K)$ be the frame maps corresponding to the open and closed sublocales attached to $U$, with [[right adjoints]] $i_\ast$, $j_\ast$. Again we have a left exact functor 

$$f = j^\ast i_\ast \colon O(U) \to O(K).$$

Observe that this gives rise to a left exact comonad 

$$O(U) \times O(K) \to O(U) \times O(K): (W, W') \mapsto (W, W' \wedge f(W)) \qquad (2)$$ 

whose coalgebras are pairs $(W, W')$ such that $W' \leq f(W)$. The coalgebra category forms a frame.  

+-- {: .un_thm}
######Theorem 
The frame map $\langle i^\ast, j^\ast \rangle \colon O(X) \to O(U) \times O(K)$ is identified with the comonadic functor attached to the comonad (2).  In particular, $O(X)$ can be recovered from $O(U)$, $O(K)$, and the comonad (2).
=-- 

Since $O(U + K) \cong O(U) \times O(K)$, we can think of the frame map $\langle i^\ast, j^\ast \rangle$ as giving a localic surjection $U + K \to X$. 

Again, we can turn all this around and say that given any two locales $U$, $K$ and a left exact functor 

$$f \colon O(U) \to O(K),$$ 

we can manufacture a locale $X$ whose frame $O(X)$ is the category of coalgebras for the comonad 

$$1_{O(U)} \times \wedge \circ (f \times 1_{O(K)}) \colon O(U) \times O(K) \to O(U) \times O(K) \qquad (3)$$ 

so that $U$ is naturally identified with an open sublocale of $X$, $K$ with the corresponding closed sublocale, and with a localic surjection $U + K \to X$. This is the (Artin) **gluing construction** for $f$. 

## The toposic case 

Now suppose given [[topos|toposes]] $E$, $E'$ and a [[left exact functor]] $\Phi \colon E \to E'$. There is an induced left exact [[comonad]] 

$$E \times E' \stackrel{\delta \times 1}{\to} E \times E \times E' \stackrel{1 \times \Phi \times 1}{\to} E \times E' \times E' \stackrel{1 \times product}{\to} E \times E' \qquad (3)$$ 

whose category of coalgebras is again (by a basic theorem of topos theory; see for instance [here](http://ncatlab.org/toddtrimble/published/Three+topos+theorems+in+one)) a topos, called the **Artin gluing** construction for $\Phi$, denoted $\mathbf{Gl}(\Phi)$.   

Objects of $\mathbf{Gl}(\Phi)$ are triples $(e, e', f \colon e' \to \Phi(e))$. A morphism from $(e_0, e_0^', f_0)$ to $(e_1, e_1^', f_1)$ consists of a pair of maps $g \colon e_0 \to e_1$, $g'\colon e_0^' \to e_1^'$ which respects the maps $f_0, f_1$ :

$$
 \array{
    e_0^' &\overset{f_0}{\to} & \Phi (e_0)
    \\
    g'\downarrow &&\downarrow \Phi(g)
    \\
    e_1^' &\underset{f_1}{\to} & \Phi(e_1) 
  }
$$

In other words, the Artin gluing is just the [[comma category]] $E' \downarrow \Phi$.  (In fact, this comma category is a topos whenever $\Phi$ preserves pullbacks.)

On the other hand, if $E$ is a topos and $U\in E$ is a [[subterminal object]], then it generates two [[subtoposes]] that are [[complement|complements]] in the [[lattice of subtoposes]], namely, an [[open subtopos]] whose [[reflector]] is $(-)^U$, and a [[closed subtopos]] whose reflector is the [[pushout]] $A\mapsto A +_{A\times U} U$.  If $E=Sh(X)$ is the topos of sheaves on a locale, then $U$ corresponds to an element of $O(X)$, hence an open sublocale with complement $K$ (say), and the open subtopos can be identified with $Sh(U)$ and the closed one with $Sh(K)$.

Returning to the general case, let us denote the [[geometric embedding]] of the open subtopos by $i\colon E_U \hookrightarrow E$ and that of the closed subtopos by $j\colon E_{\neg U}\hookrightarrow E$.  Then we have a composite functor, sometimes called the **fringe functor**,
$$ E_U \xrightarrow{i_*} E \xrightarrow{j^*} E_{\neg U} $$
which is left exact.

+-- {: .un_thm} 
######Theorem 
Let $U$ be a subterminal object of a topos $E$, as above.  Then the left exact left adjoint 
$$\langle i^\ast, j^\ast \rangle \colon E \to E_U \times E_{\neg U}$$
is canonically identified with the comonadic gluing construction $\mathbf{Gl}(j^\ast i_\ast) \to E_U \times E_{\neg U}$.  In particular, $E$ can be recovered from $E_U$, $E_{\neg U}$, and the functor $j^* i_*$.
=-- 

For a proof, see A4.5.6 in the [[Elephant]]. 

Once again, the import of this theorem may be turned around. If $f \colon E \to F$ is any left exact functor, then the projection 

$$\mathbf{Gl}(f) \to E \times F \stackrel{proj}{\to} E$$ 

is easily identified with a [[logical functor]] $\mathbf{Gl}(f) \to \mathbf{Gl}(f)/X$ where $X$ is the [[subterminal object]] $(1, 0, 0 \to f(1))$. This realizes $E$ as an [[open subtopos]] of $\mathbf{Gl}(f)$. 
On the other hand, for the same subterminal object $X \hookrightarrow 1$, the corresponding classifying map 

$$[X] \colon 1 \to \Omega$$ 

induces a [[Lawvere-Tierney topology]] $j$ given by 

$$\Omega \cong 1 \times \Omega \stackrel{[X] \times 1}{\to} \Omega \times \Omega \stackrel{\wedge}{\to} \Omega.$$ 

Then, the category of sheaves $Sh(j)$, or more exactly the left exact left adjoint $\mathbf{Gl}(f) \to Sh(j)$ to the category of sheaves, is naturally identified with the projection 

$$\mathbf{Gl}(f) \to E \times F \stackrel{proj}{\to} F,$$ 

thus realizing $F$ as equivalent to the [[closed subtopos]] ([[Elephant]], A.4.5, pp. 205-206) attached to the subterminal object $X$. 

### Some details and further adjunctions

The sheaves in $\mathbf{Gl}(f)$ corresponding to the open resp. closed subtoposes can be described explicitly. Recall that the objects of $\mathbf{Gl}(f)$ have the form $(X, Y, u:Y\to f(X))$: then the open copy of $E$ corresponds to the subcategory on those objects $(X, Y, u:Y\to f(X))$ with $u$ an isomorphism in $F$ and the closed copy of $F$  to the subcategory with objects $(X, Y, u:Y\to f(X))$ such that $X\simeq 1$ in $E$.

The [[open subtopos]] corresponding to $E$ is [[dense subtopos|dense]] in $\mathbf{Gl}(f)$ precisely if $f:E\to F$ preserves the initial object since $(0,0,0\to f(0))$ is the initial object in $\mathbf{Gl}(f)$ and $0\to f(0)$ is an isomorphism precisely if $f$ preserves $0$. 

To summarize: given a left exact $f\colon E\to F$ we get an open inclusion of $E$ with a further left adjoint:

$$ i_\ast \colon E\to \mathbf{Gl}(f) \qquad X\mapsto (X,f(X),id_{f(X)})$$

$$ i^\ast\colon \mathbf{Gl}(f)\to E \qquad (X,Y,u)\mapsto X$$

$$ i_{!} \colon E\to \mathbf{Gl}(f) \qquad X\mapsto (X,0,0\to f(X)) \quad ,$$
 
and a closed inclusion of $F$ into $\mathbf{Gl}(f)$ with

$$ j_\ast \colon F\to \mathbf{Gl}(f) \qquad X\mapsto (1,X,X\to 1)$$

$$ j^\ast\colon\mathbf{Gl}(f)\to F \qquad (X,Y,u)\mapsto Y$$

that will lack the left adjoint $j_!$ in general. The situation when $j_!$ exists is characterized by the following observation:

+-- {: .un_thm} 
######Proposition 
The closed inclusion $j$ is essential i.e. $j^\ast$ has a left adjoint $j_!$ precisely if the fringe functor $f$ has a left adjoint $l$.
=--

+-- {: .proof} 
######Proof
Suppose $j_!$ exists. The fringe functor $f$ is up to natural isomorphism just $j^\ast i_\ast$ and $i^\ast j_!\dashv j^\ast i_\ast$ since adjoints compose.

Conversely, suppose that $l\dashv f$ with $\eta\colon id\to f{l}$ the corresponding [[unit of an adjunction|unit]]. Define 

$$ j_{!} \colon F\to \mathbf{Gl}(f) \qquad Y\mapsto (l(Y),Y,\eta_Y\colon Y\to f{l}(Y)) \quad .$$

Now given morphisms $\alpha\colon Y_1\to Y$ and $u\colon Y\to f(X)$ in $F$ by general properties of a unit there is precisely one morphism $\overline{u\circ\alpha}\colon l(Y_1)\to X$ corresponding to $u\circ\alpha$ under the adjunction such that the following diagram commutes:

$$
 \array{
    Y_1 &\overset{\eta_{Y_1}}{\to} & f{l}(Y_1)
    \\
    \alpha\downarrow &&\downarrow f(\overline{u\circ\alpha})
    \\
    Y &\underset{u}{\to} & f(X) 
  }
$$

This establishes a bijective correspondence between $Y_1\to j^\ast(X,Y,u)$ and $j_!(Y_1)\to (X,Y,u)$ which is natural since $\eta$ is.

=--

In particular, the left adjoint $j_!$ exists if the fringe functor $f$ is the [[direct image]] of a geometric morphism, or the [[inverse image]] of an [[essential geometric morphism]].

The existence of a _right_ adjoint for the fringe functor: $f\dashv r\colon F\to E$, on the other hand, corresponds to the existence of an 'amazing' right adjoint for the open subtopos inclusion: $i_\ast\dashv i^!:\mathbf{Gl}(f)\to E$.

One direction follows again from the composition of adjoints: $j^\ast i_\ast\dashv i^! j_\ast$ , whereas for the other direction we define:

$$
 i^!\colon \mathbf{Gl}(f)\to E \qquad (X,Y,u)\mapsto r(Y)\quad .
$$

Note that in this case $E$ is dense and we get a 'co-cohesive' adjoint string 

$$i_!\dashv i^\ast\dashv i_\ast \dashv i^!\colon \mathbf{Gl}(f)\to E$$

where $i_!$ and $i_\ast$ are fully faithful.

In particular, when the fringe functor is the inverse image of an essential geometric morphism, we get an additional shorter adjoint string involving the closed subtopos as well:

$$j_!\dashv j^\ast\dashv j_\ast \colon \mathbf{Gl}(f)\to F\quad .$$

### Examples 

Since $i:\ast\hookrightarrow E$ is left exact where $\ast$ is the degenerate topos with one identity morphism, _every_ topos $E$ is trivially a result of Artin gluing: $E\simeq E\downarrow i$.

Of course, more interesting examples of the gluing construction abound as well. Here are a few:  

* Let $E$ be an (elementary, not necessarily Grothendieck) topos, and let $\hom(1, -): E \to Set$ represent the terminal object $1$ -- this of course is left exact. The gluing construction $\mathbf{Gl}(\hom(1, -))$ is called the **scone** (Sierpinski cone), or the [[Freyd cover]], of $E$. 

* If $E$ is a Grothendieck topos and $\Delta \colon Set \to E$ is the (essentially unique) left exact left adjoint, then we have a gluing construction $E \downarrow \Delta$. This gluing may be regarded as the result of _attaching a generic open point_ to $E$. 

* A concrete instance of the constructions in both the preceding examples is the [[Sierpinski topos]] $Set^{\to}$ corresponding e.g. to $Set\downarrow id_{Set}$: its objects are functions $X\to Y$ between sets $X,Y$ and the closed copy of $Set$ sits on the objects of the form $X\to 1$ and the open copy on the objects $X\overset{\simeq}{\to}Y$.

* Since a topos $\mathcal{E}$ is finitely bicomplete, the product functor $\sqcap:\mathcal{E}\times\mathcal{E}\to\mathcal{E}$ with $(X,Y)\mapsto X\times Y$ is part of an adjoint string $\sqcup\dashv\triangle\dashv\sqcap$ involving the [[diagonal functor]] and the coproduct functor. Since $\sqcap$ is left exact, Artin gluing applies. In the case $\mathcal{E}=Set$ , $\mathbb{Gl}(\sqcap)$ yields the [[hypergraph|topos of hypergraphs]]; this example is discussed in detail at [[hypergraph]]. These cases are somewhat unusual in that the fringe functor here has a left adjoint which itself has a further left adjoint.

### Remarks

* Artin gluing for toposes carries over in some slight extra generality, replacing left exact functors $f$ by _pullback-preserving functors_. 

* Artin gluing applies also to other [[doctrine|doctrines]]: [[regular category|regular categories]], [[pretopos|pretoposes]], [[quasitopos|quasitoposes]], etc. See ([Carboni-Johnstone](#CJ)) and ([Johnstone-Lack-Sobocinski](#JLS07)).


## Related entries

* [[Freyd cover]]

* [[comma category]]

* [[recollement]]

## References 

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (expos&#233; IV, sect. 9; in particular: sect. 9.5) {#SGA4}

* [[Gavin Wraith]], _Artin Glueing_ , JPAA **4** (1974) pp.345-358 [link](http://www.sciencedirect.com/science/article/pii/0022404974900140).

* [[Aurelio Carboni]], [[Peter Johnstone]], _Connected limits, familial representability and Artin glueing_ , Mathematical Structures in Computer Science **5** (1995) pp.441-459. ([pdf](http://journals.cambridge.org/article_S0960129500001183))
{#CJ}

* [[Aurelio Carboni]], [[Peter Johnstone]], _Corrigenda to 'Connected limits...'_ , Mathematical Structures in Computer Science **14** (2004)  pp.185-187.

* Peter F. Faul, Graham R. Manuell, _Artin Glueings of Frames as Semidirect Products_ , arXiv:1907.05104 (2019). ([abstract](https://arxiv.org/abs/1907.05104))

* Peter F. Faul, Graham Manuell, José Siqueira, _Artin glueings of toposes as adjoint split extensions_ , arXiv:2012.04963 (2020). ([abstract](https://arxiv.org/abs/2012.04963))

* [[Mamuka Jibladze]], _Lower Bagdomain as a Glueing_ , Proc. A. Razmadze Math. Inst. **118** (1998) pp.33-41. ([pdf](http://www.rmi.ge/~jib/pubs/baglue.pdf))

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). (section 4.2, pp.107-112)

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ , Oxford UP 2002. (sec. A2.1.12, pp.82-84; A4.5.6, p.208)
  {#Johnstone}

* {#JLS07}[[Peter Johnstone]], [[Steve Lack]], [[Pawel Sobocinski]], _Quasitoposes, Quasiadhesive Categories and Artin Glueing_ , pp.312-326 in LNCS **4624** Springer Heidelberg 2007. ([preprint](http://users.ecs.soton.ac.uk/ps/papers/calco07.pdf)) 

* [[Anders Kock|A. Kock]], T. Plewe, _Glueing analysis for complemented subtoposes_ , TAC **2** (1996) pp.100-112. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n9/n9.pdf))

* J. C. Mitchell, A. Scedrov, _Notes on sconing and relators_ , Springer LNCS **702** (1993) pp.352-378. ([ps-draft](ftp://ftp.cis.upenn.edu/pub/papers/scedrov/rel.ps.Z)) [PDF](https://pdfs.semanticscholar.org/ba4e/b38b05470481dc3c912fb37f0598bbda94fe.pdf)

* [[Susan Niefield]], _The glueing construction and double categories_ , JPAA **216** no.8/9 (2012) pp.1827-1836.

[[!redirects Artin-Wraith gluing]]
[[!redirects Artin-Wraith glueing]]
[[!redirects Artin glueing]]