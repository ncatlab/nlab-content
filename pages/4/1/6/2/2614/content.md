Classically, a [[logic]] is __two-valued__ if every [[proposition]] (without free variables) is either true or false and none is both.  Being two-valued logic is a key feature of [[classical logic]]; any logic that is not two-valued is ipso facto nonclassical.

We do not expect that a [[predicate]] (statements with free variables) is either true or false (although it will become true or false if applied to a term with no free variables).  We can call a [[context]] __two-valued__ if every proposition in that context is either true or false; a logic is two-valued iff its global context is two-valued.

Famously, [[intuitionistic logic]] is not two-valued, although it may be two-valued in a weaker sense.  Let a logic be __intuitionistically two-valued__ if every proposition is false if and only if it is not true.  On the other hand, we can call a logic __paraconsistently two-valued__ if every proposition is true if and only if it is not false.  (Take this paragraph with a grain of salt.)

Applying [[topos theory]] to logic, we call a [[topos]] __two-valued__ if every [[global element]] of its [[subobject classifier]] is false if and only if it is not true.  Note that we have phrased the definition in the intuitionistic fashion; that way, the theorem that a [[well-pointed topos]] is two-valued survives even in [[constructive mathematics]].


## Two-valued vs boolean

Although being two-valued and being boolean are both key features of [[classical logic]] and are closely related, they are not the same thing.  It is easy to find multi-valued logics which are boolean in that they satisfy the law of [[excluded middle]]; indeed, any [[boolean algebra]] provides a model.  Conversely, a logic may be two-valued in an external sense without being able to prove it of itself.

Similarly, a topos may be two-valued without being [[Boolean topos|Boolean]], and for purposes of doing mathematics in the topos it is the latter property which determines whether the [[internal logic]] satisfies [[excluded middle]].  However, a [[well-pointed topos]] (even working in a constructive metatheory, where such toposes might not be boolean or two-valued) is two-valued (in the stong classical sense) if and only if it is boolean.


[[!redirects two-valued context]]
[[!redirects two-valued topos]]
