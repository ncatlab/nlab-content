
#Idea#

A _strong monad_ over a [[monoidal category]] $V$ is a [[monad]] in the [[bicategory]] of $V$-[[actions]].

# Definition #

+-- {: .un_defn}
###### Definition

For $V$ a [[monoidal category]] a **strong monad** over $V$ is a [[monad]] 

* in the $2$-[[2-category|category]] $V\text{-}Act$ of left $V$-[[actions]] on [[category|categories]] 

* on the object $V$ itself.
=--

Here we regard $V$ as equipped with the canonical $V$-action on itself.


## Details ##

If we write $\mathbf{B}V$ for the one-object [[bicategory]] obtained by [[delooping]] $V$ once, we have

$$
  V\text{-}Act \simeq Lax2Funct(\mathbf{B}V, Cat)
  \,,
$$
where on the right we have the $2$-category of [[lax functor|lax 2-functors]] from $\mathbf{B}V$ to [[Cat]], lax [[natural transformations]] of and [[modifications]].

The category $V$ defines a canonical functor $\hat V : \mathbf{B}V \to Cat$.

The strong monad, being a [[monad]] in this [[lax functor]] [[bicategory]] is given by

* a lax [[natural transformation]] $T : \hat V \to \hat V$;

* [[modifications]] 

  * unit: $\eta : Id_V \Rightarrow T$ 

  * product: $\mu : T \circ T \Rightarrow T$

* satisfying the usual uniticity and associativity constraints.

By the general logic of $(2,1)$-[[(n,k)-transformation|transformations]] the components of $T$ are themselves a certain [[functor]].

Then the [usual diagrams](http://en.wikipedia.org/wiki/Strong_monad) that specify a strong monad


* unitalness and functoriality of the component functor of $T$;

* naturalness of unit and product modifications.


# References #

Usually strong monads are described explicitly in terms of the components of the above structure. The above repackaging of that definition is due to John Baez

* [[John Baez]], _The Monads Hurt My Head -- But Not Anymore_ ([blog](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025476))