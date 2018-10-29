# Python-3.x #

This Documents will explains alomst all the python concepts from zero level to advanced level. Every Chapter in this tutorials explains the concepts in very easy way and also provide the coding.

-------------------------------------------------------------------------------------------------------------------------------

[1. Python Intorduction](#1-python-introduction)

[2. Python Setup](#2-python-setup)

[3. Python Comments](#3-python-comments)

[4. Python DataTypes](#4-python-datatypes)

[5. Python Basics](#5-python-basics)

  - [5.1 Command Line Arguments](#5.1-command-line-arguments)
  - [5.2 Import Statements](#5.2-import-statements)
  - [5.3 If-Else Statement](#5.3-if-else-statement)
  - [5.4 Switch Statement](#5.4-switch-statement)
  - [5.5 While Loop Statement](#5.5-while-loop-statement)
  - [5.6 For Loop Statement](#5.6-for-loop-statement)  
  - [5.7 Functions](#5.7-functions)
  - [5.8 Return](#5.8-return)
  - [5.9 Continue](#5.9-continue)
  - [5.10 Break](#5.10-break)
  - [5.11 Pass](#5.11-pass)

[6. Python String](#6-python-string)

[7. Python File Operation](#7-python-file-operation)

[8. Python Collection](#8-python-colllection)

[9. Python Exceptions Handling](#9-python-exception-handling)

[10. Python Regular Expression](#10-python-regular-expression)

[11. Python Object Oriented Programming](#11-python-object-oriented-programming)

[12. Python Importaint Libraries](#12-python-importaint-libraries)

[13. Python Networking](#13-python-networking)

-----------------------------------------------------------------------------------------------------------------------------

## 1. Python Intorduction ##
  - Python is a very polpular language now a days. This language is used in every areas like AI/ML, Data Analytics, Web-Devlopment, Mobile Apps Development, e.t.c.
  - Currently Python latest version is version 3.
  - Python is platform independent.
  - Python is a dynamic, interpreted (bytecode-compiled) language. There are no type declarations of variables, parameters, functions, or methods in source code. This makes the code short and flexible, and you lose the compile-time type checking of the source code.
  - Python tracks the types of all values at runtime and flags code that does not make sense as it runs. 
  - Python source files use the ".py" extension and are called "modules."


## 2. Python Setup ##

## 3. Python Comments ##

## 4. Python DataTypes ##

## 5. Python Basics ##

## 6. Python String ##
  - Python has in-built class for string operations know as 'str'.
  - String literals can be enclosed by either double or single quotes, although single quotes are more commonly used. 
  - Backslash escapes work the usual way within both single and double quoted literals -- e.g. \n \' \".
  - Python strings are "immutable" which means they cannot be changed after they are created
  - A Double quote string can contains single quote and vice-versa.
      
        e.g.: "This is 'red' pen".
              'This is "green" pen'.
  - A string literal can span multiple lines, but there must be a backslash **(\)** at the end of each line to escape the newline.
  
        e.g.: To print "This is my tutorials" in different line.
        
            print("This \
                    is my \
                    tutorials")
   - String literals inside triple quotes, """ or ''', can span multiple lines of text.
   
          e.g.: if we want to print the some sentence in multiple line the  we've to use either """ or '''.
          
                print("""This 
                        is my
                        tutorials""")
                
                Output: This
                        is my
                        turorials
   - A "raw" string literal is prefixed by an 'r' and passes all the chars through without special treatment of backslashes.
    
          e.g.: r'x\nx' evaluates to the length-4 string 'x\nx'.
          
   - A 'u' prefix allows you to write a unicode string literal.
   
   - Python doesn't have **char** type. So if s[0] = 'A' means this will be treated as a string only with 1-length-string and all the string functions will be applicable on this.
   
   
   - **String Functions.**
      
      1. **_str()_** function: This function convert any data type into string datatype.
        
              e.g.: print( "Hello" + 2) : gives an error
                    print( "Hello" + str(2) ): correct
                    
      2. **_len()_** function: This functions returns the length(number of character) in the given string.
      
              e.g.: var = "India"
                    print( len(var) ) : 5
      
      3. **_[]_** operator: We can access the string with index directory.
      
              e.g.: var = "Hello"
                    var[0] = 'H'
                    var[3] = 'l'
                    
      4. **_s.lower(), s.upper()_**: returns the lowercase or uppercase version of the string.
      
      5. **_s.strip()_**: returns a string with whitespace removed from the start and end.
      
      6. **_s.isalpha()/s.isdigit()/s.isspace()..._**: tests if all the string chars are in the various character classes.
      
      7. **_s.startswith('other'), s.endswith('other')__**:tests if the string starts or ends with the given other string.
      
      8. **_s.find('other')_**: searches for the given other string (not a regular expression) within s, and returns the first index where it begins or -1 if not found.
      
      9. **_s.replace('old', 'new')_**: returns a string where all occurrences of 'old' have been replaced by 'new' .
      
      10. **_s.split('delim')_**: returns a **list of subsstring** separated by the given delimiter. The delimiter is not a regular expression, it's just text.
      As a convenient special case s.split() (with no arguments) splits on all whitespace chars.
      
              e.g.:  'aaa.bbb.ccc'.split('.') --> ['aaa', 'bbb', 'ccc']
              
      
      11. **_s.join(list)_**: opposite of split(), joins the elements in the given list together using the string as the delimiter.
      
              e.g.: '.'.join(['aaa','bbb','ccc']) --> 'aaa.bbb.ccc'
              
      
      12. **_String slices()_**:
  
        - a. The "slice" syntax is a handy way to refer to sub-parts of sequences -- typically strings and lists.
        - b. The slice string[start:end] is the elements beginning at start and extending up to but not including end.
        - c. For Example: 
        
                var = "Hello World"  --> [H|e|l|l|o| |w|o|r|l|d|]
                                          0 1 2 3 4 5 6 7 8 9 10
                                        -11-10-9-8-7-6-5-4-3-2-1
                        
                var[0,2] = "He"
                var[1:] = "ello world"
                var[:] = "Hello world"  ==> gives a copy of string
                var[2:10000] = "llo world" ==> if end string lenght specfied which does not exists in real, then python just consider the lenght till the string and rest will be auto turncated.
                
                var[-1] = "d" ==> Last character in the string.
                var[-4] = "o" ==> 4th from last position in the string.
                var[:-3] = 'He' ==> starts with 0th index and goes upto -3(i.e. from last to strat in the string but excluding the last indexing).
                var[-3:] = 'ld' ==> starts from -3 to goes last index(postive) of string. since the index default considered as +ve. hence -3 to last.
                
      13. **_String %_**: 
          
        - a. Python has a printf()-like facility to put together a string. 
        - b. The % operator takes a printf-type format string on the left. Like:  (%d int, %s string, %f/%g floating point).
        - c. The matching values in a tuple on the right by comma separated.
            
              e.g.: text = "%d little pigs come out or I'll %s and %s and %s" % (3, 'huff', 'puff', 'blow down')
                    print(text):
                    3 little pigs come out or I'll huff and puff and blow down
              
      14. **_i18n Strings (Unicode)_**:
       
        - a. To create a unicode string just prefix the string with 'u' character.
        - b. For example:
              
                e.g.: text = u'A unicode \u018e string \xf1'
                      print(text): u'A unicode \u018e string \xf1'
        - c. Regular expressions works exaclty correct manner if passed a unicode string.
        - d. To Convert a unicode string to byte, just pass the **utf-8** in encoding and vice-versa.
        
        - For example: 
        
                e.g.: ## (ustring from above contains a unicode string)
                      > s = ustring.encode('utf-8')
                      > s
                      'A unicode \xc6\x8e string \xc3\xb1'  ## bytes of utf-8 encoding
                      > t = unicode(s, 'utf-8')             ## Convert bytes back to a unicode string
                      > t == ustring                      ## It's the same as the original, yay!

                      True
        

      
      
## 7. Python File Operation ##
  - Python has great support for File I/O operations. It has in built OS library which allows much better flexibility to work with files system.
  - When we want to read from or write to a file we need to open it first. When we are done, it needs to be closed, so that resources that are tied with the file are freed.
  - Hence, in Python, a file operation takes place in the following order.
    - **1. Open a file.**
    - **2. read/write (perform operation)**
    - **3. close the file.**
    
  - **_Open a file_**:
    - To a file we use **Open()** in built method.
    - The Open() methods expects one to max two arguments.
      
    - **open("fileName", "mode[Optional]")** or **open("fileName",mode = 'r',encoding = 'utf-8')**:
          
    - It should be abosulte path to the filename.                             
    - If the file doesn't exists in the directory then python will throw IOError: No Such file or directory.
    - Mode is Optional. we can file in read/write or append mode.
    - ByDefault the files gets opened in text mode only. In this mode we will get string reading from file.
    - On the other hand, binary mode returns bytes and this is the mode to be used when dealing with non-text files like image or exe files.
    - Below are the modes available in the python:
    
    ---------------------------------------------------------------------------------------------------------
    
      - **'r'** 	Open a file for reading. (default)
      - **'w'** 	Open a file for writing. Creates a new file if it does not exist or truncates(deletes all the existing file contents) the file if it exists.
      - **'x'** 	Open a file for exclusive creation. If the file already exists, the operation fails.
      - **'a'** 	Open for appending at the end of the file without truncating it. Creates a new file if it does not exist.
      - **'t'** 	Open in text mode. (default)
      - **'b'** 	Open in binary mode.
      - **'+'** 	Open a file for updating (reading and writing)
    
      - **rb**    Opens a file for reading only in binary format. The file pointer is placed at the beginning of the file. This is the default mode.
      - **r+**    Opens a file for both reading and writing. The file pointer placed at the beginning of the file.
      - **rb+**   Opens a file for both reading and writing in binary format. The file pointer placed at the beginning of the file.
      - **wb**    Opens a file for writing only in binary format. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing.
      - **w+**    Opens a file for both writing and reading. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing.
      - **ab+**   Opens a file for both appending and reading in binary format. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing.
    
    -----------------------------------------------------------------------------------------------------------
    
          e.g.: 
                f = open("test.txt")      # equivalent to 'r' or 'rt'
                f = open("test.txt",'w')  # write in text mode
                f = open("img.bmp",'r+b') # read and write in binary mode

    
    - Unlike other languages, the character 'a' does not imply the number 97 until it is encoded using ASCII (or other equivalent encodings).
    - Hence, when working with files in text mode, it is highly recommended to specify the encoding type.
    
          f = open("test.txt",mode = 'r',encoding = 'utf-8')
          
  - **_close()_ a file**
  
    - When we are done with operations to the file, we need to properly close the file.
    - Closing a file will free up the resources that were tied with the file and is done using Python close() method.
    - Python has a garbage collector to clean up unreferenced objects but, we must not rely on it to close the file.
    
            f = open("test.txt",encoding = 'utf-8')
              # perform file operations
            f.close()
    - This method is not entirely safe. If an exception occurs when we are performing some operation with the file, the code exits without closing the file.
    - A safer way is to use a try...finally block.
   
            try:
               f = open("test.txt",encoding = 'utf-8')
               # perform file operations
            finally:
               f.close()
            
            #This way, we are guaranteed that the file is properly closed even if an exception is raised, causing program flow to stop.
               
    -  The best way to do this is using the **with statement**. This ensures that the **file is closed when the block inside _with_ is exited**.
    
            with open("test.txt",encoding = 'utf-8') as f:
            # perform file operations
    
  - **_Write()_ a file**:
    - To write file we need to open file with mode 'w' or 'a' or exclusive creation mode'x'.
    - We need to be careful with the 'w' mode as it will overwrite into the file if it already exists.
    - All the previous data will be erased if it open with mode 'w'.
    - Writing a string or sequence of bytes (for binary files) is done using write() method.
    - Write() method returns the number of characters written to the file.
    
            with open("test.txt",'w',encoding = 'utf-8') as f:
              f.write("my first file\n")
              f.write("This file\n\n")
              f.write("contains three lines\n")
            
            - This program will create a new file named 'test.txt' if it does not exist. If it does exist, it is overwritten.
             
    - We must include the newline characters ourselves to distinguish different lines.

- **_read()_ a file**:
  - To read a file in Python, we must open the file in reading mode.
        
          >>> f = open("test.txt",'r',encoding = 'utf-8')
          >>> f.read(4)    # read the first 4 data
          'This'

          >>> f.read(4)    # read the next 4 data
          ' is '

          >>> f.read()     # read in the rest till end of file
          'my first file\nThis file\ncontains three lines\n'

          >>> f.read() 
          
   - read() method returns _newline_as '\n'.
   - once we reach end of the line in the file, we will get empty string in further reading.
   - We can change our current file cursor (position) using the **seek()** method.
          
          >>> f.seek(0)   # bring file cursor to initial position
          0
    
    - The **tell() method** returns our current position (in number of bytes).
    
          >>> f.tell()    # get the current file position
          56
          
          >>> print(f.read())  # read the entire file
          This is my first file
          This file
          contains three lines
          
    - we can use **readline()** method to read individual lines of a file. 
    - This method reads a file till the newline, including the newline character.
    - The readlines() method returns a list of remaining lines of the entire file.
    
          >>> f.readlines()
          ['This is my first file\n', 'This file\n', 'contains three lines\n']


- **_Python File Methods_**:
  
  ---------------------------------------------------------------------------------------------------------------------------
     - **close()** 	                    Close an open file. It has no effect if the file is already closed.
     - **detach()** 	                  Separate the underlying binary buffer from the TextIOBase and return it.
     - **fileno()** 	                  Return an integer number (file descriptor) of the file.
     - **flush()** 	                    Flush the write buffer of the file stream.
     - **isatty()** 	                  Return True if the file stream is interactive.
     - **read(n)** 	                    Read atmost n characters form the file. Reads till end of file if it is negative or None.
     - **readable()** 	                Returns True if the file stream can be read from.
     - **readline(n=-1)** 	            Read and return one line from the file. Reads in at most n bytes if specified.
     - **readlines(n=-1)** 	            Read and return a list of lines from the file. Reads in at most n bytes/characters if specified.
     - **seek(offset,from=SEEK_SET)** 	Change the file position to offset bytes, in reference to from (start, current, end).
     - **seekable()** 	                Returns True if the file stream supports random access.
     - **tell()** 	                    Returns the current file location.
     - **truncate(size=None)** 	        Resize the file stream to size bytes. If size is not specified, resize to current location.
     - **writable()** 	                Returns True if the file stream can be written to.
     - **write(s)**  	                  Write string s to the file and return the number of characters written.
     -**writelines(lines)** 	          Write a list of lines to the file.

----------------------------------------------------------------------------------------------------------------------------
   
## 8. Python Collection ##

## 9. Python Exceptions Handling ##

## 10. Python Regular Expression ##

## 11. Python Object Oriented Programming ##

## 12. Python Importaint Libraries ##

## 13. Python Networking ##
