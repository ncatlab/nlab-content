
**A couple more notorious bugs:**

\linebreak

(1.)

The following line is `!include`-ed from *[[Sandbox3]]*. The included HTML code fails to render:

[[!include Sandbox3]]

\linebreak

(2.)

Enclosing code for an Instiki-link with Instiki-code for square brackets, as in

`\[[test](Sandbox3)\]`

makes the hyperlink fail to render:

\[[test](Sandbox3)\]

One can work around this by instead HTML-coding the square brackets, as in 

`&lbrack;[test](Sandbox3)&rbrack;
`

which renders properly on the page itself

&lbrack;[test](Sandbox3)&rbrack;

but in turn fails to render properly when `!include`-ed anywhere, due to the previous bug.






