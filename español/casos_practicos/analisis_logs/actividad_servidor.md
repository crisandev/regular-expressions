Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar la actividad del servidor:

### Actividad del Servidor:

**regex**
```regex
RegexServerActivity: ^\[(INFO|ERROR|WARNING)\] .+$
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let serverActivityRegex = /^\[(INFO|ERROR|WARNING)\] .+$/;

// Ejemplo de uso:
let activity = "[INFO] Server started";
if (serverActivityRegex.test(activity)) {
    console.log("Actividad del servidor válida");
} else {
    console.log("Actividad del servidor inválida");
}
```

**Python:**
```python
import re

server_activity_regex = r'^\[(INFO|ERROR|WARNING)\] .+$'

# Ejemplo de uso:
activity = "[INFO] Server started"
if re.match(server_activity_regex, activity):
    print("Actividad del servidor válida")
else:
    print("Actividad del servidor inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String serverActivityRegex = "^\\[(INFO|ERROR|WARNING)\\] .+$";
        Pattern pattern = Pattern.compile(serverActivityRegex);

        // Ejemplo de uso:
        String activity = "[INFO] Server started";
        Matcher matcher = pattern.matcher(activity);
        if (matcher.matches()) {
            System.out.println("Actividad del servidor válida");
        } else {
            System.out.println("Actividad del servidor inválida");
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
        string serverActivityRegex = @"^\[(INFO|ERROR|WARNING)\] .+$";
        Regex regex = new Regex(serverActivityRegex);

        // Ejemplo de uso:
        string activity = "[INFO] Server started";
        if (regex.IsMatch(activity))
        {
            Console.WriteLine("Actividad del servidor válida");
        }
        else
        {
            Console.WriteLine("Actividad del servidor inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar la actividad del servidor utilizando expresiones regulares en varios lenguajes de programación.