Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar nombres de archivos:

### Nombres de Archivos:

**regex**
```regex
RegexFilename: /^[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*\.[a-zA-Z]{2,4}$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let filenameRegex = /^[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*\.[a-zA-Z]{2,4}$/;

// Ejemplo de uso:
let filename = "example-file.txt";
if (filenameRegex.test(filename)) {
    console.log("Nombre de archivo válido");
} else {
    console.log("Nombre de archivo inválido");
}
```

**Python:**
```python
import re

filename_regex = r'^[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*\.[a-zA-Z]{2,4}$'

# Ejemplo de uso:
filename = "example-file.txt"
if re.match(filename_regex, filename):
    print("Nombre de archivo válido")
else:
    print("Nombre de archivo inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String filenameRegex = "^[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*\\.[a-zA-Z]{2,4}$";
        Pattern pattern = Pattern.compile(filenameRegex);

        // Ejemplo de uso:
        String filename = "example-file.txt";
        Matcher matcher = pattern.matcher(filename);
        if (matcher.matches()) {
            System.out.println("Nombre de archivo válido");
        } else {
            System.out.println("Nombre de archivo inválido");
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
        string filenameRegex = @"^[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*\.[a-zA-Z]{2,4}$";
        Regex regex = new Regex(filenameRegex);

        // Ejemplo de uso:
        string filename = "example-file.txt";
        if (regex.IsMatch(filename))
        {
            Console.WriteLine("Nombre de archivo válido");
        }
        else
        {
            Console.WriteLine("Nombre de archivo inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar nombres de archivos utilizando expresiones regulares en varios lenguajes de programación.