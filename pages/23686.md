## Idea 

A model of the **Elementary Theory of the Category of Relations** (ETCR) is the [[dagger 2-poset]] whose [[category of maps]] is a model of [[ETCS]]. 

## Definition

A model of ETCR is a [[dagger 2-poset]] $C$ such that:

* Singleton: there is an object $\mathbb{1} \in Ob(C)$ such that for every morphism $f \in Hom(\mathbb{1},\mathbb{1})$, $f \leq 1_\mathbb{1}$, and for every object $A \in Ob(C)$ there is an [[onto morphism in a dagger 2-poset|onto morphism]] $u_A \in Hom(A,\mathbb{1})$. 

* Tabulations: for every object $A \in Ob(C)$ and $B \in Ob(C)$ and morphism $R \in Hom(A,B)$, there is an object $\vert R \vert \in Ob(C)$ and [[jointly monic]] [[map in a dagger 2-poset|maps]] $f \in Hom(\vert R \vert, A)$, $g \in Hom(\vert R \vert, B)$, such that $R = f^\dagger \circ g$. 

* Power sets: for every object $A \in Ob(C)$, there is an object $\mathcal{P}(A)$ and a morphism $\in_A:Hom(A, \mathcal{P}(A))$ such that for each morphism $R \in Hom(A,B)$, there exists a [[map in a dagger 2-poset|map]] $\chi_R \in Hom(A,P(B))$ such that $R = (\in_B^\dagger) \circ \chi_R$. 

* Function extensionality: for every object $A \in Ob(C)$ and $B \in Ob(C)$ and [[map in a dagger 2-poset|maps]] $f \in Hom(A, B)$, $g \in Hom(A, B)$ and $x \in Hom(\mathbb{1}, A)$, $f \circ x = g \circ x$ implies $f = g$. 

* Natural numbers: there is an object $\mathbb{N} \in Ob(C)$ with maps $0 \in Hom(\mathbb{1},\mathbb{N})$ and $s \in Hom(\mathbb{N},\mathbb{N})$, such that for each object $A$ with maps $0_A \in Hom(\mathbb{1},A)$ and $s_A \in Hom(A,A)$, there is a map $f \in Hom(\mathbb{N},A)$ such that $f \circ 0 = 0_A$ and $f \circ s = s_A \circ f$. 

* Choice: for every object $A \in Ob(C)$ and $B \in Ob(C)$, every [[epic map in a dagger 2-poset|epic map]] $R \in Hom(A,B)$ has a section. 

## See also 

* [[Rel]]
* [[ETCS]]
* [[SEAR]]