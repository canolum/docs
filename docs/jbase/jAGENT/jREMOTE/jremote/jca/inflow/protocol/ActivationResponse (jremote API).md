# ActivationResponse (jremote API)

**Created At:** 9/25/2017 12:02:01 PM  
**Updated At:** 4/4/2018 6:42:19 PM  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="ActivationResponse (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//--><br>var methods = {"i0":10,"i1":10,"i2":10,"i3":10,"i4":10};<br>var tabs = {65535:["t0","All Methods"],2:["t2","Instance Methods"],8:["t4","Concrete Methods"]};<br>var altColor = "altColor";<br>var rowColor = "rowColor";<br>var tableTab = "tableTab";<br>var activeTableTab = "activeTableTab";


## Class ActivationResponse

All Implemented Interfaces:[JBaseSerializable](/39250-io/com_jbase_jremote_io_jbaseserializable "interface in com.jbase.jremote.io")
* * *


```
public class ActivationResponse
extends Object
implements JBaseSerializable
```

The reply from JRemote when an activation is requested.

### Nested Class Summary

- Nested classes/interfaces inherited from interface com.jbase.jremote.io.JBaseSerializable
    - `JBaseSerializable.TYPE`






### Constructor Summary


| Constructor and Description<br> |
| --- |
| `ActivationResponse()` <br> |
| `ActivationResponse(byte[] message)` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `byte[]`<br> | `getMessage()` <br> |
| `int`<br> | `getType()` <br> |
| `int`<br> | `getVersion()` <br> |
| `void`<br> | `readObject(JBaseObjectReader reader, int version)` <br> |
| `void`<br> | `writeObject(JBaseObjectWriter writer, int version)` <br> |


- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`

### Constructor Detail



#### ActivationResponse

```
public ActivationResponse()
```



#### ActivationResponse

```
public ActivationResponse(byte[] message)
```





### 


### Method Detail



#### getType

```
public int getType()
```
Specified by:`getType` in interface `JBaseSerializable`Returns:type id of the objects, used during the serialization
#### readObject

```
public void readObject(JBaseObjectReader reader,
                       int version)
                throws IOException,
                       ClassNotFoundException
```
Specified by:`readObject` in interface `JBaseSerializable`Throws:`IOException``ClassNotFoundException`
#### writeObject

```
public void writeObject(JBaseObjectWriter writer,
                        int version)
                 throws IOException
```
Specified by:`writeObject` in interface `JBaseSerializable`Throws:`IOException`
#### getMessage

```
public byte[] getMessage()
```

#### getVersion

```
public int getVersion()
```
Specified by:`getVersion` in interface `JBaseSerializable`

Back to [jREMOTE API](com_jbase_jremote_package-summary)