Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar marcas de tiempo:

### Marcas de Tiempo:

**regex**
```regex
RegexTimestamp: /^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])T([01][0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])\.\d{3}Z$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let timestampRegex = /^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])T([01][0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])\.\d{3}Z$/;

// Ejemplo de uso:
let timestamp = "2024-02-27T08:30:45.123Z";
if (timestampRegex.test(timestamp)) {
    console.log("Marca de tiempo válida");
} else {
    console.log("Marca de tiempo inválida");
}
```

**Python:**
```python
import re

timestamp_regex = r'^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])T([01][0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])\.\d{3}Z$'

# Ejemplo de uso:
timestamp = "2024-02-27T08:30:45.123Z"
if re.match(timestamp_regex, timestamp):
    print("Marca de tiempo válida")
else:
    print("Marca de tiempo inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String timestampRegex = "^\\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])T([01][0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])\\.\\d{3}Z$";
        Pattern pattern = Pattern.compile(timestampRegex);

        // Ejemplo de uso:
        String timestamp = "2024-02-27T08:30:45.123Z";
        Matcher matcher = pattern.matcher(timestamp);
        if (matcher.matches()) {
            System.out.println("Marca de tiempo válida");
        } else {
            System.out.println("Marca de tiempo inválida");
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
        string timestampRegex = @"^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])T([01][0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])\.\d{3}Z$";
        Regex regex = new Regex(timestampRegex);

        // Ejemplo de uso:
        string timestamp = "2024-02-27T08:30:45.123Z";
        if (regex.IsMatch(timestamp))
        {
            Console.WriteLine("Marca de tiempo válida");
        }
        else
        {
            Console.WriteLine("Marca de tiempo inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar marcas de tiempo utilizando expresiones regulares en varios lenguajes de programación.