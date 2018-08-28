### Java/C# Has These, Kotlin Does Not

+ Ternary-operator (`a ? b : c`)
+ Checked exceptions
+ Primitive types that are not classes
+ Static members
+ Non-private fields

Note:
+ Ternary replacement: `if` works just fine
    + If can be be either expression or statement
    + `val max = if (a < b) b else a`
+ Checked exceptions lead to useless `try...catch` blocks
+ Instead of static members, use package-level functions
    + Also can use object declarations or companion objects
+ Use properties instead of fields
    + Can't declare fields, only ref them inside accessors 
    + Still have private, protected, internal and public modifiers available, just not to fields

