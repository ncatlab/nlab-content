# Definition #

Let $V$ be a [[closed category|closed]] [[symmetric monoidal category]].  In a $V$-[[enriched category]] $C$, the **copower** of an object $x\in C$ by an object $k\in V$ is an object $k\odot x \in C$ with a [[natural isomorphism]]

$$
  C(k\odot x, y) \cong V(k, C(x,y))
$$

where $C(-,-)$ is the $V$-valued hom of $C$ and $V(-,-)$ is the internal-hom of $V$.

# Remarks #

* In the $V$-category $V$, the copower is just the tensor product of $V$.

* Copowers are a special sort of [[weighted limit|weighted colimit]].  Conversely, all weighted colimits can be constructed from copowers together with [[conical colimits]].  The dual  limit notion of a copower is a [[power]].

* Copowers are frequently called _tensors_ and a $V$-category having all copowers is called _tensored_, while the word "copower" is reserved for the case $V=Set$.  However, there seems to be no good reason for making this distinction.  Moreover, the word "tensor" is fairly overused, and unfortunate since a tensor (= a copower) is a colimit, while a cotensor (= [[power]]) is a limit.
