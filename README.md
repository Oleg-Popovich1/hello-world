# arrays

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


