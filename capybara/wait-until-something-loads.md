# Wait Until Something Loads

The secret is using `find`. Unlike a lot of other Capybara stuff, `find`
actually waits until it can find the element on the page rather than sometimes
loading too soon and returning a nil.

`find(".some-class").click`

[The Thoughtbot Article I Always Wind Up
Googling](https://robots.thoughtbot.com/write-reliable-asynchronous-integration-tests-with-capybara)
