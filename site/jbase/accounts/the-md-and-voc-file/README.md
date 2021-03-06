# The MD/VOC File

<PageHeader />

## Description

The jBASE MD (or VOC) file is used to find jQL modifiers and resolve Q-pointer filenames, the jSHELL also uses the MD file to lookup jCL programs. The location of the jBASE MD file is determined by the **JEDIFILENAME\_MD** environment variable. This environment variable is usually set-up in the .profile script when the user logs on. If the environment variable is not set-up then the default path $HOME/MD is used when attempting to open the jBASE MD file. Most accounts/user directories have an MD file specific to that account/user directory.

If users wish to use an MD and the MD file does not already exist then the user should use the jBASE CREATE-FILE command to create a single level dictionary file as:

```
CREATE-FILE DICT MD 3
```

The modulo of the MD file should be increased depending on the number of jCL programs and Q-pointers it is expected to contain. In order to use the jQL modifiers such as SORT and SELECT then the jQL modifiers should be copied into the new MD file. This can be achieved using a jBASE script called **UpdateMD** as:

```
UpdateMD
```

or by copying from the jBASE release directory file; /opt/jbase/CurrentVersion/src/MD on UNIX, and \jBASE\CurrentVersion\src\MD on Windows.

Short jCL programs are usually placed in the MD file to action other jCL programs in a different file and/or action cataloged jBC programs for instance an APPL Account startup jCL program.

```
PQ jCL type identifier.
[PROCS APPL.CHK] jCL external routine, APPL.CHK.
HAPPL.INIT jBC cataloged program,APPL.INIT.
P
```

The MD file should be kept as a single level dictionary file to avoid confusion. The real filename is actually: ./MD]D (or .\MD]D on Windows). All single level dictionary files contain a reflexive Q-pointer entry of the same name as the filename without the appended ]D, for DICT. e.g. The reflexive Q-pointer entry in the ./MD]D file is MD, therefore the following jBASE copy command will copy the same record from the same file to the terminal.

```
CT MD MD
```

will yield the same as:

```
CT MD]D MD
```

Back to [Accounts](./../README.md)

<PageFooter />
