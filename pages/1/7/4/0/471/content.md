
In a [[closed monoidal homotopical category]] with a notion of [[homotopy]] in terms of [[path object]]s, an _interval object_ $I$ should be an object which

* represents the [[cylinder functor]] (if any) in that for any object $B$ the tensor product $B \otimes I$ is indeed a cyclinder object

* co-represents the [[path object]] in that $[I,B]$ is indeed a path object of $B$.


#Discussion#

This discussion started at [[homotopy]], but it really deserves a place of its own where it can eventually materialize into a definition.

_[[Urs Schreiber|Urs]]:_ Let me chat a bit about what I am looking for here. It seems very useful to have a good notion of what it means in a context like a [[closed category|closed]] [[category of fibrant objects]] to say that _[[path object]]s are compatibly corepresented_.

By this should be meant: there exists an object $I$ such that

* for $B$ any other object, $[I,B]$ is a path object;

* and such that $I$ has some structure and property which makes it "nice".

In something I am thinking about the main point of $I$ being _nice_ is that it can model compositon: it must be possible to put two intervals end-to-end and get an interval of twice the length. In some private notes [[schreiber:Nonabelian homotopical cohomology and fiber bundles|here]] I suggest that:

a "category with interval object" should be

* a [[closed monoidal homotopical category]]

* with a compatible structure of a [[category of fibrant objects]]

* and equipped with an **internal co-categoy** on $\sigma, \tau : pt \to I$ for $I$ the _interval object_;

* such that $I$ co-represents path objects, in that for all objects $B$, $[I,B]$ is a path object for $B$.

I think there are a bunch of obvious examples: all familiar models of higher groupoids (Kan complexes, $\omega$-groupoids etc.) with the interval object being the obvious cellular interval $\{a \stackrel{\simeq}{\to} c\}$.

I also describe one class of applications which I think this is needed/useful for: recall how Kenneth Brown in section 4 of his article on [[category of fibrant objects]] (see theorems recalled there and reference given there) describes fiber bundles in the abstract homotopy theory of a _pointed_ category of fibrant objects. This is pretty restrictive. In order to describe things like $\infty$-vector bundles in an context of [[enriched homotopy theory]] one must drop this assumption of the ambient category being pointed. The structure of it being a category with an interval object is just the necessary extra structure to still allow to talk of (principal and associated) fiber bundles in abstract homotopy theory. It seems.

Comments are very welcome.

+--{.query}
_[[Todd Trimble|Todd]]_: The original "Trimblean" definition for weak $n$-categories (I called them "flabby" $n$-categories) crucially used the fact that in a nice category $Top$, we have a highly nontrivial $Top$-operad where the components have the form $\hom_{Top}(I, I^{\vee n})$, where $X \vee Y$ here denotes the cospan composite of two bipointed spaces (each seen as a cospan from the one-point space to itself), and the hom here is the internal hom between cospans. 

My comment is that the only thing that stops one from generalizing this to general (monoidal closed) model categories is that "usually" $I$ doesn't seem to be "nice" in your sense here, and so one doesn't get an interesting (nontrivial) operad when my machine is applied to the interval object. But I'm generally on the lookout for this sort of thing, and would be very interested in hearing from others if they have interesting examples of this.

[[Urs Schreiber]]: Thanks, Todd. I should have listed the examples I had in mind: I was thinking about 
[[strict omega-category]] here, where the 1st [[oriental]]
$G_1 = I = \{a \to b\}$ should naturally be an internal 
co-category, where co-composition is the functor which
sends $a \to b$ to the composite $a_1 \to (b_1 = a_2) \to a_2$.

More generally, there are, I think $n$ different co-category
structures on the standard $n$-globe, with co-source and
co-target given by the two injections of the standard
$(k \lt n)$-globe. 

The composition operations in the internal hom 
$\omega$-category $hom(C,D)$ in strict $\omega$-categories can,  I'd think, then be thought of as coming from the image of these co-categories under
$Hom(C\otimes -, D)$.

A description of what I just tried to say with the illuminating diagrams is on [p. 35 here](http://ncatlab.org/schreiber/files/nacq.pdf#page=35).
Hope I got this right. Please let me know if I am mixed up.

_[[Todd Trimble|Todd]]_: It seems to me there might be some trickiness about which hom you want. The thing you're proposing sounds like it would work to describe the hom for $\omega$-Cat as a cartesian closed category, but I'm not sure off the bat how it will play out with respect to the Crans-Gray monoidal biclosed structure. I'd have to think about it more carefully, but there's something a little "thin" about the strict co-category structure on say the category 2 (as an interval co-category in $Cat$) which makes me wonder.

(After an email from Urs:) I think Urs is right after all -- this should work fine for either monoidal structure. 
=--