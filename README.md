# log4j-issue

Step to run the code

```
mvn clean package
java -DenableLogback=true -Dlog4j2.configurationFile=src/config/log4j2.xml -jar log4j-issue-test.jar
```

when I use "maven-assembly-plugin" 3.6.0, it show me correct log
```
2024-08-22 11:07:13,284582| INFO|TID=1|main|Main:|Hello world!
```

When I update to "maven-assembly-plugin" to 3.7.0 / 3.7.1, it will show me uncorrect log

```
ERROR StatusLogger Unrecognized format specifier [d]
ERROR StatusLogger Unrecognized conversion specifier [d] starting at position 16 in conversion pattern.
ERROR StatusLogger Unrecognized format specifier [thread]
ERROR StatusLogger Unrecognized conversion specifier [thread] starting at position 25 in conversion pattern.
ERROR StatusLogger Unrecognized format specifier [level]
ERROR StatusLogger Unrecognized conversion specifier [level] starting at position 35 in conversion pattern.
ERROR StatusLogger Unrecognized format specifier [logger]
ERROR StatusLogger Unrecognized conversion specifier [logger] starting at position 47 in conversion pattern.
ERROR StatusLogger Unrecognized format specifier [msg]
ERROR StatusLogger Unrecognized conversion specifier [msg] starting at position 54 in conversion pattern.
ERROR StatusLogger Unrecognized format specifier [n]
ERROR StatusLogger Unrecognized conversion specifier [n] starting at position 56 in conversion pattern.
ERROR StatusLogger Reconfiguration failed: No configuration found for '2a139a55' at 'null' in 'null'
```