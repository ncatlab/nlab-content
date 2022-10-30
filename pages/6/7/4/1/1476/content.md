![a pic](http://math.ucr.edu/home/baez/centipede.jpg)

**Centipede mathematics**  is where you take a mathematical concept and see how many parts you can strip away while still having it function properly.  Steven Krantz has attributed this term to Antoni Zygmund.
From _[Mathematical Apocrypha Redux](http://books.google.com/books?id=LMC5UeaStKwC&pg=PA6&lpg=PA6&dq=%22centipede+mathematics%22&source=bl&ots=aivICIZzMU&sig=2rMkg3u6tMhjQyfI-C46BZThiyk&hl=en&ei=kF46Ss_vC4yMsgPb0JD-Bg&sa=X&oi=book_result&ct=result&resnum=9)_: 'You take a centipede and pull off ninety-nine of its legs and see what it can do.'  (We do not recommend doing this to an actual centipede, unless it is a [land-mine destroying robot](http://www.washingtonpost.com/wp-dyn/content/article/2007/05/05/AR2007050501009.html?hpid=topnews).)

For example, you can start with the concept of [[abelian group]] and try removing some things:
* remove commutativity to get [[group]]s;
* then remove inverses to get [[monoid]]s;
* or remove associativity instead of inverses to get [[loop(algebra)|loops]];
* etc.

What still works?  Abelian groups form an [[abelian category]], while groups only form a [[semi-abelian category]], so [[cohomology]] gets more complicated (see [[nonabelian cohomology]]) but still makes sense.  Monoid [[representation]]s (say on [[vector space]]s) make as much sense as group representations, but loop representations are not apparently meaningful.  (But like nonabelian cohomology, maybe somebody will make sense of them some day.)  Describing homomorphisms and presentations of monoids takes a little more care than for groups, while the na&#239;ve definitions continue to work for loops.  Sometimes things actually work better; [[group object]]s make sense only in a [[cartesian monoidal category]], while [[monoid object]]s make sense in any [[monoidal category]].  By seeing what are the salient features for making sense of things like cohomology and representation theory, we also see that we can generalise these, not by simply removing clauses from the definition of group, but by reworking the concept into such things as [[category|categories]] or [[quantum group]]s.

Centipede mathematics in the context of [[foundations]] is often called __reverse mathematics__.  Here we remove axioms from [[set theory]] (or some other form of foundations) and consider what theorems can still be proved, which can be proved if reformulated into (obviously) classically equivalent forms, and which are lost entirely (ideally provably so).  On the Lab, some of us like to do this for [[constructive mathematics]], but it is also important for [[internalization]].  (Mainstream reverse mathematics has more to do with [[predicative mathematics]] than with either of these.)

Like '[[general abstract nonsense]]', the term 'centipede mathematics' can vary from tongue-in-cheek to derogatory.  Certainly there is little value in proving isolated theorems like 'Hemidemisemicontinous functions are Leibniz-integrable.' (both terms here are made up, to avoid insulting the creators of any real-life useless theorems) when one never really needs to integrate such general functions in such a restrictive way.  But sometimes thinking about what is really necessary points the way to really fruitful generalisations; like every judgement in mathematics, good taste is required.

+-- {: .query}
The term 'centipede mathematics' is new to me, but its practice is surely of great antiquity. The binomial theorem (tear off the leg that says that the exponent has to be a natural number) is a good example. A related notion is the importance of good notation and the importance of overloading, aka abuse of language, to establish useful analogies. ---Gavin Wraith
=--