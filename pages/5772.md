
# The max-plus algebra and min-plus algebra
* table of contents
{: toc}

## Definitions

The __max-plus algebra__, or __tropical semiring__, is the [[rig]] based on the set of real numbers extended by $-\infty$ (the [[upper reals]]), with addition $x \oplus y = max(x,y)$ and multiplication $x \otimes y = x + y$.
Similarly, the __min-plus algebra__, or __rig of costs__, is the [[rig]] based on the set of real numbers extended by $\infty$ (the [[lower reals]]), with addition $x \oplus y = min(x,y)$ and multiplication $x \otimes y = x + y$.  The two rigs are isomorphic, with an [[isomorphism]] (either way) given by $x \mapsto -x$; the difference is just a matter of the desired perspective.


## Applications

The max-plus algebra is an [[idempotent semiring]] and [[dioid]] that is used in the modelling of timed systems.  Typically in a simple example, the completion time of a production system will be given by a system of equations that have 'max' occurring in them. (The next process in a system cannot start until all its component parts have been themselves completed.) The use of the max-plus notation completely linearises many systems.

The min-plus algebra may be used to draw an analogy between the use of [[action form|action]] in [[classical mechanics|classical]] vs [[quantum mechanics|quantum]] systems.  While the latter involves a [[sum of histories|sum of a multiplicative action over classical trajectories]], the former involves a [[least action principle|minimisation of an additive action over classical trajectories]].  There is a similar analogy between [[statics]] and [[statistical mechanics]].


## References

* [[Stéphane Gaubert]], [Introduction aux Syst&#232;mes Dynamiques &#224; &#201;v&#233;nements Discrets](http://amadeus.inria.fr/gaubert/PAPERS/POLY12-02-1999.pdf)

* [[Stéphane Gaubert]], _Methods and Applications of $(max,+)$ Linear Algebra_ [Report 3088](https://hal.inria.fr/inria-00073603/document), January 1997, INRIA.

* [[John Baez]] & [[David Corfield]], [Changing the rig](http://math.ucr.edu/home/baez/corfield/2006/05/changing-rig.html)


## Resources

There are several research groups, world wide, with research in this area and with good websites, including simulation, and calculational, tools. One way into the network of these sites is [here](http://www-rocq.inria.fr/MaxplusOrg/).


[[!redirects max-plus algebra]]
[[!redirects min-plus algebra]]
[[!redirects tropical semiring]]
[[!redirects rig of costs]]
