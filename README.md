Shopavel Framework
==================



Collections
-----------

A basic collection has the same behaviour as an array, with some helper methods, you can extend these to provide additional checks or functionality.

Collections use "dot" syntax for array access, for example: `$collection->add('foo.bar', 'baz')` is equivalent to `$collection['foo']['bar'] = 'baz'`.

### Immutable Collections

An immutable collection once created can not be changed, the `add()` and `delete()` methods will throw a
`CollectionException`.



Controllers
-----------

All packaged shopavel controllers extend `Shopavel\Controllers\Controller`, which provides the same functionality as the default `BaseController`.



NestedSets
----------

Nested sets provide a fast way to create hierarchical relationships, e.g. categories. You can read me on [wikipedia](http://en.wikipedia.org/wiki/Nested_set_model) or in the [cartalyst docs](http://docs.cartalyst.com/nested-sets-2).



Transactions
------------

A transaction is any process or group of processes that can be taken on a database model. By extending `Shopavel\Transactions\Transaction` you can pass an array of validators when constructing your transaction. The `validate()` method can be called to check the object through these validators.



Validators
----------

Validators can be used to provide checks against objects prior to committing a transaction. If an issue is encountered an exception should be thrown.