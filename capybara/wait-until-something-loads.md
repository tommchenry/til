# Wait Until Something Loads

The secret is using `find`. Unlike a lot of other Capybara stuff, `find`
actually waits until it can find the element on the page rather than sometimes
loading too soon and returning a nil.

`find(".some-class").click`

[The Thoughtbot Article I Always Wind Up
Googling](https://robots.thoughtbot.com/write-reliable-asynchronous-integration-tests-with-capybara)

## Bonus

### Methods that Wait

```
find(selector), find_field, find_link, etc.
within(selector) (scoping)
has_selector?, has_no_selector? & assertions
form & link actions
click_link, click_button
fill_in
check, uncheck, select, choose, etc.
```

### Methods that Don't

```
visit(path)
current_path
all(selector)
first(selector) (counter-intuitively)
execute_script, evaluate_script
simple accessors: text, value, title, etc.
```

[Where I Swiped This](http://stefan.haflidason.com/testing-with-rails-and-capybara-methods-that-wait-method-that-wont/)
