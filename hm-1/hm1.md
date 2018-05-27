# OO Search Engine Implementation

In [MSAN962](https://github.com/parrt/msan692/blob/master/hw/search.md) you learned how to create and use a hash table. You did so by using sequential programming (scripting). In this homework, the task is to build a reusable library of your hash table implementation.

You are encouraged to reuse your solution and reflect on:

* How easy is your code to understand a few months later?
* Did you miss comments?
* Better variable names?
* Implementation explanations?
* Design documentation?

Once ready, go ahead and create `HashTable` class. The class should take one parameter: number of buckets. Remember, the number of buckets should be a prime number to avoid collisions.

Differently, from the MSAN 692, we want to hide all implementation details from the user. Implement following methods in your `HashTable` class:

```
buckets_str
      """
      Return a string representing the various buckets of this table. The output looks like:
          0000->
          0001->
          0002->
          0003->parrt:99
          0004->
      where parrt:99 indicates an association of (parrt,99) in bucket 3.
      """  
```

```
__str__:
      """
      Return what str(table) would return for a regular Python dict such as {parrt:99}.
      The order should be bucket order and then insertion order in the bucket.
      The insertion order is guaranteed when you append to the buckets in put.
      """
```
```
get:
      """
      Return table[key].
      Find the appropriate bucket indicated by the key and look for the association with the key. Return the value (not the key and not the association!)
      Return None if key not found.
      """
```

```
put:
      """
      Perform table[key] = value
      Find the appropriate bucket indicated by key and then append a value to the bucket.
      If the bucket for key already has a key, value pair with that key then replace it.
      Make sure that you are only adding (key, value) associations to the buckets.
      """
```

```
bucket_indexof:
      """
      Return the element within a specific bucket; the bucket is table[key].
      You have to search the bucket linearly.
      """
```

And, just to make the hashtable behave like a `dict` object, please add two methods, [__getitem__](https://docs.python.org/3/reference/datamodel.html#object.__getitem__) and [__setitem__](https://docs.python.org/3/reference/datamodel.html#object.__setitem__)  that python calls for the index operator: `[...]`. That will allow you use do things like:

```
h = HashTable()
h['a'] = 34
print(h['a'])
```


# Deliverables
You must complete and add these to the root of your `hm1-`userid repository

* htable.py
* test_htable.py (copy this from starterkit unchanged)

Ultimately, you want the test results to look like the following:
```
PYTHONPATH=. python -m pytest -v test_htableoo.py

collected 4 items

test_htableoo.py::test_empty PASSED                                                                    [ 25%]
test_htableoo.py::test_single PASSED                                                                   [ 50%]
test_htableoo.py::test_a_few PASSED                                                                    [ 75%]
test_htableoo.py::test_str_to_set PASSED                                                               [100%]

========================================== 4 passed in 0.06 seconds ==========================================
```

# How to submit

Use the invitation link to create repo.
https://classroom.github.com/a/9i7b-pBP
