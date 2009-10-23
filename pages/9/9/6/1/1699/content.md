

* [website](http://math.unice.fr/~carlos/)


#related $n$Lab entries#

* [[Simpson's conjecture]]

* [[n-category]]

* [[Pursuing Stacks]]

* [[descent]]

* [[nonabelian cohomology]]

* [[infinity-stack]]

#Simpson on descent#

In January 2009 Carlos Simpson wrote the following short note

* C. Simpson, _Descent_ ([pdf](http://math.unice.fr/~carlos/slides/ihesAGjan09.pdf))

The following reproduces the text unabridged, but equipped with hyperlinks on keywords to $n$Lab entries as far as existent.


## Descent ##

The notion of [[descent]], piecing together a global picture out of local pieces and glueing data, permeates Grothendieck's work. The history of this idea dates to the middle ages with mapmakers drawing an ever more precise picture of the world, as modern terminology of "[[atlas]]es" and "[[chart]]s" reminds us. It is crucial to the notion of [[cohomology]], where we first meet higher glueing data.

[[descent|Descent]] comes into Grothendieck's philosophy and work in a myriad of forms, starting with his papers _Technique de descente et th&#233;or&#232;mes
d'existence en g&#233;om&#233;trie alg&#233;brique_ . The technical requirements of this theory incited him to introduce the notion of [[fibered category]]. He extended
the domain of application of this point of view in a revolutionary way by introducing the notion of "[[Grothendieck topology]]", integrating all of 
[[Galois theory]] and giving us [[etale cohomology]]. A further transformation occured with the notion of [[topos]]. Another incarnation of the idea was cohomological
[[descent]] used in Deligne's papers on Hodge theory, where [[simplicial object]]s enter in a way which differs significantly from their original occurences in
[[algebraic topology]]. 

Between the 1960's and the 1980's, the notion of descent for objects of a [[category]], slowly gave way to a notion of "higher descent" for objects in generalized categorical situations. Examples include Breen's calculation
of etale Ext groups using the cohomology of simplicial [[Eilenberg-MacLane space|Eilenberg-MacLane]]
presheaves, and the theory of twisted complexes of Toledo and Tong. [[Jim Stasheff|Stasheff]] and Wirth [[gerbe|investigated  higher cocycles]] in the 1960's although Wirth's thesis was only recently [made public](http://golem.ph.utexas.edu/category/2006/09/wirth_and_stasheff_on_homotopy.html). In algebraic topology, Quillen's theory
of [[model category|model categories]] was gradually applied to simplicial diagrams. Illusie introduced the notion of [[model structure on simplicial presheaves|weak equivalence of]] [[simplicial presheaf|simplicial presheaves]] on a [[site|Grothendieck site]].

Grothendieck came out of isolation with the manuscript [[Pursuing Stacks|La poursuite des champs]], which at its start refers to a letter from Joyal to Grothendieck
developing the [[model category structure on simplicial sheaves]]. This led to Jardine's [[model structure on simplicial presheaves|model category structure for simplicial presheaves]] enhancing
Illusie's weak equivalences. We enter into the modern period in which Jardine's model structure and its variants have been used and developped with
applications in a wide range of mathematics including Thomason's work in K-theory and then Voevodsky's theory of $A^1$-homotopy and [[motive]]s. [[algebraic stack|Algebraic
stack]]s, the first step in the "higher descent!" direction, are now used without restraint in all of [[algebraic geometry]].

In Grothendieck's vision as set out in "[[Pursuing Stacks|La poursuite des champs]]", higher descent is just the same as usual descent, but for [[infinity-stack|n-stacks]] of [[n-catefory|n-categories]]
over a [[site]]. The theory of [[2-category|2-categories]] was developped early on by Benabou,
having occured also in the book of Gabriel and Zisman. The theory of [[strict omega-category|strict n-categories]] was thoroughly investigated by Street and the Australian
school, and Brown and Loday introduced other related algebraic objects which could model [[homotopy type]]s. Grothendieck set out the goal of finding
an adequate theory of [[omega-category|weak n-categories]] where composition would be associative only up to a coherent system of higher equivalences. Similar ideas
were being developped by Dwyer and Kan in algebraic topology, and Cordier and [[Tim Porter|Porter]] in [[category theory]]. Several definitions of [[weak omega-category|weak n-categories]] have been proposed, by Baez-Dolan, Tamsamani, Batanin and others. It is now well understood that the [[homotopy coherent category theory|homotopy coherence]] problems inherent in [[higher category theory|higher categories]], are basically the same as those which were studied by [[topology|topologists]] for [[delooping hypothesis|delooping machines]]. Segal's simplicial approach and May's operadic approaches
play important roles in all of the current definitions. Maltsiniotis
points out that Batanin's definition is the closest to Grothendieck's original idea. The topologists, notably Rezk and Bergner, have developped model
structures on simplicial categories and simplicial spaces, and Joyal gives a model structure on the restricted Kan complexes originally defined by
Boardman and Vogt in the 1960's. Cisinski and Maltsiniotis have built on
a somewhat different direction of "[[Pursuing Stacks|La poursuite des champs]]" which aims to
characterize the algebraic models for [[homotopy theory]].

My own work in this area is inspired by the phrase in "[[Pursuing Stacks|La poursuite des champs]]" where Grothendieck forsees [[infinity-stack|n-stacks]] as the natural coefficients for higher [[nonabelian cohomology]]. With Hirschowitz, we have developped the
notion of [[infinity-stack|n-stack]] based on Tamsamani's definition of [[n-category]], and proven
that the association $U \mapsto \{n-stacks on U\}$ is an $(n+1)$-stack.

The theory of "[[derived algebraic geometry]]" originated by Kontsevich, Kapranov and Ciocan-Fontanine is now cast by Toen, Vezzosi and [[Jacob Lurie|Lurie]]
in a foundational framework which relies on [[higher category theory|higher categories]] and [[infinity-stack|higher
stacks]] for glueing. In the future derived geometry should be a key ingredient in Hodge theory for 
higher [[nonabelian cohomology]], to be compared with
Katzarkov, Pantev and [[Bertrand Toen|Toen]]'s Hodge theory on the schematic homotopy
type. The latter is a higher categorical version of Grothendieck's reinterpretation
of [[Galois theory]], forseen in "[[Pursuing Stacks|La poursuite des champs]]", or really
its Tannakian counterpart. Grothendieck also mentionned, somewhat cryptically, a potential application to stratified spaces. The respective theses of
Treumann and Dupont go in this direction by using exit-path n-categories to classify constructible complexes of sheaves.

Up-to-the-minute developments include [Hopkins and Lurie's proof](http://golem.ph.utexas.edu/category/2006/09/wirth_and_stasheff_on_homotopy.html) of a part of the [[generalized tangle hypothesis|Baez-Dolan system of conjectures ]] relating higher categories to
[[TQFT|topological]] [[quantum field theory]]. And [[derived algebraic geometry]] permits
us to imagine a local notion of descent as was explained to me by [[David Ben-Zvi]]: using the derived non-transverse intersections, Schlessinger-[[Jim Stasheff|Stasheff]]-
Deligne-Goldman-Millson theory should be viewed as descent for the inclusion of a [[point]] into a local formal space, with the neighborhood intersection being the [[geometric infinity-function theory|derived loop space of Ben-Zvi and Nadler]]. 

