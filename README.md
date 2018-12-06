# FileShark!
What is FileShark! ?

### A generic tool that aids with doing file mapping of csv files.

In other words you use FileShark to transform a source csv file to a target csv file. Everything is done with Streams so
there is no writing files to disk.


FileShark! Description of feautres to come:

Construct a FileShark object with an Inputstream and  numberOfColumns for targetFile. 
The IS has to have rows in csv format otherwise an error is thrown.
A builder provides an option to include header. True/false is given, provideHeader is false by default.
The builder also returns an option withInterval(var) where you can set an interval, intervals transformations are placed in the order that that they are set in the builder in the target file and are direct mappings, you can call with interval as many times as you want. But an error is thrown if you call it so many times/and your intervals are outside the bounds of the target array. You can also call withCustomMapping(var, (item)->). It takes 2 arguments the first argument is a string, it can be a string as a number (index), a string in the form of an interval (index interval), or a comma separated values in the form 1:1. The number before the colon represents the source index, and the number after the colon represents the target index. The second argument is a lambda which is used to implement the custom logic for the mapping for the designated indexes. Once all the intervals are set, then .build() is called which makes the transformation and returns an the data as an OutputStream which can be used to write to file, S3, or whatever. 
