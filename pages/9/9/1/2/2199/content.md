[[!redirects Boolean domain]]
[[!redirects boolean variable]]
[[!redirects Boolean variable]]

A __boolean domain__ $\mathbb{B}$ is a generic 2-element set, say, $\mathbb{B} = \{ 0, 1 \}$, whose elements are intended for interpretation as logical values, commonly but not invariably, with $0 = \mathop{false}$ and $1 = \mathop{true}$.

A __boolean variable__ $x$ is a variable that takes its value from a boolean domain, as $x \in \mathbb{B}$.

# Discussion #

[[JA]]: What I wrote above is all I really intended to say here.  The bit about "intended for interpretation as logical values" is not just waffling --- I want to leave room for considering "generic 2-element sets" that enjoy dual interpretations as logical values.  We might call it a "binary domain" if we really had to --- dunno, that seems likely to cause other problems --- but there is historical precedent for treating boolean material as if it were "dual all the way down".

[[JA]]: I am bracketing the following additions by Toby, as I can't tell whether they fit the intentions I have here.  (Partly because one of my intentions is to keep this particular base of conceptual recursion as simple as possible.)

> In particular, the set of [[truth values]] in [[classical logic]], $\{ \bot, \top \}$, is a Boolean domain.

> If we think of $\mathbb{B}$ as a [[pointed set]] equipped with the element that is interpreted as $true$ (so that the other element must be interpreted as $false$), then there is an [[generalized the|effectively unique]] boolean domain.

> If this variable depends on parameters, then it is (or defines) a [[Boolean-valued function]], that is a [[function]] whose target if $\mathbb{B}$.

[[JA]]: The way I'll be doing things, there is actually an important distinction between the mathematical object $\mathbb{B} = \{ 0, 1 \}$ and the set of logical values $\{ \mathop{false}, \mathop{true} \}$.  There is a step of interpretation --- or "applying the mathematics to the logical subject matter" --- that separates them.  There is of course the usual interpretation, so we often get sloppy about when exactly we cross the line of interpretation, but there are good reasons for observing it at other times.

Toby: Well, maybe you should just go ahead and write what you intend to write here;  everything here is a work in progress and your text can clash with mine for a bit until we work it out.  But on the nLab, we\'re very much into a structural approach to mathematics, and we\'ll want to say when one thing can be interpreted as another, and when two things are equivalent, and if so in what ways.

[[Mike Shulman]]: Agreed with Toby, perhaps even more strongly.  I think his additions should definitely be part of the page.

Toby: Regarding the middle bracketed item, it might work to separate this from [[Boolean field]], the latter being for a *pointed* (or equivalently *ordered*) $2$-element set, with this page for an *unstructured* $2$-element set.  That said, I don\'t see how you can disagree with the other two bracketed items; the first one is certainly true ($\{ \bot, \top \}$ is as much a $2$-element set as $\{ 0, 1 \}$) and the last one is necessary to agree with the usual meaning of the term 'variable' in logic.

Also, Jon, I think that you should seriously think about Todd\'s suggestion at [[graph]] to get a personal web here.  (Like [[tobybartels:HomePage|mine]].)  Then you wouldn\'t run into people interfering with your intentions so much, but you\'d still get some of the benefits of a large group looking over the material and adding comments or minor corrections.  (The group of people that read the personal webs is smaller, but it includes me and Mike.  I *think* that you\'ve found some of my edits useful.)  Then when something there gets into a state where the rest of us can clearly see the broader picture, you can move (or copy) it here and we\'ll have a better understanding of what it\'s for.  (This is largely how [[schreiber:HomePage|our most prolific contributor]] operates.)  In the meantime, you can still link that material from here, so it won\'t get lost in a ghetto.

[[JA]]: I said "I can't tell whether they fit", so let's see if we can see.

[[JA]]: All I want is a generic 2-element set whose elements _can be_ interpreted as logical values.  The 2-element set is a formal or mathematical object that is _more abstract_ than the set of logical values.  Being more abstract it has more than one interpretation as a set of logical values.  If you are allowing for the symbols "$\bot$" and "$\top$" to be interpreted in such a way that $\bot = true$ and $\top = false$, then that would make $\{ \bot, \top \}$ a boolean domain in the sense defined above.  So that is the first question.

Toby: Yeah, you could do that; even the function from $\{\bot, \top\}$ to itself that maps $\bot \mapsto \top$ and $\top \mapsto \bot$ exists.  But the fact that you ask this makes it more clear to me that your Boolean domain is an *unstructured* $2$-element set, where mine is *structured* (pointed or ordered), so it would be proper to move the second bracketed item to [[boolean field]] or something.  If you like, I\'ll do that and also try to rewrite the other bracketed items in a way that fits better.

[[JA]]: I didn't find the word "field" on that page --- is the redirect meant to say that [[boolean field]] = [[boolean algebra]]?  That might cause confusion with the field GF(2), so watch out for that.

[[JA]]: As for the third item, I personally like that usage, as it connects with the item of catechism that says "a random variable is a function on a sample space $X$", and the connection between "square" probability densities $p : X \to \{ 0, 1 \} = \mathbb{B}$ and "curvy" probability densities $q : X \to [0, 1] \subseteq \mathbb{R}$ is one of the things that is motivating this approach.  So it was only expository simplicity that was constraining me here.

Toby:  Sorry about [[boolean field]]; I should have clarified.  One meaning of 'boolean field' is [[boolean algebra]], which is how the redirect got there (somewhat thoughtlessly) a while back; but I would make it a separate page (focusing on $\{\bot, \top\}$ or $\{0, 1\}$ with its usual structures as a boolean algebra) instead.  Under the identification of [[boolean algebras]] with [[boolean rings]], that\'s actually the same as $GF(2)$; that should also be discussed there.