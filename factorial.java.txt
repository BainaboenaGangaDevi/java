import java.util.Scanner;

public class FactorialCalculator {

    // Method to calculate factorial of a number
    public static long factorial(int num) {
        if (num < 0) {
            throw new IllegalArgumentException("Number must be non-negative.");
        }
        long result = 1;
        for (int i = 1; i <= num; i++) {
            result *= i;
        }
        return result;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter the first number
        System.out.print("Enter the first number: ");
        int number1 = scanner.nextInt();

        // Prompt user to enter the second number
        System.out.print("Enter the second number: ");
        int number2 = scanner.nextInt();

        // Calculate factorials
        long factorial1 = factorial(number1);
        long factorial2 = factorial(number2);

        // Display results
        System.out.println("Factorial of " + number1 + " is: " + factorial1);
        System.out.println("Factorial of " + number2 + " is: " + factorial2);

        // Close the scanner
        scanner.close();
    }
}
