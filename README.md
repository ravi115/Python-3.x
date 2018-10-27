# Python-3.x

This Documents will explains alomst all the python concepts from zero level to advanced level. Every Chapter in this tutorials explains the concepts in very easy way and also provide the coding.

[1. Python Intorduction](#1.-python-introduction)

[2. Python Setup](#2.-python-setup)

[3. Python Comments](#3.-python-comments)

[4. Python DataTypes](#4.-python-datatypes)

[5. Python Basics](#5.-python-basics)

  [5.1 Command Line Arguments](#5.1.-command-line-arguments)
  [5.2 Import Statements](#5.2.-import statements)
  [5.3 If-Else Statement](#5.3.-if-else-statement)
  [5.4 Switch Statement](#5.4.-switch-statement)
  [5.5 While Loop Statement](#5.5-while-loop-statement)
  [5.6 For Loop Statement](#5.6.-for-loop-statement)  
  [5.7 Functions](#5.7.-functions)
  [5.8 Return](#5.8.-return)
  [5.9 Continue](#5.9.-continue)
  [5.10 Break](#5.10.-break)
  [5.11 Pass](#5.11.-pass)

[6. Python String](#6.-python-string)

[7. Python File Operation](#7.-python-file-operation)

[8. Python Collection](#8.-python-colllection)

[9. Python Exceptions Handling](#9.-python-exception-handling)

[10. Python Regular Expression](#10.-python-regular-expression)

[11. Python Object Oriented Programming](#11.-python-object-oriented-programming)

[12. Python Importaint Libraries](#12.-python-importaint-libraries)

[13. Python Networking](#13.-python-networking)



### 1. Python Intorduction
  - Python is a very polpular language now a days. This language is used in every areas like AI/ML, Data Analytics, Web-Devlopment, Mobile Apps Development, e.t.c.
  - Currently Python latest version is version 3.
  - Python is platform independent.
  - Python is a dynamic, interpreted (bytecode-compiled) language. There are no type declarations of variables, parameters, functions, or methods in source code. This makes the code short and flexible, and you lose the compile-time type checking of the source code.
  - Python tracks the types of all values at runtime and flags code that does not make sense as it runs. 
  - Python source files use the ".py" extension and are called "modules."


### 2. Python Setup

### 3. Python Comments

### 4. Python DataTypes

### 5. Python Basics

### 6. Python String
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
      
              e.g.: '.'join(['aaa','bbb','ccc']) --> 'aaa.bbb.ccc'
      
      12 **_String slices()_**:
      
        a.
        b.
         
              
      
      
### 7. Python File Operation


### 8. Python Collection

### 9. Python Exceptions Handling

### 10. Python Regular Expression

### 11. Python Object Oriented Programming

### 12. Python Importaint Libraries

### 13. Python Networking
