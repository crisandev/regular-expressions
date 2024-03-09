Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar URLs:

### URLs:

**regex**
```regex
RegexURL: /^(https?|ftp):\/\/[^\s\/$.?#].[^\s]*$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let urlRegex = /^(https?|ftp):\/\/[^\s\/$.?#].[^\s]*$/;

// Ejemplo de uso:
let url = "https://www.example.com";
if (urlRegex.test(url)) {
    console.log("URL válida");
} else {
    console.log("URL inválida");
}
```

**Python:**
```python
import re

url_regex = r'^(https?|ftp):\/\/[^\s\/$.?#].[^\s]*$'

# Ejemplo de uso:
url = "https://www.example.com"
if re.match(url_regex, url):
    print("URL válida")
else:
    print("URL inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String urlRegex = "^(https?|ftp):\\/\\/[^\\s\\/$.?#].[^\\s]*$";
        Pattern pattern = Pattern.compile(urlRegex);

        // Ejemplo de uso:
        String url = "https://www.example.com";
        Matcher matcher = pattern.matcher(url);
        if (matcher.matches()) {
            System.out.println("URL válida");
        } else {
            System.out.println("URL inválida");
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
        string urlRegex = @"^(https?|ftp):\/\/[^\s\/$.?#].[^\s]*$";
        Regex regex = new Regex(urlRegex);

        // Ejemplo de uso:
        string url = "https://www.example.com";
        if (regex.IsMatch(url))
        {
            Console.WriteLine("URL válida");
        }
        else
        {
            Console.WriteLine("URL inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar URLs utilizando expresiones regulares en varios lenguajes de programación.