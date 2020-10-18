# Hash Table Implementation
Implementing a hash table of linked lists in Java.

## Purpose
Getting familiar with hashing strategies, maintaining a constant load factor, and implementing relevant functions for use. Used as lab work for a data structures and algoithms course.

## Content Path
https://github.com/quinnwai/hash-table-impl/blob/master/labs/hash/StringTable.java

## Overview
The most important functions are `StringTable`, `insert`, `find`, `remove`, and `toIndex`. Here is more about each function:
 - `public StringTable(int nBuckets)`: Constructor method, which instantiates the number of buckets `nBuckets` and an empty array of LinkedLists `buckets`
 - `public boolean insert(Record r)`:  Iteratively searches through a bucket for a key, returning true and adds the given record to the list if that key does not already exist and false if otherwise. To associate the key (field of record r.key) with a bucket, the method calls on the StringToHashCode and toIndex method to convert the String key into an integer hashcode and then index of a specific bucket.
 - `public Record find(String key)`: Iteratively searches through the bucket for a key, returning the key’s record if found and null otherwise. To associate the key with a bucket, the method calls on the StringToHashCode and toIndex method to convert the String key into an integer hashcode and then index of a specific bucket.
 - `public void remove(String key)`: Iteratively searches through a bucket for a key, removing the record containing the key if found. To associate the key with a bucket, the method calls on the StringToHashCode and toIndex method to convert the String key into an integer hashcode and then index of a specific bucket.
 - `private int toIndex(int hashcode)`: Creates an index that is less than the number of buckets (nBuckets) so that each key is always associated with the same index within the hash table
