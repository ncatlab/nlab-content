#Idea#

_Enriched homotopy theory_ is about combining the notion of categories that model aspects of [[homotopy theory]] (such as [[homotopical category|homotopical categories]] and [[model category|model categories]]) with the ideas and tools of [[enriched category theory]].

On the one hand, enriched category theory is already used in many places in ordinary homotopy theory, usually for the particular case of enrichment over [[topological space]]s or [[simplicial set]]s.  Just as an ordinary category has a _set_ of morphisms between any two objects, an ordinary homotopy theory has a _space_ of morphisms between any two objects (including morphisms, homotopies between them, higher homotopies, and so on).  From a [[higher category theory|higher categorical]] viewpoint, a homotopy theory is a presentation of an $(\infty,1)$-[[(infinity,1)-category|category]], and $(\infty,1)$-categories can be viewed as categories enriched (perhaps weakly) over $\infty$-groupoids (that is, spaces).  Many of the model categories used in homotopy theory come with natural topological or simplicial enrichments that make them better-behaved and easier to work with.  The enrichment can also be used in a detailed study of homotopy coherence, without necessarily needing model-categorical tools.  See [[homotopy coherent category theory]].

On the other hand, instead of using enriched category theory as a tool to understand ordinary homotopy theory, one can look for a common generalization of them both.  Now we take the point of view that spaces (or $\infty$-groupoids, or simplicial sets) are the higher-categorical counterpart of _sets_, and look for an analogue of the passage from Set-enriched categories to $V$-enriched categories that starts from ordinary (space-enriched) homotopy theories and ends up at $V$-enriched homotopy theories.  Note that now $V$ need not be any space-like category, so that $V$-enriched homotopy theories need not be very similar to $(\infty,1)$-categories.  One use of this approach is to get at a sort of higher categories with noninvertible $k$-cells for $k\gt 1$, by taking $V$ to be [[folk model structure|categories]], 2-categories, and so on (perhaps [[Trimble n-category|iteratively]]).  But $V$ could also be [[chain complex]]es, or $W$-categories for some other $W$, or [[spectrum|spectra]], or some other category with even less resemblance to "spaces."

Fortunately, both of these approaches can be handled by many of the same technical tools, including but not limited to:

* [[monoidal model category|Monoidal model categories]] and [[enriched model category|enriched model categories]].

* [[closed monoidal homotopical category|Closed monoidal homotopical categories]] and [[enriched homotopical category|enriched homotopical categories]].

* [[operad|Operads]] and $A_\infty$-[[A-infinity-category|categories]].
