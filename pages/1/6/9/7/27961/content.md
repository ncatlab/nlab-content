
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


\tableofcontents

## Idea
 {#Idea}

By reference to the [[superembedding formalism]] for [[super p-branes]], the existence of "$L_p$-branes" has been argued &lbrack;[Howe & Sezgin 1997, p. 8](#HoweSezgin97a)&rbrack;, for small [[natural numbers]] $p$, with the following properties:

The $p+4$-dimensional [[target spacetime]] $X^{p+4}$ carries [[flux densities]] 

$$
  \begin{aligned}
    G_2 & \in \Omega^2_{dR}\big(X^{p+4}\big)
    \\
    G_{p+1} & \in \Omega^{p+1}_{dR}\big(X^{p+4}\big)
    \\
    G_{p+2} & \in \Omega^{p+2}_{dR}\big(X^{p+4}\big)
    \mathrlap{\,,}
  \end{aligned}
$$

subject to the [[Bianchi identities]]

$$
  \begin{aligned}
    \mathrm{d} G_2 & = 0
    \\
    \mathrm{d} G_{p+1} & = 0
    \\
    \mathrm{d} G_{p+2} & = G_2 \wedge G_{p+1} 
    \mathrlap{\,;}
  \end{aligned}
$$

and on the brane's [[worldvolume]] 

$$
  \Sigma^{p+1} 
    \xrightarrow{\phantom{-}\phi\phantom{-}} 
  X^{p+4}
$$ 

there is a flux density 

$$
  \begin{aligned}
    F_p & \in \Omega^p_{dR}(X^{p+1})
  \end{aligned}
$$

satisfying the [[Bianchi identity]]

$$
  \begin{aligned}
    \mathrm{d} \, F_p 
    & = \phi^\ast G_{p+1}
    \,.
  \end{aligned}
$$

In [Howe, Raetzel & Sezgin 1998, p 3](#HoweRaetzelSezgin98) this is claimed for $p \in \{1,2,3,4,5\}$. The followup article [Howe, Raetzel & Rudychev 1999](#HoweRaetzelRudychev99) considers it for $p \in \{3,4,5\}$.

## Examples

### $L_1$-brane
  {#L1Brane}

For $p = 1$ the [above](#Idea) [[Bianchi identities]] read:

$$
  \begin{aligned}
    \mathrm{d} G_2 & = 0
    \\
    \mathrm{d} G_3 & = G_2 \wedge G_2
    \\
    \mathrm{d} H_1 & = \phi^\ast G_2
    \mathrlap{\,.}
  \end{aligned}
$$

The first two are the Bianchi identities of [[5D Maxwell-Chern-Simons theory]], hence of the gauge sector of minimal [[D=5 supergravity]].

There is a close [structural analogy](D=5+supergravity#ViaCYCompactificationOf11dSupergravity) between this [[D=5 supergravity]] on one hand and [[D=11 supergravity]] on the other. The latter has [[Bianchi identities]] (for the [[supergravity C-field]] [[flux densities]] $G_4$ and $G_7$) of this form:

$$
  \begin{aligned}
    \mathrm{d} G_4 & = 0
    \\
    \mathrm{d} G_7 & = G_4 \wedge G_4
    \\
    \mathrm{d} H_3 & = \phi^\ast G_4
    \mathrlap{\,,}
  \end{aligned}
$$

where in the last line $H_3$ is the [[self-dual higher gauge field|chiral flux]] on the [[M5-brane]] worldvolume. 

This makes the $L_1$-brane structure above look like it matches the [[probe brane]] version of the known [[black string]] [of](black+string#ReferencesIn5DSuGra) [[D=5 supergravity]].



## References

Original articles:

* {#HoweSezgin97a} [[Paul S. Howe]], [[Ergin Sezgin]], p. 8 of:  *Superbranes*, Phys. Lett. B **390** (1997) 133-142 &lbrack;[arXiv:hep-th/9607227](https://arxiv.org/abs/hep-th/9607227), <a href="https://doi.org/10.1016/S0370-2693(96)01416-5">doi:10.1016/S0370-2693(96)01416-5</a>&rbrack;

* {#HoweRaetzelSezgin98} [[Paul S. Howe]], O. Raetzel, [[Ergin Sezgin]], pp. 3-4 of: *On Brane Actions and Superembeddings*, JHEP 9808 (1998) 011 &lbrack;[arXiv:hep-th/9804051](https://arxiv.org/abs/hep-th/9804051), [doi:10.1088/1126-6708/1998/08/011](https://doi.org/10.1088/1126-6708/1998/08/011)&rbrack;

* {#HoweRaetzelRudychev99} [[Paul S. Howe]], O. Raetzel, I. Rudychev, [[Ergin Sezgin]]: *L-branes*, Class. Quant. Grav. **16** (1999) 705-722 &lbrack;[arXiv:hep-th/9810081](https://arxiv.org/abs/hep-th/9810081), [doi:10.1088/0264-9381/16/3/006](https://doi.org/10.1088/0264-9381/16/3/006)&rbrack;

Review:

* [[Steven Duplij]]: *L-Brane*, in: *Concise Encyclopedia of Supersymmetry*, Springer (2017) 225 &lbrack;[doi:10.1007/1-4020-4522-0_294](https://doi.org/10.1007/1-4020-4522-0_294), [[Duplij-LBrane.pdf:file]]&rbrack; 

[[!redirects L-branes]]

[[!redirects Lp-brane]]
[[!redirects Lp-branes]]


