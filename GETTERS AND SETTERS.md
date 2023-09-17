#OOP 
1. `get;`
    
    - Use `get;` when you want to create a read-only property, meaning it can only be read from but not written to.
    - The value of the property can only be set within the constructor or directly within the class.
    
2. `get; set;`
    
    - Use `get; set;` for a read-write property, where the property value can be both read and modified outside the class.
    - This provides the most open access to the property, allowing any code to read or write to it.
    
3. `get; private set;`
    
    - Use `get; private set;` for a property that can be read from any code, but only the class itself can modify the property value.
    - This pattern is useful when you want to expose the property's value without allowing external code to modify it directly.
    
4. `get; init;` (C# 9.0 and later)
    
    - Use `get; init;` for an immutable property, where the property value can be read from any code, but it can only be set during object initialization or within the class.
    - This is particularly useful when you want to set the property value at object creation and then ensure it cannot be changed afterward.