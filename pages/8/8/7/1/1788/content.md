

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***


**Mackey theory**

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
  
1. The representations $\theta_{i,\rho}$ (eq:MackeyIrrepForFiniteSemProdWithAbelian) are irreducible.

1. If $\theta_{i,\rho} \simeq \theta_{i',\rho'}$ then $i = i'$ and $\rho \simeq \rho'$.

1. Every irrep of $G$ is of the form $\theta_{i, \rho}$, up to isomorphism.

\end{proposition}

([Serre 1977 Prop. 25 p 62](#Serre77))


## References

The original article:

* {#Mackey68} [[George Mackey]]: *Induced representations of groups and quantum mechanics*, W. A. Benjamin, New York (1968) &lbrack;[ark:/13960/t6841m201](https://archive.org/details/inducedrepresent0000mack)&rbrack;

General discussion:

* J. M. G. Fell, R. S. Doran: *Representations of $\ast$-Algebras, Locally Compact Groups, and Banach $\ast$-Algebraic Bundles*, volume 2: *Banach $\ast$-Algebraic Bundles, Induced Representations, and the Generalized Mackey Analysis*, Academic Press (1988) &lbrack;[ISBN:9780122527227](https://shop.elsevier.com/books/representations-of-algebras-locally-compact-groups-and-banach-algebraic-bundles/fell/978-0-12-252722-7)&rbrack;

Review for the case of [[finite groups]]:

* [[Charles Curtis]], [[Irving Reiner]], around Prop. 11.8 of: _Representation theory of finite groups and associative algebras_, AMS (1962) &lbrack;[ISBN:978-0-8218-4066-5](https://bookstore.ams.org/chel-356.h)&rbrack;

* {#Serre77} [[Jean-Pierre Serre]], section 8.2 of : *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;

* Amirtanshu Prasad, M. K. Vemuri: *Mackey's Little Group Method* &lbrack;[pdf](https://www.imsc.res.in/~amri/little_groups.pdf)&rbrack;

Further developments:

* Geetha Venkataraman: *On irreducibility of induced modules and an adaptation of the Wigner--Mackey method of little groups*, J. Korean Math. Soc. **50** 6 (2013) 1213-1222 &lbrack;[arXiv:0908.0026](https://arxiv.org/abs/0908.0026), [doi:10.4134/JKMS.2013.50.6.1213](https://doi.org/10.4134/JKMS.2013.50.6.1213)&rbrack;

Review for the case of [[Lie groups]] (cf. *[[Wigner classification]]*):

* [[José Figueroa-O’Farrill]]: *The Theory of Induced Representations in Field Theory* &lbrack;[pdf](https://webhomes.maths.ed.ac.uk/~jmf/Teaching/Projects/Poincare/IndReps.pdf), [[Figueroa-InducedReps.pdf:file]]&rbrack;





\linebreak



Let $\mathbb{Z}^n_{\sum= [0]_k } \hookrightarrow \mathbb{Z}^n$ be the subgroup on those [[n-tuple|$n$-tuples]] of [[integers]] $(n_i)_{i = 1}^n$ whose [[sum]] is a multiple of $k \in \mathbb{Z}$, hence whose sum vanishes [[modulo]] $k$: $\sum_i n_i = 0 \,mod\, k$.

The [[cosets]] of this [[subgroup]] inclusion are clearly indexed by $C_k \equiv \mathbb{Z}/k$, and an element $(n_i)_{i=1}^k \,\in\,\mathbb{Z}^n$ belongs to the coset $r \,mod\, k$ if $\sum_i n_i = r \,mod\, k$. Hence we have a [[short exact sequence]] 

$$
  0 
    \to 
  \mathbb{Z}^n_{\sum = [0]_k}
    \longrightarrow
  \mathbb{Z}^n
    \xrightarrow{\sum \,\mathrm{mod}\, k}
  C_k
    \to 
  0
$$





(...)