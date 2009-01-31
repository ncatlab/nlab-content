The term _higher dimensional algebra_ is used in various senses to include various forms of research into higher order categories, often  of a lax nature. A more specific definition is to say it means the study of systems of partial algebraic structures whose domains of definition are given by geometric conditions. 

Of course the partial composition of paths or of functions was used if not formalised early on. The earliest formal use  of partial operations was that of a [[groupoid]] as defined by Brandt in 1926, in connection with the laws for the classification of quaternary quadratic forms, generalising Gauss' work on binary quadratic forms. Curiously, groupoids were  not given as an example in Eilenberg and Mac Lanes fundamental paper on category theory, although they were well known by the Chicago algebraists. The general theory of such partial algebra was developed by Philip Higgins.

The next easiest to understand example in dimension 2 is possibly that of  maps $a: I^2 \to X$ where $X$ is a topological space, called _squares in $X$_. Such a map determines  four paths $\partial^\epsilon _i a: I \to X$ for $i=1,2, \epsilon=\pm$ given by $\partial^- _1 a(t)= a(0,t), \partial^+ _1 a(t)=a(1,t), \partial^- _2 a(t)= a(t,0), \partial^+ _2 a(t)=a(t,1)$. Such squares in $X$  have 2 obvious partial compositions $\circ_1,\circ_2$ where for example $a\circ_1 b$ is defined if and only if $\partial^+ _1 a= \partial^- _1 b$. 

The problem is to obtain a double groupoid out of such squares. Brown and Higgins realised in 1974 that this could be relatively easily done in a relative situation, i.e. if we are given a triple $X_*=(X,A,C)$ where $C \subseteq A \subseteq X$ and consider maps $I^2 \to X$ which take the edges into $A$ and the vertices into $C$, and then form $\rho X_*$ of homotopy classes of such maps rel vertices. It is not quite trivial to prove that the partial compositions of such squares are inherited by $\rho X_*$ to make it a double groupoid with an extra structure of _connections_. This extra structure makes the category of such objects equivalent to the category of [[crossed module]]s but of groupoids, rather than just groups. 

Under this equivalence, the double groupoid $\rho X_*$ becomes the crossed module $\Pi X_* $ consisting of the family of relative homotopy groups $\pi_2(X,A,c)$, $c \in C$, with the boundary to the [[fundamental groupoid]] $\pi_1(A,C)$ and the operations of this groupoid. Hence a van Kampen type theorem for $\rho$ yields a van Kampen type theorem for $\Pi$ and so  previously unobtainable determinations of some nonabelian second relative homotopy groups. 

Notice that the compositions in $\pi_2(X,A,c)$ require a choice of direction, whereas $\rho$ is a _symmetric_ construction. Also $\rho$ allows for convenient multiple compositions appropriate to _algebraic inverses to subdivision_. 

==
References

*P.J.Higgins, Algebras with a scheme of operators,  Math. Nachr. 27 1963 115--132.

*R. Brown and P.J. Higgins, On the connection between the second relative homotopy groups of some related spaces,  Proc. London Math.  Soc. (3) 36 (1978) 193-212.  