A **locally cartesian closed category** is a [[category]] $C$ whose [[over category|slice categories]] $C/x$ are all [[cartesian closed category|cartesian closed]]. If $C$ has a [[terminal object]], then $C$ is itself cartesian closed and in fact [[finitely complete category|has all finite limit]]s; often this requirement is included in the definition.

Equivalently, $C$ is a category with [[pullback]]s (and a terminal object, if required) such that each [[base change]] functor $f^*: C/y \to C/x$ has a right adjoint $\Pi_f$. In particular, such pullbacks preserve all [[colimit]]s. Therefore, if a locally cartesian closed category [[finitely cocomplete category|has finite colimit]]s, it is automatically a [[coherent category]] and in fact a [[Heyting category]].

The [[internal logic]] of locally cartesian closed categories is dependent [[type theory]].  In particular, $\Pi_f$ is interpreted as a [[dependent product]].

There are categories which are cartesian closed and not locally cartesian closed, but in which for some $f$ the  base change functor $f^*: C/y \to C/x$ has a right adjoint. This includes $Cat$, $Gpd$, and the category of [[crossed complex]]es; in the latter two cases, it is necessary and sufficient for $f$ to be a [[fibration]], while in $Cat$ it is sufficient for $f$ to be a fibration or an opfibration.

#References#

* Conduch&#233;, Fran&#231;ois.  Au sujet de l'existence d'adjoints &#224; droite aux foncteurs "image r&#233;ciproque" dans la cat&#233;gorie des cat&#233;gories. (French)  C. R. Acad. Sci. Paris S&#233;r. A-B  275  (1972), A891--A894.

* Howie, J.. Pullback functors and crossed complexes, Cahiers Topologie G\'eom. Diff\'erentielle, 20 (1979) 281--296.

* Bunge, Marta and Niefield, Susan.  Exponentiability and single universes. J. Pure Appl. Algebra 148 (2000) 217--250.

[[!redirects locally cartesian closed categories]]
[[!redirects LCCC]]
