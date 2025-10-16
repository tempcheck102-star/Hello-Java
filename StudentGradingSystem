import java.util.Scanner;

class Student {
    String name;
    int[] marks;
    int total;
    double average;

    Student(String name, int numSubjects) {
        this.name = name;
        marks = new int[numSubjects];
    }

    void inputMarks(Scanner sc) {
        total = 0;
        for (int i = 0; i < marks.length; i++) {
            System.out.print("Enter marks for Subject " + (i + 1) + ": ");
            marks[i] = sc.nextInt();
            total += marks[i];
        }
        average = total / (double) marks.length;
    }

    void displayResult() {
        System.out.println("\nStudent: " + name);
        System.out.println("Total Marks: " + total);
        System.out.println("Average: " + average);

        if (average >= 80)
            System.out.println("Grade: A");
        else if (average >= 70)
            System.out.println("Grade: B");
        else if (average >= 60)
            System.out.println("Grade: C");
        else
            System.out.println("Grade: Fail");
    }
}

public class StudentGradeSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();

        System.out.print("Enter number of subjects: ");
        int sub = sc.nextInt();

        Student[] students = new Student[n];

        for (int i = 0; i < n; i++) {
            System.out.print("\nEnter name of student " + (i + 1) + ": ");
            String name = sc.next();
            students[i] = new Student(name, sub);
            students[i].inputMarks(sc);
        }

        System.out.println("\n===== Student Results =====");
        for (Student s : students) {
            s.displayResult();
            System.out.println("---------------------------");
        }

        sc.close();
    }
}
