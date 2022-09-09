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
