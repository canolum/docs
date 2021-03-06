# READXML

<PageHeader />

## Description

This function reads a record and from it, outputs the data retrieved in XML format. The style sheet held in DICT-&gt;@READXML is used to transform the data.

If the file to be read is composed of customer information, this can be illustrated as:

```
READ rec FROM file,id THEN
    CRT rec
END
```

to output a record for instance:

```
Clive^Pipenslippers^999 Letsbe Avenue
```

or

```
READXML xml FROM file,id THEN
    CRT xml
END
```

to output for instance:

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<mycustomer>
<firstname>Clive</firstname>
<lastname>Pipenslippers</lastname>
<address>999 Letsbe Avenue</address>
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
