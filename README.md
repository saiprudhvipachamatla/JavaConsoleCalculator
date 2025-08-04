import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char operator;
        double number1, number2, result;

        while (true) {
            System.out.print("Enter operator (+, -, *, /) or 'q' to quit: ");
            operator = sc.next().charAt(0);

            if (operator == 'q') {
                break;
            }

            System.out.print("Enter first number: ");
            number1 = sc.nextDouble();
            System.out.print("Enter second number: ");
            number2 = sc.nextDouble();

            switch (operator) {
                case '+':
                    result = add(number1, number2);
                    break;
                case '-':
                    result = subtract(number1, number2);
                    break;
                case '*':
                    result = multiply(number1, number2);
                    break;
                case '/':
                    result = divide(number1, number2);
                    break;
                default:
                    System.out.println("Invalid operator!");
                    continue;
            }

            System.out.println("Result: " + result);
        }

      
    }

    public static double add(double num1, double num2) {
        return num1 + num2;
    }

    public static double subtract(double num1, double num2) {
        return num1 - num2;
    }

    public static double multiply(double num1, double num2) {
        return num1 * num2;
    }

    public static double divide(double num1, double num2) {
        if (num2 == 0) {
            System.out.println("Error! Division by zero is not allowed.");
            return 0; 
        }
        return num1 / num2;
    }
}
