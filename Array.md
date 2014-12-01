#Array Cheatsheet

###Creating of new Array
| Code  | What does it do?  |
|-------|-------------------|
| `var collection = [Int]` | Shorthand for creating an Array  |
| `var collection = [1, 3, 7, 12, 40]`  | Shorthand for creating an Array. **Must be same type**  |
| `var collection = [Int]()`  | Create new Array  |
| `var collection:Array<Int> = []`  | Create new Array  |
| `var collection = Array<Int>()`  | Create new Array   |
| `var collection = [Int](count: 3 repeatedValue: 42)`  | Creates an array with 3 times 42 in it  |

###Retrieving element from Array
| Code  | What does it do?  |
|-------|-------------------|
| `collection[0]`  | Retrieve first element, index zero  |
| `collection.first`  | Retrieve an optional containing the first element, or nil when empty. |
| `collection.last`  | Retrieve an optional containing the last element, or nil when empty. |

###Adding element to Array
| Code  | What does it do?  |
|-------|-------------------|
| `collection.append(9)`  | Add same type element to Array |
| `collection.insert(42, atIndex: n)`  | Add same type element at specific index |
| `collection += [5, 4, 3]`  | Concat two, same type Array's |

###Remove element from Array
| Code  | What does it do?  |
|-------|-------------------|
| `collection.removeAtIndex(2)`  | Remove element from index 2 from Array. Returns removed value |
| `collection.removeLast()`  | Removes last element from Array. Returns removed value |
| `collection.removeAll()`  | Removes all elements from array.  Can take a Bool for keepCapacity to not change length. |

###Handy methods on Array
| Code  | What does it do?  |
|-------|-------------------|
| `collection.isEmpty`  | Boolean representing an empty or filled Array. If count is 0, returns true  |
| `collection.count`  | Returns the amount of element contained in Array. |
| `collection.reverse()`  | Returns a new array that is in reverse order. |

###Looping over Array
There are different methods to loop over a Array. Here are some:

####for-in with range
	for i in 0..<9
	{
	    println(i)
	}
	
####for-in
		
	let primeNumbers = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31]
 
	for number in primeNumbers
	{
	    println("\(number)")
	}



####for-in

	var index = 0
	 
	for i in myArray
	{
	    index += i
	}
	

####for-in with a tuple
Uses the higher-level `enumerate()` function to iterate through a collection. 
		
	for (index, number) in enumerate(someArray)
	{
	    println("Fibonacci Number \(index):  \(number)")
	}

===

More on `enumerate()` and other sequence and collection functions [Swift Standard Libraries: Sequence and Collection Functions](http://iosdeveloperzone.com/2014/10/15/swift-standard-libraries-sequence-and-collection-functions/)

