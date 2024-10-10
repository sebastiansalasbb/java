
# Ejemplos de Métodos de ArrayList en Java (Parte 3)

### 21. **listIterator( index)**
Este método devuelve un `ListIterator` que comienza en una posición específica.
```java
import java.util.ArrayList;
import java.util.ListIterator;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        
        ListIterator<String> it = list.listIterator(1);  // Comienza en la posición 1 (Banana)
        
        while (it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```

### 22. **spliterator()**
---------------muy dificil todavia------------


### 23. **clone()**
Este método devuelve una copia superficial (shallow copy) de la lista.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");

        ArrayList<String> clonedList = (ArrayList<String>) list.clone();
        
        System.out.println(clonedList);  // Salida: [Manzana, Banana]
    }
}
```

### 24. **removeRange( fromIndex,  toIndex)**
Este método elimina los elementos dentro del rango especificado (desde `fromIndex`, inclusivo, hasta `toIndex`, exclusivo). 
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");
        list.add("Durazno");

        // Eliminamos los elementos desde el índice 1 al 3 (exclusivo)
        list.subList(1, 3).clear();  // Se puede usar clear en la sublista

        System.out.println(list);  // Salida: [Manzana, Durazno]
    }
}
```

### 25. **ensureCapacity(int minCapacity)**
----------poco util--------------------


### 26. **forEach(action)**
Este método ejecuta la acción especificada para cada elemento de la lista. Es útil cuando se usa junto con expresiones lambda o referencias de métodos.
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Manzana");
        list.add("Banana");
        list.add("Cereza");

        // Usamos una expresión lambda para imprimir cada elemento
        list.forEach(fruit -> System.out.println(fruit));
    }
}
```
