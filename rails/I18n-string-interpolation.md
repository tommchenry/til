#I18n String Interpolation

You can't do Rails-style string interpolation in YAML, so the way you do you internationalization around variables and such is like this:

in your locale file:

```
en: 
  some_text: This is the text for %{user_name}
```

and then pass a value for `user_name` in the call like so: 

```
I18n.t('.some_text', user_name: current_user.name)
```
