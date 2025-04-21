START
Basic
Front: Describe the heap structure of G1 GC
Back: 
Fixed-size regions (2048 by default), each one representing a particular generation. Region size is power of 2 (1-32 MB), to increase GC process predictability.

- **eden** — new objects are created here
- **survivor**— objects that survived the 1st GC are moved here
- **old** — objects that survived the subsequent GCs are moved from survivor regions here
- **humongous** — at least 1/2 of such region is occupied by a "humongous object", this region may be comprised of multiple smaller regions
<!--ID: 1745138723654-->
END
