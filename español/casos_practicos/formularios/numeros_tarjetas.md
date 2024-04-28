Aquí tienes los regex y las implementaciones en JavaScript, Python, Java y C# para validar números de tarjeta de crédito:

### Números de Tarjeta de Crédito:

**regex**
```regex
RegexCreditCard: /^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9]{2})[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])?[0-9]{11})$/
```

**Implementaciones en los lenguajes:**

**JavaScript:**
```javascript
const creditCardRegex = /^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9]{2})[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])?[0-9]{11})$/;

// Ejemplo de uso:
let creditCardNumber = "1234567890123456";
if (creditCardRegex.test(creditCardNumber)) {
    console.log("Número de tarjeta de crédito válido");
} else {
    console.log("Número de tarjeta de crédito inválido");
}
```

**Python:**
```python
import re

credit_card_regex = r'^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9]{2})[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])?[0-9]{11})$'

# Ejemplo de uso:
credit_card_number = "1234567890123456"
if re.match(credit_card_regex, credit_card_number):
    print("Número de tarjeta de crédito válido")
else:
    print("Número de tarjeta de crédito inválido")
```

**Java:**
```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
    public static void main(String[] args) {
        String creditCardRegex = "^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9]{2})[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])?[0-9]{11})$";
        Pattern pattern = Pattern.compile(creditCardRegex);

        // Ejemplo de uso:
        String creditCardNumber = "1234567890123456";
        Matcher matcher = pattern.matcher(creditCardNumber);
        if (matcher.matches()) {
            System.out.println("Número de tarjeta de crédito válido");
        } else {
            System.out.println("Número de tarjeta de crédito inválido");
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
        string creditCardRegex = @"^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9]{2})[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])?[0-9]{11})$";
        Regex regex = new Regex(creditCardRegex);

        // Ejemplo de uso:
        string creditCardNumber = "1234567890123456";
        if (regex.IsMatch(creditCardNumber))
        {
            Console.WriteLine("Número de tarjeta de crédito válido");
        }
        else
        {
            Console.WriteLine("Número de tarjeta de crédito inválido");
        }
    }
}
```

Estas implementaciones te permitirán validar números de tarjeta de crédito utilizando expresiones regulares en varios lenguajes de programación.