Given a presheaf $T$ on a CwF $C$, let $T^\Pi(\Gamma) = \Sigma_{A \in Ty(\Gamma)}T(\Gamma . A)$, so that $Ty^\Pi$ is the presheaf consisting of pairs of a type $A$ and a type $B$ in a context extended by $A$ and $Tm^\Pi$ is the presheaf of pairs of a type $A$ and a term in a context extended by $A$.

+--{: .un_defn}
######Definition
Let $C$ be a CwF. A **$\Pi$-type** structure on $C$ consists of :

* a natural transformation $\Pi : Ty^\Pi \to Ty$
* a natural transformation $\lambda : Tm^\Pi \to Tm$
* and a natural isomorphism 
$$\langle -, -\rangle : [C^{op}, Set]( -, Ty^\Pi) \times [C^{op}, Set](-, Tm) \to [C^{op}, Set](-, Tm^\Pi)$$
exhibiting the following square as a pullback-square
$$
\array{
Tm^\Pi & \xrightarrow{\lambda} & Tm \\
of^\Pi \downarrow & & \downarrow of \\
Ty^\Pi & \xrightarrow{\Pi} & Ty
}
$$
=--
