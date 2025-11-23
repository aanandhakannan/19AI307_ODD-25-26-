# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

## **Aim**

To create an abstract class `BankAccount` with an abstract method `calculateInterest()`, and extend it through subclasses `SavingsAccount` and `FixedDepositAccount`, each providing its own implementation of interest calculation.



## **Algorithm**

1. Start the program.
2. Create an abstract class **BankAccount**.
3. Declare an abstract method **calculateInterest()** inside the class.
4. Create a subclass **SavingsAccount** that extends BankAccount.
5. Provide a concrete implementation of `calculateInterest()` in SavingsAccount.
6. Create another subclass **FixedDepositAccount** that also extends BankAccount.
7. Implement the `calculateInterest()` method differently in FixedDepositAccount.
8. Create objects of both subclasses and call their `calculateInterest()` methods to demonstrate different behaviors.
9. End the program.






## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

abstract class BankAccount{
    
    abstract double calculateInterest();
    
}

class SavingsAccount extends BankAccount{
    double balance;
    
    SavingsAccount(double balance){
        this.balance = balance;
    }
    
    double calculateInterest() {
        return balance * 0.04;
    }
}

class FixedDepositAccount extends BankAccount{
    
    double amount;
    int years;
    
    FixedDepositAccount(double amount,int years) {
        this.amount = amount;
        this.years = years;
    }
    
    double calculateInterest() {
        return amount * 0.07 * years;
    }
}

public class prog{
    
    public static void main(String[] args) {
        
        Scanner scan = new Scanner(System.in);
        
        int type = scan.nextInt();
        
        if(type==1){
            double balance = scan.nextDouble();
            SavingsAccount obj = new SavingsAccount(balance);
            System.out.printf("%.2f",obj.calculateInterest());
        }
        
        else if(type==2) {
            double amount = scan.nextDouble();
            int years = scan.nextInt();
            FixedDepositAccount obj1 = new FixedDepositAccount(amount,years);
            System.out.printf("%.2f",obj1.calculateInterest());
        }
        
        else{
            System.out.print("Invalid type");
        }
    }
}
```





## OUTPUT:
<img width="464" height="372" alt="image" src="https://github.com/user-attachments/assets/d5b4b8cc-bf07-44d0-b9c8-f9fa1dd0ad03" />



## RESULT:
Thus java program executed successfully.

