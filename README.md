# Un array o tabla es un tipo de dato capaz de almacenar múltiples valores. Se utiliza para agrupar datos muy parecidos, por ejemplo, si se necesita almacenar la temperatura media diaria en Palma durante el último año se pueden utilizar las variables temp0, temp1, temp2, temp3, temp4, … y así hasta 365 variables distintas pero sería poco práctico; es mejor utilizar un array de nombre temp y usar un índice para referenciar la temperatura de un día concreto del año.

# Ejemplo 1. En el siguiente ejemplo se muestra un array de 4 números de tipo double que almacena notas de alumnos.

      Algoritmo CalculoNotaMedia
          Dimension nota[4]
      
          Escribir "Para calcular la nota media necesito saber la nota de cada uno de tus exámenes."
      
          Para i = 0 Hasta 3 Paso 1 Hacer
              Escribir "Nota del examen nº ", i + 1, ": "
              Leer nota[i]
          Fin Para
      
          Escribir "Tus notas son: "
      
          suma = 0
      
          Para i = 0 Hasta 3 Paso 1 Hacer
              Escribir nota[i], "  "
              suma = suma + nota[i]
          Fin Para
      
          Escribir "La media es ", suma / 4
      FinAlgoritmo


# Ejercicio resuelto 1. Escribir una aplicación que solicite al usuario cuántos números desea introducir. A continuación, introducir por teclado esa cantidad de números enteros, y por último, mostrar en el orden inverso al introducido.

# Ejercicio resuelto 2. Para recorrer un array de un modo más práctico y sencillo, sin que tengamos que preocuparnos de los límites, podemos utilizar el bucle for con el formato foreach

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
