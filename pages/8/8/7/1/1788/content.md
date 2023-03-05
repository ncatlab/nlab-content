
Suppose that `A` is the name of the page to be kept and and that `B` is the name of the one to be deleted.

1. Edit `A` 

   1. so that it looks like the intended merged entry.

   1. Finally add the line "<nowiki>[[!redirects B]]</nowiki>" to the bottom.  

   1. Submit.

1. Edit `B`

   1. by first clearing its content (e.g. with a keystroke such as `Ctrl-A` `Del`)

   1. Click the checkbox 'Change page name.', which will bring up a new field 'New name:'.

   1.  In that field, append "`> history`" to the string "`B`", so that the new page name becomes "`B > history`".

       > (The idea is to change to any name that is neither coincides with an existing nor with a future entry.)

       Do *not* submit the edit *yet*.

   1. Before finishing we need to work around what Instiki thinks is intended behaviour:

      1. Click in the big edit box -- this make will automatically add the line "<nowiki>[[!redirects B]]</nowiki>".

         > (Instiki is trying to be helpful, not knowing that we want to delete the entry for good.)

      1. Delete that line (to ensure that all requests for `B` will now take the reader to `A`).

      1. and instead add "`see` <nowiki>[[A]]</nowiki>". 

         (This just in case anyone ever comes across this page in the future -- which should not actually happen, due to the `[[!redirects B]]`-command meanwhile added to `A`.)

   1. Finally ready to submit this quasi-deletion of `B`. 

      But since the page's name was changed in the process, the software will require announcing this edit in the box below the edit box. 

      Type there something like:

      "`As we discussed, I am orphaning this page in order to merge it with A.`"

   1. Submit.
