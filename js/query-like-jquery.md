# Query Like jQuery

Chrome's Javascript console can treat rendered HTML and Javascript like jQuery, even if it's totally vanilla:

```
$('#some_div')
```

will return:

```
<div id="some_div"></div>
```

which can then be acted on to get many of the same returns. In a pinch, you can also use

```
document.querySelectorAll('#some_div')
```
