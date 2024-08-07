- 
import java.util.Scanner;

public class Game {
    private static Registration registration = new Registration();
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        while (true) {
            System.out.println("1. Reģistrēties");
            System.out.println("2. Pieslēgties");
            System.out.println("3. Iziet");
            System.out.print("Izvēlieties opciju: ");
            int choice = scanner.nextInt();
            scanner.nextLine(); // Patērēt jauno rindu

            if (choice == 1) {
                register();
            } else if (choice == 2) {
                login();
            } else {
                break;
            }
        }
    }

    private static void register() {
        System.out.print("Ievadiet lietotājvārdu: ");
        String username = scanner.nextLine();
        System.out.print("Ievadiet paroli: ");
        String password = scanner.nextLine();
        if (registration.register(username, password)) {
            System.out.println("Reģistrācija veiksmīga!");
        } else {
            System.out.println("Lietotājvārds jau eksistē.");
        }
    }

    private static void login() {
        System.out.print("Ievadiet lietotājvārdu: ");
        String username = scanner.nextLine();
        System.out.print("Ievadiet paroli: ");
        String password = scanner.nextLine();
        User user = registration.login(username, password);
        if (user != null) {
            System.out.println("Pieslēgšanās veiksmīga! Sveicināti, " + user.getUsername());
            startGame();
        } else {
            System.out.println("Nepareizs lietotājvārds vai parole.");
        }
    }

    private static void startGame() {
        System.out.println("Spēles sākums...");
        // Pievieno spēles līmeņu kodu šeit
    }
}
