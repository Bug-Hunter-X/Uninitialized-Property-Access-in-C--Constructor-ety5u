# Uninitialized Property Access in C# Constructor

This repository demonstrates a common error in C#: accessing a property before it's properly initialized within a constructor.  The `bug.cs` file shows the problematic code, while `bugSolution.cs` provides a corrected version.

**Problem:**
When an object of `MyClass` is created, `MyProperty` is accessed before it's assigned a value in the constructor. This leads to an unpredictable state or, in some cases, a `NullReferenceException` if the property involves referencing another object.

**Solution:**
The solution involves initializing `MyProperty` within the constructor's body before any other code that might access it. This ensures a well-defined and predictable state for the object upon creation.