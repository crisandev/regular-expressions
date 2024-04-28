Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar diferentes tipos de datos en formularios:

**Validación de Formularios:**

**Direcciones de correo electrónico:**
```regex
RegexEmail: /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/
```

Implementaciones en los lenguajes:

**JavaScript:**
```javascript
const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

// Ejemplo de uso:
let email = "example@example.com";
if (emailRegex.test(email)) {
    console.log("Correo electrónico válido");
} else {
    console.log("Correo electrónico inválido");
}
```

**Python:**
```python
import re

email_regex = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'

# Ejemplo de uso:
email = "example@example.com"
if re.match(email_regex, email):
    print("Correo electrónico válido")
else:
    print("Correo electrónico inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String emailRegex = "^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$";
        Pattern pattern = Pattern.compile(emailRegex);

        // Ejemplo de uso:
        String email = "example@example.com";
        Matcher matcher = pattern.matcher(email);
        if (matcher.matches()) {
            System.out.println("Correo electrónico válido");
        } else {
            System.out.println("Correo electrónico inválido");
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
        string emailRegex = @"^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$";
        Regex regex = new Regex(emailRegex);

        // Ejemplo de uso:
        string email = "example@example.com";
        if (regex.IsMatch(email))
        {
            Console.WriteLine("Correo electrónico válido");
        }
        else
        {
            Console.WriteLine("Correo electrónico inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar diferentes tipos de datos en formularios utilizando expresiones regulares en varios lenguajes de programación.