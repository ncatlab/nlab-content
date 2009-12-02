A [[category]] $C$ is __locally cartesian__ if each of its [[slice categories]] $C/x$ is a [[cartesian monoidal category]], meaning that $C/x$ has all finite [[products]].  Another way to say this is that $C$ has all finite [[fibred products]] or equivalently that $C$ has all [[pullbacks]].


## Discusssion ##

Here is some discussion on terminology from [[cartesian monad]]:

+--{.query}
I would call a category with all pullbacks 'locally cartesian'.  Shouldn\'t a cartesian category at least have a terminal object?  Would a terminal object make any difference here?  &#8212;[[Toby Bartels|Toby]]

I think you're right about the standard terminology.
Both Tom Leinster and Jurgen Koslowski ([pdf](http://www.tac.mta.ca/tac/volumes/14/7/14-07.pdf))
use the terminology above.
I'm not sure how we want to resolve this here.
I'll think about it, and look at the standard references, and fix the terminology on this page if nobody else does first.  -Patrick

How is this?  -Patrick

_[[Mike Shulman|Mike]]_: The [[Elephant]] definitely uses "cartesian" to mean "all finite limits."  However, I'm not sure how universal that is; I think at least in the past, some people have used "cartesian" to refer only to finite _products_.  I'm sure that a [[cartesian object]] in a 2-category has been defined to be one such that $A\to A\times A$ and $A\to 1$ have right adjoints.  Also the notion of "cartesian bicategory" refers only to finite products (and extra stuff too).  And [[cartesian monoidal category]] and [[cartesian closed category]] certainly only means finite products.  On the other hand, of course as you say, in this context "cartesian monads" only refer to pullbacks, not terminal objects and hence not products.  There is also the use of "cartesian square" to mean a pullback square, which generalizes to "cartesian morphism" in a [[Grothendieck fibration|fibration]].

_Toby_: Yes, despite the historical justification that Johnstone gives in the Elephant, I\'d stick with (what I understand to be) the usual terminology: 'cartesian' means finite products.  Then 'locally cartesian' means each slice is cartesian, hence pullbacks.  Now the term for all finite limits is 'cartesian locally cartesian' (and topologists, at least, do say things like 'connected locally connected'), but that mouthful just tells us that the time has come to say 'left exact' or 'finitely complete' instead.

_Mike_: I assume you mean that 'cartesian' means finite _products_.  "Finitely complete" is also an reasonable term meaning "having finite limits."

_Toby_: Yes, of course, fixed.
=--