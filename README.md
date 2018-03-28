# JenkinsDocs
how to run powershell script via jenkins groovy script.
---
```groovy
import jenkins.model.Jenkins
def sout = new StringBuilder(), serr = new StringBuilder()
def proc = "Powershell.exe -ExecutionPolicy bypass -command get-psdrive".execute()
proc.consumeProcessOutput(sout, serr)
proc.waitForOrKill(1000)
println "out> $sout err> $serr"
```
