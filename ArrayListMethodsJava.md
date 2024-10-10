
# Ejemplos de Métodos de ArrayList en Java (Parte 1)

### 1. **add( Element)**
Este método añade un elemento al final de la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        
        System.out.println(list); // Salida: [Manzana, Banana, Cereza]
    }
}
```

### 2. **add( index, Element)**
Este método inserta un elemento en una posición específica de la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Cereza");
        
        // Insertamos "Banana" en la posición 1
        list.add(1, "Banana");
        
        System.out.println(list); // Salida: [Manzana, Banana, Cereza]
    }
}
```

### 3. **addAll(list)**
Este método añade todos los elementos de otra colección al final de la lista.
```java
import java.util.ArrayList;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        
        ArrayList<String> otherList = new ArrayList<>(Arrays.asList("Banana", "Cereza"));
        
        // Añadimos todos los elementos de otherList a list
        list.addAll(otherList);
        
        System.out.println(list); // Salida: [Manzana, Banana, Cereza]
    }
}
```

### 4. **addAll( index, list)**
Este método inserta todos los elementos de otra colección en una posición específica de la lista.
```java
import java.util.ArrayList;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Cereza");
        
        ArrayList<String> otherList = new ArrayList<>(Arrays.asList("Banana", "Durazno"));
        
        // Insertamos los elementos de otherList en la posición 1
        list.addAll(1, otherList);
        
        System.out.println(list);  // Salida: [Manzana, Banana, Durazno, Cereza]
    }
}
```

### 5. **clear()**
Este método elimina todos los elementos de la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        
        list.clear();  // Limpiamos la lista
        
        System.out.println(list); // Salida: []
    }
}
```

### 6. **contains(Element)**
Este método verifica si la lista contiene un elemento específico.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        
        boolean containsBanana = list.contains("Banana"); // true
        boolean containsCereza = list.contains("Cereza"); // false
        
        System.out.println(containsBanana); // Salida: true
        System.out.println(containsCereza); // Salida: false
    }
}
```

### 7. **get( index)**
Este método devuelve el elemento en una posición específica de la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        
        String fruit = list.get(1);  // Banana está en la posición 1
        
        System.out.println(fruit);  // Salida: Banana
    }
}
```

### 8. **indexOf(Element)**
Este método devuelve la primera posición del elemento en la lista, o -1 si no se encuentra.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        
        int index = list.indexOf("Banana"); // 1
        int notFound = list.indexOf("Pera"); // -1
        
        System.out.println(index);    // Salida: 1
        System.out.println(notFound); // Salida: -1
    }
}
```

### 9. **isEmpty()**
Este método devuelve `true` si la lista está vacía.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        
        boolean emptyBeforeAdd = list.isEmpty();  // true
        list.add("Manzana");
        boolean emptyAfterAdd = list.isEmpty();   // false
        
        System.out.println(emptyBeforeAdd);  // Salida: true
        System.out.println(emptyAfterAdd);   // Salida: false
    }
}
```

### 10. **remove( index)**
Este método elimina el elemento en la posición especificada.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        
        list.remove(1);  // Eliminamos el elemento en la posición 1 (Banana)
        
        System.out.println(list);  // Salida: [Manzana, Cereza]
    }
}
```
