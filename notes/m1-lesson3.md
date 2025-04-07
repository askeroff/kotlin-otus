```kotlin
fun mapArray(a: List<Int>, b: (i: Int) -> Int) {
   for (item in a) {
      println(b(item))
   }
}

val a = listOf<Int>(1, 2, 3, 4)

// Lesson # 2
// lambdas : check
// higher order functions: check
```


# scope functions
```kotlin
//let: basically this is to create a block of code with separate scope that works on an object
   Person("Alice", 20, "Amsterdam").let {
      println(it)
      it.moveTo("London")
      it.incrementAge()
      println(it)
   }
```


**apply**: I think works as in javascript. it changes context of the 'this' value <br>
инлайн функции, инфкси и тейлрек скорее всего не нужны на начальных этапах точно. <br>
инфикс просто синтакс.сахар вместо .to убирает точку и делает a to b

# Ranges Диапазоны

```kotlin
val range1 = 1..5   // от 1 до 5 (включительно)
val range2 = 1 until 5  // от 1 до 4 (5 не включается)
val range3 = 10 downTo 1  // от 10 до 1 (в обратном порядке)
val range4 = 1..10 step 2  // от 1 до 10 с шагом 2
```

# Collections
Все могут быть mutable <br>

```kotlin
val list = listOf(1,2,3) // список может повторять элементы
val set = setOf(1,2,3) // уникальные элементы только
val map = mapOf("age" to 23) // пары ключ значение
```

## Обход коллекций

```kotlin
val items = listOf("apple", "banana", "cherry")

for (item in items) {
    println(item)
}

items.forEach { println(it) } // forEach с лямбда выражением и it


val userData = mapOf("id" to 1, "name" to "Alice")

for ((key, value) in userData) {
    println("$key: $value")
}

```

## Функциональные расширения для обхода коллекций

**Методы**: как и в js есть map, filter, forEach,find и т.д.
