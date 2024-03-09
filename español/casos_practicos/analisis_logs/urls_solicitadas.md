Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar URLs solicitadas:

### URLs Solicitadas:

**regex**
```regex
RegexURL: ^(?:GET|POST|PUT|DELETE) \S+ HTTP\/1\.[01]$
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let urlRegex = /^(?:GET|POST|PUT|DELETE) \S+ HTTP\/1\.[01]$/;

// Ejemplo de uso:
let url = "GET /example/path HTTP/1.1";
if (urlRegex.test(url)) {
    console.log("URL solicitada válida");
} else {
    console.log("URL solicitada inválida");
}
```

**Python:**
```python
import re

url_regex = r'^(?:GET|POST|PUT|DELETE) \S+ HTTP\/1\.[01]$'

# Ejemplo de uso:
url = "GET /example/path HTTP/1.1"
if re.match(url_regex, url):
    print("URL solicitada válida")
else:
    print("URL solicitada inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String urlRegex = "^(?:GET|POST|PUT|DELETE) \\S+ HTTP\\/1\\.[01]$";
        Pattern pattern = Pattern.compile(urlRegex);

        // Ejemplo de uso:
        String url = "GET /example/path HTTP/1.1";
        Matcher matcher = pattern.matcher(url);
        if (matcher.matches()) {
            System.out.println("URL solicitada válida");
        } else {
            System.out.println("URL solicitada inválida");
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
        string urlRegex = @"^(?:GET|POST|PUT|DELETE) \S+ HTTP\/1\.[01]$";
        Regex regex = new Regex(urlRegex);

        // Ejemplo de uso:
        string url = "GET /example/path HTTP/1.1";
        if (regex.IsMatch(url))
        {
            Console.WriteLine("URL solicitada válida");
        }
        else
        {
            Console.WriteLine("URL solicitada inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar URLs solicitadas utilizando expresiones regulares en varios lenguajes de programación.