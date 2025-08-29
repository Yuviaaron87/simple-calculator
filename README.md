import java.util.Scanner;

public class Main{

    public static void main(String args[]){

        Scanner scan = new Scanner(System.in);

        double num1;
        double num2;
        char operator;
        double result = 0;

        System.out.print("Enter the First Number: ");
        num1 = scan.nextDouble();

        System.out.print("Enter the Operator( + , -, * , / , ^): ");
        operator = scan.next().charAt(0);

        System.out.print("Enter the Second Number: ");
        num2 = scan.nextDouble();

        switch(operator){

        case '+' -> result = num1 + num2;
        case '-' -> result = num1 - num2;
        case '*' -> result = num1 * num2;
        case '/' -> { 
            if(num2==0){
                System.out.println("Cannot divide by Zero!");
            }
            else{
                result = num1 / num2;

            }
        }
        case '^' -> result = Math.pow(num1,num2);
        default  -> {
            System.out.println("Invalid operator");
        }
    }

        System.out.println(result);

       
    }
    
}
