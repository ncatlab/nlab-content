## Renormalization
 {#Renormalization}





By prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}  the [[renormalization|("re"-)normalization]] of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ is [[induction|inductively]] in $k \in \mathbb{N}$ a choice of [[extension of distributions]] of $T_{k}$ from the [[complement]] $\Sigma^k \setminus diag(\Sigma)$ of the [[diagonal]] to all of $\Sigma^k$.

If $\Sigma = \mathbb{R}^{p,1}$ is [[Minkowski spacetime]] so that the [[free field]] [[vacuum]] (def. \ref{VacuumFree}) is translation invariant, then translation invariance reduces this to an [[extension of distributions]] of $T_{k}$ from the [[complement]] $\mathbb{R}^{k(p+1)} \setminus \{0\}$ of a single point to that point.

If $T_{k}$ has finite [[degree of divergence of a distribution|degree of divergence]] at the origin, then by [this prop.](extension+of+distributions#SpaceOfPointExtensions) there is a [[finite dimensional vector space|finite dimensional]] [[affine space]] of choices of such extensions, which each themselves have finite degree of divergence.

Explicitly, the difference between any two choices of extensions of $T_k$ to the diagonal is a sum of [[derivative of a distribution|partial derivatives]] of the [[delta distribution]] $\delta_0$ [[support of a distribution|supported]] at the origin:

$$
  \underset{ {\alpha \in \mathbb{N}^{k(p+1)}} \atop { {\vert \alpha\vert} \leq deg(T_k) } }{\sum}
  c_k^\alpha \partial_\alpha \delta_0
$$

These $c_k^\alpha$ are the _("re"-)normalization constants_ at order $k$.

They describe "new" local interaction that appear whenever $k$ of the given interaction vertices $g S_{int} + j A$ coincide.

By prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} and [this prop.](scaling+degree+of+a+distribution#ScalingDegreeOfProductDistribution) it follows that with these choices made then the uniquely induced $T_{k+1}$ on $\Sigma^{k+1}\setminus diag(\Delta)$ has finite degree of divergence, and hence the inductive ("re"-)normalization may continue to the next order.

If there is $n \in \mathbb{N}$ such that $c^\alpha_k = 0$ for all $g \gt n$, then the [[perturbative QFT]] (specified by the [[free field]] [[vacuum]] and an [[interaction]] $g S_{int}$) is called _[[renormalizable perturbative QFT|renormalizable]]_, otherwise _non-renormalizable_. 

Beware that this terminology has its pitfalls: The above theorem says that for _all_ (translation invariant) perturbative QFTs exist constructions of [[time-ordered products]] on the diagonal, hence [[renormalization|("re"-)normalizations]]. The issue expressed with the term "non-renormalizable" at this point is not a mathematical statement, but a physical sentiment. Presently it is popular to think of this "non-renormalizable" situation as expessing "[[effective field theory]]".

This perspectived on [[renormalization|("re"-)normalization]] by inductive construction of [[time-ordered products]] as [[distributions]] on [[Cartesian products]] of [[spacetime]] is called _[[Epstein-Glaser renormalization]]_. In the original  ([Epstein-Glaser 73](causal+perturbation+theory#EpsteinGlaser73)) this is phrased in terms of causal splitting of distributions. The perspective in terms of [[extensions of distributions]] appears in ([Brunetti-Fredenhagen 99](Epstein-Glaser+renormalization#BrunettiFredenhagen99)), following ([Popineau-Stora 82](Epstein-Glaser+renormalization#PopineauStora82), [Stora 93](Epstein-Glaser+renormalization#Stora93)) which in turn (according to [Dütsch 18, footnote 57](#Duetsch18)) followed personal communication with [[Henri Epstein]]

[[main theorem of perturbative renormalization]]

[[renormalization group]]

* [[Stückelberg-Petermann renormalization group]]

* [[Gell-Mann-Low renormalization cocycles]]



