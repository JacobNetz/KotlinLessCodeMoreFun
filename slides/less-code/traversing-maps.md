### Traversing Maps

```java
// Java
public void printTeams(Map<String, Team> teamMap) {
    for(Map.Entry<String, Team> entry : teamMap.entrySet()) {
        System.out.println(entry.getKey() + " - " + entry.getValue());
    }
}
```

```csharp
public void PrintTeams(Dictionary<string, Team> teamDictionary)
{
    // .NET Full Framework
    foreach (var entry in teamDictionary)
        Console.Out.WriteLine($"{entry.Key} - {entry.Value}");
    // .NET Core
    foreach (var (key, value) in teamDictionary)
        Console.Out.WriteLine($"{key} - {value}");
}
```

```kotlin
// Kotlin
fun printTeams(teamMap: Map<String, Team>) {
    for ((key, value) in teamMap) {
        println("$key - $value")
    }
}
```

Note:
+ Deconstructed declaration of the entry