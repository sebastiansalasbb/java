
# Ejemplos de Métodos de ArrayList en Java (Parte 2)

### 11. **remove(Element)**
Este método elimina la primera ocurrencia del elemento especificado.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        list.add("Banana");

        list.remove("Banana");  // Elimina la primera ocurrencia de "Banana"
        
        System.out.println(list);  // Salida: [Manzana, Cereza, Banana]
    }
}
```

### 12. **size()**
Este método devuelve el número de elementos en la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        
        int size = list.size();
        
        System.out.println(size);  // Salida: 2
    }
}
```

### 13. **subList( fromIndex,  toIndex)**
Este método devuelve una vista de una porción de la lista entre los índices especificados.
```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        list.add("Durazno");
        
        // Sublista desde el índice 1 hasta el 3 (excluye el 3)
        List<String> subList = list.subList(1, 3);
        
        System.out.println(subList);  // Salida: [Banana, Cereza]
    }
}
```

### 14. **sort(Comparator)**
Este método ordena la lista según el comparador especificado.
#### Ordenar en orden alfabético:
```java
import java.util.ArrayList;
import java.util.Collections;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Cereza");
        list.add("Banana");
        list.add("Manzana");
        
        // Ordenamos la lista en orden alfabético
        Collections.sort(list);
        
        System.out.println(list);  // Salida: [Banana, Cereza, Manzana]
    }
}
```

#### Ordenar en orden descendente:
```java
import java.util.ArrayList;
import java.util.Collections;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>();
        list.add(3);
        list.add(1);
        list.add(4);
        list.add(2);
        
        // Ordenamos en orden descendente
        Collections.sort(list, Collections.reverseOrder());
        
        System.out.println(list);  // Salida: [4, 3, 2, 1]
    }
}
```

### 15. **retainAll(list)**
Este método conserva solo los elementos que están en la colección especificada.
```java
import java.util.ArrayList;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(Arrays.asList("Manzana", "Banana", "Cereza"));
        ArrayList<String> retainList = new ArrayList<>(Arrays.asList("Banana"));
        
        list.retainAll(retainList);  // Conserva solo "Banana"
        
        System.out.println(list);  // Salida: [Banana]
    }
}
```

### 16. **removeAll(list)**
Este método elimina de la lista todos los elementos que están en la colección especificada.
```java
import java.util.ArrayList;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(Arrays.asList("Manzana", "Banana", "Cereza", "Durazno", "Banana"));
        ArrayList<String> removeList = new ArrayList<>(Arrays.asList("Banana"));
        
        // Eliminamos todas las ocurrencias de "Banana"
        list.removeAll(removeList);
        
        System.out.println(list);  // Salida: [Manzana, Cereza, Durazno]
    }
}
```

### 17. **replaceAll(UnaryOperator)**
Este método reemplaza cada elemento de la lista aplicando la operación especificada.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>();
        list.add(1);
        list.add(2);
        list.add(3);
        
        // Multiplicamos cada elemento por 2
        list.replaceAll(n -> n * 2);
        
        System.out.println(list);  // Salida: [2, 4, 6]
    }
}
```

### 18. **removeIf(Condition)**
Este método elimina todos los elementos que cumplan con una condición (predicado).
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>();
        list.add(1);
        list.add(2);
        list.add(3);
        list.add(4);
        
        // Eliminamos todos los números impares
        list.removeIf(n -> n % 2 != 0);
        
        System.out.println(list);  // Salida: [2, 4]
    }
}
```

### 19. **lastIndexOf(Element)**
Este método devuelve la última posición del elemento en la lista o -1 si no se encuentra.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Banana");
        
        int lastIndex = list.lastIndexOf("Banana"); // 2
        
        System.out.println(lastIndex);  // Salida: 2
    }
}
```

### 20. **listIterator()**
Este método devuelve un `ListIterator` que permite recorrer la lista en ambas direcciones.
```java
import java.util.ArrayList;
import java.util.ListIterator;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        
        ListIterator<String> it = list.listIterator();
        
        // Recorremos hacia adelante
        while (it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```

Ejemplo de cómo recorrer la lista al revés:

```java
import java.util.ArrayList;
import java.util.ListIterator;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        
        // Creamos un ListIterator empezando desde el final de la lista
        ListIterator<String> it = list.listIterator(list.size());
        
        // Recorremos hacia atrás
        while (it.hasPrevious()) {
            System.out.println(it.previous());
        }
    }
}

```

```java
import java.util.ArrayList;
import java.util.ListIterator;

public class Main {
    private static ListIterator<String> iterator;

    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");

        // Inicializamos el iterador
        iterator = list.listIterator();

        // Avanzamos paso a paso usando una función
        avanzar();  // Salida: Manzana
        avanzar();  // Salida: Banana
        avanzar();  // Salida: Cereza
        avanzar();  // Salida: Fin de la lista
    }

    // Función para avanzar al siguiente elemento
    public static void avanzar() {
        if (iterator.hasNext()) {
            System.out.println(iterator.next());
        } else {
            System.out.println("Fin de la lista");
        }
    }
}

```