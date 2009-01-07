#Idea#

The **simplex category** $\Delta$ encodes one of the main [[geometric shapes for higher structures]]. Its objects are the standard cellular $n$-[[simplex|simplices]].


#Definition#

(In all of the following "occupied" is a [[constructivism|constructivist]] substitute for the word "nonempty".)

* The __simplex category__ $\Delta$ is the full [[subcategory]] of [[Cat]] consisting of the finite occupied linear [[quiver]]s.

* Equivalently: $\Delta$ is the category of finite occupied [[totally ordered set]]s and order-preserving functions between them.

#Remarks#

* [[presheaf|Presheaves]] on $\Delta$ are [[simplicial set|simplicial sets]]. Embedded into its presheaf category the object $[n]$ in the simplex category may be identified with the standard simplicial $n$-[[simplex]].

* Often, it is highly convenient to extend the category $\Delta$ to contain also the empty totally ordered set. This is called the _augmented_ simplex category $\Delta_a$, and presheaves on it are _augmented simplicial sets._ The category $\Delta_a$ may be characterized as the initial strict monoidal category equipped with a monoid; the monoidal product is ordinal sum, and the monoidal unit is the empty ordinal. This style of definition also opens up the possibility of using string diagrams to visualize the structure of $\Delta_a$ and of the [[cube category]] $\Box$. 

#Discussion#

An earlier version of this entry started the following discussion:

[[Todd Trimble|Todd]] _says_: Historically, and especially for algebraic topologists, $\Delta$ refers to the category of nonempty totally ordered sets and order-preserving maps; an adjective like "augmented" would be attached to "simplicial object" if they wanted to refer to a contravariant functor coming out of what is being defined here as $\Delta$. While I understand arguments why one might wish to redefine $\Delta$ this way, there are also countervailing arguments (cf. Tom's Caf&#233; post How I Came to Love the Nerve Construction); in any event, given the weight of history, the "sometimes" strikes me as inappropriate understatement. I think more discussion is called for before we appropriate $\Delta$ for the lesser-used concept, and rename the more commonly used one as $\Delta$ with a dot over it (do other people use that notation?). 

_[[Urs Schreiber|Urs]]:_ I have tried to change the entry accordingly now. 

_[[Todd Trimble|Todd]]:_ Having said all of the above, I myself prefer (on conceptual grounds) to treat the category of all finite ordinals (Ross Street used to call it "algebraists' $\Delta$") as the primary concept, and the category of finite nonempty ordinals ("topologists' $\Delta$") as secondary. It's just that I worried about introducing confusion, since my own opinion may well be a minority opinion. 

_[[Mike Shulman|Mike]]_: I think there are many good reasons, including but not limited to tradition, to give the unadorned name to the topologists' $\Delta$.  In my experience, in most applications to [[homotopy theory]], the topologists' $\Delta$ is the important object, both conceptually and mathematically, with its augmented version playing at most a technical role occasionally.  And while the augmented $\Delta$ does have a cute universal property as a monoidal category, the category of simplicial sets (presheaves on the unaugmented $\Delta$) also has a good universal property: it is the [[classifying topos]] for linear orders.
