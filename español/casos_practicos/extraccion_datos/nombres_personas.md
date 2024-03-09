Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar nombres de personas:

### Nombres de Personas:

**regex**
```regex
RegexPersonName: /^[a-zA-Z]+(([',. -][a-zA-Z ])?[a-zA-Z]*)*$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let personNameRegex = /^[a-zA-Z]+(([',. -][a-zA-Z ])?[a-zA-Z]*)*$/;

// Ejemplo de uso:
let name = "John Doe";
if (personNameRegex.test(name)) {
    console.log("Nombre de persona válido");
} else {
    console.log("Nombre de persona inválido");
}
```

**Python:**
```python
import re

person_name_regex = r'^[a-zA-Z]+(([\',. -][a-zA-Z ])?[a-zA-Z]*)*$'

# Ejemplo de uso:
name = "John Doe"
if re.match(person_name_regex, name):
    print("Nombre de persona válido")
else:
    print("Nombre de persona inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String personNameRegex = "^[a-zA-Z]+(([',. -][a-zA-Z ])?[a-zA-Z]*)*$";
        Pattern pattern = Pattern.compile(personNameRegex);

        // Ejemplo de uso:
        String name = "John Doe";
        Matcher matcher = pattern.matcher(name);
        if (matcher.matches()) {
            System.out.println("Nombre de persona válido");
        } else {
            System.out.println("Nombre de persona inválido");
        }
    }
}
```

**C#:**
```csharp
using System;
using System.Text.RegularExpressions;

class Program
{
    static void Main()
    {
        string personNameRegex = @"^[a-zA-Z]+(([',. -][a-zA-Z ])?[a-zA-Z]*)*$";
        Regex regex = new Regex(personNameRegex);

        // Ejemplo de uso:
        string name = "John Doe";
        if (regex.IsMatch(name))
        {
            Console.WriteLine("Nombre de persona válido");
        }
        else
        {
            Console.WriteLine("Nombre de persona inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar nombres de personas utilizando expresiones regulares en varios lenguajes de programación.