<div class="rightHandSide toc">
   [[!include AQFT and operator algebra contents]]
</div>

#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The $DHR$ category is built from data used in [[DHR superselection theory]] and is used to provide a simplified proof of the [[Doplicher-Roberts reconstruction theorem]]. 


## Abstract ##
After the definition of objects and arrows we show several structures that the DHR category has.

## Definition ##

See [[DHR superselection theory]] and [[Haag-Kastler vacuum representation]] for the terminology used here.

+-- {: .un_defn}
###### Definition
The transportable endomorphisms are the **objects** of the DHR category $\Delta$.
=--

+-- {: .un_defn}
###### Definition
For two transportable endomorphisms the **set of intertwiners** are the **arrows**.
=--


## Properties ##
It is straightforward to see that $\Delta$ is a category:

The identity arrow for each object in $\Delta$ is given by the identiy in $\mathcal{A}$. The composition of arrows is simply the composition of intertwiners:

From
$$
R \rho_1 = \rho_2 R
$$

$$
T \rho_2 = \rho_3 T
$$
follows
$$
T R \rho_1 = \rho_3 T R
$$

Several structural properties follow immediatly from the definition:

+-- {: .un_lemma }
###### Lemma
$\Delta$ is a $\mathbb{C}-$[[algebroid]].
=--

+-- {: .un_lemma }
###### Lemma
$\Delta$ is a [[dagger-category]] since, if $R$ is an intertwiner of the pair $(\rho_1, \rho_2)$, then $R^*$ is obviously an intertwiner of the pair $(\rho_2, \rho_1)$.
=--

Combining these two structures we get that $\Delta$ is a [[star-category]].

Since the arrows inherit a norm, we actually get


+-- {: .un_lemma }
###### Lemma
$\Delta$ is a [[C-star-category]].
=--


+-- {: .un_prop}
###### Proposition
It is possible to introduce a finite [[direct product]] in $\Delta$, if the net satisfies the [[Borchers property]].
=--

_Remark_: The [[Haag-Kastler vacuum representation]] that we talk about here satisfies the [[Borchers property]].

+-- {: .proof}
###### Sketch of the Proof
Let $\pi_1, \pi_2$ be admissible representations and $\rho_1, \rho_2$ be their transportable endomorphisms localized in $K_1, K_2$ respectively. Choose a double cone $K_0 \in \mathcal{J}_0$ that contains $K_1$ and $K_2$. Since the local von Neumann algebra $\mathcal{M}(K_0)$ is not trivial, it contains a nontrivial projection $E$, that is $0 \le E \le \mathbb{1}$.

Thanks to the Borchers property there is a double cone $K$ containing the closure of $K_0$, and partial isometries $W_1, W_2 \in \mathcal{M}(K)$ such that $W_1 W_1^* = E, W_2 W_2^* = \mathbb{1} - E$. 

Now we set
$$
\rho := W_1 \rho_1 W_1^* + W_2 \rho_2 W_2^*
$$
It is possible to show that $\pi_0 \rho$ is unitarily equivalent to $\pi_1 \oplus \pi_2$ and that $\rho$ is a transportable (and therefore in particular a localized) endomorphism. So we will call $\rho$ a **direct sum** of $\rho_1$ and $\rho_2$.
=--
## References ##

See [[DHR superselection theory]]