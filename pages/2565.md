
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Information geometry aims to apply the techniques of [[differential geometry]] to [[statistics]]. Often it is useful to think of a family of probability distributions as a _statistical_ [[manifold]]. For example, normal [[Gaussian distribution]]s form a 2-[[dimension]]al manifold, parameterised by $(\mu, \sigma)$, mean and standard deviation. On such manifolds there are notions of [[Riemannian metric]], [[connection]], [[curvature]], and so on, of statistical relevance.

More precisely, 

> [[Kullback-Leibler information]], or [[relative entropy]], features as a measure of [[divergence]] (not quite a [[metric]], because it's asymmetric), and [[Fisher information]] takes the role of [[curvature]]. One useful aspect of information geometry is that it gives a means to prove results about statistical models, simply by considering them as well-behaved geometrical objects. For instance, it's basically a tautology to say that a [[manifold]] is not changing much in the vicinity of points of low curvature, and changing greatly near points of high curvature. Stated more precisely, and then translated back into probabilistic language, this becomes the [[Cramer-Rao inequality]], that the variance of a parameter estimator is at least the reciprocal of the [[Fisher information]]. ([Shalizi](#Shalizi))

Founders of the systematical theory are N. N. Chentsov and Shun-ichi [Amari](http://www.brain.riken.jp/labs/mns/amari/home-E.html).

## Definitions

For $X$ a [[measurable space]] let $S$ be (a subspace of) the space of probability [[measure]]s on $X$, equipped with the structure of a [[smooth manifold]].

The **Fisher metric** on $S$ is the [[Riemannian metric]] given on two [[vector field]]s $v,w \in T S$ by

$$
  g(v,w)_s := E_s( v(log s) w(log s))
  \,,
$$

where $E_s(\cdots)$ denotes the [[expectation value]] under the measure $s \in S$ of the function $x \mapsto  v(log s)_x w(log s)_x$ on $X$.

For instance ([Amari, Section 2.1](#AmariTextbook)).

## Related concepts

* [[entropy]]
* [[Fisher metric]]
* [[quantum information]]
* [[relative entropy]], also known as the Kullback-Leibler divergence

## References

See also [[Fisher metric]], where Fisher metric in other contexts and quantum generalizations are treated. See also [[quantum information]].

Textbooks providing the big picture

* Nihat Ay, Jürgen Jost, Hông Vân Lê, Lorenz Schwachhöfer, _Information geometry_, Ergeb. der Mathematik and ihrer Grenzgebiete 3. Folge, 64, Springer 2017
* Shun-ichi Amari, O. E. Barndorff-Nielsen, R. E. Kass, S. L. Lauritzen, and C. R. Rao, _Differential geometry in statistical inference_ ([project Euclid](http://projecteuclid.org/euclid.lnms/1215467056))
 {#AmariTextbook}
* Shun-ichi Amari, _Information geometry and its applications_, Applied Mathematical Sciences 194, Springer 2016
*  Shun-ichi Amari, Hiroshi Nagaoka, _Methods of information geometry_, Transactions of mathematical monographs; v. 191, American Mathematical Society, 2000. 

For a series of articles, see

* [[John Baez]], [Information Geometry](http://math.ucr.edu/home/baez/information/)


Lecture notes include

*  Shun-ichi Amari, MaxEnt 2007 [lecture](http://video.google.com/videoplay?docid=2175767568645553282#)
*  Shun-ichi Amari, ETVC08 [lecture](http://videolectures.net/etvc08_amari_igaia/).
*  Sanjoy Dasgupta, [lecture](http://videolectures.net/mlss05us_dasgupta_ig/).

See also

*  H&#244;ng V&#226;n L&#234;, Statistical manifolds are statistical models, Journal of Geometry 84(1-2), March 2006, pp. 83-93.


*  Blog [post](http://golem.ph.utexas.edu/category/2006/11/infinitedimensional_exponentia.html).

A brief introduction with more references is

* Cosma Shalizi, _Information geometry_ ([webpage](http://www.cscs.umich.edu/~crshalizi/notabene/info-geo.html))
 {#Shalizi}

Several people have noted an equivalence between statistic inference as parametric model selection and statistical mechanics on a statistical manifold, e.g., 

* [[Vijay Balasubramanian]], _Statistical Inference, Occam’s Razor and Statistical Mechanics on the Space of Probability Distributions_, Neural Comp.9(2)(1997) 349–368, ([arXiv:cond-mat/9601030](https://arxiv.org/abs/cond-mat/9601030)).

The interpretation of a [[quantum field theory]] as a probability distribution on the space of field configurations so as to allow the conversion of techniques from information geometry to analogous measures of proximity between QFTs is in

* [[Vijay Balasubramanian]], [[Jonathan Heckman]], Alexander Maloney, _Relative Entropy and Proximity of Quantum Field Theories_, ([arXiv:1410.6809](https://arxiv.org/abs/1410.6809))

A treatment of collective statistical inference as resulting in the partition function of a non-linear [[sigma model]] is in

* [[Jonathan Heckman]], _Statistical Inference and String Theory_, ([arXiv:1305.3621](https://arxiv.org/abs/1305.3621))

More in the context of [[quantum field theory]]:


* Johanna Erdmenger, Kevin T. Grosvenor, Ro Jefferson, _Information geometry in quantum field theory: lessons from simple examples_ ([arXiv:2001.02683](https://arxiv.org/abs/2001.02683))



