The original entry [[omega-category]] suggested that [[omega-category]] is supposed to implicitly mean [[strict omega-category]]. 

After the following discussion, we renamed that entry to [[strict omega-category]].

***

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



_[[Mike Shulman|Mike]]_: I don't want to reopen this can of worms, although I am just as sad as Toby.  Can I at least request that we at the nLab try to say "strict $\omega$-category" when that is what we mean, rather than just saying "$\omega$-category" and assuming that the reader knows that we mean the strict version?  In particular, since we have a page called [[strict 2-category]] rather than "2-category," it would seem only fair for this page to be called "strict omega-category," with the page "omega-category" containing links and pointing out the variations in terminology.  

_Urs_: I really don't want to come across as dogmatic here, but I am confused: if "$\omega$-category" is supposed to have precisely the same (vague) meaning as "$\infty$-category", why should we have the two different terms then in the first place?

_Mike_: No particular reason, except that we're already stuck with both of them.  I would be just as happy to use one exclusively, with adjectives.  (In particular, I wouldn't mind being able to use "(weak) $\omega$-category" for the weak version, to avoid confusion with things like $\infty$-pretoposes and Lurie's use of "$\infty$-category".)  I just get confused by trying to force them to have different, specific meanings, with no mnemonic to help me remember which is supposed to imply "weak" and which "strict" (except the "anti-mnemonic" that $\omega$, being Greek, implies strictness, while the prefixes "bi-" and "tri-", also Greek, imply weakness).  Especially since they have each already been used by different people with different meanings.  And especially if we are trying to make "$n$-category" not imply strictness (in the face of tradition), it seems inconsistent to insist that "$\omega$-category" does imply strictness.  I feel sure that there is far more literature using "2-category" to mean "strict 2-category" than there is using "$\omega$-category" to mean "strict $\omega$-category," so why should we feel bound by the latter but not the former?

_Toby_: We could have the general concept at [[infinity-category]], the strict concept at [[strict omega-category]], and the discussion of terminology at [[omega-category]]. (It sounds like a joke, but it really may be the best use for each term!)

_[[Urs Schreiber|Urs]]_: Okay. In that case let me suggest the following: instead of "strict omega-category" let's have an entry "strict globular infinity-category" in which we give the above material and remark that "strict globular infinity-categories" are sometimes just called "omega-categories". Then we need another entry "strict cubical infinity-category" or "infinity-fold category" and mention the relation to "strict globular infinity-category".

_[[Todd Trimble|Todd]]_: 
I'm pretty sure the literature is mixed on this point. I don't recall seeing infinity-category being used much at all in the days when the subject was first born (mid to late nineties); people said either "strict" or "weak" omega-category. Tom Leinster in his
book for example has an entry in the index of his book:
"infinity-category: see omega-category" and never uses the term infinity-category anywhere else, as far as I know. I don't think I ever heard Ross Street say infinity-category -- I really think this
usage must have caught on more recently, with a different crowd.

I don't really mind infinity-category; I'm just not used to saying it myself, and until now was confused by what people like you meant when you used that or omega-category, except in specific contexts, as for example discussing the work of Crans. So now I know! 

[I should add that the above was given in am email to Urs, which he reproduced here; hence the phrase "people like you". I added at the end that I was not pushing an agenda.]

_Mike_: I was going to say that I liked Toby's suggestion, but it seems to have already been implemented, so I am satisfied.  Let me just say, in response to Urs' suggestion, that since [[2-category|2-categories]] don't need the word "globular" to distinguish them from [[double categories]] (aka 2-fold categories), I would rather not have to say "globular $\infty$-category (or $\omega$-category)" to distinguish it from cubical or $\infty$-fold ones.  Of course, it's fine to add "globular" for emphasis occasionally.

=--
