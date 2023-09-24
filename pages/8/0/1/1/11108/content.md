
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Traditional notation in [[physics]] &lbrack;[Dirac 1939](#Dirac39)&rbrack; for writing down [[pure state|pure]] [[quantum states]] (elements of [[Hilbert spaces]]), their [[hermitian adjoints]] and [[Hermitian form|Hermtian]] [[inner products]]:

With the [[Hermitian form|Hermitian]] [[inner product]] on the [[underlying]] [[vector space]] of a [[Hilbert space]] $H$ denoted $\langle-\vert-\rangle$, element $\psi \,\in\, H$ are turned into elements of the [[linear dual space]] $H^\ast$ by $\langle \psi \vert -\rangle \,\in\, H^\ast$, whose [[evaluation]] on another $\phi \in H$ is the given [[Hermitian form]] $\langle \psi \vert \phi\rangle$. Hence if one declares notation such that

$$
  \array{
     \vert \phi \rangle \;\equiv\; \phi \,\in\, H
     \\
     \langle \psi \vert \;\equiv\; \langle \psi \vert -\rangle \,\in\, H^\ast
  }
$$

then the [[evaluation]]-pairing in the [[Hermitian form]] is essentially juxtaposition 

$$
  \array{
    H^\ast \otimes H &\longrightarrow& \mathbb{C}
    \\
    \langle \psi \vert 
    ,
    \vert \phi \rangle
    &\mapsto&
    \langle \psi \vert \phi \rangle
  }
$$

With the inner product $\langle-\vert-\rangle$ referred to as a *bracket* this suggest to refer to "$\langle \psi \vert$" as a "bra" and "$\vert \phi \rangle$" as a "ket" &lbrack;[Dirac 1939, last line](#Dirac39)&rbrack;.

The notation may be udnerstood as a lightweight precursor to the [[string diagram]]-calculus in [[dagger-compact categories]] &lbrack;[Abramsky & Coecke 2004 §7.2](#AbramskyCoecke04), [2007 pp. 6](#AbramskyCoecke2007), [2008 §4.4](#AbramskyCoecke08), [Coecke 2010 §3.3](#Coecke10)&rbrack;.

For instance, if $\mathscr{H}$ is a [[finite-dimensional Hilbert space]] with [[orthonormal basis]] $\big(\left\vert w \right\rangle\big)_{w \colon W}$, then the [[compact closed category|compact closure]] is witnessed by the following [[isomorphism]] between the vector space of linear maps out of $\mathscr{H}$ and a vector space of [[matrices]]:

$$
  \array{
    \Big(
      \mathscr{H}
      \multimap
      \mathscr{H}'
    \Big)
    &\longrightarrow&
    \mathscr{H}' \otimes \mathscr{H}^\ast
    \\
    \Big(
      \left\vert w \right\rangle
      \,\mapsto\,
      \underset{w'}{\sum}
      \left\vert w' \right\rangle
      A_{w', w}
    \Big) 
    &\mapsto&
      \underset{w,w'}{\sum} 
      \left\vert w' \right\rangle
      A_{w', w}
      \left\langle w \right\vert
    \mathrlap{\,.}
  }
$$



## Related concepts

[[!include states and observables -- content]]


## References

The bra-ket notation is due to:

* {#Dirac39} [[Paul A. M. Dirac]], *A new notation for quantum mechanics*, Mathematical Proceedings of the Cambridge Philosophical Society **35** 3 (1939) 416-418 &lbrack;[doi:10.1017/S0305004100021162](https://doi.org/10.1017/S0305004100021162), [pdf](https://www.ifsc.usp.br/~lattice/wp-content/uploads/2014/02/Dirac_notation.pdf)&rbrack;

Textbook accounts:

* [[Jun John Sakurai]], Jim Napolitano, §1.2 in: *Modern Quantum Mechanics*, Cambridge University Press (1985, 1994, 2020) &lbrack;[doi:10.1017/9781108587280](https://doi.org/10.1017/9781108587280), [Wikipedia](https://en.wikipedia.org/wiki/Modern_Quantum_Mechanics)&rbrack;

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], Fig. 2.1 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[Robert B. Griffiths]], *Linear Algebra in Dirac notation*, Section 3 in: *Consistent Quantum Theory*, Cambridge University Press (2002) &lbrack;[doi:10.1017/CBO9780511606052](https://doi.org/10.1017/CBO9780511606052), [webpage](https://quantum.phys.cmu.edu/CQT)&rbrack;

See also:

* Wikipedia, _[Bra-ket notation](http://en.wikipedia.org/wiki/Bra&#8211;ket_notation)_

Discussion in the (broader) context of [[string diagram]]-calculus for [[dagger compact categories]] (cf. *[[quantum information theory via dagger-compact categories]]*):

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], §7.2 in: _A categorical semantics of quantum protocols_ , Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130)&rbrack;

* {#AbramskyCoecke2007} [[Samson Abramsky]], [[Bob Coecke]], pp. 6 in: *Physics from Computer Science: a Position Statement*, [International Journal of Unconventional Computing **3** 3 (2007)](https://www.oldcitypublishing.com/journals/ijuc-home/ijuc-issue-contents/ijuc-volume-3-number-3-2007/) $[$[pdf](https://www.cs.ox.ac.uk/files/349/YORKIJUC.pdf), [ijuc-3-3-p-179-197](https://www.oldcitypublishing.com/journals/ijuc-home/ijuc-issue-contents/ijuc-volume-3-number-3-2007/ijuc-3-3-p-179-197/)$]$

* {#AbramskyCoecke08} [[Samson Abramsky]], [[Bob Coecke]], §4.4 in: *Categorical quantum mechanics*, in *[[Handbook of Quantum Logic and Quantum Structures]]*, Elsevier (2008) &lbrack;[arXiv:0808.1023](http://arxiv.org/abs/0808.1023), [ISBN:9780080931661](https://www.sciencedirect.com/book/9780444528698/), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)&rbrack; 

* [[Bob Coecke]], §3.e in: _Kindergarten quantum mechanics_ &lbrack;[arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032)&rbrack;

* {#Coecke10} [[Bob Coecke]], §3.3 in: *Quantum Picturalism*, Contemporary Physics **51** 1 (2010) &lbrack;[arXiv:0908.1787](http://arxiv.org/abs/0908.1787), [doi:10.1080/00107510903257624](https://doi.org/10.1080/00107510903257624)&rbrack;

[[!redirects bra]]
[[!redirects ket]]
[[!redirects bras]]
[[!redirects kets]]

[[!redirects bra-ket notation]]
