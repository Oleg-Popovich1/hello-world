# hello-world
int balance = 1000;
        int function;
        String reallogin = new String("oleh");
        int realparol = 256;
         Scanner scanner = new Scanner(System.in);
        System.out.println("Please enter your login");
        String login = scanner.next();
        System.out.println("Please enter your parol");
        int parol = scanner.nextInt();
        if(reallogin.equals(login) & realparol == parol) {
            do {
                System.out.println("balance -1,add - 2,minus - 3.Enter number please!");
                function = scanner.nextInt();
                switch (function) {

                    case 1:
                        System.out.println("Balance is " + balance);
                        break;
                    case 2:
                        System.out.println("How much do you want to add?");
                        String adder = scanner.next();
                        int add = Integer.parseInt(adder.replaceAll("[^0-9]", ""));
                        balance += add;
                        System.out.println("After add count is " + balance);
                        break;
                    case 3:
                        System.out.println("How much do you want to withdrav?");
                        String minus = scanner.next();
                        int min = Integer.parseInt(minus.replaceAll("[^0-9]", ""));
                        if (min > balance) {
                            System.out.println("On your balance not this money");
                        } else {
                            balance -= min;
                            System.out.println("after minus count is " + balance);
                        }
                        break;

                    default:
                        System.out.println("You enter valid number." +
                                "If you want exit enter - 0");
                        break;
                }
            }while (function!=0);
}



array
int[] array = new int[10];
0000000000
array[4]=80;
000,80,00000
int nes[]={2.50.30.8.600};





package com.company;


import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        String[] animals = {"monkey", "snake", "lion", "kivi", "eagel", null, null, null, null, null};
        Scanner scanner = new Scanner((System.in));
        int function;
        int k=0;
        do {
            System.out.println("if you want to check animals - 1" +
                    " for add animal - 2," +
                    " for remove animals - 3," +
                    "for show all animals - 4" +
                    "for exit - 5");
            function = scanner.nextInt();

            switch (function) {
                case 1:
                    System.out.println("enter animal");
                    String check = scanner.next();
                    for (int i = 0; i < animals.length; i++) {
                        if (check.equals(animals[i])) {
                            System.out.println("we have this animal");
                            break;
                        }

                        if (i == animals.length - 1) {
                            System.out.println("we do not have this animals");
                            break;
                        }

                    }
                    break;
                case 2:
                    System.out.println("add animals");
                    String addAnimal = scanner.next();
                    for (int j = 0; j < animals.length; j++) {
                        if (animals[j] == null) {
                            animals[j] = addAnimal;
                            break;

                        }
                    }
                    for (int j = 0; j < animals.length; j++) {
                        System.out.println(animals[j]);
                    }
                    break;
                case 3:
                    System.out.println("remove animals");
                    String removeAnimal = scanner.next();
                    for (int j = 0; j < animals.length; j++) {
                        if (removeAnimal.equals(animals[j])) {
                            animals[j] = null;
                        }
                        System.out.println(animals[j]);
                    }
                    break;
                case 4:
                    System.out.println("all animals");
                    for (int i = 0; i < animals.length; i++) {
                        System.out.println(animals[i]);
                    }
                    break;
                case 5:
                    System.out.println("exit");
                    System.exit(0);


            }

            /*System.out.println("enter 1 for check animal");
            System.out.println("enter 2 for add animal");
            System.out.println("enter 3 for remove animal");
            System.out.println("enter 4 for show all animals");
            System.out.println("enter 5 to exit");
    */
        } while (function!=k);

    }

}


