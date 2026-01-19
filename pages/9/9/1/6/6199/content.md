
#Contents#
* table of contents
{:toc}


## Idea

A __dynamical system__ is a [[space]] $X$ (often a bare [[set]] or a [[manifold]]) together with a "law of motion" expressed by the [[action]] of a [[monoid]] $A$:

$$
  A \times X \longrightarrow X
  \,.
$$

To model continuous [[time]]-evolution one may take $A = (\mathbb{R}, +)$ to be the additive [[group]] of [[real numbers]]. 

For discrete time evolution $A = (\mathbb{Z}, +)$ is the additive group of [[integers]] (or just the monoid $(\mathbb{N}, +)$ of [[natural numbers]]). In this case the law of motion is often given by an [[initial value problem]] for a [[differential equation]] "of evolution type".

In this case, the dynamical system is equivalently a space $X$ equipped with an [[automorphism]] (this being the action of the [[unit element]] in $\mathbb{Z}$, sometimes called the "shift").
  

Sometimes the evolution is only partially defined; this is most often in dynamical systems induced by evolution differential equations which do not necessarily have existence of solutions for arbitrary large time, or the dynamical system is defined only for nonnegative time. 

The definition evidently makes sense quite generally [[internalization|internal to]] various ambient [[categories]]: For instance one considers complex dynamics, [[algebraic dynamics]], arithmetic dynamics and so on. 

Dynamical systems are used to describe not only physical motions but also the behaviour of parameters of various systems, e.g. in sociological, financial, weather and other models.  

## Related concepts

* [[categorical systems theory]]

* [[zeta function of a dynamical system]]

* [[arithmetic topology]]

* [[cohomology of dynamical systems]]

* [[chaos]]

* [[Furstenberg-Zimmer structure theorem]]

* [[shifts]]

* [[control theory]]

## References

### General

* Boris Hasselblatt, Anatole Katok, _Handbook of dynamical systems_, [contents](http://www.math.psu.edu/katok_a/handbook.html)

See also

* Wikipedia [dynamical system](http://en.wikipedia.org/wiki/Dynamical_system), [autonomous system](http://en.wikipedia.org/wiki/Autonomous_system_%28mathematics%29)

### Category-theoretic formulations

Discussion of dynamical systems in terms of [[category theory]] (see also at *[[categorical systems theory]]*):

* [[William Lawvere]], [_Functorial Remarks on the General Concept of Chaos_](http://www.ima.umn.edu/preprints/Functional-Remarks-General-Concept-Chaos), IMA reprint 87, 1984 ([pdf](http://www.ima.umn.edu/sites/default/files/87s.pdf))

* George Dimitrov, Fabian Haiden, [[Ludmil Katzarkov]], [[Maxim Kontsevich]], _Dynamical systems and categories_, &lbrack;[arxiv/1307.8418](http://arxiv.org/abs/1307.8418)&rbrack;

* Mike Behrisch, Sebastian Kerkhoff, Reinhard Pöschel, Friedrich Martin Schneider, Stefan Siegmund, _Dynamical systems in categories_. Applied Categorical Structures 25, 2017. ([link](https://tud.qucosa.de/api/qucosa%3A27340/attachment/ATT-0/))

* [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *Flows: cocyclic and almost cocyclic*, Theory Appl. Categories **25** 18 (2010) 490–507 &lbrack;[tac:25-18](http://www.tac.mta.ca/tac/volumes/25/18/25-18abs.html)&rbrack;


* [[Patrick Schultz]], [[David I. Spivak]], [[Christina Vasilakopoulou]], *Dynamical Systems and Sheaves*, Appl Categor Struct **28** (2020) 1–57 &lbrack;[arXiv:1609.08086](https://arxiv.org/abs/1609.08086), [doi:10.1007/s10485-019-09565-x](https://doi.org/10.1007/s10485-019-09565-x)&rbrack;

* [[David Jaz Myers]], *Double Categories of Open Dynamical Systems*, EPTCS **333** (2021) 154-167 &lbrack;[arXiv:2005.05956](https://arxiv.org/abs/2005.05956), [doi:10.4204/EPTCS.333.11](https://doi.org/10.4204/EPTCS.333.11)&rbrack;


Monograph:

* {#Myers} [[David Jaz Myers]], *Categorical systems theory*, book project &lbrack;[github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book), [pdf](http://davidjaz.com/Papers/DynamicalBook.pdf)&rbrack;

Exposition:

* [[David Jaz Myers]], *[Categorical systems theory](https://topos.institute/blog/2021/11/categorical-systems-theory/)*, [[Topos Institute]] [Blog](https://topos.institute/blog/) (Nov 2021)

* [[David Jaz Myers]], *Double Categories of Dynamical Systems* (2020) &lbrack;[pdf](http://davidjaz.com/Talks/DJM_Dyn2020.pdf)&rbrack;

* [[David Jaz Myers]], *A general definition of open dynamical systems*, talk at *MIT Category Theory Seminar* (2020) &lbrack;video:[YT](https://youtu.be/8T-Km3taNko)&rbrack;

[[!redirects dynamical systems]]
