# a-math-puzzle-for-elementary-by-Java
import java.util.Scanner;

public class EasyMathPuzzleNoFile {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Choose difficulty (easy/medium/hard): ");
        String level = sc.nextLine();

        int score = 0;

        System.out.println("\n=== Math Puzzle Started ===\n");

        
        for (int i = 1; i <= 5; i++) {

            int a = (int) (Math.random() * 10);   // numbers 0–9
            int b = (int) (Math.random() * 10);

            System.out.print("Question " + i + ": " + a + " + " + b + " = ? ");

            int userAns = sc.nextInt();
            int correctAns = a + b;

            if (userAns == correctAns) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Wrong! Correct answer: " + correctAns + "\n");
            }
        }

        System.out.println("=== Game Finished ===");
        System.out.println(name + ", Your Total Score: " + score + " out of 5");
    }
}
