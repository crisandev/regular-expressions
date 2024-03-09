Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar direcciones IP:

### Direcciones IP:

**regex**
```regex
RegexIPAddress: /^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let ipAddressRegex = /^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/;

// Ejemplo de uso:
let ipAddress = "192.168.1.1";
if (ipAddressRegex.test(ipAddress)) {
    console.log("Dirección IP válida");
} else {
    console.log("Dirección IP inválida");
}
```

**Python:**
```python
import re

ip_address_regex = r'^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$'

# Ejemplo de uso:
ip_address = "192.168.1.1"
if re.match(ip_address_regex, ip_address):
    print("Dirección IP válida")
else:
    print("Dirección IP inválida")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String ipAddressRegex = "^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$";
        Pattern pattern = Pattern.compile(ipAddressRegex);

        // Ejemplo de uso:
        String ipAddress = "192.168.1.1";
        Matcher matcher = pattern.matcher(ipAddress);
        if (matcher.matches()) {
            System.out.println("Dirección IP válida");
        } else {
            System.out.println("Dirección IP inválida");
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
        string ipAddressRegex = @"^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$";
        Regex regex = new Regex(ipAddressRegex);

        // Ejemplo de uso:
        string ipAddress = "192.168.1.1";
        if (regex.IsMatch(ipAddress))
        {
            Console.WriteLine("Dirección IP válida");
        }
        else
        {
            Console.WriteLine("Dirección IP inválida");
        }
    }
}
```

Estas implementaciones te permitirán validar direcciones IP utilizando expresiones regulares en varios lenguajes de programación.