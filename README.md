
public class Level1 {
    public static void main(String[] args) {
        // Definēt mainīgos
        int karavīruSkaits = 100;
        int ieročuSkaits = 50;
        double pārtikasResursi = 1000.5;

        // Izmantot mainīgos
        System.out.println("Karavīru skaits: " + karavīruSkaits);
        System.out.println("Ieroču skaits: " + ieročuSkaits);
        System.out.println("Pārtikas resursi: " + pārtikasResursi);
    }
}
public class Level2 {
    public static void main(String[] args) {
        // Definēt ienaidnieku spēkus
        int enemy1Strength = 70;
        int enemy2Strength = 40;

        // Nosacījuma loģika
        if (enemy1Strength > enemy2Strength) {
            System.out.println("Uzbrūk ienaidniekam 1.");
        } else {
            System.out.println("Uzbrūk ienaidniekam 2.");
        }
    }
}
public class Level3 {
    public static void main(String[] args) {
        // Karaspēka kustība uz priekšu
        for (int i = 0; i < 10; i++) {
            System.out.println("Karaspēks pārvietojas uz priekšu " + (i+1) + " soļus.");
        }

        // Karaspēka kustība, kamēr netiek sasniegts mērķis
        int distance = 0;
        while (distance < 100) {
            distance += 10;
            System.out.println("Karaspēks ir pārvietojies " + distance + " metrus.");
        }
    }
}
public class Level4 {
    public static void main(String[] args) {
        // Izsaukt metodes
        uzlabotIeroci("Zobens", 5);
        uzlabotIeroci("Loka šaujamierocis", 3);
    }

    // Metode ieroča uzlabošanai
    public static void uzlabotIeroci(String ierocis, int līmenis) {
        System.out.println("Uzlabojam " + ierocis + " līdz līmenim " + līmenis);
    }
}
class Soldier {
    String name;
    int strength;

    // Konstruktors
    public Soldier(String name, int strength) {
        this.name = name;
        this.strength = strength;
    }

    // Metode, lai parādītu informāciju
    public void showInfo() {
        System.out.println("Karavīrs: " + name + ", Spēks: " + strength);
    }
}

public class Level5 {
    public static void main(String[] args) {
        // Izveidot karavīra objektus
        Soldier soldier1 = new Soldier("Jānis", 75);
        Soldier soldier2 = new Soldier("Pēteris", 80);

        // Parādīt informāciju par karavīriem
        soldier1.showInfo();
        soldier2.showInfo();
    }
}
import java.util.ArrayList;

public class Level6 {
    public static void main(String[] args) {
        // Definēt sarakstu resursiem
        ArrayList<String> resursi = new ArrayList<>();
        resursi.add("Koks");
        resursi.add("Metāls");
        resursi.add("Pārtika");

        // Parādīt resursus
        System.out.println("Pieejamie resursi:");
        for (String resurss : resursi) {
            System.out.println("- " + resurss);
        }

        // Definēt karavīru sarakstu
        ArrayList<Soldier> karavīri = new ArrayList<>();
        karavīri.add(new Soldier("Jānis", 75));
        karavīri.add(new Soldier("Pēteris", 80));

        // Parādīt karavīrus
        System.out.println("Karaspēks:");
        for (Soldier karavīrs : karavīri) {
            karavīrs.showInfo();
        }
    }
}
