# CHANGE()

**Created At:** 9/19/2019 4:56:41 PM  
**Updated At:** 9/19/2019 10:06:14 PM  


```
CHANGE( variable, expression1, expression2 )
```



Where:

- **expression1** may evaluate to any result and is the string of characters that will be replaced,
- **expression2** may also evaluate to any result and is the string of characters that will replace**expression1**,
- **variable** may be any previously assigned variable in the program.




### Info

Either string can be of any length and is not required to be the same length. See also the [SWAP](/36868-jbase-basic/278849-swap) function.

The jBC language also supports the [CHANGE](/36868-jbase-basic/264325-change) statement.


An example of use is:

| `String1 = "Jim" String2 = "James" Variable = "Pick up the tab Jim" CRT CHANGE( Variable, String1, String2) CRT CHANGE( Variable, "tab", "check")`<br> |
| --- |




Go back to [jBASE BASIC](263498-jbase-basic).