
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _QED project_ was a project -- or at least a manifesto for a project, see [below](TheQED) -- for the formalization of large parts of [[mathematics]] ([[formal proof]]) in formal language supported by [[proof assistants]].

* [The QED Project Webpage](http://mizar.org/qed/)

While as a project this seems to have died out around 1996, the idea of the manifesto itself is still pertinent and waiting for its implementation (see also [Wiedijk 07](#Wiedijk07)).

Notice that since then the issues discussed in ([Wiedijk 07](#Wiedijk07)) may appear in a different light in view of developments in [[homotopy type theory]] ("univalent foundations for mathematics").

## The QED manifesto
 {#TheQED}

The following is taken literally from _[The QED Manifesto](ftp://mizar.uwb.edu.pl/pub/qed/manifesto)_.



> The development of mathematics toward greater precision has led, as is well known, to the formalization of large tracts of it, so that one can prove any theorem using nothing but a few mechanical rules. -- [[Kurt Gödel]]

> If civilization continues to advance, in the next two thousand years the overwhelming novelty in human thought will be the dominance of mathematical understanding.  -- [[Alfred North Whitehead]]



### 1 What Is the QED Project and Why Is It Important?

QED is the very tentative title of a project to build a computer
system that effectively represents all important mathematical
knowledge and techniques.  The QED system will conform to the highest
standards of mathematical rigor, including the use of strict formality
in the internal representation of knowledge and the use of mechanical
methods to check proofs of the correctness of all entries in the
system.

The QED project will be a major scientific undertaking requiring the
cooperation and effort of hundreds of deep mathematical minds,
considerable ingenuity by many computer scientists, and broad support
and leadership from research agencies. In the interest of enlisting a
wide community of collaborators and supporters, we now offer reasons
that the QED project should be undertaken.


First, the increase of mathematical knowledge during the last two
hundred years has made the knowledge, let alone understanding, of all,
or even of the most important, mathematical results something beyond the
capacity of any human.  For example, few mathematicians, if any, will
ever understand the entirety of the recently settled structure of
simple finite groups or the proof of the four color theorem.
Remarkably, however, the creation of mathematical logic and the
advance of computing technology have also provided the means for
building a computing system that represents all important mathematical
knowledge in an entirely rigorous and mechanically usable fashion.
The QED system we imagine will provide a means by which mathematicians
and scientists can scan the entirety of mathematical knowledge for
relevant results and, using tools of the QED system, build upon such
results with reliability and confidence but without the need for
minute comprehension of the details or even the ultimate foundations
of the parts of the system upon which they build.  Note that the
approach will almost surely be an incremental one: the most important
and applicable results will likely become available before the more
obscure and purely theoretical ones are tackled, thus leading to a
useful system in the relatively near term.


Second, the development of high technology is an endeavor of fabulously
increasing mathematical complexity.  The internal documentation of the next
generation of microprocessor chips may run, we have heard, to thousands of
pages.  The specification of a major new industrial system, such as a
fly-by-wire airliner or an autonomous undersea mining operation, is likely to
be even an order of magnitude greater in complexity, not the least reason being
that such a system would perhaps include dozens of microprocessors.  We believe
that an industrial designer will be able to take parts of the QED system and
use them to build reliable formal mathematical models of not only a new
industrial system but even the interaction of that system with a formalization
of the external world.  We believe that such large mathematical models will
provide a key principle for the construction of systems substantially more
complex than those of today, with no loss but rather an increase in
reliability.  As such models become increasingly complex, it will be a major
benefit to have them available in stable, rigorous, public form for use by
many.  The QED system will be a key component of systems for verifying and
even synthesizing computing systems, both hardware and software.


The third motivation for the QED project is education.  Nothing is more
important than mathematics education to the creation of infrastructure for
technology-based economic growth.  The development of mathematical ability is
notoriously dependent upon `doing' rather than upon `being told' or
`remembering'.  The QED system will provide, via such techniques as interactive
proof checking algorithms and an endless variety of mathematical results at all
levels, an opportunity for the one-on-one presenting, checking, and debugging
of mathematical technique, which it is so expensive to provide by the method of
one trained mathematician in dialogue with one student.  QED can provide an
engaging and non-threatening framework for the carrying out of proofs by
students, in the same spirit as a long-standing program of Suppes at Stanford
for example.  Students will be able to get a deeper understanding of
mathematics by seeing better the role that lemmas play in proofs and by seeing
which kinds of manipulations are valid in which kinds of structures.  Today few
students get a grasp of mathematics at a detailed level, but via
experimentation with a computerized laboratory, that number will increase.  In
fact, students can be used (eagerly, we think) to contribute to the development
of the body of definitions and proved theorems in QED.  Let also us make the
observation that the relationship of QED to education may be seen in the
following broad context: with increasing technology available, governments will
look not only to cut costs of education but will increasingly turn to make
education and its delivery more cost-effective and beneficial for the state and
the individual.


Fourth, although it is not a practical motivation, nevertheless
perhaps the foremost motivation for the QED project is cultural.
Mathematics is arguably the foremost creation of the human mind.  The
QED system will be an object of significant cultural character,
demonstrably and physically expressing the staggering depth and power
of mathematics.  Like the great pyramids, the effort required
(especially early on) may be great; but the rewards can be even more
staggering than this effort.  Mathematics is one of the most basic
things that unites all people, and helps illuminate some of the most
fundamental truths of nature, even of being itself.  In the last one
hundred years, many traditional cultural values of our civilization
have taken a severe beating, and the advance of science has received
no small blame for this beating.  The QED system will provide a
beautiful and compelling monument to the fundamental reality of truth.
It will thus provide some antidote to the degenerative effects of
cultural relativism and nihilism.  In providing motivations for
things, one runs the danger of an infinite regression.  In the end, we
take some things as inherently valuable in themselves.  We believe
that the construction, use, and even contemplation of the QED system
will be one of these, over and above the practical values of such a
system.  In support of this line of thought, let us cite Aristotle,
the Philosopher, the Father of Logic, `That which is proper to each
thing is by nature best and most pleasant for each thing; for man,
therefore, the life according to reason is best and pleasantest, since
reason more than anything else is man.'  We speculate that this
cultural motivation may be the foremost motivation for the QED
project.  Sheer aesthetic beauty is a major, perhaps the major, force
in the motivation of mathematicians, so it may be that such a
cultural, aesthetic motivation will be the key motivation inciting
mathematicians to participate.


Fifth, the QED system may help preserve mathematics from corruption.
We must remember that mathematics essentially disappeared from Western
civilization once, during the dark ages.  Could it happen again?  We
must also remember how unprecedented in the history of mathematics is
the clarity, even perfection, that developed in this century in regard
to the idea of formal proof, and the foundation of essentially the
entirety of known mathematics upon set theory.  One can easily imagine
corrupting forces that could undermine these achievements.  For
example, one might suspect that there is already a trend towards
believing some recent "theorems" in physics because they offer some
predictive power rather than that they have any meaning, much less
rigorous proof, with a possible erosion in established standards of
rigor.  The QED system could offer an antidote to any such tendency.
The standard, impartial answer to the question `Has it been proved?'
could become `Has it been checked by the QED system?'.  Such a
mechanical proof checker could provide answers immune to pressures of
emotion, fashion, and politics.


Sixth, the `noise level' of published mathematics is too high.  It
has been estimated that something between 50 and 100 thousand
mathematical papers are published per year.  Nobody knows for sure
how many contain errors or how many are repetitions, but some
pessimists claim the number of both is high.  QED can help to reduce
the level of noise, both by helping to find errors and by helping to
support computer searches for duplication.


Seventh, QED can help to make mathematics more coherent.  There are
similar techniques used in various fields of mathematics, a fact that
category theory has exploited very well.  It is quite natural for
formalizers to generalize definitions and propositions because it can
make their work much easier.


Eighth, by its insistence upon formalization, the QED project will
add to the body of explicitly formulated mathematics.  There is
mathematical knowledge that is neither taught in classes nor
published in monographs.  It is below what mathematicians call
"folklore," which is explicitly formulated.  Let us call this lower
level of unformulated knowledge "mathlore".  In formalization
efforts, we must formalize everything, and that includes mathlore
lemmas.


Ninth, the QED project will help improve the low level of
self-consciousness in mathematics.  Good mathematicians understand
trends and connections in their field.  The QED project will enable
mathematicians to analyze, perhaps statistically, the whole structure
of the mathematics, to discover new trends, to forecast developments
and so on.

## Related projects

* [[Xena project]]

* [[UniMath project]]

* [[ForMath project]]


## Related entries

* [[formal proof]]

## References

* _The QED Manifesto_ in _Automated Deduction - CADE 12_, Springer-Verlag, Lecture Notes in Artificial Intelligence, Vol. 814, pp. 238-251, 1994. ([web](ftp://mizar.uwb.edu.pl/pub/qed/manifesto))

* [Wikipedia article](http://en.wikipedia.org/wiki/QED_manifesto)

* {#Wiedijk07} [[Freek Wiedijk]], _The QED Manifesto Revisited_, 2007 ([pdf](http://mizar.org/trybulec65/8.pdf))

[[!redirects The QED project]]