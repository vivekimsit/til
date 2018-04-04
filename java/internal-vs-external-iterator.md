```java
import java.util.Arrays;
import java.util.List;
import java.util.function.Consumer;

class Main {
  public static void main(String[] args) {
    List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8);
    
    // External iterators
    for (int i = 0; i < numbers.size(); i++) {
      System.out.println(numbers.get(i));
    }
    
    // less boilerplate
    for (Integer number : numbers) {
      System.out.println(number);
    }
    
    // Internal iterators
    
    numbers.forEach(new Consumer<Integer>() {
      public void accept(Integer number) {
        System.out.println(number);
      }
    });
    
    // less boilerplate
    numbers.forEach((Integer number) -> System.out.println(number));
    
    // even better
    numbers.forEach((number) -> System.out.println(number));
    
    // cooler, with method reference
    numbers.forEach(System.out::println);
  }
}
```
