# 1. Escribir una aplicación que solicite al usuario cuántos números desea introducir. A continuación, introducir por teclado esa cantidad de números enteros, y por último, mostrar en el orden inverso al introducido.

# 2. Para recorrer un array de un modo más práctico y sencillo, sin que tengamos que
preocuparnos de los límites, podemos utilizar el bucle for con el formato foreach

      public class ArrayForEach {
      public static void main(String[] args) {
      double[] nota = new double[4];
      System.out.println("Para calcular la nota media necesito saber la ");
      System.out.println("nota de cada uno de tus exámenes.");
      for (int i = 0; i < 4; i++) {
      System.out.print("Nota del examen nº " + (i + 1) + ": ");
      nota[i] = Double.parseDouble(System.console().readLine());
      }
      System.out.println("Tus notas son: ");
      double suma = 0;
      for (double n : nota) { // for al estilo foreach
      System.out.print(n + " ");
      suma += n;
      }
      System.out.println("\nLa media es " + suma / 4);
      }
      }
