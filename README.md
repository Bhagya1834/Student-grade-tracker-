#codeAplha_ Student-grade-tracker-
import java.util.ArrayList;
import java.util.Scanner;

public class StudentGradeTracker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Double> grades = new ArrayList<>();

        System.out.println("Welcome to the Student Grade Tracker!");
        System.out.println("Enter student grades (type -1 to finish):");

        // Input loop
        while (true) {
            System.out.print("Enter grade: ");
            double grade = scanner.nextDouble();

            if (grade == -1) break;
            if (grade < 0 || grade > 100) {
                System.out.println("Please enter a valid grade between 0 and 100.");
                continue;
            }
            grades.add(grade);
        }

        if (grades.isEmpty()) {
            System.out.println("No grades were entered.");
        } else {
            double sum = 0;
            double highest = grades.get(0);
            double lowest = grades.get(0);

            for (double grade : grades) {
                sum += grade;
                if (grade > highest) highest = grade;
                if (grade < lowest) lowest = grade;
            }

            double average = sum / grades.size();

            System.out.println("\n--- Grade Statistics ---");
            System.out.println("Total Students: " + grades.size());
            System.out.printf("Average Grade: %.2f\n", average);
            System.out.println("Highest Grade: " + highest);
            System.out.println("Lowest Grade: " + lowest);
        }

        scanner.close();
    }
}


output:
Welcome to the Student Grade Tracker!

Enter student grades Jype -1 to finish):

Enter grade:

90

Enter grade:

78

Enter grade:

66

Enter grade:

89

Enter grade:

97

Enter grade:

56

Enter grade:

48

Enter grade:

33

Enter grade:

59

Enter grade:

96-1

Enter grade:

---Grade Statistics

Total Students:

10

Average Grade:

71.20

Highest Grade:

97.0

Lowest Grade:

33.0

---Code Execution Successful

n

---
