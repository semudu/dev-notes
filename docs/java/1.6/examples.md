# Java 1.6 (Java 6) - Kod Örnekleri

## 1. Scripting API Kullanımı
```java
import javax.script.ScriptEngineManager;
import javax.script.ScriptEngine;

public class ScriptExample {
    public static void main(String[] args) throws Exception {
        ScriptEngineManager manager = new ScriptEngineManager();
        ScriptEngine engine = manager.getEngineByName("JavaScript");
        engine.eval("print('Hello from Java 6 Scripting!');");
    }
}
```

## 2. Web Servisleri (JAX-WS) ile Basit Servis
```java
import javax.jws.WebService;
import javax.jws.WebMethod;

@WebService
public class MerhabaServis {
    @WebMethod
    public String merhaba(String isim) {
        return "Merhaba, " + isim + "!";
    }
}
```

## 3. Compiler API ile Dinamik Derleme
```java
import javax.tools.JavaCompiler;
import javax.tools.ToolProvider;

public class CompileExample {
    public static void main(String[] args) {
        JavaCompiler compiler = ToolProvider.getSystemJavaCompiler();
        int result = compiler.run(null, null, null, "Test.java");
        System.out.println("Derleme sonucu: " + result);
    }
}
```

Daha fazla örnek ve açıklama için diğer dosyalara bakınız.
