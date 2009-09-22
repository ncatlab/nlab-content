{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

_Diffeological spaces_ are a  kind of [[generalized smooth spaces]], namely [[concrete sheaf|concrete]] [[smooth spaces]].


Diffeological spaces were originally described by J.M. Souriau in 1980.  They have subsequently been developed by [Patrick Iglesias-Zemmour](http://www.umpa.ens-lyon.fr/~iglesias/) who is writing a book on the subject.

+-- {: mynumdef #DiffSp}
###### Definition
Let $Diff$ denote the [[site]] whose objects are open subsets of Euclidean spaces and whose morphisms are $C^\infty$-maps.

A _diffeological space_ is a pair $(X,\mathcal{D})$ where $X$ is a set and $\mathcal{D}$ is a [[sheaf]] on $Diff$ that is a subsheaf of the sheaf $U \mapsto X^{|U|}$.

A morphism of diffeological spaces is a map of the underlying sets which defines a natural transformation on the sheafs.
=--

A diffeological space is an example of a [[concrete sheaf]] on a [[concrete site]] and as such is covered by Baez and Hoffnung in [0807.1704](http://arxiv.org/abs/0807.1704).

The concreteness condition on the sheaf is a reiteration of the fact that a diffeological space is a subsheaf of the sheaf $U \mapsto X^{|U|}$.  In this way, one does not have to explicitly mention the underlying set $X$ as it is determined by the sheaf on the one-point open subset of $\mathbb{R}^0$.


# References #

* [Groupes diff\'erentiels](http://www.ams.org/mathscinet-getitem?mr=607688)

* Patrick Iglesias-Zemmour,
_Diffeology_
([web](http://math.huji.ac.il/~piz/Site/The%20Book/The%20Book.html), [pdf](http://math.huji.ac.il/~piz/documents/Diffeology.pdf))

The thesis

* Patrick Iglesias-Zemmour, _Fibrations diff&#233;ologie et Homotopie_,  PhD thesis [pdf](http://math.huji.ac.il/~piz/documents/TheseEtatPI.pdf)

contains some useful material that hasn't yet made it into the book.

* John C. Baez, Alexander E. Hoffnung, _Convenient Categories of Smooth Spaces_ ([arXiv](http://arxiv.org/abs/0807.1704))

[[!redirects diffeological spaces]]