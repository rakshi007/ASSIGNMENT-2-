# ASSIGNMENT-2-
Nimesa Technology Pvt. Ltd

package qsp;
import java.util.Scanner;

public class WeatherDataProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int option;
        do {
            printMenu();
            option = scanner.nextInt();

            switch (option) {
                case 1:
                    getTemperature();
                    break;
                case 2:
                    getWindSpeed();
                    break;
                case 3:
                    getPressure();
                    break;
                case 0:
                    System.out.println("Terminating the program.");
                    break;
                default:
                    System.out.println("Invalid option. Please select a valid option.");
                    break;
            }
        } while (option != 0);

        scanner.close();
    }

    public static void printMenu() {
        System.out.println("\nMenu:");
        System.out.println("1. Get Temperature");
        System.out.println("2. Get Wind Speed");
        System.out.println("3. Get Pressure");
        System.out.println("0. Exit");
        System.out.print("Select an option: ");
    }

    public static void getTemperature() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter date with time: ");
        String dateTime = scanner.nextLine();

    
        System.out.println("Temperature for " + dateTime + ": 25°C"); // Example temperature value

        scanner.close();
    }

    public static void getWindSpeed() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter date with time: ");
        String dateTime = scanner.nextLine();

        
        System.out.println("Wind Speed for " + dateTime + ": 10 m/s"); // Example wind speed value

        scanner.close();
    }

    public static void getPressure() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter date with time: ");
        String dateTime = scanner.nextLine();

        // Here, you can implement logic to fetch pressure based on the input date and time.
        // Replace the following line with your actual implementation.
        System.out.println("Pressure for " + dateTime + ": 1013 hPa"); // Example pressure value

        scanner.close();
    }
}



