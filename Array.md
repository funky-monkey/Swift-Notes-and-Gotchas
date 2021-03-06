#Array Cheatsheet
An Array is an ordered list and strict typed. So an array can only hold one type.

###Creating of new Array
| Code  | What does it do?  |
|-------|-------------------|
| `var collection = [Int]` | Shorthand for creating an Array  |
| `var collection = [1, 3, 7, 12, 40]`  | Shorthand for creating an Array. **Must be same type**  |
| `var collection = [Int]()`  | Create new Array  |
| `var collection:Array<Int> = []`  | Create new Array  |
| `var collection:[String] = []`  | Create new Array  |
| `var collection = Array<Int>()`  | Create new Array   |
| `var collection = [Int](count: 3 repeatedValue: 42)`  | Creates an array with 3 times 42 in it  |

###Mutability / Immutability
By using `var` or `let` you make it mutable and immutable respectively.
You can still do stuff like:

`let letters = ["A", "B", "C"]` Creates a immutable array

`var mutableLetters = letters` Create a mutable copy of `letters`

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

####for (WILL BE DEPRECATED IN SWIFT3)
Standard 'for loop'. Apple' Swift book talks about the **++i** (this will first increment, then add to i)

	for var i = 0; i < 99; ++i
	{
	    println("I've got \(i) problems but Swift aint one!")
	}


####for-in with range
	// Same thing as previous loop
	for i in 0..<9
	{
	    println("I've got \(i) problems but Swift aint one!")
	}
	
####for-in
		
	let lostNumbers = [4, 8, 15, 16, 23, 42]
 
	for number in lostNumbers
	{
	    println("\(number)")
	}



####for-in

	var index = 0
	 
	for i in myArray
	{
	    index += i
	}
	

####for-in with tuple
(Brainfart: Is it 'a tuple' or just 'tuple'? And since it has more than one value - does that make it 'tuples'? So is then the singular form always pronounced in plural? )

Uses the `enumerate()` function from Array to iterate through a collection. 
		
	for (index, number) in lostNumbers.enumerate()
	{
	    println("LOST number sequence  \(index):  \(number)")
	}

===

More on `enumerate()` and other sequence and collection functions [Swift Standard Libraries: Sequence and Collection Functions](http://iosdeveloperzone.com/2014/10/15/swift-standard-libraries-sequence-and-collection-functions/)

