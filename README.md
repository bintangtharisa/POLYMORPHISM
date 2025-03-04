1.	package tugaspbo;
2.	// Parent Class BangunDatar
3.	abstract class BangunDatar {
4.	abstract float luas();
5.	abstract double keliling();
6.	}
7.	
8.	 // Kelas Anak : Persegi
9.   class Persegi extends BangunDatar {
10.	   float s; // sisi
11.	
12.	   Persegi(float s) {
13.	   this.s= s;
14.	}
15.	
16.	   @Override
17.	   float luas() {
18.	   return s * s;
19.	}
20.	
21.	   @Override
22.	   double keliling() {
23.	   return 4 * s;
24.	  }
25.	}
26.	
27.	   // Kelas Anak : Lingkaran
28.	   class Lingkaran extends BangunDatar {
29.	   float r; // jari-jari
30.	
31.	   Lingkaran(float r) {
32.	   this.r = r;
33.	}
34.	
35.	   @Override
36.	   float luas() {
37.	   return (float) (Math.PI * r * r);
38.	}
39.	
40.	   @Override
41.    double keliling() {
42.	   return 2 * Math.PI * r;
43.	  }
44.	}
45.	
46.	   // Kelas Anak : Segitiga
47.	   class Segitiga extends BangunDatar {
48.	   float a, t; // alas, tinggi
49.	
50.	   Segitiga(float a, float t) {
51.	   this.a= a;
52.	   this.t= t;
53.	}
54.	
55.	   @Override
56.	   float luas() {
57.	   return 0.5f * a* t;
58.	}
59.	
60.	   @Override
61.	   double keliling() {
62.	   // Mengasumsikan segitiga siku-siku, sehingga sisi miring bisa dihitung dengan Pythagoras
63.	   double sisiMiring = Math.sqrt(a* a + t * t);
64.	   return a+ t+ sisiMiring;
65.	  }
66.	}
67.	
68.	// Kelas Main untuk menjalankan program
69.	public class Main {
70.	public static void main(String[] args) {
71.	   Persegi persegi = new Persegi(4);
72.	   Lingkaran lingkaran = new Lingkaran(7);
73.	   Segitiga segitiga = new Segitiga(3, 4);
74.	
75.	   System.out.println("Luas Persegi: " + persegi.luas());
76.	   System.out.println("Keliling Persegi: " + persegi.keliling());
77.	
78.	   System.out.println("Luas Lingkaran: " + lingkaran.luas());
79.	   System.out.println("Keliling Lingkaran: " + lingkaran.keliling());
80.	
81.	   System.out.println("Luas Segitiga: " + segitiga.luas());
82.	   System.out.println("Keliling Segitiga: " + segitiga.keliling());
83.	 }
84.	}
