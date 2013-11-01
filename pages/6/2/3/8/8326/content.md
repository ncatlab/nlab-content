
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

This page collects resources related to


* [[Hegel]]

  _Wissenschaft der Logik_

  ([web version](http://www.marxists.org/reference/archive/hegel/works/hl/), [Wikipedia entry](http://en.wikipedia.org/wiki/Science_of_Logic))


on [[logic]].

#Contents#
* table of contents
{:toc}

## Survey
 {#Survey}

> With Hegel you're getting what seems to us today a curious package. The whole dynamic (or 'dialectic') of the unfolding of the Logik is prior to any actual thinking, realised in concrete humans. In fact, the world, and that part of it which is human thought, is the Idea (or Spirit) realising itself. I say 'curious', but in a way I'm hearing echoes of this in things Urs is suggesting, as though the universe worked itself out according to type theory. For Hegel one isn't to be a Kantian, where what one theorises about the universe is just how the universe is taken up by the human understanding, with the further idea that this will be limited in certain ways, e.g., no access to the thing-in-itself. For Hegel, the human mind itself is part of the universe and as such part of the unfolding of the Idea/Spirit. $[\cdots]$ It's a dizzying picture which tends either to delight or revolt people. $[$ See at _[[absolute idealism]]_ $]$ ([Corfield](http://nforum.mathforge.org/discussion/4117/the-wiki-history-of-the-universe/?Focus=34343#Comment_34343))


## Topics

### On being and becoming
 {#OnBeingAndBecoming}

from ([EPSBOI](#EPSBOI))*:

* Sec. 86 Pure [[being]] constitutes the beginning, because it is pure thought as well as the undetermined, simple immediate, and the first beginning cannot be anything mediated and further determined.

* 87 Now this pure being is a pure abstraction and thus the absolutely negative which, when likewise taken immediately, is nothing.

* 88 Conversely, nothing, as this immediate, self-same [category], is likewise the same as being. The truth of being as well as of nothing is therefore the unity of both; this unity is [[becoming]].


Remark: A proposal for a formalization of _[[being]]_ and _[[becoming]]_ is later given by [[Bill Lawvere]] in terms of the notion of _[[cohesive topos]]_, see at _[[Some Thoughts on the Future of Category Theory]]_.

### On cohesion / attraction

* 395 Attraction is in this way the moment of continuity in quantity.

attraction $\simeq$ [[cohesion]]


### On discreteness and continuum

* 397 In continuity, therefore, magnitude immediately possesses the moment of discreteness &#8212; repulsion, as now a moment in quantity. 

continuous object $X$ possesses moment 
of [[discrete object|discreteness]]= [[flat modality]] $\flat X$

* 398 Quantity is the unity of these moments of continuity and discreteness,

the [[flat modality]] [[counit of a comonad|co-unit]]:

$$
  quantity
  \;\colon\;
  \array{ 
    \flat X &\longrightarrow& X
    \\
    discreteness && continuity
  } 
$$

Notice that we may regard a [[morphism]] as the collection of its [[homotopy fibers]] and that the homotopy fiber of $\flat X \to X$ is the [de Rham coefficient object](cohesive+(infinity,1)-topos+--+structures#deRhamCohomology) $\flat_{dR} X$.

* 400 Mathematics, on the other hand, rejects a metaphysics which would make time consist of points of time; space in general &#8212; or in the first place the line &#8212; consist of points of space; the plane, of lines; and total space of planes. It allows no validity to such discontinuous ones. Even though, for instance, in determining the magnitude of a plane, it represents it as the sum of infinitely many lines, this discreteness counts only as a momentary representation, and the sublation of the discreteness is already implied in the infinite plurality of the lines, since the space which they are supposed to constitute is after all bounded.

The [[continuum]].


> Diese Antinomie besteht allein, darin da&#223; die Diskretion eben so sehr als die Kontinuit&#228;t behauptet werden mu&#223;. Die einseitige Behauptung der Diskretion giebt das unendliche oder absolute Getheiltseyn, somit ein Untheilbares zum Princip; die einseitige Behauptung der Kontinuit&#228;t dagegen die unendliche Theilbarkeit.


### On space, time, matter

* 432 Space, time, matter, and so forth are continuous magnitudes 


### On identity

On [[identity]].

* **903** All things are different; or: there are no two things like each other.

Reminiscent of [[identity types]] in [[intensional type theory]].



## Related entries

* [[being]], [[becoming]]

## References


* _Enzyklop&#228;die der philosophischen Wissenschaften im Grundrisse_ (1830) W. Bonsiepen und H.-C. Lucas (eds.) in _Gesammelte Werke_, Rheinisch-Westf&#228;lischen Akademie der Wissenschaften, and xx. Hamburg: Felix Meiner, 1992 ( Bonsiepen/Lucas 1992).

  [Encyclopedia of the Philosophical Sciences in Basic Outline, Part I: Science of Logic](http://ndpr.nd.edu/news/24778-encyclopedia-of-the-philosophical-sciences-in-basic-outline-part-i-science-of-logic/)
 {#EPSBOI}

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_