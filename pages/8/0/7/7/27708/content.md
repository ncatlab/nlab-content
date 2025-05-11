
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



\tableofcontents


## Idea

In [[representation theory]], *Mackey theory* refers to a set of tools for constructing and classifying [[irreducible representations]] of a [[group]] $G$ from that of a [[normal subgroup]] $N \subset G$, by using [[induced representation|induction]] from the [[stabilizer groups]] of the [[adjoint action]] of $G$ on the set of [[irreps]] of $N$. 

(Also referred to as *[[little group]]*-methods, cf. *[[Wigner classification]]*.)

## Details

### For finite semidirect products with abelian groups

Consider

* $A$ an [[abelian group]]

* $G \,\equiv\, H \rtimes A$ a [[semidirect product group]].

and denote:

* $\widetilde A \,\coloneqq\, Hom(A, \mathbb{C}^\times)$ the dual group of [[group characters]], hence, since $A$ is [[abelian group|abelian]], of [[irreducible representations]] of $A$,

* the [[adjoint action]] of $G$ on $A$ and the induced action on $\widetilde A$:

  $$
    \begin{array}{ccc}
      G \times \widetilde A &\longrightarrow& \widetilde A
      \\
      \big(g, A \xrightarrow{\chi} \mathbb{C}^\times \big)
        &\mapsto&
      \chi\big(g^{-1} (\text{-}) g\big)
    \end{array}
  $$

* $(\chi_i)_{i \in \widetilde{A}/H}$ a set of representatives of the resulting [[orbits]] of $H$ in $\widetilde A$,

* $H_i \,\coloneqq\, Stab_H(\chi_i)$ the corresponding [[stabilizer subgroups]] of $H$,

* $G_i \,\coloneqq\, H_i \rtimes A$ the corresponding [[subgroups]] of $G$

Finally, denote

$$
  \widehat{\chi}_i 
    \,\colon\, 
  G_i 
    \twoheadrightarrow 
  A 
    \xrightarrow{\chi_i} 
  \mathbb{C}^{\times}
  \,,
$$

which is a [[group character]] on $G_i$, by the definition of $H_i$. 

Similarly, for $\rho \in Irr(H_i)$ an irrep of $H_i$, write

$$
  \widehat{\rho}
    \,\colon\, 
  G_i
    \twoheadrightarrow 
  H_i 
    \xrightarrow{\rho} 
  GL(V)
$$

and consider the [[induced representations]] of the [[tensor product of representations|tensor products]]:

\[
  \label{MackeyIrrepForFiniteSemProdWithAbelian}
  \theta_{i,\rho}
  \;\coloneqq\;
  Ind_{G_i}^G \big(
    \widehat{\chi}_i \otimes \widehat{\rho}
  \big)
  \;\in\;
  Rep_{\mathbb{C}}(G)
  \,.
\]

\begin{proposition}
\label{ForFiniteSemidirectProductsWithAbelianGroups}
  
1. The representations $\theta_{i,\rho}$ (eq:MackeyIrrepForFiniteSemProdWithAbelian) are irreducible.

1. If $\theta_{i,\rho} \simeq \theta_{i',\rho'}$ then $i = i'$ and $\rho \simeq \rho'$.

1. Every irrep of $G$ is of the form $\theta_{i, \rho}$, up to isomorphism.

\end{proposition}

([Serre 1977 Prop. 25 p 62](#Serre77))

## Examples

\begin{example}
\label{ExampleIrrepsOfZnRtimesZTwo}
Consider the semidirect product group $G \equiv \mathbb{Z}_n \rtimes \mathbb{Z}_2$, with

* $A \equiv \mathbb{Z}_n \,\coloneqq\, \mathbb{Z}/n$ the [[cyclic group]] of [[order of a group|order]] $n \in \mathbb{N}$,

* $H \equiv \mathbb{Z}_2$ the [[cyclic group of order 2]] acting on $\mathbb{Z}_n$ via the sign [[involution]].

In order find all the (complex) [[irreps]] of $\mathbb{Z}_n \rtimes \mathbb{Z}_2$ we unwind the statement of Prop. \ref{ForFiniteSemidirectProductsWithAbelianGroups}:

> (We denote [[congruence classes]] by square brackets: $[-] \colon \mathbb{Z} \twoheadrightarrow \mathbb{Z}_n$.)

First, the complex irreps of the [[normal subgroup]] $\mathbb{Z}_n$ are themselves labeled by $[k] \in \mathbb{Z}_n$ and given by

$$
  \begin{array}{ccc}
    \mathbb{Z}_n 
       &\xrightarrow{\;\; \chi_{[k]} \;\;}& 
    \mathbb{C}^\times
    \\
    [r] &\mapsto& e^{2 \pi \mathrm{i} \tfrac{r k}{n}}
    \mathrlap{\,.}
  \end{array}
$$

On these, the nontrivial element $\sigma \in \mathbb{Z}_2$ acts by $\sigma \colon [k] \mapsto [-k]$:
$$
  \begin{array}{l}
    (\sigma \chi_{[k]})\big([r]\big)
    \\
    \;\equiv\;
    \chi_{[k]}\big(\sigma^{-1}\cdot [r] \cdot \sigma\big)
    \\
    \;\equiv\;
    \chi_{[k]}\big(\sigma^{-1}\cdot \sigma\cdot [-r]\big)
    \\
    \;=\;
    \chi_{[k]}\big([-r]\big)
    \\
    \;\equiv\;
    e^{2 \pi \mathrm{i} \tfrac{(-r)k}{n}}
    \\
    \;=\;
    e^{2 \pi \mathrm{i} \tfrac{r (-k)}{n}}
    \\
    \;\equiv\;
    \chi_{[-k]}\big([r]\big)
    \mathrlap{\,.}
  \end{array}
$$

From this we have two kinds of orbits:

1. the [[singleton]] orbits with stabilizer $\mathbb{Z}_2$:

   $\big\{ [0] \big\}$, which always exists

   and $\big\{ [n/2] \big\}$, which exists when $n$ is an [[even number]],

2. the pairs with stabilizer the [[trivial group]] $1$:

   $\big\{[k],[-k]\big\}$, for $k \in \{1, \cdots, \lfloor(n-1)/2\rfloor\}$ (with $\lfloor-\rfloor$ the [[floor]]).

The first singleton in the first case gives rise to two irreps, corresponding to the two irreps of $\mathbb{Z}_2$ (the [[trivial representation]] and the [[sign representation]]):

$$
  \underset{Id}{
  \underbrace{
  Ind
    ^{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
    _{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
  }
  }
  \Big(
    \big(
      ([r], [s]) \mapsto 1
    \big)
    \otimes
    \big(
      ([r], [s]) \mapsto 1
    \big)
  \Big)
  \;=\;
  triv
$$

and

$$
  Ind
    ^{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
    _{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
  \Big(
    \big(
      ([r], [s]) \mapsto 1
    \big)
    \otimes
    \big(
      ([r], [s]) \mapsto e^{\pi \mathrm{i} s}
    \big)
  \Big)
  \;=\;
  \big(
    ([r], [s]) \mapsto e^{\pi \mathrm{i} s}
  \big)
  \,,
$$

while the second singleton in the first case similarly gives 

$$
  Ind
    ^{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
    _{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
  \Big(
    \big(
      ([r], [s]) \mapsto e^{\pi \mathrm{i} r}
    \big)
    \otimes
    \big(
      ([r], [s]) \mapsto 1
    \big)
  \Big)
  \;=\;
  \big(
    ([r], [s]) \mapsto e^{\pi \mathrm{i} r}
  \big)
$$

and


$$
  Ind
    ^{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
    _{\mathbb{Z}_p \rtimes \mathbb{Z}_2}
  \Big(
    \big(
      ([r], [s]) \mapsto e^{\pi \mathrm{i} r}
    \big)
    \otimes
    \big(
      ([r], [s]) \mapsto e^{\pi \mathrm{i} s}
    \big)
  \Big)
  \;=\;
  \big(
    ([r], [s]) \mapsto e^{\pi \mathrm{i} (r + s)}
  \big)
  \,.
$$


The second case gives rise to one irrep for each $k \in \{1, \cdots, \lfloor(n-1)/2\rfloor\}$:

$$
  \begin{array}{l}
  Ind
    ^{ \mathbb{Z}_p \rtimes \mathbb{Z}_2 }
    _{ \mathbb{Z}_p }
  \Big(
    \big(
      [r] \mapsto e^{2 \pi \mathrm{i} \tfrac{r k}{n}}
    \big)
    \otimes
    \big(
      [r] \mapsto 1
    \big)
  \Big)
  \\
  \;\simeq\;
  \mathbb{C}\big[
    \mathbb{Z}_p \rtimes \mathbb{Z}_2
  \big]  
  \otimes_{ \mathbb{C}[\mathbb{Z}_p] }
    \Big(
      [r] \mapsto e^{2 \pi \mathrm{i} \tfrac{r k}{n}}
    \Big)
   \mathrlap{\,.}
  \end{array}
$$

These latter irreps are 2-dimensional, with an evident matrix representation $\widehat{(-)}$ given by

$$
  \widehat{
  \big(
    [1], [0]
  \big)
  }
  \;=\;
  \left[
    \begin{matrix}
       e^{+ 2 \pi \mathrm{i} \tfrac{k}{n}} & 0
       \\ 
       0 & e^{- 2 \pi \mathrm{i} \tfrac{k}{n}} 
    \end{matrix}
  \right]
  \,,\;\;\;\;\;\;
  \widehat{
  \big(
    [0], [1]
  \big)
  }
  \;=\;
  \left[
  \begin{matrix}
     0 & 1 
     \\
     1 & 0
  \end{matrix}
  \right]
  \mathrlap{\,.}
$$
 
As a consistency check that we found all irreps, we verify that the [sum of squares formula](regular+representation#SumOfSquaresFormula) holds:

We have found two 1-dimensional irreps when $n$ is odd and four of them when $n$ is even, together with 
$\lfloor (n-1)/2\rfloor$ irreps of dimension 2, whence the sum of their squares of dimensions is,

for odd $n$:

$$
  2 \cdot 1^2
  \,+\,
  \lfloor (n-1)/2\rfloor \cdot 2^2
  \;=\;
  2 + \frac{n-1}{2} 4
  \;=\;
  2 + 2 (n-1)
  \;=\;
  2 n 
$$

and for even $n$:

$$
  4 \cdot 1^2
  \,+\,
  \lfloor (n-1)/2\rfloor \cdot 2^2
  \;=\;
  2 \cdot 2 
  \,+\,
  \frac{n-2}{2} 4
  \;=\;
  2 \cdot 2 + 2 \cdot (n-2)
  \;=\;
  2 n
  \,,
$$

correctly coinciding with 
the [[order of a group|order]] of our group :

$$
  {\vert \mathbb{Z}_n \rtimes \mathbb{Z}_2 \vert} 
  \;=\;  
  {\vert \mathbb{Z}_2 \vert} 
  \cdot
  {\vert \mathbb{Z}_n \vert} 
  \;=\;  
  2 n
  \,.
$$
\end{example}

\begin{example}
  For construction of irreps of [[wreath products of groups]] see [there](wreath+product+of+groups#IrreducibleRepresentations).
\end{example}


## References

The original article:

* {#Mackey68} [[George Mackey]]: *Induced representations of groups and quantum mechanics*, W. A. Benjamin, New York (1968) &lbrack;[ark:/13960/t6841m201](https://archive.org/details/inducedrepresent0000mack)&rbrack;

General discussion:

* J. M. G. Fell, R. S. Doran: *Representations of $\ast$-Algebras, Locally Compact Groups, and Banach $\ast$-Algebraic Bundles*, volume 2: *Banach $\ast$-Algebraic Bundles, Induced Representations, and the Generalized Mackey Analysis*, Academic Press (1988) &lbrack;[ISBN:9780122527227](https://shop.elsevier.com/books/representations-of-algebras-locally-compact-groups-and-banach-algebraic-bundles/fell/978-0-12-252722-7)&rbrack;

Review for the case of [[finite groups]]:

* [[Charles Curtis]], [[Irving Reiner]], around Prop. 11.8 of: _Representation theory of finite groups and associative algebras_, AMS (1962) &lbrack;[ISBN:978-0-8218-4066-5](https://bookstore.ams.org/chel-356.h)&rbrack;

* {#Serre77} [[Jean-Pierre Serre]], section 8.2 of: *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;

* [[Brian Conrad]]: *Mackey theory and applications* &lbrack;[pdf](https://math.stanford.edu/~conrad/210BPage/handouts/mackey.pdf), [[Conrad-MackeyTheory.pdf:file]]&rbrack;

* Amirtanshu Prasad, M. K. Vemuri: *Mackey's Little Group Method* &lbrack;[pdf](https://www.imsc.res.in/~amri/little_groups.pdf), [[PrasadVemuri-MackeyMethod.pdf:file]]&rbrack;

* S. Martin: *Mackey Theory*, chapter 12 of *[Representation Theory](https://dec41.user.srcf.net/h/II_L/representation_theory/)*, notes by [[Dexter Chua]] (2016) &lbrack;[pdf](https://dec41.user.srcf.net/h/II_L/representation_theory/12)&rbrack;

Further developments:

* Geetha Venkataraman: *On irreducibility of induced modules and an adaptation of the Wigner--Mackey method of little groups*, J. Korean Math. Soc. **50** 6 (2013) 1213-1222 &lbrack;[arXiv:0908.0026](https://arxiv.org/abs/0908.0026), [doi:10.4134/JKMS.2013.50.6.1213](https://doi.org/10.4134/JKMS.2013.50.6.1213)&rbrack;

Review for the case of [[Lie groups]] (cf. *[[Wigner classification]]*):

* [[José Figueroa-O’Farrill]]: *The Theory of Induced Representations in Field Theory* &lbrack;[pdf](https://webhomes.maths.ed.ac.uk/~jmf/Teaching/Projects/Poincare/IndReps.pdf), [[Figueroa-InducedReps.pdf:file]]&rbrack;
