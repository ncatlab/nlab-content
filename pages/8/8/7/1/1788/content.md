


[[CQTS-QuantumIndustryDay-Nov2024.jpg:file]]


\linebreak


***


* Niccolò Cribiori, Dieter Lust: *String dualities and modular symmetries in supergravity: a review*, in: *Half a century of Supergravity*, Cambridge University Press &lbrack;[arXiv:2411.06516](https://arxiv.org/abs/2411.06516)&rbrack;




***


**A notorious bug:**

The code 

"<nowiki>[[Set]] [[topos]]</nowiki>"

renders as:

[[Set]] [[topos]]

(lacking the whitespace).

Similarly the code

"<nowiki>[[Set]] &dollar;topos&dollar;</nowiki>"

renders without the whitespace:

[[Set]] $topos$ 

This issue goes away when we are not at the beginning of a line. For instance

"<nowiki>A [[Set]] [[topos]]</nowiki>"

renders correctly as

A [[Set]] [[topos]]

and 

"<nowiki>A [[Set]] &dollar;topos&dollar;</nowiki>"

renders correctly as

A [[Set]] $topos$

\linebreak

More testing:

[[topos]] [[topos]] [[topos]] [[topos]]
[[Set]]  [[topos]] (two whitespaces)

\linebreak

\linebreak

***

\linebreak

\linebreak

\linebreak

[[test2.txt:file]]

\linebreak

\linebreak

\linebreak


***

\linebreak

\linebreak

\linebreak

### The lattice of subtoposes

Since the maps in $\Delta_+$ are all strictly monotone, any object $[n]$ receives only (finitely many) morphisms from objects $[m]$ with $m\leq n$ whence all [[slice category|slices]] $\Delta_+/[n]$ are [[finite category|finite]]. This is sufficient for all [[Grothendieck topology|Grothendieck topologies]] on $\Delta_+$ to be [[rigid topology|rigid]] whence all subtoposes of $Set^{\Delta_+^{op}}$ are [[level of a topos|essential]] and of [[presheaf topos|presheaf type]] and their lattice is isomorphic to the lattice of [[Cauchy-complete category|Cauchy-complete]] [[full subcategory|full subcategories]] of $\Delta_+$.

This situation is familiar from $\Delta$ but in the latter case there are considerable fewer Cauchy-complete subcategories available, since an object $[n]$ having non-trivial idempotents its inclusion automatically requires the presence of all $[m]$ with $m\,$<$\,n$ in the subcategory whence there a countably many subtoposes corresponding to the $n$-truncated subcategories on the objects $[0],\dots [n]$.

For further details on the topologies, [[closure operator|closure operators]] and [[sheaf|sheaves]] involved in both cases see [Rosset-Hansen-Endrullis](#RHE24)).

 
## Sugimoto string theory


The *Sugimoto string theory* is a non-[[supersymmetry|supersymmetric]] version of [[type I string theory]], given by 10d [[type IIB string theory]] on an $O9^+$ [[orientifold]] (instead of $O9^-$), hence with [[RR-field tadpole cancellation]] by 32 *[[anti-brane|anti]]* [[D9-branes]] (instead of plain D9-branes), whose [[gauge group]] is the [[symplectic group]] $USp(32)$.

## References

The original article:

* {#Sugimoto99} [[Shigeki Sugimoto]]: *Anomaly Cancellations in the Type I D9-anti-D9 System and the $USp(32)$ String Theory*, Prog. Theor. Phys. **102** (1999) 685-699 &lbrack;[arXiv:hep-th/9905159](https://arxiv.org/abs/hep-th/9905159), [doi:10.1143/PTP.102.685](https://doi.org/10.1143/PTP.102.685)&rbrack;

Further discussion:

* Sanefumi Moriyama: *$USp(32)$ String as Spontaneously Supersymmetry Broken Theory*, Phys. Lett. B **522** (2001) 177-180 &lbrack;[arXiv:hep-th/0107203](https://arxiv.org/abs/hep-th/0107203), <a href="https://doi.org/10.1016/S0370-2693(01)01278-3">doi:10.1016/S0370-2693(01)01278-3</a>&rbrack;

* Hector Parra de Freitas, p. 166 of: *String Compactifications with Half-maximal Supersymmetry*, PhD thesis, Université Paris-Saclay (2023) &lbrack;[hal/tel-04234221](https://theses.hal.science/tel-04234221), [pdf](https://theses.hal.science/tel-04234221v1/file/133300_PARRA_DE_FREITAS_2023_archivage.pdf)&rbrack;




