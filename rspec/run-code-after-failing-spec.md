# Run Code After Failing Spec

To run some code only after a failing test:

```
after(:each) do |spec|
  if spec.exception
    save_and_open_page
  end
end
```
