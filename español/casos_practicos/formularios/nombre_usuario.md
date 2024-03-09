Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar nombres de usuario:

### Nombres de Usuario:

**regex**
```regex
RegexUsername: /^[a-zA-Z0-9._-]{3,16}$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let usernameRegex = /^[a-zA-Z0-9._-]{3,16}$/;

// Ejemplo de uso:
let username = "user123";
if (usernameRegex.test(username)) {
    console.log("Nombre de usuario válido");
} else {
    console.log("Nombre de usuario inválido");
}
```

**Python:**
```python
import re

username_regex = r'^[a-zA-Z0-9._-]{3,16}$'

# Ejemplo de uso:
username = "user123"
if re.match(username_regex, username):
    print("Nombre de usuario válido")
else:
    print("Nombre de usuario inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String usernameRegex = "^[a-zA-Z0-9._-]{3,16}$";
        Pattern pattern = Pattern.compile(usernameRegex);

        // Ejemplo de uso:
        String username = "user123";
        Matcher matcher = pattern.matcher(username);
        if (matcher.matches()) {
            System.out.println("Nombre de usuario válido");
        } else {
            System.out.println("Nombre de usuario inválido");
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
        string usernameRegex = @"^[a-zA-Z0-9._-]{3,16}$";
        Regex regex = new Regex(usernameRegex);

        // Ejemplo de uso:
        string username = "user123";
        if (regex.IsMatch(username))
        {
            Console.WriteLine("Nombre de usuario válido");
        }
        else
        {
            Console.WriteLine("Nombre de usuario inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar nombres de usuario utilizando expresiones regulares en varios lenguajes de programación.