Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar contraseñas:

### Contraseñas:

**regex**
```regex
RegexPassword: /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let passwordRegex = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$/;

// Ejemplo de uso:
let password = "Password123";
if (passwordRegex.test(password)) {
    console.log("Contraseña válida");
} else {
    console.log("Contraseña inválida");
}
```

**Python:**
```python
import re

password_regex = r'^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$'

# Ejemplo de uso:
password = "Password123"
if re.match(password_regex, password):
    print("Contraseña válida")
else:
    print("Contraseña inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String passwordRegex = "^(?=.*\\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$";
        Pattern pattern = Pattern.compile(passwordRegex);

        // Ejemplo de uso:
        String password = "Password123";
        Matcher matcher = pattern.matcher(password);
        if (matcher.matches()) {
            System.out.println("Contraseña válida");
        } else {
            System.out.println("Contraseña inválida");
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
        string passwordRegex = @"^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$";
        Regex regex = new Regex(passwordRegex);

        // Ejemplo de uso:
        string password = "Password123";
        if (regex.IsMatch(password))
        {
            Console.WriteLine("Contraseña válida");
        }
        else
        {
            Console.WriteLine("Contraseña inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar contraseñas utilizando expresiones regulares en varios lenguajes de programación.