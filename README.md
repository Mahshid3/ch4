# ch4
import java.util.Scanner;

public class Student {
    private String name;
    private double[] grades;

    public Student(String name, int numGrades) {
        this.name = name;
        this.grades = new double[numGrades];
    }

    public void inputGrades() {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter grades for " + name + ": ");
        for (int i = 0; i < grades.length; i++) {
            grades[i] = scanner.nextDouble();
        }

        scanner.close();
    }

    public double calculateAverage() {
        double sum = 0;
        for (double grade : grades) {
            sum += grade;
        }
        return sum / grades.length;
    }

    public void displayAverage() {
        double average = calculateAverage();
        System.out.println("Average grade for " + name + ": " + average);
    }

    public static void main(String[] args) {
        Student student = new Student("John Doe", 5);
        student.inputGrades();
        student.displayAverage();
    }
}
