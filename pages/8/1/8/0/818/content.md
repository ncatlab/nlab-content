This page is intended as a gathering place for unanswered mathematical queries.  It is particularly intended for those queries on a topic that are most likely to be answerable by an expert from a slightly different area than that of the immediate subject.  Such a person might not look at the original page and so not realise that there is a query there that they can answer.  Think of this as the virtual equivalent of having an equation on the board in your office where passers-by can glance at it and say "Oh, that looks awfully like Kipling's theory of Armadillos.  In fact, I think that the Proposition of the Painted Jaguar would solve your problem there."

Try to make the questions concise; a link to the original page should be included for extra background.

+--{: .query}
_Mike_: what is the procedure when answering a question here?  I presume it should be answered on the original page, but at what point does it get removed from this page?  Perhaps one should insert a note here that at least one answer has been given, and let the original asker remove the question from this page if they think it has been fully answered?

_Andrew_: I think that that is an excellent idea.  I certainly don't see any reason to have a record of these questions (beyond what is forced by being on a wiki).  I also think that it should be primarily up to the questioner to remove the question.

Maybe the page should be a little more structured with "New Questions", "Open Questions", "Partially Answered Questions", and "Answered, 'but just seeing if anyone else has anything to say' Questions".  But maybe first we should see how useful this page is before spending too much time on it.

(though it's already proved its worth for me!)
=--

## Questions ##

### The most abstract way to say "Fr&#246;licher space"? ###

From [[Froelicher space|Frölicher spaces]]: I want to discuss the following type of "thing": one starts with a category and takes triples $(C,F,c)$ where $C$ is a presheaf, $F$ is a copresheaf, and $c$ is a natural transformation to the $Hom$ functor (composition).  [[Urs Schreiber|Urs]] suggested looking at this in one of the comparative smootheology threads.  This is what I would like to call a "generalised space".  Is it known by some name already?  Is there some literature on this?  I would also like to consider (full) subcategories where there is some extra condition, the most obvious being that $C$ and $F$ satisfy the Isbell duality condition, but there are others.  This generalises the notion of the category of sheaves somewhat.  Is this known and/or studied somewhere?

[[Urs Schreiber|Urs]]: maybe if we formulate this as much as possible within $V$-[[enriched category theory]] it rings a bell with something in somebody. 

So for $V$ a symmetric closed monoidal category, for $S$ a $V$-enriched category, we are looking for the natural home of diagrams of the form

$$
  In(-) \otimes Out(-) \to S(-,-)
  :
  S^{op} \otimes S \to V
$$

for $V$-functors $In : S^{op} \to V$ and $Out : S \to V$.


### How to handle size issues in this context? ###

From [[Froelicher space|Frölicher spaces]]: When considering functor categories such as the above, there's clearly some size issues.  What's the "standard" way to avoid this?  Is it to insist that the original category have a small skeleton?

_Mike_: Yes, you almost certainly want it to be essentially small (see my comment at [[Froelicher space]]).


### How to detect morphisms from a concrete category? ###

From [[Froelicher space|Frölicher spaces]]: I want to consider the case of a concrete category and a (maybe full) subcategory which can detect which set-morphisms come from the original category.  A bit like the idea that one can detect which set maps are smooth maps between, say, manifolds by testing with smooth maps from $R$.

_Mike_: Perhaps "concretely dense" or "relatively dense?"  (See my comment at [[Froelicher space]])


category: meta
