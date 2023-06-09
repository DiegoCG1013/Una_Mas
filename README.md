# Una_Mas

# Repositorio: https://github.com/DiegoCG1013/Una_Mas.git

### 1. Dado el siguiente fragmento de código C:

    static final double N = 2;
    static final double PREC = 1e-6;
    
    static double f (double x){
      return x*x-N;
    }
    
    static double bisect (double min, double max){
      double med = (min+max)/2;
      if (max-min<PREC) {
        return med;
      } else if (f(min)*f(med)<0) {
        return bisect (min,med);
      } else {
        return bisect (med,max);
      }
    }
    
* ¿Qué calcula la llamada a la función recursiva bisect(0,N)? Si cambiamos el
valor de N, ¿qué estaríamos calculando? ¿Y si cambiásemos la función f(x)?
      
      Calcula un numero entre 0 y N que se aproxime con una precision de PREC a la raiz cuadrada de N.
      
      Si cambias el valor de N cambias el numero del cual se calcula la media, y entre que numeros se buscaria esta.
      
      Si cambiaramos la funcion f(x) el codigo funcionaria mal ya que este es imprescindible para saber por cual
      de las 2 mitades continuar.
      
* Implemente un algoritmo iterativo equivalente.
      
      Codigo añadido en: src/main/java/Metodo_Bisectriz.java

### 2. Dado el siguiente algoritmo recursivo:

    void f(int num, int div){
        if (num>1) {
            if ((num%div) == 0) {
                System.out.println(div);
                f(num/div,div);
            } else {
            f(num,div+1);
            }
        }
    }

* Dado un número cualquiera x, ¿qué nos muestra por pantalla la llamada a la función
recursiva f(x,2)? ¿Cuál sería un nombre más adecuado para la función f?

        Muestra una especie de descomposicion factorial de x, empezando esta con el numero 2, y 
        subiendo a medida que avanza el codigo.
        
        Un nombre mas adecuado seria descomposicionFactorial().

* Implemente un algoritmo iterativo y uno implementado mediante expresiones lambda
equivalentes.

        Codigo en: src/main/java/Metodo_Descomposicion.java

### 3. 
__Construya una función que convierta un número decimal en una cadena que represente el
valor del número en hexadecimal (base 16). A continuación, generalice la función para
convertir un número decimal en un número en base B (con B<10). Resuélvalo mediante
expresiones lambda.
Recordatorio: El cambio de base se realiza mediante divisiones sucesivas por 16
en las cuales los restos determinan los dígitos hexadecimales del número según
la siguiente correspondencia:
Resto 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15
Dígito 0 1 2 3 4 5 6 7 8 9 A B C D E F
Por ejemplo:
65029|10 = FE05|16__

    Codigo en: src/main/java/Cambio_De_Base.java

### 4. 
__Implemente, tanto de forma recursiva como de forma iterativa, una función que nos diga
si una cadena de caracteres es simétrica (un palíndromo). Por ejemplo,
“DABALEARROZALAZORRAELABAD” es un palíndromo.__

    Codigo en: src/main/java/Palindromo.java

### 5. 
__Implemente, tanto de forma recursiva como de forma iterativa y con expresiones lambda,
una función que nos devuelva el máximo común divisor de dos números enteros
utilizando el algoritmo de Euclides.
ALGORITMO DE EUCLIDES
Dados dos números enteros positivos m y n, tal que m > n,
para encontrar su máximo común divisor
(es decir, el mayor entero positivo que divide a ambos):
- Dividir m por n para obtener el resto r (0 ≤ r < n)
- Si r = 0, el MCD es n.
- Si no, el máximo común divisor es MCD(n,r).

      Codigo en: src/main/java/MCD.java
