#YAML Block Literals

Strings do not require quotation marks in YAML, so when you want to pass a multi-line string and preserve newlines, add `|`.

```
some_data: | 
   This is some text
   I want to keep the newline break
```

if you'd prefer newlines to work as spaces, use `>`

```
some_data: > 
   This is some text
   I want the newlines folded together
```
