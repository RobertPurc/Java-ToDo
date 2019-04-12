# Java-ToDo
To-Do list wrote in Java language

Code exist in src file or below :




import java.util.ArrayList;
import java.util.Scanner;
public class Main {

    public static void main(String[] args){
    
        System.out.println("Welcome in program called TO-DO list");
        System.out.println("Choose one option by writing a number");
        String myFirstTask = "Add a new task!";
        ArrayList<String> tasks = new ArrayList<>();
        tasks.add(myFirstTask); // Adding a new task
        for(;;){        //infinite loop
            showMenu();
            Scanner input = new Scanner(System.in);
            String choice = input.nextLine();
            System.out.println("You chosen " + choice);


            switch (choice){
                case "1":
                    System.out.println("Yours today tasks");
                    System.out.println(tasks);
                    break;
                case "2":
                    System.out.println("Add a new task!");
                    String newTask = input.nextLine();
                    tasks.add(newTask);
                    System.out.println("Added task " + newTask);
                    break;

                case "3":
                    System.out.println("Deleted first task");
                    tasks.remove(0);
                    break;
                case "4":
                    System.out.println("I'm killing the program");
                    return;
            }
        }
    }
    public static void showMenu(){
        System.out.println("1 - Show list of tasks");
        System.out.println("2 - Add a new task");
        System.out.println("3 - Uncheck a first done task");
        System.out.println("4 - Close the program");
    }
}

