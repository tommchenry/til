# View A Screenshot

This will drop a screenshot called `borked.png` of the site at this point in the
feature spec:

`page.driver.save_screenshot("/Users/Tom/Desktop/borked.png")`

## Bonus Points

The above test will only save a screenshot the size of your current viewport. In order to save a full screenshot of the page, you need to pass in the additional argument `full:true`

For example

```
page.driver.save_screenshot("/Users/Tom/Desktop/borked.png", full:true)
```
