Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar fechas:

### Fechas:

**regex**
```regex
RegexDate: /^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/(19|20)\d{2}$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
const dateRegex = /^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/(19|20)\d{2}$/;

// Ejemplo de uso:
let date = "12/31/2023";
if (dateRegex.test(date)) {
    console.log("Fecha válida");
} else {
    console.log("Fecha inválida");
}
```

**Python:**
```python
import re

date_regex = r'^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/(19|20)\d{2}$'

# Ejemplo de uso:
date = "12/31/2023"
if re.match(date_regex, date):
    print("Fecha válida")
else:
    print("Fecha inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String dateRegex = "^(0[1-9]|1[0-2])\\/(0[1-9]|[12][0-9]|3[01])\\/(19|20)\\d{2}$";
        Pattern pattern = Pattern.compile(dateRegex);

        // Ejemplo de uso:
        String date = "12/31/2023";
        Matcher matcher = pattern.matcher(date);
        if (matcher.matches()) {
            System.out.println("Fecha válida");
        } else {
            System.out.println("Fecha inválida");
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
        string dateRegex = @"^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/(19|20)\d{2}$";
        Regex regex = new Regex(dateRegex);

        // Ejemplo de uso:
        string date = "12/31/2023";
        if (regex.IsMatch(date))
        {
            Console.WriteLine("Fecha válida");
        }
        else
        {
            Console.WriteLine("Fecha inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar fechas utilizando expresiones regulares en varios lenguajes de programación.