#Dictionary Cheatsheet
A Dictionary is an unordered list, with strict typing. Trying to put a different type that what you specified will result in a error / crash.

###Creating of new empty Dictionary
| Code  | What does it do?  |
|-------|-------------------|
| `var collection = [String:AnyObject]` | Shorthand for creating an Dictionary  |
| `var collection = [:]` | Shorthand for creating an Dictionary,   |
| `var collection = [String, Int]()` | Shorthand for creating an Dictionary  |
| `var collection = Dictionary<String, Int>()` | Creating a new Dictionary  |
| `var collection:Dictionary<String, Int> = [:]` | Creating a new Dictionary  |
| `var collection: [String, Int] = [:]` | Creating a new Dictionary  |

###Mutability / Immutability
By using `var` or `let` you make it mutable and immutable respectivly.
You can still do stuff like:

`let letterCiphers = ["A":1, "B": 2, "C":4]` Creates a immutable dictionary

`var mutableLetters = letterCiphers` Create a mutable copy of `letterCiphers`

###Creating of new Dictionary with data

| Code  | What does it do?  |
|-------|-------------------|
| `var artistsReleases = ["Mampi":2, "Cutmaster": 4, "Taylor":4]` | Shorthand for creating an Dictionary with data |


###Retrieving element from Dictionary
| Code  | What does it do?  |
|-------|-------------------|
| `artistsReleases["Mampi"]`  | Retrieve value with key "Mampi", using subscripting  |
| `collection.startIndex`  | The position of the first element in a non-empty dictionary. (Identical to endIndex in an empty dictionary) | 
| `collection.endIndex`  | The collection's "past the end" position. endIndex is not a valid argument to subscript, and is always reachable from startIndex by zero or more applications of successor() | 

###Adding / Updating element to Dictionary
| Code  | What does it do?  |
|-------|-------------------|
| `collection["Mampi"] = 42`  | Use subscripting to add elements to Dictionary |
| `collection.updateValue(42, forKey: "Mampi")`  | Update a value by a specific key to update elements in Dictionary. Returns the value that was replaced, or nil if a new key-value pair was added. |



###Remove element from Dictionary
| Code  | What does it do?  |
|-------|-------------------|
| `collection.removeValueForKey("Taylor")`  | Remove element with key "Taylor" from Dictionary. Returns the value that was removed, or nil if the key was not present. |
| `collection.removeAtIndex( n )`  | Remove the key-value pair at index i. |
| `collection.removeAll()`  | Removes all elements from Dictionary. |


###Handy methods on Dictionary
| Code  | What does it do?  |
|-------|-------------------|
| `collection.isEmpty`  | Boolean representing an empty or filled Dictionary. If count is 0, returns true  |
| `collection.count`  | Returns the amount of elements contained in Dictionary. |
| `collection.keys`  | Returns a collection of keys (Not an Array!) |
| `collection.values`  | Returns a collection of values (Not an Array!) |

###Get information from Dictionary
Uses the higher-level `dump()` function to 'dump' contents of collection in the console. 

| Code  | What does it do?  |
|-------|-------------------|
| `dump(collection)`  | Prints all contents from Dictionary, is like print/println for collections  |

More on `dump()` and other sequence and collection functions [Swift Standard Libraries: Sequence and Collection Functions](http://iosdeveloperzone.com/2014/10/15/swift-standard-libraries-sequence-and-collection-functions/)



###Looping over Dictionary

	
####for-in
		
	let errorCodes = ["Bad Request":400, "Unauthorized":401, "Payment Required":402, "Forbidden":403, "Page not found":404]
 
	for (errorDescription, errorCode) in errorCodes 
	{
		println("Server error code:  \(errorCode):  \(errorDescription)")
	}
