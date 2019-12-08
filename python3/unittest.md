# Unit Testing
Notes on code and practices.

## Mock
`import mock` or `from unittest import mock`

Mock testing makes tests faster and less computationally expensive since the object mocked is a non-functional version of the real object, i.e. mock a database so you don't have to build one yourself but still produce behavior of a database.  

### @mock.patch vs @mock.patch.object
`@mock.patch` To use a function, class, object as a mock object.

`@mock.patch.object` Same as above but you have to import the object whereas the previous decorator can call any object.  

Example: `@mock.patch('class.method')` as opposed to `@mock.patch.object(class, 'method')`

After the decorator, pass in the mock object:

```
@mock.patch.object(class, 'function')
def testAMethod(self, mock_function):
  mock_function()
```

`@mock.patch` will replace the calling of the original function.  Calling either will reference the same instance of mock object.

Example:

```
def calculate():
  # Code

@mock.patch.object(class, 'calculate')
def testCalculate(self, mock_calculate):
  calculate()         # Returns mock
  mock_calculate()    # Returns mock
```

### Mock() vs mock.patch
When using `mock.Mock()`, the target mock object will be overridden as a mock object. <br>
Example: `requests = mock.Mock()` creates a mock object out of the `requests` library.  Any requests calls will now be mocks.


### Mock() vs MagicMock()




[Medium - Python Mocking](https://medium.com/python-pandemonium/python-mocking-you-are-a-tricksy-beast-6c4a1f8d19b2)

[Test Doubles, Fakes, Mocks, and Stubs](https://blog.pragmatists.com/test-doubles-fakes-mocks-and-stubs-1a7491dfa3da)
