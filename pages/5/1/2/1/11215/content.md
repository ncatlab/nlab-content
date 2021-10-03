
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Related concepts

* [[realizability]]

* [[Kleene's second algebra]]

The subcategory on the effectively computable morphisms of the [[function realizability topos]] $RT(\mathcal{K}_2)$ is the [[Kleene-Vesley topos]] $KV$. The category of "admissible representations" $AdmRep$ (whose morphisms are [[computable functions (analysis)]], see there) is a [[reflective subcategory]] of $RT(\mathcal{K}_2)$ ([BSS 07](#BSS07)) and the restriction of that to $KV$ is $AdmRep_{eff}$

$$
  \array{
     AdmRep_{eff} &\hookrightarrow& KV
     \\
     \downarrow && \downarrow
     \\
     AdmRep &\hookrightarrow& RT(\mathcal{K}_2)
  }
$$

[[!include computable mathematics -- table]]


## References

* {#Streicher07} [[Thomas Streicher]], around p. 17 of  _Realizability_ (2017/18) ([pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/REAL/REAL.pdf))

* {#vanOosten08} [[Jaap van Oosten]], _Realizability: an introduction to its categorical side_, Studies in Logic and the Foundations of Mathematics, vol. 152, Elsevier, 2008 ([preface pdf](http://www.staff.science.uu.nl/~ooste110/boekbegin.pdf))

* {#BSS07} [[Ingo Battenfeld]], Matthias Schr&#246;der, [[Alex Simpson]], _A convenient category of domains_, in L. Cardelli, M. Fiore and G. Winskel (eds.), _Computation, Meaning and Logic_, Articles dedicated to Gordon Plotkin  Electronic Notes in Computer Science, 34 pp., to appear, 2007  ([[BattenfeldDomains.pdf:file]])


[[!redirects function realizability]]
[[!redirects function realizability topos]]
[[!redirects function ralizability]]
