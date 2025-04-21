START
Basic
Front: Describe the types of GC under G1
Back: 
- **Young GC** — only young generation, STW; the regions with the greatest amount of garbage are collected first (hence G1 = "garbage first"). The pause is limited (by default, 10% of application time)
- **Mixed GC** — Young GC + at least one old region
- **Full GC** — cleanup of the whole heap space, if Mixed GC didn't reclaim enough memory
<!--ID: 1745138723651-->
END
