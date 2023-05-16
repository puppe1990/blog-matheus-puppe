---
title: "Diference between Mock and Stub"
datePublished: Tue May 16 2023 14:15:20 GMT+0000 (Coordinated Universal Time)
cuid: clhqcw4tv00090alf4t7hg0ew
slug: diference-between-mock-and-stub
tags: ruby

---

Mocks and stubs are both used in testing to replace real objects. The main differences between mocks and stubs are:

Mocks:

* Are used to verify interactions with an object. For example, you can assert that a method was called a certain number of times, with certain arguments, in a certain order, etc.
    
* Have expectations set on them to verify the interactions. For example:
    

```ruby
mock_object.expects(:message).with('Hello').returns('Hi')
```

* Raises an error if it receives an unexpected message.
    

Stubs:

* Are used simply to replace an object with a hardcoded response.
    
* Do not care about the messages they receive or verify interactions. They just return a stubbed response.
    
* Do not raise errors on unexpected messages.
    

So in summary:

Mocks:

* Set expectations
    
* Verify interactions
    
* Raise errors if those expectations are not met
    

Stubs:

* Simply provide stubbed responses
    
* Do not verify interactions
    
* Do not raise errors on unexpected messages
    

Some examples to illustrate the difference:

Mock:

```ruby
mock_object = mock('name')
mock_object.expects(:message).with('Hello').returns('Hi')
mock_object.message('Hello')  # Returns 'Hi'
mock_object.message('Goodbye') # Raises error - unexpected message
```

Stub:

```ruby
stub_object = stub('name') 
stub_object.stubs(:message).returns('Hi')
stub_object.message('Hello') # Returns 'Hi'
stub_object.message('Goodbye') # Also returns 'Hi' - stub doesn't care
```

cheers!