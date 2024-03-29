
For $R$ a [[ring]] write $R$[[Mod]] for its category of [[modules]].
Given a [[homomorphism]] of [[ring]] $f : R_1 \to R_2$ and an $R_2$-[[module]] $N$ there are composites of [[base change]] along $f$ with the [[hom-functor]] and the [[tensor product]] functor

$$
  R_1 Mod \stackrel{\otimes_{R_1} R_2}{\to} R_2 Mod \stackrel{\otimes_{R_2} N}{\to} Ab
$$

$$
  R_1 Mod \stackrel{Hom_{R_1 Mod}(-,R_2)}{\to}
  R_2 Mod
  \stackrel{Hom_{R_2}(-,N)}{\to}
  Ab
  \,.
$$

The [[derived functors]] of $Hom_{R_2}(-,N)$ and $\otimes_{R_2} N$ are the [[Ext]]- and the [[Tor]]-functors, respectively, so the [[Grothendieck spectral sequence]] applied to these composites is the _base change spectral sequence_ for these.
