#Idea#

...

#Definition#

The **cardinality** of a [[groupoid]] $X$ is

$$|X| = \sum_{[x]} \frac{1}{|Aut(x)|}$$

where the sum is over isomorphism classes of objects of $X$ and $|Aut(x)|$ is the cardinality of the automorphism group of an object $x$ in $X$. If this sum diverges, we say $|X| = \infty$. If the sum converges, we say $X$ is **tame**.

#Examples#

* Let $E$ be the groupoid of finite sets and bijections.

$$|E| = \sum_{n\in \mathbb{N}} \frac{1}{|S_n|} = \sum_{n\in \mathbb{N}} \frac{1}{n!} = e.$$

#References#

* John C. Baez, Alexander E. Hoffnung, and Christopher D. Walker, _Groupoidification Made Easy_ ([web](http://math.ucr.edu/home/baez/groupoidification.pdf), [blog](http://golem.ph.utexas.edu/category/2008/12/groupoidification_made_easy.html))

* John C. Baez, James Dolan, _From Finite Sets to Feynman Diagrams_ ([arXiv](http://arxiv.org/abs/math.QA/0004133))

* Tom Leinster, _The Euler characteristic of a category_ ( [arXiv](http://arxiv.org/abs/math.CT/0610260), [TWF](http://math.ucr.edu/home/baez/week244.html), [blog](http://golem.ph.utexas.edu/category/2007/02/this_weeks_finds_in_mathematic_5.html), [blog](http://golem.ph.utexas.edu/category/2006/10/euler_characteristic_of_a_cate.html))