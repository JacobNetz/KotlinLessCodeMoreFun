### Companion Objects

```kotlin
data class Team(val city: String, val name: String, var sport: Sport) {
    companion object {
        fun createBaseballTeam(city: String, name: String)
            = Team(city, name, Sport.Baseball)
    }
}

val cubs = Team.createBaseballTeam("Chicago", "Cubs")
```

```kotlin
interface Factory<T> {
    fun create(): T
}

class MyClass {
    companion object : Factory<MyClass> {
        override fun create(): MyClass = MyClass()
    }
}
```

Note:
+ Functions like static methods on a class
+ Can implement interfaces
