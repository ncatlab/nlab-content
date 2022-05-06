In a CwF $C$, let $Ty^\Pi = \Sigma_{Ty}\Pi_{of}Tm^*(Ty)$ and $Tm^\Pi = \Sigma_{Ty}\Pi_{of}Tm^*(Tm)$ where $\Sigma_{Ty}$ is composition by the unique arrow $Ty \to 1$,
$\Pi_{of}$ is right-adjoint to pull-back along $of : Tm \to Ty$ and $Tm^*$ is pulling-back along the unique arrow $Tm \to 1$.


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
