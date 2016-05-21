# Render a Rails Partial

Seems straightforward enough

```
=render 'yourdir/your_partial'
```

but remember: 

- `yourdir` is relative to `app/views`
- 'your_partial' is expecting '_your_partial.haml' to exist at `app/views/yourdir/`
- `your_partial` can't have any hyphens in it, only underscores
