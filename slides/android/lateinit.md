### Kotlin on Android
#### `lateinit`

```kotlin
private lateinit var logo: ImageView
...
this.logo = this.findViewById<ImageView>(R.id.logo)
```

```kotlin
public class MyTest {
    lateinit var subject: TestSubject

    @SetUp fun setup() {
        subject = TestSubject()
    }

    @Test fun test() {
        subject.method()  // dereference directly
    }
}
```

Note:
+ lateinit allows initializing a non-null property outside of a constructor
    + Also useful in depedency injection or testing