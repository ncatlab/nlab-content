## Idea

Given a [[category]] $C$ one can consider the [[category]] of [[spectrum objects]] in $C$.  When $C$ is [[symmetric monoidal category|symmetric monoidal]], there is an induced [[symmetric monoidal structure]] on the [[category]] of [[spectrum objects]], generalizing the [[symmetric monoidal smash product of spectra]].

## Definitions

### Symmetric monoidal category of spectrum objects

Let $T$ be an [[object]] of a [[symmetric monoidal category]] $C$.  Following [Ayoub](#Ayoub) we can define a [[category]] $\Spect^\Sigma_T(C)$ of symmetric $T$-spectra in $C$ as described at [[spectrum object]].

In that case the category of $\Sigma$-[[symmetric sequences]] $\Seq(\Sigma, C)$ inherits a [[symmetric monoidal structure]] as described at [[symmetric sequence]].

Consider the [[symmetric sequence]] $Sym(T)$ whose $n$th component is $Sym(T)_n = T^{\otimes n}$ (with the [[actions]] of the [[symmetric group]] $\Sigma_n$ by permuting the $n$ factors).  It turns out that $Sym(T)$ is a commutative [[algebra object]] in the [[symmetric monoidal category]] $Seq(\Sigma, C)$.

As a consequence there is a [[symmetric monoidal structure]] on $Mod_\ell(Sym(T))$ where $X \otimes_{Sym(T)} Y$ is defined as the [[coequalizer]] of the diagram
  $$ X \otimes Sym(T) \otimes Y \rightrightarrows X \otimes Y. $$

By noting the tautological [[equivalence of categories]]
  $$ \Spect^\Sigma_T(C) \stackrel{\sim}{\longrightarrow} \Mod_\ell(Sym(T)) $$
one gets a [[symmetric monoidal structure]] on $Spect^\Sigma_T(C)$.

### Symmetric monoidal (infinity,1)-category of spectrum objects

...

## See also

* [[spectrum object]]
* [[symmetric sequence]]
* [[symmetric monoidal smash product of spectra]]

## References

The last chapter of

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))
