START
Basic
Front: 
How to make the plugin depend on classes from another plugin?
If you get `java.lang.NoClassDevFoundError` at runtime for your plugin, what does that mean?
How to find an ID of a bundled plugin? An external plugin?
Back: 
To make the plugin depend on classes from other plugins:
1. Locate plugin ID
2. Set up the project
3. Add a declaration to `plugin.xml`
If you get `java.lang.NoClassDefFoundError` at runtime, most likely you've forgot to add the declaration to `plugin.xml`.
To find an ID of a bundled plugin, run the `listBundledPlugins` task. For external plugins, 
Reference: https://plugins.jetbrains.com/docs/intellij/plugin-dependencies.html#1-locating-plugin-id-and-preparing-sandbox
<!--ID: 1745136966269-->
END
