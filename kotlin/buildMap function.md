START
Basic
Front: Describe Kotlin's **buildMap** function. What are the variants of this function? What are the properties of the returned map?
Back:
```
inline fun <K, V> buildMap(
    builderAction: MutableMap<K, V>.() -> Unit 
): Map<K, V> 
```

The function is defined in the **kotlin.collection** package of the **kotlin-stdlib** library. It builds a read-only map by populating a **MutableMap** using the given **builderAction** and returning a read-only map with the same key-value pairs. The mutable map is passed as a receiver to the **builderAction**.  
  
Entries of the map are iterated in the order they were added by the **builderAction**. The returned map is serializable (JVM).

A variant of this function accepts the **capacity** as the first argument, which hints the expected number of pairs added in the **builderAction**. If the capacity is negative, an **IllegalArgumentException** is thrown:

```
inline fun <K, V> buildMap(
	capacity: Int,
	builderAction: MutableMap<K, V>.() -> Unit 
): Map<K, V> 
```
  
Source: [https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/build-map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/build-map.html)
<!--ID: 1745138784662-->
END
