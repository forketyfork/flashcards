START
Basic
Front: What is G1GC? In which HotSpot version was G1 introduced? When was G1 made the default GC collector of HotSpot? What are the main design goals of G1GC?
Back: 
G1GC is a region-based generational GC.  
It was introduced in Java 6, supported from 7 update 4, made default in Java 9.  
Designed to replace CMS collector as a server-side GC.  
It's designed to keep GC pauses under the specified value while providing good throughput.
<!--ID: 1745138723650-->
END
