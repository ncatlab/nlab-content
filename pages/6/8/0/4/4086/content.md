{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

# Idea

As [[TVS|topological vector spaces]] are [[uniform spaces]], it is appropriate to discuss [[complete uniform space|completeness]].  As with a uniform space, a topological vector space is _complete_ if it has no holes: everything that should be there actually is there.

Where this gets interesting is in the question as to what _should_ be there.  To determine this, one has to have some method of discovering holes.  This is usually done by means of [[Cauchy nets]], but in a given application it may not be necessary that all holes be filled and this leads to weaker notions of completeness.

The more general notions make sense for arbitrary [[topological vector spaces]] but some more refined notions are only used for [[locally convex topological vector spaces]].

# Definitions

In strict order of decreasing strength, we have the following notions of completeness.

+-- {: mynumdef #WeakCplt}
###### Definition
A [[locally convex topological vector space]] is **weakly complete** if it is complete for its weak topology.
=--


+-- {: mynumdef #BCplt}
###### Definition
A [[locally convex topological vector space]] is **$B$-complete** or is a **Ptak space** if a subspace of its [[continuous dual]] is [[weakly closed]] whenever its intersection with any [[equicontinuous]] subset is weakly closed (in the subset).
=--

+-- {: mynumdef #BCplt}
###### Definition
A [[locally convex topological vector space]] is **$B_r$-complete** if a dense subspace of its [[continuous dual]] is [[weakly closed]] whenever its intersection with any [[equicontinuous]] subset is weakly closed (in the subset).
=--


+-- {: mynumdef #Cplt}
###### Definition
A [[topological vector space]] is **complete** if every Cauchy net converges.
=--

+-- {: mynumdef #QuasiCplt}
###### Definition
A [[topological vector space]] is **quasi-complete** if every [[bornology|bounded]], [[closed]] subset is complete.
=--

+-- {: mynumdef #SeqCplt}
###### Definition
A [[topological vector space]] is **sequentially complete** or **semi-complete** if every [[Cauchy sequence]] [[converges]].
=--

+-- {: mynumdef #LocCplt}
###### Definition
A [[locally convex topological vector space]] is **locally complete** if for $B \subseteq E$ a [[bounded]], [[closed]], [[absolutely convex]] subset then its norm space, $E_B$, is a Banach space.
=--

# Properties
##Sequentially Complete versus Locally Complete
Sequentially complete implies locally complete because every locally Cauchy sequence is a Cauchy sequence. The inverse implication "locally complete" $\Rightarrow$ sequentially complete is true for example in metrizable locally convex topological vector spaces, but not in general: A Cauchy sequence will not be locally Cauchy in general.

The problem to precisly characterize the spaces in which every convergent sequence is locally convergent is an open problem according to K&#246;the volume 1 (which is quite old, so it could have been solved in the meantime).


# References

See [[functional analysis bibliography]]

[[!redirects quasi-complete topological vector space]]
[[!redirects semi-complete topological vector space]]
[[!redirects sequentially complete topological vector space]]
[[!redirects complete topological vector spaces]]
[[!redirects quasi-complete topological vector spaces]]
[[!redirects semi-complete topological vector spaces]]
[[!redirects sequentially complete topological vector spaces]]
[[!redirects complete locally convex topological vector spaces]]
[[!redirects quasi-complete locally convex topological vector space]]
[[!redirects semi-complete locally convex topological vector space]]
[[!redirects sequentially complete locally convex topological vector space]]
[[!redirects complete locally convex topological vector spaces]]
[[!redirects quasi-complete locally convex topological vector spaces]]
[[!redirects semi-complete locally convex topological vector spaces]]
[[!redirects sequentially complete locally convex topological vector spaces]]
[[!redirects complete TVS]]
[[!redirects complete LCTVS]]
[[!redirects quasi-complete TVS]]
[[!redirects quasi-complete LCTVS]]
[[!redirects semi-complete TVS]]
[[!redirects semi-complete LCTVS]]
[[!redirects sequentially complete TVS]]
[[!redirects sequentially complete LCTVS]]