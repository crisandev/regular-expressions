Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar precios:

### Precios:

**regex**
```regex
RegexPrice: /^\d+(\.\d{1,2})?$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
let priceRegex = /^\d+(\.\d{1,2})?$/;

// Ejemplo de uso:
let price = "10.99";
if (priceRegex.test(price)) {
    console.log("Precio válido");
} else {
    console.log("Precio inválido");
}
```

**Python:**
```python
import re

price_regex = r'^\d+(\.\d{1,2})?$'

# Ejemplo de uso:
price = "10.99"
if re.match(price_regex, price):
    print("Precio válido")
else:
    print("Precio inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String priceRegex = "^\\d+(\\.\\d{1,2})?$";
        Pattern pattern = Pattern.compile(priceRegex);

        // Ejemplo de uso:
        String price = "10.99";
        Matcher matcher = pattern.matcher(price);
        if (matcher.matches()) {
            System.out.println("Precio válido");
        } else {
            System.out.println("Precio inválido");
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
        string priceRegex = @"^\d+(\.\d{1,2})?$";
        Regex regex = new Regex(priceRegex);

        // Ejemplo de uso:
        string price = "10.99";
        if (regex.IsMatch(price))
        {
            Console.WriteLine("Precio válido");
        }
        else
        {
            Console.WriteLine("Precio inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar precios utilizando expresiones regulares en varios lenguajes de programación.