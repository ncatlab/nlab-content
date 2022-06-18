[[!redirects HoTT Mini-Course]]
#Contents#
* table of contents
{:toc}

## HoTT Mini-Course at CMU ##
### Marc Bezem, Spring Semester 2016 ###

####Place and Time####
* Baker Hall 152
* Monday and Wednesday 13:30 - 16:30
* Exercises 13:30 - 15:00
* Lectures 15:00 -16:30
* We continue during the Spring break
* No lectures 23,28,30 March

####Resources####
* [The HoTT book](http://www.homotopytypetheory.org/book)
* Slides [[DTUA.pdf:file]]
* Slides [[HoTT.pdf:file]]

####Recordings and Homework####
* 2 March [video](https://www.youtube.com/watch?v=G4quix5Z51g)
  1. Prove that Eq_A on slide 2 of DTUA.pdf is an equivalence relation for all types A. 
  1. Untyped $\lambda$-calculus: maximally reduce (+ 1 2) and (* 3 0).
  1. Maximally reduce (+ 0 x) and (+ x 0). Is there a difference?
* 7 March [video](https://www.youtube.com/watch?v=DY5DzmIfVDo)
  1. Let = be Eq_A (slide 2 of DTUA.pdf). Try to prove the groupoid laws on slide 9 of DTUA.pdf (not all are provable, which shows that Leibniz equality is too weak to give types groupoid structure).
  1. Same task as previous, but now with Eq_A from slide 8 of DTUA.pdf (now they are
all provable).
  1. Read the Introduction of the HoTT book.
* 9 March [video](https://www.youtube.com/watch?v=Xhu3VVyIdH8)
  1. Find the term _ac_ on slide 21 of HoTT.pdf.
  1. Do Exercise 1.1 and 1.2 of the HoTT book.
  1. Let _Bool_ be the inductive type with two nullary constructors _false: Bool_ and _true: Bool_. Formulate formation, introduction, elimination and computation rules for Bool. 
  1. Find a term _t: U ->  U -> Bool -> U_ such that _t A B true = A_ and _t A B false = B_, for all _A,B: U_.
* 14 March [video](https://www.youtube.com/watch?v=Jzb8mXXz7xI)
  1. Do as many exercises from Chapter 1 of the HoTT book as you can. You can find some solutions in the [HoTT library](https://github.com/HoTT/HoTT/blob/master/contrib/HoTTBookExercises.v)
and by running `make exercise_solutions.pdf` after forking the [HoTT book](https://github.com/HoTT/book) on Github.
* 16 March (no video due to connectivity problems)
  1. As to Exercises 1.7 and 1.14, give the $\Sigma$-type $S$ and prove for all $a:A$ that $(a,refl_a) =_S (x,p)$ for all $x:A, p: a =_A x$.
  1. Do Exercises 2.1 - 2.4 in the HoTT book.
* 21 March [video](https://www.youtube.com/watch?v=Cd8rHVnSCwg)
  1. Do Exercises 2.5 - 2.10 in the HoTT book.
* 4 April
  1. Do as many of the remaining exercises from Chapter 2 of the HoTT book as you can.
* 6 April
  1. Investigate the action on paths of the function $f : \Sigma A B \to \Sigma A' B'$ given by $g: A\to A'$ and $h: \Pi x:A. B x \to B' (g x)$ in the following canonical way: $f(a,b) = (g a,h a b)$. (Hint: this is a dependent version of a simpler result for Cartesian products).
  2. Prove that for all $x,y : *$ we have $(x=_*y) \simeq \mathbf{1}$.

## See also

* [[CMU HoTT Research Group's local activities]]

category: people
