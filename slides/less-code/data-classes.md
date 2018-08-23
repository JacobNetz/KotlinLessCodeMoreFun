### Data Classes

<table style="margin-left:-10%">
    <tr>
        <td style="padding:0">
             <pre>
                <code class="lang-java hljs">//Java
public class Person {
    private final String first;
    private final String last;
    private int age;

    public Person(String first, String last, int age) {
        this.first = first;
        this.last = last;
        this.age = age;
    }

    public String getFirst() {
        return first;
    }

    public String getLast() {
        return last;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}    
                </code>
            </pre>
        </td>
        <td style="padding:0">
            <pre>
                <code class="lang-csharp hljs">//C#
public class Person
{
    public string First { get; }
    public string Last { get; }
    public int Age { get; set; }
    
    public Person(string first, string last, int age)
    {
        First = first;
        Last = last;
        Age = age;
    }
}
                </code>
            </pre>
        </td>
    </tr>
</table>

```kotlin
// Kotlin
data class Person(val first: String, val last: String, var age: Int)
```

Note:
+ Compiler automatically creates:
    + `equals()` and `hashCode()`
    + `toString()` -> `Person(first=Michael, last=Fazio, age=33)`
    + `componentN()` functions in order of declaration
        + e.g. val first = person.component1(), val age = person.component3()
+ Cannot be `abstract`, `open`, `sealed`, or `inner`
     