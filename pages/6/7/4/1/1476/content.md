[[!redirects centipede mathematics]]

# Contents 
* table of contents 
{:toc}

## Introduction 

Abstraction or generalization is a basic tactic in mathematics research. By formulating an argument or placing a concept in 'proper generality', one not only strengthens results and widens applicability, but one also perceives much more clearly what is truly at stake within the sphere of concepts where the mathematics takes place. 

Without too much of an exaggeration, one could say that the development of modern algebra generally, and categorical algebra in particular, has been driven by the need to extract the essence of mathematical structures and situate them within axiomatic frameworks of general type. This is certain true of such concepts as [[topos]], [[abelian category]], [[scheme]], [[cohomology theory]], and countless others. 

Finding the 'right' generality (as opposed to merely maximal generality) of concepts is a kind of dialectical process, in which generality in the strictly logical sense must be balanced against other considerations such as simplicity, ease of application, suggestiveness, aesthetics, etc. The result of such persistent conceptual polishing is often a theory that becomes concentrated in its well-chosen definitions, from which key summary results flow naturally. 

Occasionally throughout the history of mathematics (and physics, etc.), the drive to abstraction has met with suspicion. To some extent this may be a generational phenomenon, where shifting conceptual landscapes and pressure to relearn the foundations of a subject may meet with resistance from mathematicians long accustomed to older insights. There can also be justice in the charge that generality for the sake of generality is a sterile pursuit, and a typical counter-reaction is that further layers of abstraction should "prove themselves", e.g., by leading to solutions of venerable problems. 

## Styles of abstraction 


### Centipede mathematics 

<div style="float:left;margin:0 10px 10px 0;"><img src="http://math.ucr.edu/home/baez/centipede.jpg" alt="" width="208" height="150" /></div>

**Centipede mathematics**  is where you take an extant mathematical concept and see how many parts you can strip away without completely destroying its ability to function properly.  Steven Krantz has attributed this term to Antoni Zygmund.
From _[Mathematical Apocrypha Redux](http://books.google.com/books?id=LMC5UeaStKwC&pg=PA6&lpg=PA6&dq=%22centipede+mathematics%22&source=bl&ots=aivICIZzMU&sig=2rMkg3u6tMhjQyfI-C46BZThiyk&hl=en&ei=kF46Ss_vC4yMsgPb0JD-Bg&sa=X&oi=book_result&ct=result&resnum=9)_: 'You take a centipede and pull off ninety-nine of its legs and see what it can do.'  (We do not recommend doing this to an actual centipede, unless it is a [land-mine destroying robot](http://www.washingtonpost.com/wp-dyn/content/article/2007/05/05/AR2007050501009.html?hpid=topnews).)

For example, you can start with the concept of [[abelian group]] and try removing some things:

* remove commutativity to get [[groups]];
* then remove inverses to get [[monoids]];
* or remove associativity instead of inverses to get [[loop+(algebra)|loops]];
* etc (see [[group]] for more).

What still works?  Abelian groups form an [[abelian category]], while groups only form a [[semi-abelian category]], so [[cohomology]] gets more complicated (see [[nonabelian cohomology]]) but still makes sense.  Monoid [[representation|representations]] (say on [[vector space|vector spaces]]) make as much sense as group representations, but loop representations are not apparently meaningful.  (But like nonabelian cohomology, maybe somebody will make sense of them some day.)  Describing homomorphisms and presentations of monoids takes a little more care than for groups, while the na&#239;ve definitions continue to work for loops.  Sometimes things actually work better; [[group object|group objects]] make sense only in a [[cartesian monoidal category]], while [[monoid object|monoid objects]] make sense in any [[monoidal category]].  By seeing what are the salient features for making sense of things like cohomology and representation theory, we also see that we can generalise these, not by simply removing clauses from the definition of group, but by reworking the concept into such things as [[category|categories]] or [[quantum group|quantum groups]].

Centipede mathematics in the context of [[foundations]] is often called __[[reverse mathematics]]__.  Here we remove axioms from [[set theory]] (or some other form of foundations) and consider what theorems can still be proved, which can be proved if reformulated into (obviously) classically equivalent forms, and which are lost entirely (ideally provably so).  On the Lab, some of us like to do this for [[constructive mathematics]], but it is also important for [[internalization]].  (Mainstream reverse mathematics has more to do with [[predicative mathematics]] than with either of these and works with subsystems of [[higher-order arithmetic]].)

Like '[[general abstract nonsense]]', the term 'centipede mathematics' can vary from tongue-in-cheek to derogatory.  Certainly there is little value in proving isolated theorems like 'Hemidemisemicontinuous functions are Leibniz-integrable.' when one never really needs to integrate such general functions in such a restrictive way (both terms here are made up, to avoid insulting the creators of any real-life useless theorems).  But sometimes thinking about what is really necessary points the way to really fruitful generalisations; like every judgement in mathematics, good taste is required. 

## Illustrative quotes 

From [[Lawvere]], in [An interview with F. William Lawvere](#picado): 

> What is the primary tool for such summing up of the essence of ongoing 
mathematics?  Algebra!  Nodal points in the progress of this kind of research occur when, as in the case with the finite number of axioms for the metacategory of categories, all that we know so far can be expressed in a single sort of algebra.  I am proud to have participated with Eilenberg, Mac Lane, Freyd, and many others, in bringing about the contemporary awareness of Algebra as Category Theory. 

From [Miles Reid](#reid), p. 123: 

> Many students of the time could apparently not think of any higher ambition than &#201;tudier les EGAs. The study of category theory for its own sake (surely one of the most sterile of all intellectual pursuits) also dates from this time; Grothendieck himself can't necessarily be blamed for this, since his own use of categories was very successful in solving problems. 

From [[Tom Leinster]], referring to the quotation from Reid, [Leinster2010](#leinster): 

> I've become rather fond of that quotation, though not for the reason that Reid intended. 'Sterile' doesn't only mean infertile or unproductive. It's also what you want surgical instruments to be: clean, uncontaminated, disease-free. No one wants to be operated on with a dirty scalpel.

> I'm going to clarify that point, because I can hear a sarcastic voice saying 'oh, so you want to do category theory uncontaminated by real mathematics'. Category theory is at its best, I think, when it reflects what mathematicians actually do and shows how to do it better, when it functions as the [mathematics of mathematics](http://cheng.staff.shef.ac.uk/misc/4000.pdf). 

From [[Categories for the Working Mathematician]], p. 108: 

> One may speculate as to why the discovery of adjoint functors was so delayed. (...) Bourbaki just missed... Bourbaki's idea of universal construction was devised to be so general as to include more [than the problem of finding a left adjoint] ... [his] formulation lacks the symmetry of the adjunction problem ... and so missed a basic discovery; this discovery was left to a younger man, perhaps one less beholden to tradition or to fashion. Put differently, good general theory does not search for the maximum generality, but for the right generality. 

## Related entries 

* [[abstract general, concrete general and concrete particular]] 

* [[concrete structure]] 

## References 

* Jorge Picado, _An interview with F. William Lawvere_, ([pdf](http://www.mat.uc.pt/~picado/lawvere/interview.pdf)) 
 {#picado} 

* Miles Reid, _Undergraduate Algebraic Geometry_, available from [Reid's web page](https://homepages.warwick.ac.uk/staff/Miles.Reid/) as ([pdf](https://homepages.warwick.ac.uk/staff/Miles.Reid/MA4A5/UAG.pdf)) 
 {#reid} 

* Tom Leinster, _A Perspective on Higher Category Theory_, $n$-Category Caf&eacute; post (March 8, 2010), ([link](https://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html)) 
 {#leinster} 

* [[Saunders Mac Lane]], _Categories for the Working Mathematician_ ($2^{nd}$ edition), Springer Verlag New York, 1998. ([pdf](http://www.maths.ed.ac.uk/~aar/papers/maclanecat.pdf)) 


