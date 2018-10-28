# Python-3.x #

This Documents will explains alomst all the python concepts from zero level to advanced level. Every Chapter in this tutorials explains the concepts in very easy way and also provide the coding.

-------------------------------------------------------------------------------------------------------------------------------

[1. Python Intorduction](#1.-python-introduction)

[2. Python Setup](#2.-python-setup)

[3. Python Comments](#3.-python-comments)

[4. Python DataTypes](#4.-python-datatypes)

[5. Python Basics](#5.-python-basics)

  - [5.1 Command Line Arguments](#5.1.-command-line-arguments)
  - [5.2 Import Statements](#5.2.-import-statements)
  - [5.3 If-Else Statement](#5.3.-if-else-statement)
  - [5.4 Switch Statement](#5.4.-switch-statement)
  - [5.5 While Loop Statement](#5.5-while-loop-statement)
  - [5.6 For Loop Statement](#5.6.-for-loop-statement)  
  - [5.7 Functions](#5.7.-functions)
  - [5.8 Return](#5.8.-return)
  - [5.9 Continue](#5.9.-continue)
  - [5.10 Break](#5.10.-break)
  - [5.11 Pass](#5.11.-pass)

[6. Python String](#6.-python-string)

[7. Python File Operation](#7.-python-file-operation)

[8. Python Collection](#8.-python-colllection)

[9. Python Exceptions Handling](#9.-python-exception-handling)

[10. Python Regular Expression](#10.-python-regular-expression)

[11. Python Object Oriented Programming](#11.-python-object-oriented-programming)

[12. Python Importaint Libraries](#12.-python-importaint-libraries)

[13. Python Networking](#13.-python-networking)

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
      
      12 **_String slices()_**:
  
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
        -c. Regular expressions works exaclty correct manner if passed a unicode string.
        -d. To Convert a unicode string to byte, just pass the **utf-8** in encoding and vice-versa.
        
        - For example: 
        
                e.g.: ## (ustring from above contains a unicode string)
                      > s = ustring.encode('utf-8')
                      > s
                      'A unicode \xc6\x8e string \xc3\xb1'  ## bytes of utf-8 encoding
                      > t = unicode(s, 'utf-8')             ## Convert bytes back to a unicode string
                      > t == ustring                      ## It's the same as the original, yay!

                      True
        

      
      
## 7. Python File Operation ##


## 8. Python Collection ##

## 9. Python Exceptions Handling ##

## 10. Python Regular Expression ##

## 11. Python Object Oriented Programming ##

## 12. Python Importaint Libraries ##

## 13. Python Networking ##
