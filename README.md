Project 4 Report
Introduction
I was given the task of creating a dictionary for this project. A red-black tree or a hash table with
linear probing were the two alternatives for creating this dictionary. I chose the hash table
method for my project since it appeared to be easier. After the hash table had been created, I was
required to insert all the words from the dictionary .txt file provided in the hash table. I had to
create a new file with my favorite poem and utilize the dictionary as a spell checker for the poem
as part of my testing. A spell checker just looks up words in the dictionary to determine if they
exist. I had to keep track of the time it took to generate the dictionary and the time it took to spell
check. I utilized the method to keep track of the time. currentTimeMillis(). The first class I
created was the ‘HashNode’ class. This class would create a key-value object from a string
imputed. This is important because in a hash table, elements are inserted as a key-value pair. This
class only contains getter methods. After that I created the ‘Dictionary’ class which represents
the hash table I created in this project. I built a hash table from the ground up to store n
key-value pairs in a hash table of size m (> n) and resolve collisions by searching the table for
empty entries. Lookup, insert, and delete are the three basic functions. In this hash table, I
employed linear probing, which is an open-addressing hashing method based on the notion that
when there is a collision, the next element in the table is checked. When searching for a key, we
have three options: search hit, search miss, or try the next entry. This hash table is also dynamic
and has no initial size assumed, meaning when the load factor is not in between 60% and 80%,
the hash table will automatically resize itself. After the ‘Dictionary’ class was done, I created the
‘Reader’ class which contains two static methods. One static method reads the dictionary file and
inserts the words into a hash table which it returns. The other static method returns the array
representation of the poem to be tested on. After that I created the ‘Tester’ class which contains
the Junit test cases and the ‘Timer’ class which times how long different functions of the
‘Dictionary’ class take.
insert()
This method is void and takes one argument which is a string. The following method inserts the
string argument into the array instance using linear probing. The average time of insertion in a
hash table with linear probing with O(1), however if the first index is already taken and is not
null, then insertion will take O(n). We use the hash function method to determine what index to
check first and if it is taken we use the equation, index = (index + 1) % size, to figure out where
to insert the value. After we have inserted the string, we check to see if the array needs to be
resized by calling ‘reSizeLarger()’.
delete()
This method is boolean and takes one argument which is a string. The method will return true if
the string argument was deleted successfully and false if the argument was not found. The
following method removes the string argument into the array instance using linear probing. The
method works the exact same and takes the same amount of time as insert; the only difference is
that when we find the key that matches the argument, we remove it. After we have deleted the
string, we check to see if the array needs to be resized by calling ‘reSizeSmaller()’.
lookUp()
This method returns a string and takes one argument which is a string. The following method
looks to see if the string argument is in the array by using linear probing.. The method works the
exact same and takes the same amount of time as insert and delete; the only difference is that
when we find the key that matches the argument, we return it back. If when searching, we find a
null value, it means the argument is not in the array and we return null.
reSizeLarger()
This method checks if the load factor is greater than 0.8; if it is, the array is resized. To resize the
array the first step is to find the next prime number. I used an algorithm that involves a for loop
to find the next prime number. After the next prime number has been found, I moved the
elements in the array instance into an array list, set the new size of the array instance, and
rehashed all the elements from the array list back into the array instance. The final step was to
make sure the size had been updated. This method takes O(n) time.
reSizeSmaller()
This method checks if the load factor is less than 0.6; if it is, then the array is resized. This
method works the exact same and takes the same time as the ‘reSizeLarger()’ method; the only
difference is that when we are finding the prime number we go backwards and find the first
prime number that comes before the size.
hash()
This method takes a string argument which is the key and returns an int which represents the
index. The following method puts the key through the hash function which was given to us and
returns the result. This takes O(1) time.
getLoadFactor()
This method takes no arguments and returns a float which represents the load factor of the array.
The load factor is how much of the array is actually filled. This method takes O(1) time.
Conclusion
For my Junit test cases I decided to test the ‘insert’, ‘lookUp’, and ‘delete’ method. All of the test
cases were successful. After the test cases were successful, I decided to time some of the
‘Dictionary’ class’s methods. I found that the amount of time it took to fill up the entire
dictionary with the words from the .txt file was 45150 milliseconds. I also was able to record the
size of the dictionary. After reading a file with 84095 words, the size of the array had gotten up
to 105137 and the load factor was 0.79986113. I found that when I tried to insert my name into
the dictionary and delete it, it took 0.0 milliseconds. In the test cases, the average time to look up
a word from the poem was 0. All in all, this project gave me a good understanding of hash tables
and how they operate. There were some minor inconveniences I faced with this project but I was
able to overcome those hurdles. I would recommend others to perform this project if they would
like to get more familiar with hash tables.
