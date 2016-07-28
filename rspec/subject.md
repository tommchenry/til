#Subject in Rspec

Subject in Rspec works similarly to `let` and `let!`, but allows you to specify the thing you are going to be testing in a series of tests as laid out in the `describe` block.

```
subject(:book) { Book.new }
```

What you're actually doing when you explicitly declare a `subject`, though is overwriting the `subject` that can be expected by the `describe` block:

```
describe Book do
  it { should validate_presence_of(:title) }
end
```

which is secretly

```
describe Book do 
  it 'should have a title' do
    subject.should validate_presence_of(:title)
  end
end
```

and because the `subject` is named by `describe Book`, you can get away without explicitly stating it.

-[A helpful article on subject and code smell](http://blog.davidchelimsky.net/blog/2012/05/13/spec-smell-explicit-use-of-subject/)
