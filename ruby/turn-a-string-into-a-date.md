# Turn a String Into a Date

If you need to get more explicit than `Date.parse`, you can provide a string to `.strptime` along with a second argument that describes how to parse the string provided into date information.

For example

```
"2016-07-26"
```

```
Date::strptime(time_string, "%Y-%m-%d")
```
