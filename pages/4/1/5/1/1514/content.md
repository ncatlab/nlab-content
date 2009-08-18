
Ours is the age whose central fundamental theoretical physics question is: 

>_What is [[quantum field theory]]_? 

A closely related question is:

> _What is the path integral_ ? 

After its conception by Feynman in the middle of the 20th century It was notably Edward Witten's achievement in the late 20th century to make clear the vast potential for fundamental physics and pure math underlying the concept of the quantum field theoretic path integral.

And yet, among all the aspects of QFT, the notion of the path integral is the one that has resisted attempts at formalization the most.

While [[FQFT|functorial quantum field theory]] is the formalization of the properties that the _locality_ and the _sewing law_ of the path integral is demanded to have -- whatever the path integral is, it is a process that in the end yields a [[functor]] on a [[(infinity,n)-category of cobordisms]] -- by itself, this sheds no light on what that procedure called "path integration" or "path integral quantization" is.

The single major insight into the right [[higher category theory|higher categorical]] formalization of the path integral is probably the idea indicated in

* Dan Freed

  * _Quantum groups from path integrals_ ([arXiv](http://xxx.lanl.gov/abs/q-alg/9501025))

  * _Higher algebraic structures and quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

which says that

* it is wrong to think of the _action functional_ that the path integral integrates over as just a _function_: it is a higher categorical object;

* accordingly, the path integral is not something that just controls the numbers or linear maps assigned by a $d$-dimensional [[quantum field theory]] in dimension $d$: also the assignment to higher codimensions is to be regarded as part of the path integral;

  * notably: the fact that quantum mechanics assigns a (Hilbert) space of sections of a vector bundle to codimension 1 is to be regarded as due to a _summing operation_ in the sense of the path integral, too: the space of sections of a vector bundle is the continuum equivalent of the direct sum of its fibers


More recently, one sees attempts to formalize this observation of Freed's, notably in the context of the [[cobordism hypothesis]]:

* [[geometric infinity-function theory]] is used to compute at least something like a path integral in codimension 1 and 2 in the context of [[sigma-model]] QFT;

* something not unsimilar is [[schreiber:Nonabelian cocycles and their sigma model QFTs|here]], the underlying idea of which for a toy example is spelled out at

  *[[exercise in groupoidification - the path integral]];

* and something similar or is indicated in section 3 and section 6 of

  * Freed, Hopkins, Lurie, Teleman, _Topological QFT from Compact Lie Groups_ ([arXiv](http://arxiv.org/abs/0905.0731))

based on material (on categories of "families") in _[[On the Classification of Topological Field Theories]]_ . 


