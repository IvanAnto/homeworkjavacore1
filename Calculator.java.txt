import java.util.function.*;

class Calculator {
  
  private static Supplier<Integer> callback; // создаем статическую переменную (поле) типа Supplier. Функциональный интерфейс реализует метод get().
  
  public Calculator(Supplier<Integer> callback) {
    this.callback = callback; 
  }
  
  public Calculator(){}
}