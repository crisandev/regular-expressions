
Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar códigos postales:

### Códigos postales:

**regex**
```regex
RegexPostalCode: /^\d{5}(?:[-\s]\d{4})?$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let postalCodeRegex = /^\d{5}(?:[-\s]\d{4})?$/;

// Ejemplo de uso:
let postalCode = "12345";
if (postalCodeRegex.test(postalCode)) {
    console.log("Código postal válido");
} else {
    console.log("Código postal inválido");
}
```

**Python:**
```python
import re

postal_code_regex = r'^\d{5}(?:[-\s]\d{4})?$'

# Ejemplo de uso:
postal_code = "12345"
if re.match(postal_code_regex, postal_code):
    print("Código postal válido")
else:
    print("Código postal inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String postalCodeRegex = "^\\d{5}(?:[-\\s]\\d{4})?$";
        Pattern pattern = Pattern.compile(postalCodeRegex);

        // Ejemplo de uso:
        String postalCode = "12345";
        Matcher matcher = pattern.matcher(postalCode);
        if (matcher.matches()) {
            System.out.println("Código postal válido");
        } else {
            System.out.println("Código postal inválido");
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
        string postalCodeRegex = @"^\d{5}(?:[-\s]\d{4})?$";
        Regex regex = new Regex(postalCodeRegex);

        // Ejemplo de uso:
        string postalCode = "12345";
        if (regex.IsMatch(postalCode))
        {
            Console.WriteLine("Código postal válido");
        }
        else
        {
            Console.WriteLine("Código postal inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar códigos postales utilizando expresiones regulares en varios lenguajes de programación.