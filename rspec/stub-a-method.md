# Stub a Method

In Rspec, you can force your objects (both real and fake test objects) to return a 
known value in response to your test's call

`allow(some_object).to receive(:return_four) { 4 }`

means the value of 

`some_object.return_four`

will be `4`, no matter what it might ordinarily be. The symbol is the message to 
respond to, the block is the thing returned.
