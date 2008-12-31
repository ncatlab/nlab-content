If $C$ is a finitely complete category, a _subobject classifier_ is a [[representable|representing object]] for the functor 

$$Sub: C^{op} \to Set$$ 

which assigns to each object $c$ of $C$ its set of subobjects. In topos theory, the subobject classifier is traditionally denoted $\Omega$; it is also called the "truth value object". 

(For this description to parse, we should ask that $C$ be [[locally small]] and [[well-powered]], but actually it won't matter because presently we will redefine the notion in elementary terms, without reference to the category of sets). 

In more detail: given a morphism $f: c \to d$ in $C$, the function 

$$Sub(f): Sub(d) \to Sub(c)$$ 

takes a subobject $i: t \hookrightarrow d$ to the subobject of $d$ obtained by pulling back $i$ along $f$. [An easy basic lemma of category theory states that the pullback of a mono $i$ along any morphism $f$ is still a [[monomorphism|mono]].] The representability of this functor means there is an object $\Omega$ together with a subobject $t: T \hookrightarrow \Omega$ which is <i>universal</i>, meaning that given any subobject $i: s \hookrightarrow c$, there is a unique morphism $f: c \to \Omega$ such that $i$ is obtained as the pullback of $t$ along $f$. 

It is not hard to show that the domain $T$ of the universal subobject is a terminal object, typically denoted $1$. Therefore the elementary definition of subobject classifier becomes 

**Definition:** A _subobject classifier_ in a finitely complete category $C$ is an object $\Omega$ together with a morphism $t: 1 \to \Omega$ such that for any mono $i: s \to c$ in $C$, there exists a unique morphism $\chi_i: c \to \Omega$ such that $i$ arises as the pullback of $t$ along $\chi_i$. The morphism $\chi_i$ is called the _classifying map_ or _characteristic map_ (of the subobject or isomorphism-equivalence class of $i$). $\Box$

Elements $\phi: 1 \to \Omega$ are often referred to as "truth values"; the distinguished element $t: 1 \to \Omega$ is referred to as "true". 

<h3>
Examples
</h3>

* In the category of sets, the 2-element set $\mathbf{2} = \{f, t\}$ plays the role of $\Omega$; the morphism $t: 1 \to \mathbf{2}$ just names the element $t$. Given a subset $S \subseteq X$, the characteristic function $\chi_S: X \to \mathbf{2}$ is the function defined by $\chi_S(x) = t$ if $x \in S$, and $\chi_S(x) = f$ if $x \notin S$. 

* It is not usually true in toposes that $\Omega$ is the coproduct $\mathbf{2} = 1 + 1$; toposes where that occurs are called <i>Boolean</i>. Thus the category $Set$ of sets is a Boolean topos, as is the presheaf topos $Set^G$ when $G$ is a groupoid. 

* An example of a non-Boolean topos is the category of sheaves over a "typical" topological space $X$ such as $\mathbb{R}$ in its usual topology. In this case, $\Omega$ is the sheaf where the set of sections over an open set $U$ is the set of open subsets of $U$, with the obvious restriction maps; the [[sheaf and topos theory|sheaf topos]] in this case is guaranteed to be non-Boolean provided there are some non-regular open sets in $X$ (a open set is <i>regular</i> if it is the interior of its closure). The "internal logic" of such a topos is [[intuitionistic logic|intuitionistic]]. 

