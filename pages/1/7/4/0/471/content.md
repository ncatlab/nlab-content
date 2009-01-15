#Idea#

The structure of a category $C$ with _interval object_ is supposed to be the right structure to ensure 

1. that there is an object $I$ in $C$ such that for every object $B$ of $C$ the [[closed monoidal category|internal hom object]] $[I,B]$ exists and behaves like a [[path object]] for $B$;

2. that there is a notion of composition on these path objects which induces on $[I,B]$ a structure of a (higher) category internal to $C$.

The following definition is tentative.

#Definition#

A _category with interval object_ is

* a $V$-[[enriched homotopical category]];

* equipped with a co-span 
$$
  \array{
    && I
    \\
    & {}^\sigma \nearrow && \nwarrow^{\tau}
    \\
    pt &&&& pt
  }
$$
in $V$, with $I$ called the **interval** object
(the notation $I$ is not (necessrily) referring to the tensor unit object!)

such that

* all compositions
$$
  \array{
    && I^{\vee n}
    \\
    & {}^\sigma \nearrow && \nwarrow^{\tau}
    \\
    pt &&&& pt
  }
$$
of $n \in \mathbb{N}$ copies of the cospan $I$ with itself by pushout over adjacent legs exist in $V$;

* all internal hom $V$-objects of cospans 
 $hom_{Cospans(V)}(I,I^{\vee n})$ are _contractible_ in that they are
 weakly equivalent to the point:
 $$ 
   hom(I,I^{\vee n}) \stackrel{\simeq}{\to} pt
   \,.
 $$


#Induced structure#

The above data induces the following further structure.

The collection of objects $\{ hom(I,I^{\vee n})\}_{n \in \mathbb{N}}$ in a category with interval object naturally comes equipped with the structure of an [[operad]]: the tautological operad on the object $I$ in the monoidal category of cospans from $pt$ to $pt$. 

This induces in turn for all objects $B \in C$ on the object $[I,B]$ the structure of an operad, which is naturally interpreted as an internal [[A-infinity category]] structure on

$$
  (B_0 := [pt,B]) 
  \stackrel{s := [\sigma,B]}{\leftarrow}  
  [I,B] 
  \stackrel{t := [\tau, B]}{\to} (B_0 := [pt,B])
  \,.  
$$

This internal $A_\infty$-category is denoted 

$$
  \Pi_1(B)
$$

and interpreted as the [[fundamental groupoid]] or rather, in general, the [[fundamental category]] of the object $B$ with respect to the interval object $I$ -- all internal to $C$.

Moreover, by iterating this process as described at [[Trimble's notion of weak n-category]] one obtains on $B$ the structure of a [[Trimble's notion of weak n-category|Trimblean]] weak [[omega-category]] and indeed a functor

$$
  \Pi_\omega : C_0 \to Trible \omega Cat
  \,.
$$

(is this last statement correct as given?)

#Remarks#

* The condition that all $hom(I, I^{\vee n})$ are contractible is the _coherence condition_ on all composition operations. 

* The above is _not_ demanding that the interval object $I$ itself is is weakly equivalent to the point. If it is, then $\Pi_1(B)$ is indeed a [[fundamental groupoid]]. If it is not, then $\Pi_1(B)$ may just be a [[fundamental category]].

* If $C_0$ has a notion of [[path object]] one may consider imposing the condition that $[I,B]$ is a path object of $B$ for all $B$. Similarly, if $C_0$ has a [[cylinder functor]], one may consider imposing the condition that it is given by $-\otimes I$.

#Examples#

* For $V = C = Top$ with its standard model structure the standard topological closed interval  $I := [0,1]$ with $pt \stackrel{\sigma, \tau}{\to}$ the maps to 0 and 1, respectively. This is the case describe in detail at [[Trimble's definition of weak n-category]].

* For $V = C = \omega Cat$ the category of [[strict omega-category|strict omega-categories]] the first [[oriental]], the 1-[[globe]] $I = \{a \to b\}$ is an interval object. In this strict case in fact all hom objects are already equal to the point $hom(I, I^{\vee n}) = pt$ and 
$$
  (B = [pt,B]) 
  \stackrel{s := [\sigma,B]}{\leftarrow}  
  [I,B] 
  \stackrel{t := [\tau, B]}{\to} (B = [pt,B])
$$
is a strict co-category internal to $\omega$Cat. 
In this case, for $B$ any $\omega$-category 
the $A_\infty$-category $\Pi_1(B)$ is just an ordinary category, namely the 1-category obtained from truncation of $B$. Similarly, probably $\Pi_\omega(B) = B$ in this case.

(Todd, please check this last statement!)



#Discussion#

We had originally started discussing the notion of interval objects at [[homotopy]] but then moved it to this entry here. The above entry grew out of the following discussion we had, together with discussion at [[Trimble's notion of weak n-category]].

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

_[[Urs Schreiber|Urs]]_: Also by email, Todd points out that of course more generally, we want our interval objects to form internal co-categories only _up to coherent homotopy_, because otherwise the example of $G_1$ in strict $\omega$-categories is likely to be essentially the only good example.  We want internal _homotopy co-categories_.

I need to learn more about how one would go about systematically defining concepts internal to a model category up to homotopy. What are the available tools for handling higher coherent homotopies in an arbitrary model category?

My understanding is that Todd is going to write an entry on the Trimble definition of $\infty$-categories, and that this  issue appears there in some guise. So maybe I'll just wait for Todd's entry to appear...
=--