
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Over an algebraic theory

We discuss here how in the context of [[space]]s modeled on duals of algebras over an [[algebraic theory]] $T$, there is a canonical space $\mathbb{A}_T$ which generalizes the [[real line]] $\mathbb{R}$. 

### Definition

For $T$ (the [[syntactic category]] of) any [[Lawvere theory]] we have that [[Isbell conjugation]] 

$$
  (\mathcal{O} \dashv Spec)
  : 
   T Alg^{op} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
   Sh(C)
$$

relates $T$-algebras to the [[sheaf topos]] over duals $T \hookrightarrow C \subset T Alg^{op}$ of $T$-algebras, for $C$ a [[small category|small]] [[full subcategory]] with [[subcanonical coverage]].

By the <a href="http://ncatlab.org/nlab/show/Lawvere%20theory#FreeAlgebras">free T-algebra adjunction</a>

$$
  (F_T \dashv U_T) : T Alg \stackrel{\overset{F_T}{\leftarrow}}{\underset{U_T}
{\to}}
  Set
$$

we have the free $T$-algebra $F_T(*) \in TAlg$ on a single generator.

+-- {: .un_defn}
###### Definition

The **$T$-line object** is 

$$
  \mathbb{A}_T := Spec F_T(*) \in Sh(C)
  \,.
$$

=--

### Examples

* For $T$ the theory of ordinary [[associative algebra]]s over a [[ring]] $R$, we have that $\mathbb{A}_T = \mathbb{A}_R$ is what is called the _[[affine line]]_ over $R$.

* For $T := Smooth :=$ [[CartSp]] the theory of [[smooth algebra]]s, we have that $\mathbb{A}_{Smooth} = \mathbb{R}$ is the [[real line]] regarded as a [[diffeological space]].

### The group object

For $\mathcal{Ab}$ the [[Lawvere theory]] of [[abelian group]]s, say that a morphism $ab : \mathcal{Ab} \to T$ of Lawvere theories is an **abelian Lawvere theory**. Algebras over abelian Lawvere theories have underlying abelian groups

$$
  (ab_* \dashv ab^*)
  :
  T Alg \stackrel{\overset{ab_*}{\leftarrow}}{\underset{ab^*}{\to}}
  Ab
  \,.
$$

+-- {: .un_defn}
###### Definition

For $T$ an abelian Lawvere theory, by its underlying abelian group we have that $\mathcal{A}_T$ inherits the structure of an abelian [[group object]] in $Sh(C)$. Write

$$
  \mathbb{G}_T \in Ab(Sh(C))
$$

for this group object induced by $\mathcal{A}_T$.

=--


### References

The notion of a line object over general abelian Lawvere theories has been considered in

* [[nLab:Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

in the context of [[function algebras on ∞-stacks]].


[[!redirects line object]]