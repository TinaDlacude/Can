import java.util.Scanner;

public class Insurance {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the current year: ");
        int currentYear = scanner.nextInt();

        System.out.println("Enter your birth year: ");
        int birthYear = scanner.nextInt();

        int age = calculateAge(currentYear, birthYear);
        int decade = calculateDecade(age);
        double premium = calculatePremium(decade);

        System.out.println("Your age is: " + age);
        System.out.println("Your annual policy premium is: $" + premium);
    }

    public static int calculateAge(int currentYear, int birthYear) {
        return currentYear - birthYear;
    }

    public static int calculateDecade(int age) {
        return age / 10;
    }

    public static double calculatePremium(int decade) {
        return (decade + 15) * 20;
    }
}
