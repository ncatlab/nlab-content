**Warning: This page is under construction. Feedback welcome.**

See [[Understanding Constructions in Categories]]

* [[Understanding Limits in Set]]
* [[Understanding Colimits in Set]]

***

## Other Constructions ##

#### Exponential Objects

[[exponential objects]]

#### Dependent Products

[[dependent products]]

#### Power Objects

[[power objects]]

## Discussion ##

+--{.query}
[[Eric]]: How is this (note: terminal object) the universal cone over the empty diagram?

_Toby_:  It seems to me that this is really a question about terminal objects in general than about terminal objects in $Set$.  A cone over the empty diagram is simply an object, and a morphism of cones over the empty diagram is simply a morphism.  A universal cone over a diagram $J$ is a cone $T$ over $J$ such that, given any cone $C$, there is a unique cone morphism from $C$ to $T$.  So a univeral cone over the empty diagram is an object $T$ such that, given any object $C$, there is a unique morphism from $C$ to $T$.  In other words, a universal cone over the empty diagram is a terminal object.

I don\'t see the point of the last paragraph before this query box.  Already at the end of the previous paragraph, we\'ve proved that $\bullet$ is a terminal object, since there is a unique function (morphism) to $\bullet$ from any set (object) $C$.  It almost looks like you wrote that paragraph by modifying the paragraph that *I* had written in that place, but that paragraph did something different: it proved that ${!}$ was unique.  Apparently, you thought that this was obvious, since you simply added the word 'unique' to the previous paragraph.

Alternatively, if you *want* to keep a paragraph that proves unicity, then you can remove 'unique' and rewrite my original unicity proof in terminology more like yours, as follows:
> Now let ${!}'\colon C \to \bullet$ be any function. Then
> $$ {!}'(z) = * = {!}(z)$$
> for any element $z$ of $C$, so ${!}' = {!}$.

[[Eric]]: Thanks Toby. I think what I'm looking for is a way to understand that a singleton set is the universal cone over the empty diagram. All these items should be seen as special cases of [[limit]]. Unfortunately, I don't understand limit well enough to explain it. In fact, that is one of the reasons to create this page, i.e. so that I can understand limits :)

The preceding paragraph was my attempt to make it look like a limit, but I obviously failed :)

Ideally, this section would show how terminal object is a special case of limit somehow.

=--


[[!redirects Understanding Set]]
[[!redirects Understanding Constructions on Set]]
[[!redirects understanding constructions in Set]]
[[!redirects understanding Set]]
[[!redirects understanding constructions on Set]]
