# Change The Default Wait Time

By default, Capybara will only wait two seconds before returning that an element is not found on the page, even if you're using `find` or another wait-based check.

There are multiple ways to increase the default wait time past 2 seconds. The most basic way is to simply set `Capybara.default_wait_time = 10`; however, this will change the value for _all_ Capybara-based tests, causing legitimately failing tests to take ages to properly fail.

To change the default wait time for a single test, adding `wait: 10` (for example) as an argument is recommended

```
expect(page).to have_selector("#some_div", wait:10)
```

I had mixed results getting it to work. The more effective technique proved to be wrapping the tests that need extra time in a block

```
Capybara.using_wait_time 10 do
  expect(page).to have_selector("#some_div")
end
```
