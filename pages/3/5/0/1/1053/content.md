## Idea ##

Unlike traditional logics, which deal with the truth of
propositions, linear logic is often described as dealing
with the availability of resources.  A proposition, if it is
true, remains true no matter how we use that fact in proving
other propositions.  By contrast, in using a resource $A$ to
make available a resource $B$, $A$ itself may be consumed or
otherwise modified.  Linear logic deals with this by
restricting our ability to duplicate or discard resources
freely.  For example, we have

$$\text{have cake}\vdash\text{eat cake}$$

from which we can prove

$$\text{have cake},\text{have cake}\vdash \text{have cake}
\wedge \text{eat cake}$$

which by left contraction (duplication of inputs) in classical logic yields

$$\text{have cake}\vdash\text{have cake}\wedge\text{eat cake}$$

Linear logic would disallow the contraction step and treat
$\text{have cake},\text{have cake}\vdash A$ as explicitly
meaning that _two_ slices of cake yield $A$.  Disallowing contraction then corresponds to the fact that we can't turn one slice of cake into two (more's the pity), so you can\'t have your cake and eat it too.

+--{: .query}
Lynn, I can\'t believe that you shied away from the punchline!  ---Toby

[[Finn Lawler]]: (Who's Lynn?)  I thought I'd be subtle, but maybe I was a bit too subtle!

_Toby_:  Sorry: Finn!  You weren\'t so subtle that I didn\'t get it, obviously; we just have different styles of humour, I guess.
=--

Linear logic was introduced in \[1\].  Although it is
usually presented in terms of inference rules, it was
apparently discovered by Girard while studying [coherent
spaces](http://en.wikipedia.org/wiki/Coherent_space) (not
the topological kind).

## Discussion ##

Probably the best way to explain LL to a category theorist
is to say that its models are
[[*-autonomous categories]] with extra
structure (see \[2\]).

Firstly, there is a monoidal 'tensor' connective
$A \otimes B$.  [[negation|Negation]] $A^\bot$ is modelled by the duality
involution $(-)^*$, while linear implication $A\multimap B$
corresponds to the internal hom, which can be defined as
$(A\otimes B^\bot)^\bot$.  There is a [[de Morgan duality|De Morgan dual]] of the
tensor called 'par', with 
$A \parr B = (A^\bot\otimes B^\bot)^\bot$.  Tensor and par are the
'multiplicative' connectives, which roughly speaking represent the
parallel availability of resources. 

+--{: .query}
[[Mike Shulman|Mike]]: I've usually seen $(-)^\bot$ for the linear negation; did you choose $(-)^*$ just to emphasize the connection with  $*$-autonomous categories?

[[Finn Lawler|Finn]]: Well, $(-)^*$ above is the duality involution, really -- I haven't quite got to the syntax yet.  But, yes, that's what I mean.

What I might do is move this basic stuff to the $*$-autonomous category page and make this page more about syntax.

_Finn_: I've created [[*-autonomous category]] and
changed the above to refer to the syntax of LL.

_Eric_: Hi! Technical note on n-Lab. Jacques recently implemented redirects for us. I've added redirects for <nowiki>[[*-autonomous category]] and [[*-autonomous categories]]. From now on, these will point to [[star-autonomous category]]. Just FYI. Hope it makes life a little easier for you. Now you can avoid typing things like $*$-[[star-autonomous category|autonomous categories]].</nowiki>

_Toby_:  Actually, I write things like '$*$-[[star-autonomous category|autonomus category]]' and even '$2$-[[2-category|category]]' quite deliberately, to maintain the typographical distinction between text mode and math mode.  I can see the argument for the other side, of course; what would really be nice is iTeX in wiki links (at least on the left side of a pipe).
=--

The 'additive' connectives $\&$ and $\oplus$, which
correspond in another way to traditional conjunction and
disjunction, are modelled as usual by [[product]]s and
[[coproduct]]s.  Seely notes \[2\] that products are sufficient, as $*$-autonomy then guarantees the existence of coproducts; that is, they are also linked by [[de Morgan duality]].

LL recaptures the notion of a resource that can be discarded
or copied arbitrarily by the use of the modal operator $!$:
$!A$ denotes an '$A$-factory', a resource that can produce
zero or more $A$s on demand.  It is modelled using a comonad
$!$ on the underlying $*$-autonomous category that is
(symmetric) monoidal, in the sense that there is an
isomorphism $!A\otimes!B \cong !(A\times B)$.  Since every
$A$ is canonically a symmetric $\times$-comonoid, $!A$ is
then a symmetric $\otimes$-comonoid.

An LL sequent
$$A_1,\ldots,A_n \vdash B_1,\ldots,B_m$$
is interpreted as a morphism
$$ \otimes_i A_i \to \parr_j B_j $$
The comonoid structure on $!A$ then yields the weakening
$$ \Gamma\otimes !A \to \Gamma \otimes I \to \Gamma$$
and contraction
$$ \Gamma\otimes !A \to \Gamma \otimes !A \otimes !A $$
maps.  The corresponding rules are interpreted by
precomposing the interpretation of a sequent with one of
these maps.

The (co)Kleisli category of $!$ is [[cartesian closed category|cartesian closed]], and
the product there coincides with the product in the base
category.  The exponential (unsurprisingly for a Kleisli
category) is $B^A \cong !A\multimap B$.


## References ##

1. Girard, Jean-Yves, 'Linear logic'.  _Theoretical Computer
   Science_ 50:1, 1987.

2. Seely, R. A. G., 'Linear logic, $*$-autonomous categories
   and cofree coalgebras', _Contemporary Mathematics_ 92,
   1989.  Available at
   <http://www.math.mcgill.ca/rags/nets/llsac.ps.gz>.

3. The [article](https://secure.wikimedia.org/wikipedia/en/wiki/Linear_logic) on the English Wikipedia has good summaries of the meanings of the logical operators and of the commonly studied fragments.