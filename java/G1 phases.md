START
Basic
Front: Describe the G1 garbage collection phases. Which of them are STW, which of them are concurrent?
Back: 
- **initial mark** (STW) — performed together with Young GC, finds and marks S regions containing references to the O regions
- **root region scanning** — scanning S regions to mark objects with references to O regions
- **concurrent marking** — scan and search live objects in the entire heap
- **remark** (STW) — additional search of live objects using SATB (snapshot at the beginning) algorithm to find **floating garbage** (objects live at the beginning of concurrent marking but not reachable anymore)
- **cleanup** (partly STW) — accounting live objects and free regions; resetting empty regions to include them in the free region list.
- **copying** (STW) — live objects are evacuated (copied) into new unused regions, this is performed with both Y and O generations.
<!--ID: 1745138723653-->
END
