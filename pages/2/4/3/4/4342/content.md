#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The $DHR$ category is built from data used in [[DHR superselection theory]] and is used to provide a simplified proof of the [[Doplicher-Roberts reconstruction theorem]]. 

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

## References ##

See [[DHR superselection theory]]