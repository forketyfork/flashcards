START
Basic
Front: Why does IDEA need a boot runtime? How to switch IDEA to a different runtime? How to switch it back if it crashes after? Where is this setting stored? How to set it via an environment variable?
Back: 
IDEA is a Java application and therefore needs a JRE. JetBrains Runtime (JBR) is a fork of OpenJDK and is bundled with IDEA. It fixes some known issues and provides better performance and stability.
To change, press ⌘+⇧+A, choose "Choose Boot Java Runtime for the IDE..." and select a runtime. Click "Use Default Runtime" to reset.
The path is stored in the IDEA configuration directory, in the `idea.jdk` or `idea64.jdk` file. Remove it to reset to the default value.
You can also override this path with the `IDEA_JDK` environment variable.

See https://www.jetbrains.com/help/idea/switching-boot-jdk.html
<!--ID: 1745136966273-->
END
