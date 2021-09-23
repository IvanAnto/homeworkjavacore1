import java.util.function.*;

class Main {
  public static void main(String[] args) {
    
    static Supplier<Calculator> instance = Calculator::new;
    
    Calculator calc = Calculator.instance.get(); // создаем экземпляр класса Calculator через вызов статической переменной instance
   // Calculator calc = new Calculator(instance);
    //System.out.println(calc);
    
    BinaryOperator<Integer> plus = (x, y) -> x + y;
    BinaryOperator<Integer> minus = (x, y) -> x - y;
    BinaryOperator<Integer> multiply = (x, y) -> x * y;
    BinaryOperator<Integer> devide = (x, y) -> x / y;

    int a = calc.plus.apply(2, 1);
    int b = calc.minus.apply(3, 1);
    int c = calc.devide.apply(a, b);
    calc.println.accept(c);

    // plus.apply(2, 1);
    // System.out.println(plus.apply(2, 1));
    // minus.apply(2, 1);
    // System.out.println(minus.apply(2, 1));
    // multiply.apply(2, 1);
    // System.out.println(multiply.apply(2, 1));
    // devide.apply(2, 1);
    // System.out.println(devide.apply(2, 1));    
  }
}