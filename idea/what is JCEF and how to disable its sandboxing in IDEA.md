START
Basic
Front: What is JCEF and how to disable its sandboxing in IDEA?
Back: JCEF is Java Chromium Embedded Framework, it's a framework for embedding Chromium-based browsers into Java applications. IDEA uses it e.g. for Markdown rendering, among other things.
Some features are available in the sandboxing mode, but it might cause issues in IDEA. To disable it, set `ide.browser.jcef.sandbox.enable=false`.
<!--ID: 1745136966266-->
END
