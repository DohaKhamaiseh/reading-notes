## WHAT
**Hash:** A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

**Buckets:**  A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

**Collisions:** A collision is what happens when more than one key gets hashed to the same location of the hashtable.


## WHY
1. Hold unique values
2. Dictionary
3. Library


## HOW

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a ``hash``. A ``hash`` is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.