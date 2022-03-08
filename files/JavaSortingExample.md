```java
import java.util.function.*;
public class Main {
  public static void someSortingMethod(int[] arr) {
    // Definitely doing some sorting stuff
  }
  public static void conductExperiment(int[] sizes, Consumer<int[]> sort, String fileName) {
    // TODO: open file
    for(int size : sizes) {
      int[] arr = Main.randomArray(size);
      // TODO: begin stopwatch
      sort.accept(arr);
      // TODO: end stopwatch
      // TODO: record time
    }
    // TODO: close file
  }

  public static void main(String[] args) {
    int[] sizes = {10, 30, 100, 300, 1000};
    conductExperiment(sizes, arr -> Main.someSortingMethod(arr), "sort0.tab");
  }
}
```