# Unit Testing
Notes on code and practices.

## Mock
`import mock` or `from unittest import mock`

Mock testing makes tests faster and less computationally expensive since the object mocked is a non-functional version of the real object, i.e. mock a database so you don't have to build one yourself but still produce behavior of a database.  

### Decorators
`@mock.patch` To use a function, class, object as a mock object.

`@mock.patch.object` Same as above but you have to import the object whereas the previous decorator can call any object.  

Example: `@mock.patch('class.method')` as opposed to `@mock.patch.object(class, 'method')`

After the decorator, pass in the mock object:

```
@mock.patch.object(class, 'function')
def testAMethod(self, mock_function):
  mock_function()
```

(https://medium.com/python-pandemonium/python-mocking-you-are-a-tricksy-beast-6c4a1f8d19b2)
