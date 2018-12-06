# fileShark!
What is FileShark! ?

### A generic tool that aids with doing file mapping of csv files.

In other words you use FileShark to transform a source csv file to a target csv file. Everything is done with Streams so
there is no writing files to disk.




FileShark! feautres to come:

Construct a FileShark object with an Inputstream. The IS has to have rows in csv format otherwise an error is thrown.
Decide whether to deserialize to a specific java object or keep rows/objects available in an Array structure after reading IS.
Decide whether to build object of a specific class or build a line and write it to a Stream after each line mapping cycle is complete.
Decide whether to include heading or not.
Designate intervals of direct mapping along with custom mapping. Example properties 1-3 of source object map 
to properties 1-3 of target object, target 4 has custom mapping, properties 5-7 of source object map directly 
to properties 5-7 of target object.

Build a line/object in the following ways.
Direct mapping, map a property from the source bean to a property of the target bean.
Map from an index value of the source object to index value of target object.
Map from an index value of source object to property of target object.
Get value by index value, transform it, map it to index value of target object.
Get value by property, transform it then map it to property of target object.
Get value by index value, transform it, map to it to property of target object.
Get value by property, transform it, then map it to index of target object.
