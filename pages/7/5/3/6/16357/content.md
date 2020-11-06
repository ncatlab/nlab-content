+-- {: .num_prop} 
###### Proposition 
Every [[epimorphism]] in the [[Grp|category of groups]] is [[surjective function|surjective]] (a [[regular epimorphism]]). Equivalently, the category of groups is [[balanced category|balanced]] (every [[monomorphism|monic]] epimorphism is an [[isomorphism]]). 
=-- 

There are probably many proofs. Some (for example, I think the one in [[Saunders Mac Lane|Mac Lane's]] [[Categories for the Working Mathematician]]) involve some mild case analysis. The following (originally written up [here](http://ncatlab.org/toddtrimble/published/epimorphisms+in+the+category+of+groups)) is more uniform (and constructive). 

+-- {: .proof} 
###### Proof 
Suppose $i: H \hookrightarrow G$ is a monic epi. Let $A$ be a nontrivial [[abelian group]], say $\mathbb{Z}/(2)$. There is a left [[action]] of $G$ on $A^G = \prod_{g \in G} A$, the group of *[[functions]]* $G \to A$, where $(g \cdot \phi)(g') \coloneqq \phi(g'g^{-1})$; this gives rise to a left $G$-[[module]]. It suffices to prove that any element $m \in A^G$ of the form 

$$G \stackrel{proj}{\to} G/H \to A$$ 

is a [[constant function]], i.e., is [[fixed point|fixed]] under the action of $G$, or in other words that the map $\phi_m: G \to A^G$ mapping $g \in G$ to $g \cdot m - m$ is identically $0$. As $\phi_m$ is an $A^G$-valued [[derivation on a group|derivation]], it yields a [[splitting]] of the [[exact sequence]] of groups 

$$0 \to A^G \to G \ltimes A^G \to G \to 1$$ 

given by $k: G \to G \ltimes A^G$, with $k(g) \coloneqq (g, \phi_m(g))$. Of course we also have the trivial splitting $j(g) \coloneqq (g, 0)$. But note that the [[restrictions]] along $i: H \hookrightarrow G$ coincide: $j \circ i = k \circ i$ since $\phi_m(h) = 0$ for all $h \in H$ (as $H$ acts trivially on the right on [[cosets]] $g H$). Since $i$ is epic, we conclude $j = k$, or that $\phi_m \equiv 0$, as was to be shown. 
=-- 
