# ch4
import java.util.Scanner;

public class StudentGrading {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of grades: ");
        int numGrades = scanner.nextInt();
        double total = 0;

        System.out.println("Enter the grades:");
        for (int i = 0; i < numGrades; i++) {
            double grade = scanner.nextDouble();
            total += grade;
        }

        double average = total / numGrades;

        System.out.println("Average grade: " + average);

        scanner.close();
    }
}
