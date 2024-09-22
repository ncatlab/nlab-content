

## Fixed point subgroup

Given a [[group]] $G$ and an [[automorphism]] (or just an [[endomorphism]]) $\phi \colon G \xrightarrow{\;} G$, its [[set]] of [[fixed points]]

$$
  G^\phi
  \;\coloneqq\;
  \Big\{
    g \in G
    \;\Big\vert\;
    \phi(g)
    =
    g
  \Big\}
  \;\subset\;
  G
$$

evidently constitutes a [[subgroup]], called the *fixed-point subgroup* of $\phi$.

The analogous statement holds for $G$ replaced by any [[algebra|algebraic]] [[structure]]: The endomorphism property ensures that with a [[pair]] of [[elements]] being fixed by $\phi$, so is their [[binary operation|product]] in the algebra:

$$
  \phi(g_i)
  =
  g_i
  \;\;
  \Rightarrow
  \;\;
  \phi\big(
    g_1 \cdot g_2
  \big)
  \;=\;
  \phi(g_1)
  \cdot
  \phi(g_2)
  \;=\;
  g_1 \cdot g_2
$$

## Examples

\begin{example}
  If $\phi = Ad_g$ is an [[inner automorphism]] ancting by [[conjugation action|conjugation]] with an element$g \in G$, then its fixed-point subgroup $G^\phi$ is the *[[centralizer subgroup]]* $C_G(g)$.
\end{example}

## References

* Wikipedia: *[Fixed-point subgroup](https://en.wikipedia.org/wiki/Fixed-point_subgroup)*




## Sugimoto string theory


The *Sugimoto string theory* is a non-[[supersymmetry|supersymmetric]] version of [[type I string theory]], given by 10d [[type IIB string theory]] on an $O9^+$ [[orientifold]] (instead of $O9^-$), hence with [[RR-field tadpole cancellation]] by 32 *[[anti-brane|anti]]* [[D9-branes]] (instead of plain D9-branes), whose [[gauge group]] is the [[symplectic group]] acting on $\mathbb{R}^{32}$ (beware the different notations: either "$Sp(32;\mathbb{R})$" or "$Sp(16)$", [Sugimoto 1999](#Sugimoto99) wrote "$USp(32)$").

## Referemces

The original article:

* {#Sugimoto99} [[Shigeki Sugimoto]]: *Anomaly Cancellations in the Type I D9-anti-D9 System and the $USp(32)$ String Theory*, Prog. Theor. Phys. **102** (1999) 685-699 &lbrack;[arXiv:hep-th/9905159](https://arxiv.org/abs/hep-th/9905159), [doi:10.1143/PTP.102.685](https://doi.org/10.1143/PTP.102.685)&rbrack;

Further discussion:

* Sanefumi Moriyama: *$USp(32)$ String as Spontaneously Supersymmetry Broken Theory*, Phys. Lett. B **522** (2001) 177-180 &lbrack;[arXiv:hep-th/0107203](https://arxiv.org/abs/hep-th/0107203), <a href="https://doi.org/10.1016/S0370-2693(01)01278-3">doi:10.1016/S0370-2693(01)01278-3</a>&rbrack;

* Hector Parra de Freitas, p. 166 of: *String Compactifications with Half-maximal Supersymmetry*, PhD thesis, Université Paris-Saclay (2023) &lbrack;[hal/tel-04234221](https://theses.hal.science/tel-04234221), [pdf](https://theses.hal.science/tel-04234221v1/file/133300_PARRA_DE_FREITAS_2023_archivage.pdf)&rbrack;


