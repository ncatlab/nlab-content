#Idea#

The term "$\omega$-category" is in the existing literature usually meant to refer to precisely those [[globular set|globular]] [[infinity-category|infinity-categories]] which are _strict_.



This means that 

 1. all composition operations are strictly associative;

 2. all composition operations strictly commute with all others (strict [[exchange law]]s);

 3. all identity $k$-morphisms are strict identies under all compositons.

#Definition#

An **$\omega$-category** $C$ [[internalization|internal to]]  $Sets$ is 

* a [[globular set]] 
$$
  C :=
  (\cdots
  C_3 \stackrel{\to}{\to}
  C_2 \stackrel{\to}{\to}
  C_1 \stackrel{\to}{\to}
  C_0
 )
$$

* together with the structure of a [[category]] on 
all
$(  C_{k} \stackrel{\to}{\to} C_l )$ for all $k \gt l$;

* such that 
$(  C_{k} \stackrel{\to}{\to}
  C_{l} \stackrel{\to}{\to} C_m )$ for all $k \gt l \gt m$;
is a [[strict 2-category]].

Similarly for an $\omega$-category [[internalization|internal to]]  another ambient category $A$.

The category $\omega Cat(A)$ of $\omega$-categories [[internalization|internal to]] $A$ has $\omega$-categories
as its objects and morphism og the underlying globular objects respecting all the above extra structure as morphisms.

##Remarks##

* The last condition in the above definition says that all pairs of composition operations satisfy the [[exchange law]].

* $\omega$-Categories can also be understood as the directed limit of the sequence of iterated [[enriched category theory|enrichements]]
$$
  (0 Cat = Set)
  \hookrightarrow
  (1 Cat = Set-Cat)
  \hookrightarrow
  (2 Cat = Cat-Cat)
  \hookrightarrow
  \left(3 Cat = (2Cat)-Cat = (Cat-Cat)-Cat\right)
  \hookrightarrow
  \cdots
  \,.
$$

* Terminology on $\omega$-categories varies. We here follow section 2.2 of Sjoerd Crans: [Pasting presentations for $\omega$-categories](http://crans.fol.nl/papers/thpp.html), where it says 

  * _Street allowed $\omega$-categories to have infinite dimensional cells. Steiner has the extra condition that every cell has to be finite dimensional, and called them $\infty$-categories, following Brown and Higgins. I will use Steiner's approach here since that's the one that reflects the notion of higher dimensional homotopies closest, but I will nonethless call them $\omega$-categoires, and I agree with Verity's suggestion to call the other ones $\omega^+$-categories._



* [[Simpson's conjecture]], a statement about [[semi-strict infinity-category|semi-strictness]], states that every weak $\infty$-category should be equivalent to an $\infty$-category in which strictness conditions 1. and 2. hold, but not 3.


#Literature#

$\omega$-categories were introduced, together with [[oriental]]s, in 

* Ross Street, _The algebra of oriented simplices_,
J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).


A review of some of the theory in the context of some of the history is given in 

* Ross Street, _An Australian conspectus of higher categories_ ([pdf](http://www.math.mq.edu.au/~street/Minneapolis.pdf))

and also in

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

The theory of $\omega$-categories was further developed by Sjoerd Crans in parts 2 and 3 of his [thesis](http://crans.fol.nl/papers/comb.html)

* Sjord Crans, _Pasting presentations for $\omega$-categories_ ([link](http://crans.fol.nl/papers/thpp.html))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([link](http://crans.fol.nl/papers/thten.html))

See also the 

* [Introduction](http://crans.fol.nl/papers/thintro.ps.gz) 

to his thesis, in particular section I.3 "$\omega$-categories".


#Further resources#

* While creating this entry we had the following discussion about terminology:

+-- {: .query}

[[Toby Bartels]]: Who actually uses the language this way? If anything, it should be the reverse, as 'omega' is Greek (like 'bi', 'tri', and 'tetra') and 'infinity' is not.  

[[John Baez]]: For a long time, for most category theorists, the default meaning of '$n$-category' has been 'strict globular $n$-category' &#8212; especially since weak $n$-categories had not yet been defined (except for very low $n$).   So when Street invented '$\omega$-categories' in his paper on orientals, he meant 'globular strict $\infty$-categories'.  Now there are many definitions of 'weak $n$-category', terminology is in flux, and people like [[Tom Leinster]] and myself advocate a new system in which '$n$-category' means 'some sort of possibly weak $n$-category' &#8212; at least until one has defined it more precisely in a specific context.  It is still true that most papers referring to $\omega$-categories mean 'globular strict $\infty$-categories'.

We may want to discuss whether the $n$Lab adopts traditional terminology, or takes this historic opportunity to play Bourbaki and choose consistent terminology for the future (while still explaining the traditional terms, or course).  In any event, globular strict $\omega$-categories are worth talking about, and that's what this page is about!

[[Toby Bartels]]: I agree with you and Tom about '$n$-category', and I agree that the strict globular case is worth talking about. I only question making a terminological distinction between '$\omega$-category' for the strict globular concept and '$\infty$-category' for the general weak case; (this seems to go against both the Greek-prefixes-for-the-weak-concept convention *and* the usual-name-for-the-weak-concept convention!). And I'm wondering if this distinction is established somewhere.

[[Urs Schreiber]]: I am not dogmatic about this, but I did not make this up, I think. I thought I followed the standard convention. 

I jumped on the $\omega$-category train after 

1. I learned about [Sjoerd Crans' work](http://crans.fol.nl/papers/comb.html) on $\omega$-categories from Todd. Sjoerd Crans uses the term "$\omega$-cvategory" for strict $\infty$-categories throughout;

and

2. after Mike Shulman pointed out that there is now an extension of the [[folk model structure]] to it, described by Lafont, M&#233;tayer and Worytkiewicz [here](http://arxiv.org/abs/0712.0617). They use the term "$\omega$-category" in this article and in all their other previous articles for strict $\infty$-catgeories.

Together with Ross Street's original work on $\omega$-categories this seems to say that _all_ the substantial work on the theory of strict $\infty$-categories uses the term "$\omega$-category" for them. 

I have added more references below, all of which use the term $\omega$-category exclusively for strict $\infty$-categories. Please have a look.

Finally, I thought that the terminology was actually a good idea: I was thinking of the "$\omega$" as indicating the (important) fact that $\omega$-categories are the directed limit of the iterated enrichment process

$$
  Cat \hookrightarrow
  2Cat = Cat-Cat
  \hookrightarrow
  2Cat = (Cat-Cat)-Cat
  \hookrightarrow
  3Cat = ((Cat-Cat)-Cat)-Cat
  \hookrightarrow 
  \cdots
  \,.
$$

[[Toby Bartels]]: Hey, you don\'t have to give me references that use '$\omega$-category' for the strict notion; I know all about that. What I want are references that use '$\infty$-category'! Keep in mind what John said that he and Tom propose above: that the usual term '$n$-category', although historically most used for the strict concept, should really be applied to the weak concept; you add the word 'strict' (or 'globular strict' to be more clear) if that\'s what you want. Maybe you\'re not folowing this &#8230; but then shouldn't you use the adjective 'weak' instead?

In other words: Who makes this *distinction* between '$\omega$-category' and '$\infty$-category'? (And secondarily, of course, is this a good way to do things?)

[[Urs Schreiber]]: All right, now I am confused about what I am being asked! :-)
I read you very first remark above -- "Who actually uses the language this way?" -- following the statement that "$\omega$-Categories are precisely those [[globular set|globular]] [[higher category theory|infinity-categories]] which are _strict_.
" as asking "Who says '$\omega$-category' for 'strict $\infty$-category'. "

But you maybe meant: "Who uses '$\infty$'-category to mean 'weak $\infty$-category'?"? The answer to that seems to be: pretty much everybody nowadays. I happen to have the following example in fron of me as we speak: To&#235;n, [Higher and derived stacks: a global overview](http://arxiv.org/abs/math.AG/0604504). See in particular on [p. 4](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=4) the first lines of section 2.2 and the footnote on that page.

This follows of course what seems to have become the "Lurie school". Jacob Lurie has introduced his own, slightly weird, convention, to say "$\infty$-category" for "weak $(\infty,1)$-category". 

It seems to me the upshot is:

* at least in more recent texts "$\infty$-category" is always meant to include the weak version

* no reference I know of uses "$\omega$-category" for anything but strict $\infty$-categories.

(If and when we have sorted this out, the essence of our discussion should be turned into content on the entry [[higher category theory]])

[[Toby Bartels]]: Who uses '$\omega$-category' for the weak notion? I know one reference: John Baez! (from whom I\'ve learned most of my terminology). The first use of '$\omega$-category' for the weak notion that I can find in TWF is [weak 100](http://math.ucr.edu/home/baez/week100.html); search for '&#969;' (second hit). Maybe it\'s just him (and presumably Tom, and of course some of his students like me). If the distinction between '$\omega$-category' and '$\infty$-category' is established, then I guess that we have to live with it. But I don\'t have to like it! ^_^

[[Urs Schreiber]]: You don't have to like it. And I don't really care as long as we can reduce the general confusion of terms. But one question: why would one say _$\omega$-category_ and not _$\infty$-category_ if one wants to refer to _weak_ $\infty$-categories. I mean, if the "$\omega$" does not indicate the degree of weakening, what then is it supposed to indicate in this context?

[[Toby Bartels]]: In general, '$\omega$' and '$\infty$' mean the same thing: infinity; that\'s what it means in this context too. It\'s kind of arbitrary that one would use one symbol instead of the other; I certainly don\'t think that Street (or whoever originally picked the name '$\omega$-category') meant anything special in picking the symbol '$\omega$', since after all the term '$n$-category' defaulted to the strict concept for them too (as it did for everybody at the time, I believe). In other words, the strictness was in the term '$n$-category', not in the symbol '$\omega$'. Somehow that symbol has acquired extra connotations, and accordingly the new term '$\infty$-category' has been invented, I\'m not sure how or why.

Also note that your directed limit above applies equally well to the weak case as long $2Cat$ etc are interpreted in a weak sense. So again, $\omega$ means infinity, which is independent of strictness.

[[Urs Schreiber]] says: Hm, in TWF 100 I see Batanin's title with "weak $\omega$-categories". Is there anyone saying just "$\omega$-category" to mean "weak $\infty$-category"??

[[Toby Bartels]]: Yes, John says that, just above that title. He states (earlier in TWF 100) his general philosophy (also given earlier in this query box) that one should use '$n$-category' for the general weak concept, then applies this later to casually refer to weak $\omega$-categories simply as '$\omega$-categories', then points to a reference on that subject, the paper by Batanin (which does *not* follow John\'s convention and so includes the adjective 'weak', thereby confirming that John meant the weak concept). And I like John\'s convention, so I\'ve used it too (not that I\'ve published anything), which is why it\'s now disconcerting to be told that now '$\omega$' *implies* strictness even when (following John\'s convention) '$n$-category' does not, so now I have to relearn all my language.

Which, in light of the references that use '$\infty$-category' for the weak concept, is apparently what I really will have to do. \(;_;\) \([crying emoticon](https://secure.wikimedia.org/wikipedia/en/wiki/List_of_common_emoticons#Simple_examples)\)

[[Urs Schreiber]] say: Okay, I have modified the first sentence in the entry a bit.

=--

Unfortunately, another discussion about terminology has begun...

+--{.query}

_[[Mike Shulman|Mike]]_: I don't want to reopen this can of worms, although I am just as sad as Toby.  Can I at least request that we at the nLab try to say "strict $\omega$-category" when that is what we mean, rather than just saying "$\omega$-category" and assuming that the reader knows that we mean the strict version?  In particular, since we have a page called [[strict 2-category]] rather than "2-category," it would seem only fair for this page to be called "strict omega-category," with the page "omega-category" containing links and pointing out the variations in terminology.  

_Urs_: I really don't want to come across as dogmatic here, but I am confused: if "$\omega$-category" is supposed to have precisely the same (vague) meaning as "$\infty$-category", why should we have the two different terms then in the first place?

_Mike_: No particular reason, except that we're already stuck with both of them.  I would be just as happy to use one exclusively, with adjectives.  (In particular, I wouldn't mind being able to use "(weak) $\omega$-category" for the weak version, to avoid confusion with things like $\infty$-pretoposes and Lurie's use of "$\infty$-category".)  I just get confused by trying to force them to have different, specific meanings, with no mnemonic to help me remember which is supposed to imply "weak" and which "strict" (except the "anti-mnemonic" that $\omega$, being Greek, implies strictness, while the prefixes "bi-" and "tri-", also Greek, imply weakness).  Especially since they have each already been used by different people with different meanings.  And especially if we are trying to make "$n$-category" not imply strictness (in the face of tradition), it seems inconsistent to insist that "$\omega$-category" does imply strictness.  I feel sure that there is far more literature using "2-category" to mean "strict 2-category" than there is using "$\omega$-category" to mean "strict $\omega$-category," so why should we feel bound by the latter but not the former?

=--
