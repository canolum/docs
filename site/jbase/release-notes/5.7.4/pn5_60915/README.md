# PN5_60915

<PageHeader />

## Description

Transaction Journaling: Prevent a segmentation violation when one of the log sets could not be accessed

### Previous Release Behavior

There are a number of reasons a log set defined for Transaction Journaling (TJ) might become unavailable. It might have been deleted. It might have permissions that the user doesn't have access for. In the circumstances, a suitable error message is displayed and logged to the TJ log file, but the program then continues and will quickly give a segmentation violation.

For example, one of the log sets was made inaccessible using **chmod a-w logset3** so nobody could open it.

```
$ COUNT LOGSET1
/home/jbase/logger/logset3: Permission denied

FATAL ERROR: From user  at Thu Sep 26 17:39:15 2019
Process ID 92398 , Port 0 , tty
    Unable to open logger file /home/jbase/logger/logset3

jBASE pid 92398: Segmentation violation. Aborting.

$
```

### Current Release Behavior

In these circumstances, the program no longer generates segmentation violations, but instead terminates cleanly

```
$ COUNT LOGSET1
/home/jbase/logger/logset3: Permission denied

FATAL ERROR: From user  at Thu Sep 26 17:46:38 2019
Process ID 92768 , Port 0 , tty
    Unable to open logger file /home/jbase/logger/logset3
TJLOG: No logger files exist
No file name could be found for your query
$
```

Back to [5.7.4 Release Notes](./../jbase-5.7.4-release-notes/README.md)
  
<PageFooter />
