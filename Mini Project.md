```java
import java.util.Random;
import java.util.Scanner;

public class CricketBetting {
    public int score;
    public int[] runs = {1,2,4,6};
    public int points1, points2, points3, points4;
    public void batsManRun() {
        for (int i = 1; i <= 6; i++) {
            System.out.println("\n" +i + " no. ball bowled...\n");
            score = runs[new Random().nextInt(runs.length)];
            Player plyr1 = new Player("Subhasmita");
            Player plyr2 = new Player("Sangita");
            Player plyr3 = new Player("Bibhuprasad");
            Player plyr4 = new Player("Saroj");
            System.out.println("\nThe Batsman's score in this ball is : "+score);
            if (score == plyr1.choice)
                System.out.println(plyr1.playerName +", congrats.... You are correct...");
            if (score == plyr2.choice)
                System.out.println(plyr2.playerName +", congrats.... You are correct...");
            if (score == plyr3.choice)
                System.out.println(plyr3.playerName +", congrats.... You are correct...");
            if (score == plyr4.choice)
                System.out.println(plyr4.playerName +", congrats.... You are correct...");
             if (score != plyr1.choice && score != plyr2.choice && score != plyr3.choice && score != plyr4.choice)
                System.out.println("Awww.......No one is correct....");
            points1 = plyr1.points + points1;
            points2 = plyr2.points + points2;
            points3 = plyr3.points + points3;
            points4 = plyr4.points + points4;
            System.out.println("Total points of " +plyr1.playerName+ " is : " +points1);
            System.out.println("Total points of " +plyr2.playerName+ " is : " +points2);
            System.out.println("Total points of " +plyr3.playerName+ " is : " +points3);
            System.out.println("Total points of " +plyr4.playerName+ " is : " +points4);
        }
        pointsCalculator();
    }
    class Player{
        public String playerName;
        int points;
        int choice;

        Player(String name){
            Scanner sc = new Scanner(System.in);
            System.out.print("What is your guess for this ball, " +name+ ": ");
            choice = sc.nextInt();
            playerName = name;
            if (choice == 1 && choice == score) {
                points = points + 10;
            }
            else if (choice == 2 && choice == score) {
                points = points + 20;
            }
            else if (choice == 4 && choice == score) {
                points = points + 40;
            }
            else if (choice == 6 && choice == score) {
                points = points + 60;
            }
        }
    }
    public void pointsCalculator() {
        if (points1 >= points2 && points1 >= points3 && points1 >= points4){
            System.out.println("\nSubhasmita is the winner ......Congratulations....");
        }
        if (points2 >= points1 && points2 >= points3 && points2 >= points4){
            System.out.println("\nSangita is the winner ......Congratulations....");
        }
        if (points3 >= points1 && points3 >= points2 && points3 >= points4){
            System.out.println("\nBibhuprasad is the winner ......Congratulations....");
        }
        if (points4 >= points1 && points4 >= points2 && points4 >= points3){
            System.out.println("\nSaroj is the winner ......Congratulations....");
        }
    }
    public static void main (String[]args){
            CricketBetting var = new CricketBetting();
            var.batsManRun();
        }
    }
```
