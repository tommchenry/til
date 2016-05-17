# Let vs. Let!

In many ways, this difference is very similar to the difference between `before(:each)` and `before(:all)`

`let(:user) = create(:user)` is *lazily evaluated*. This means that rspec only creates 
your fake user `user` when you have some other chunk of code that calls `user`.

`let!(:user) = create(:user)`, however, is forcibly evaluated by each example whether or 
not the example uses `user`. Because of this, it makes your tests slower than a standard `let`.



