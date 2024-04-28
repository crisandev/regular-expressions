Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar números de teléfono:

### Números de teléfono:

**regex**
```regex
RegexPhoneNumber: /^\+?\d{1,3}[\s-]?\(?\d{3}\)?[\s-]?\d{3}[\s-]?\d{4}$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
const phoneRegex = /^\+?\d{1,3}[\s-]?\(?\d{3}\)?[\s-]?\d{3}[\s-]?\d{4}$/;

// Ejemplo de uso:
let phoneNumber = "+1 (555) 123-4567";
if (phoneRegex.test(phoneNumber)) {
    console.log("Número de teléfono válido");
} else {
    console.log("Número de teléfono inválido");
}
```

**Python:**
```python
import re

phone_regex = r'^\+?\d{1,3}[\s-]?\(?\d{3}\)?[\s-]?\d{3}[\s-]?\d{4}$'

# Ejemplo de uso:
phone_number = "+1 (555) 123-4567"
if re.match(phone_regex, phone_number):
    print("Número de teléfono válido")
else:
    print("Número de teléfono inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String phoneRegex = "^\\+?\\d{1,3}[\\s-]?\\(?\\d{3}\\)?[\\s-]?\\d{3}[\\s-]?\\d{4}$";
        Pattern pattern = Pattern.compile(phoneRegex);

        // Ejemplo de uso:
        String phoneNumber = "+1 (555) 123-4567";
        Matcher matcher = pattern.matcher(phoneNumber);
        if (matcher.matches()) {
            System.out.println("Número de teléfono válido");
        } else {
            System.out.println("Número de teléfono inválido");
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
        string phoneRegex = @"^\+?\d{1,3}[\s-]?\(?\d{3}\)?[\s-]?\d{3}[\s-]?\d{4}$";
        Regex regex = new Regex(phoneRegex);

        // Ejemplo de uso:
        string phoneNumber = "+1 (555) 123-4567";
        if (regex.IsMatch(phoneNumber))
        {
            Console.WriteLine("Número de teléfono válido");
        }
        else
        {
            Console.WriteLine("Número de teléfono inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar números de teléfono utilizando expresiones regulares en varios lenguajes de programación.