# SUBS

<PageHeader />

## Description

The **SUBS** function returns a dynamic array, the content of which is derived by subtracting each element of the second dynamic array argument from the corresponding element of the first dynamic array argument. It takes the general form:

```
SUBS(DynArr1, DynArr2)
```

Where:

**DynArr1** and **DynArr2** represent dynamic arrays.

Null elements of argument arrays are treated as zero. Otherwise, a non-numeric element in an argument array will cause a run-time error.

An example of use is as:

```
dynX = 1 : @VM : @VM : 5 : @VM : 8 : @SVM : 27 : @VM : 4
dynY = 1 : @VM : 5 : @VM : 8 : @VM : 70: @VM : 19

CRT SUBS(dynX, dynY)
```

to display:

```
0 ÿ -5 ÿ -3 ÿ -62 ü 27 ÿ -15
```

on the screen.

```
which is equivalent to:

0 : @VM : -5 : @VM : -3 : @VM : -62 : @SVM : 27 : @VM : -15
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
