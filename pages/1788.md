> `{:data`

Hmm. I can't find mention that Instiki actually parses that. Maybe `:data` is unknown and shows up in the error log.

testing  `{:data`

{:data 
foo=bar
}

after `:data` statement.

testing  `{:piffle` with internal `\}`

{:piffle
 foobar\}
 baz
}

after `:piffle` statement.

testing  `{:piffle` with unescaped internal `}`

{:piffle
 {foobar}
 baz
}

after `:piffle` statement.

