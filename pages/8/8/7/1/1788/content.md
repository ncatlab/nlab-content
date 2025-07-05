> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

\linebreak

The following seems to come out as intended with Firefox but not with Chrome:

* "`$\slash{D}$`" renders as "$\slash{D}$"

* "`$D\!\!\!\!\!/$`" renders as "$D\!\!\!\!\!/$"

Testing MathML code directly:

<math xmlns="http://www.w3.org/1998/Math/MathML">
  <mover>
    <mi>D</mi>
    <mo>&#x2F;</mo> <!-- Forward slash character -->
  </mover>
</math>

<math xmlns="http://www.w3.org/1998/Math/MathML">
  <menclose notation="updiagonalstrike">
    <mi>D</mi>
  </menclose>
</math>

Combining Unicode characters:

D̸

d̸

\linebreak