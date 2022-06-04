



[[!redirects sandbox]]

In [[Martin-Löf type theory]], given 

* a [[type]] $A$, 

* a [[judgment]] $z \colon A \vdash B(z) \;\mathrm{type}$ (hence an $A$-[[dependent type]] $B$), 

* [[terms]]${}$ $x \colon A$ and $y \colon A$, 

* a [[term]] of their [[identity type]] $p \colon (x =_A y)$, 

then there are compatible **transport functions** 

\[
  \label{TheTransportFunctions}
  \overrightarrow{\mathrm{tr}}_{B}^{p}:B(x) \to B(y) 
  \;\;\;
  \text{and}
  \;\;\;
  \overleftarrow{\mathrm{tr}}_{B}^{p}:B(y) \to B(x)
  \,,
\] 

such that for all $v:B(y)$, the [[fiber]] of $\overrightarrow{\mathrm{tr}}_{B}^{p}$ at $v$ is [[contractible]], and for all $u:B(x)$, the [[fiber]] of $\overleftarrow{\mathrm{tr}}_{B}^{p}$ at $u$ is [[contractible]].


***

Fictitious gauge fields:

* Mircea Trif, Pramey Upadhyaya, Yaroslav Tserkovnyak, *Theory of electromechanical coupling in dynamical graphene* $[$[arXiv:1210.7384](https://arxiv.org/abs/1210.7384), [doi:10.1103/PhysRevB.88.245423](https://doi.org/10.1103/PhysRevB.88.245423)$]$


