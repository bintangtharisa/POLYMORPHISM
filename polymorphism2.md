package tugaspbo;
class MathOperation {
    // Method untuk menjalankan pertambahan dua angka
    int add(int a, int b) {
        return a + b;
    }

    //  Method untuk menjalankan pertambahan tiga angka (Overloading)
    int add(int a, int b, int c) {
        return a + b + c;
    }

    //  Method untuk menjalankan pertambahan dua angka desimal (Overloading)
    double add(double a, double b) {
        return a + b;
    }
}

public class PolymorphismOverloading {
    public static void main(String[] args) {
        MathOperation math = new MathOperation();

        // Memanggil metode add() dengan parameter berbeda
        System.out.println("Hasil penjumlahan 2 bilangan: " + math.add(19, 10));
        System.out.println("Hasil penjumlahan 3 bilangan: " + math.add(10, 11, 24));
        System.out.println("Hasil penjumlahan desimal: " + math.add(2.1, 2.2));
    }
}
