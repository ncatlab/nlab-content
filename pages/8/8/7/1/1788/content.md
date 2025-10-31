> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***



```
instance Applicative List where
  pure x = repeat x
  fs <*> xs = zipWith ($) fs xs
  ($)

instance Monoidal List where
  unit = repeat ()
  as ⊗ bs = zip as bs
```

with the canonical strength being defined as follows:

```
strength :: Functor f => (a, f b) -> f (a, b)
strength (a, fb) = fmap (a,) fb
```


## Related concepts

* [[arrow (in computer science)]]

