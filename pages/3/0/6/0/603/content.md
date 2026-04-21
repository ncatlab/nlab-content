
\tableofcontents

## Idea

[[Nils Baas]] has been emphasizing for many years, in print and in private communication, the conviction that the usual  notions of [[n-category]], [[infinity-category]] [[omega-category]] in [[higher category theory]] are __not__ naturally suited for describing

* [[extended cobordisms]] such as appearing in 

  * the [[generalized tangle hypothesis|tangle hypothesis]]

  * in [[FQFT|extended quantum field theory]]

* hierarchical systems such as appearing in

  * complex systems;

  * biology.

The point is essentially that the _directedness_ of morphisms and --- related to that --- the binary notion of [[source]] and [[target]] in categories and higher categories are notions alien to these contexts, which in applications have to and are essentially removed again in a second step by adding extra structure and requiring further properties, such as various monoidal structures and dualities, which allow to change the direction of morphisms, to collect objects together, etc.

In contrast to that, Baas pointed out that more naturally the above situations are thought of from the beginning in terms of hierarchies of what he calls _bonds_, where, quite generally, a bond is an object equipped with information of how a collection of sub-bonds sits inside it, _bound by the bond_.

A sketch of a generic such a situation of hierarchical bonds is a diagram 

$$
  \array{
     \beta_2 &&=&& \beta_2 && \beta_4
     \\
     \downarrow && && \downarrow & \swarrow
     \\
     b_1 &\to& B &\leftarrow& b_2
     \\
     \uparrow && \uparrow  && \uparrow 
     \\
     \beta_1 && b_3 && \beta_3
     \\
     && \uparrow
     \\
     && \beta_5
  }
$$

where a bond $B$ binds sub-bonds $b_1, b_2$ and $b_3$ which in turn bind sub-bonds $\beta_i$.

For instance $B$ might be an [[extended cobordism]] with three boundary components $b_1, b_2, b_3$ which in turn have pieces of boundary components $\beta_i$.

\begin{remark}
The notion of replacing morphisms by _bonds_ is familiar and concretely realized at least in a hierarchy of depth 2 in the context of [[groupoidification]] and [[geometric function theory]], where morphisms are replaced by [[spans]]. Regarding these as [[cospans]] in the [[opposite category]] produces diagrams like the above sketch of a generic bond system. 

Accordingly, the notion of [[multispan]] and [[multi-cospan]] may come close to exhibiting some crucial aspects of the idea that motivated the concept of hyperstructures.
\end{remark}


## References

Nils Baas has made, in print and in private communication, suggestions for a formalization of such systems of hierarchical bonds and coined the term __hyperstructures__ for these. Some references are

* [[Nils A. Baas]], _Higher Algebraic Structures and General Field Theories_ &lbrack;[arXiv:2111.11205](http://arxiv.org/abs/2111.11205)&rbrack;

* [[Nils A. Baas]], _A Mathematical Approach to the Hierarchical Structure of Languages_ &lbrack;[arXiv:1806.05551](http://arxiv.org/abs/1806.05551)&rbrack;

* [[Nils A. Baas]], _On the Mathematics of Higher Structures_ &lbrack;[arXiv:1805.11944](http://arxiv.org/abs/1805.11944)&rbrack;

* [[Nils A. Baas]], _On the Philosophy of Higher Structures_ &lbrack;[arXiv:1805.11943](http://arxiv.org/abs/1805.11943)&rbrack;

* Nils A. Baas, _On Higher Order Structures_, [arXiv:1509.00403](http://arxiv.org/abs/1509.00403) (2015), 15 pp.

* Nils A. Baas, _Higher order architecture of collections of objects_, International Journal of General Systems vol. 44 (1), pp. 55-75, 2015. [arXiv:1409.0344](http://arxiv.org/abs/1409.0344)

* Nils A. Baas, N.C. Seeman and A. Stacey, _Synthesising topological links_, Journal of Mathematical Chemistry, vol. 53, pp. 183-199, 2015.

* Nils A. Baas, D.V. Fedorov, A.S. Jensen, K. Riisager, A.G. Volosniev and N.T. Zinner, _Higher-Order Brunnian Structures and Possible Physical Realizations_, Physics of Atomic Nuclei, vol. 77(3), pp. 336-343, 2014. [arXiv:1205.0746](http://arxiv.org/abs/1205.0746)

* Nils A. Baas, _New states of matter suggested by new topological structures_, International Journal of General Systems, vol. 42 (2), pp. 137-169, 2012. [arXiv:1012.2698](http://arxiv.org/abs/1012.2698)

* Nils A. Baas, _On structure and organization: an organizing principle_, International Journal of General Systems, vol. 42 (2), pp. 170-196, 2012. [arXiv:1201.6228](http://arxiv.org/abs/1201.6228)

* Nils A. Baas and N.C. Seeman, _On the chemical synthesis of new topological structures_, Journal of Mathematical Chemistry, vol. 50 (1), pp. 220-232, 2012.

* Nils A. Baas, _New structures in complex systems_, The European Physical Journal Special Topics, vol. 178 (1), pp. 25-44, 2010.

* Nils A. Baas, _Hyperstructures, Topology and Datasets_, Axiomathes, vol. 19 (3), pp. 281-295, 2009.

* Nils A. Baas, _Hyperstructures as Abstract Matter_, Advances in Complex Systems, vol. 9 (3), pp. 157-182, 2006.

* Nils A. Baas, A. Ehresmann and J.-P. Vanbremeersch, _Hyperstructures and Memory Evolutive Systems_, International Journal of General Systems, vol. 33 (5), pp. 553-568, 2004.

* Nils A. Baas, _Higher order cognitive structures and processes_. In _Toward a Science of Consciousness_, S.R. Hameroff, A.W.Kaszniak and A.C.Scott (editors), MIT Press, pp. 633-648, 1996.

* Nils A. Baas, _Hyper-structures as a tool in nanotechnology_, Nanobiology, vol. 3 (1), pp. 49-60, 1994.

For a discussion of the idea of [[multispans]] as a formalization of hyperstructures, see the thread commencing from [this comment](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html#c013165) by [[Urs Schreiber]], and its possible application to the description of extended cobordisms and the [[generalized tangle hypothesis]] in [this comment](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021486).



[[!redirects hyperstructural]]
[[!redirects hyperstructures]]