
* **On topological-hardware awareness via `TED-K`**

  From a broad perspective, all [[nLab:quantum gates]] are [[nLab:linear maps]]/[[nLab:linear operators]] ([[nLab:semantics|semantically]]), hence are [[nLab:function type|functions]] between [[nLab:linear types]] ([[nLab:syntax|syntactically]]).
On a finer level however, some such (families of) linear operators/function are much more readily implemented on given physical hardware than others.

  \linebreak

  Existing [[nLab:quantum programming languages]] (QPLs) tend to have little reflection of this more detailed information, they are not "hardware aware". In contrast, in [[nLab:twisted equivariant K-theory|`TED-K`]] implemented in [[nLab:cohesive homotopy type theory|cohesive HOTT]] one would have [[nLab:dependent linear types]] much as, say, [[nLab:Quipper]] does, but *in addition* infrastructure for naturally speaking about that particular class of these which matches expected [[nLab:topological quantum computation|TQC]] hardware functionality.

  \linebreak

  Concretely, the elementary [[nLab:quantum gates]] that are expected to be realized by a [[nLab:topological quantum computer]] are of a very specific and peculiar kind: They are families of linear maps which are parameterized by elements of a [[nLab:braid group]] and which constitute a specific class of [[nLab:braid representations]], namely
"[[nLab:Knizhnik-Zamolodchikov equation|monodromy braid representations]] on [[nLab:su(2)-anyon|$\mathfrak{su}(2)$]]-[[nLab:conformal blocks]]".

  \linebreak


  A traditional [[nLab:quantum programming language|QPL]] like [[nLab:Quipper]] has no information about this. If one were to run (in the future) a Quipper program on a [[nLab:topological quantum computer]], there would have to be a compiler involved which provides this missing information: The compiler would have to read in functions between [[nLab:linear types]] specified in Quipper, and would try to approximate them as [[nLab:composition|composites]] of linear operators appearing in a [[nLab:Knizhnik-Zamolodchikov equation|monodromy braid representations]] on [[nLab:su(2)-anyon|$\mathfrak{su}(2)$-]][[nLab:conformal blocks]].


  \linebreak

  As a result, the generic Quipper program would tend to have an inefficient compilation to any given [[nLab:topological quantum computation|TQC]] machine. It would not be "aware" that this is the hardware that it is running on.

  \linebreak


  In contrast, the [[nLab:twisted equivariant K-theory|`TED-K`]] language scheme that we are describing would be adding to the expressiveness of a language like Quipper the information about the native [[nLab:quantum gates]] that the [[nLab:topological quantum computation|TQC]] hardware would provide. The programmer would be provided with one very particular [[nLab:dependent linear type theory|dependent linear]] [[nLab:homotopy type|homotopy type]] (the fiberwise TED-K type of fibrations of [[nLab:shape modality|shapes]] of [[nLab:configuration space of points|configuration spaces]]) and would be guaranteed that the [[nLab:linear maps]] (functions between [[nLab:linear types]]) which are obtained by [[nLab:type transport]] in/on this specific dependent linear type are those which the [[nLab:topological quantum computation|TQC]] hardware has an efficient implementation of.


  \linebreak

  Of course, one could imagine adding this hardware-information by brute force to a [[nLab:quantum programming language|QPL]] [[nLab:Quipper]]: One could write a Quipper library which encodes by hand the tensor functions which arise in $\mathfrak{su}(2)$-monodromy braid representations. The programmer could then decide to prefer composites of these pre-defined linear maps to build their [[nLab:quantum circuits]], much like a contemporary high-level language programmer might choose to insert fine-tuned "assembler" commands for guarantee of verbatim efficient implementation on the underlying hardware.

  \linebreak

  However, in both cases this would be a hack: the assembler code is alien to the ambient high-level language that calls it, just as Quipper would not provide any language handle on what it is that a would-be TQC library is providing.

  \linebreak

  Our observation is that in [[nLab:homotopy type theory]] supporting a minimum of [[nLab:cohesion]], this "TQC assembler code library", if you wish, would automatically and natively be available, constructed "simply" as the
0-truncation of a certain dependent function type whose semantics is that of certain [[nLab:twisted equivariant K-theory|TED K-theory]] [[nLab:cohomology group|groups]].

  \linebreak

  This seems like a remarkable confluence of [[nLab:quantum programming language|language]] and [[nLab:quantum physics]] for [[nLab:topological quantum computation|TQC]]. In the companion note *[[schreiber:Anyonic topological order in TED K-theory|Anyonic topological order in TED-K]]* we explain that these [[nLab:twisted equivariant K-theory|TED-K]] types are a remarkably accurate reflection not just of [[nLab:topological quantum computation|topological]] [[nLab:quantum gates]] as such, but generally of the "[[nLab:topological phases of matter|topological phases of]] [[nLab:quantum materials]]" which are expected to serve as hardware implementing such gates. With a language for [[nLab:twisted equivariant K-theory|TED-K]] in [[nLab:cohesive homotopy type theory|cohesive HoTT]], the distinction between a [[nLab:quantum programming language]] and an actual simulation of the underlying topological quantum hardware at just the right "universal" level of resolution would disappear.
