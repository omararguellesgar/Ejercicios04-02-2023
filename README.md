# sesion04
actividad de clase 04/02/2023
##  Ejercicio 01


## Etapa 01. Descripción del problema

Se requiere un programa en Java para convertir una cantidad de dinero en otros tipos de monedas (al menos a cinco tipos de monedas distintas). 

## Etapa 02. Definición de la solución

~~~
- Entrada
  
  double monto , valorDolar = 18.94, valorEuro = 20.29, valorLibra = 22.86, valorFranco = 20.55, valorBit = 434812.81
  
- Proceso
  
  Conversion de dolar a peso
  Conversion de peso a dolar
  Conversion de euro a peso
  Conversion de peso a euro
  Conversion de libra a peso
  Conversion de peso a libra
  Conversion de franco a peso
  Conversion de peso a franco
  Conversion de bitcoin a peso
  Conversion de peso a bitcoin
    
- Salida
  
  +----------+---------------+----------------------+----------------+
  | CANTIDAD | MONEDA ORIGEN | CANTIDAD CONVERTIDA  | MONEDA DESTINO |
  +----------+---------------+----------------------+----------------+
  |        1 |          DLLS |               18.94  |            MXN |
  +----------+---------------+----------------------+----------------+
  |        1 |           MXN |  0.05279831045406547 |           DLLS |
  +----------+---------------+----------------------+----------------+
  |        1 |          EURO |                20.29 |            MXN |
  +----------+---------------+----------------------+----------------+
  |        1 |           MXN |  0.04928536224741252 |           EURO |
  +----------+---------------+----------------------+----------------+
  |        1 |         LIBRA |                22.86 |            MXN |
  +----------+---------------+----------------------+----------------+
  |        1 |           MXN | 0.043744531933508315 |          LIBRA |
  +----------+---------------+----------------------+----------------+
  |        1 |        FRANCO |                20.55 |            MXN |
  +----------+---------------+----------------------+----------------+
  |        1 |           MXN |    0.048661800486618 |         FRANCO |
  +----------+---------------+----------------------+----------------+
  |        1 |           BIT |            434812.81 |            MXN |
  +----------+---------------+----------------------+----------------+
  |       1  |           MXN |2.2998402461969784E-6 |            BIT |
  +----------+---------------+----------------------+----------------+

~~~

## Etapa 03. Diseño la solución
 
![](https://github.com/omararguellesgar/Ejercicios04-02-2023/blob/master/Diagrama%2004.02.2023.1.png)
  
## Etapa 04. Desarrollo de la solución
~~~
 public class Ejercicio {
    double monto, valorDolar = 18.94, valorEuro = 20.29, valorLibra = 22.86, valorFranco = 20.55, valorBit = 434812.81 ;

    public Ejercicio() {
    }

    public Ejercicio(double monto, double valorDolar, double valorEuro, double valorLibra,double valorFranco,double valorBit) {
        this.monto = monto;
        this.valorDolar = valorDolar;
        this.valorEuro = valorEuro;
        this.valorLibra = valorLibra;
        this.valorFranco = valorFranco;
        this. valorBit = valorBit;
    }

    public double conversionDolar() {
        return (this.monto * this.valorDolar);
    }

    public double conversionPeso() {
        return (this.monto / this.valorDolar);
    }

    public double conversionEuro() {
        return (this.monto * valorEuro);
    }

    public double conversionPeso1() {
        return (this.monto / valorEuro);
    }
    public double conversionLibra(){
        return (this.monto * valorLibra);
    }
    public double conversionPeso2(){
        return (this.monto / valorLibra);
    }
    public double conversionFranco(){
        return (this.valorFranco * this.monto);
    }
    public double conversionPeso3(){
        return (this.monto / this.valorFranco);
    }
    public double conversionBit(){
        return (this.monto * this.valorBit);
    }
    public double conversionPeso4(){
        return (this.monto / this.valorBit);
    }

    @Override
    public String toString(){
        return "\n Ingrese la cantidad a convertir:    " + this.monto
                + "\n DOLAR - PESO MEXICANO:     " + conversionDolar()
                + "\n PESO MEXICANO - DOLAR:    " + conversionPeso()
                + "\n EURO - PESO MEXICANO:     "+ conversionEuro()
                + "\n PESO MEXICANO - EURO:     "+ conversionPeso1()
                + "\n LIBRA - PESO MEXICANO:     "+ conversionLibra()
                + "\n PESO MEXICANO - LIBRA:     "+ conversionPeso2()
                + "\n FRANCOS - PESO MEXICANO:     "+ conversionFranco()
                + "\n PESO MEXICANO - FRANCOS:     "+ conversionPeso3()
                + "\n BIT - PESO MEXICANO:     "+ conversionBit()
                + "\n PESO MEXICANO - BIT:     "+ conversionPeso4();
    }
}
import javax.swing.*;

public class Main {
    public static void main(String[] args) {
        Ejercicio conversor = new Ejercicio();
        conversor.monto = Double.parseDouble(JOptionPane.showInputDialog("Ingrese la cantidad a convertir;    "));
        JOptionPane.showMessageDialog(null,conversor.toString());

    }
}
~~~
  
## Etapa 05. Depuración pruebas
    
En este apartado se verifica que el mensaje de salida sea el correcto y sin errores ya que puede no concatenarse correctamente.
~~~    
    @Override
    public String toString(){
        return "\n Ingrese la cantidad a convertir:    " + this.monto
                + "\n DOLAR - PESO MEXICANO:     " + conversionDolar()
                + "\n PESO MEXICANO - DOLAR:    " + conversionPeso()
                + "\n EURO - PESO MEXICANO:     "+ conversionEuro()
                + "\n PESO MEXICANO - EURO:     "+ conversionPeso1()
                + "\n LIBRA - PESO MEXICANO:     "+ conversionLibra()
                + "\n PESO MEXICANO - LIBRA:     "+ conversionPeso2()
                + "\n FRANCOS - PESO MEXICANO:     "+ conversionFranco()
                + "\n PESO MEXICANO - FRANCOS:     "+ conversionPeso3()
                + "\n SOL - PESO MEXICANO:     "+ conversionSol()
                + "\n PESO MEXICANO - SOL:     "+ conversionPeso4();
    }
~~~
 
## Etapa 06. Documentación

Mediante el codigo fuente presentado se podra observar una serie de conversiones de un tipo de moneda a otra, este software fue creado con la intecion de ayudar de una manera rapida a poder conocer los valores de intercambio de monedas de algunos paises que se tomaron como ejemplos.
 
## Ejercicio 02


## Etapa 01. Descripción del problema
 
Se requiere un programa en Java para calcular el resultado de la suma, diferencia, producto, módulo y cociente de dos números decimales de cualquier longitud.

## Etapa 02. Definición de la solución
 
~~~
- Entrada
  
  double num1
  double num2
  double suma
  double diferencia 
  double producto 
  double módulo 
  double cociente

- Proceso
  
  Solicitar numero 1 y numero 2
  Suma de ambos numeros 
  Resta de ambos numeros 
  Producto de ambos numeros
  Modulo de ambos numeros
  Cociente de ambos numeros
 
- Salida
  
  El resultado de la suma
  El resultado de la resta 
  El resultado del producto
  El resultado del modulo
  El resultado del cociente
 
 ~~~

## Etapa 03. Diseño la solución
 
![](https://github.com/omararguellesgar/Ejercicios04-02-2023/blob/master/Diagrama%2004.02.2023.png)
 
## Etapa 04. Desarrollo de la solución
~~~
 public class Ejercicio1 {
    double numero1, numero2;

    public Ejercicio1() {
    }

    public Ejercicio1(double numero1, double numero2) {
        this.numero1 = numero1;
        this.numero2 = numero2;
    }

    public double suma() {
        return (this.numero1 + this.numero2);
    }

    public double resta() {
        return (this.numero1 - this.numero2);
    }

    public double multiplicacion() {
        return (this.numero1 * this.numero2);
    }

    public double division() {
        return (this.numero1 / this.numero2);
    }
    public double resto(){
        return (this.numero1%this.numero2);
    }
    @Override
    public String toString() {
        return "Realiza operaciones basicas con 2 numeros cuales quiera" +
                "\n numero1:" + this.numero1
                + "\n numero2:" + this.numero2
                + "\n LA SUMA ES:   " + suma()
                + "\n LA RESTA ES:    " + resta()
                + "\n LA MULTIPLICACION ES:    " + multiplicacion()
                + "\n LA DIVISION ES:    " + division()
                + "\n EL RESTO ES:      "+ resto();


    }
}

 import javax.swing.JOptionPane;
public class Main {

    public static void main(String[] args) {
        Ejercicio1 c = new Ejercicio1(5, 23);
        Ejercicio1 objetoCalculadora = new Ejercicio1();
        objetoCalculadora.numero1 = Double.parseDouble(JOptionPane.showInputDialog("Ingrese un numero;    "));
        objetoCalculadora.numero2 = Double.parseDouble(JOptionPane.showInputDialog("ingrese un numero:    "));

        JOptionPane.showMessageDialog(null, objetoCalculadora.toString());
    }
}
~~~
   
## Etapa 05. Depuración pruebas 

Se verifica que los operadores sean los correctos y realizen la funcion solicitada
 public double suma() {
        return (this.numero1 + this.numero2);
    }

    public double resta() {
        return (this.numero1 - this.numero2);
    }

    public double multiplicacion() {
        return (this.numero1 * this.numero2);
    }

    public double division() {
        return (this.numero1 / this.numero2);
    }
    public double resto(){
        return (this.numero1%this.numero2);
    }
 
 
## Etapa 06. Documentación
 
Mediante el codigo fuente presentado se podran realizar las operaciones artimeticas basicas empleando los metodos implementados, dando como resultado una suma, una    resta, una multiplicación, una division y el modulo de un par de numeros.
 
 
##  Ejercicio 03


## Etapa 01. Descripción del problema

Se requiere un programa en Java para determinar cuál es el número más pequeño, cuál es el número más grande y cuál es el número intermedio de los tres ingresados.

## Etapa 02. Definición de la solución

~~~
- Entrada
  
  float numero, numero2, numero3, media = 0;
  
- Proceso
  
  Solicitar primer numero a evaluar
  Solicitar segundo numero a evaluar
  Solicitar tercer numero a evaluar
  Si el primer numero ingresado es mayor o igual que el segundo numero y es mayor o igual al tercer numero, el numero de medio es el segundo numero.
  Si el segundo numero ingresado es mayor o igual que el tercer numero y el tercer numero es mayor o igual al primer numero, el numero de medio es el tercer numero.
  Si el tercer numero ingresado es mayor o igual que el numero uno y el primer numero es mayor o igual al segundo numero, el numero de medio es el primer numero. 
  Comprobar numero mas pequeño
  Comprobar numero intermedio
  Comprobar numero mas grande

- Salida
  
  El mayor es
  El menor es
  El medio es
  
~~~
  
## Etapa 03. Diseño la solución

![](https://github.com/omararguellesgar/Ejercicios04-02-2023/blob/master/Diagrama%2004.02.2023.2.png)


## Etapa 04. Desarrollo de la solución
~~~
public class Media {
    float numero, numero2, numero3, media = 0;

    public Media() {
    }

    public Media(float numero, float numero2, float numero3, float media) {
        this.numero = numero;
        this.numero2 = numero2;
        this.numero3 = numero3;
        this.media = media;
    }

    public float mayor() {
        return (Math.max(numero, Math.max(numero2, numero3)));
    }

    public float minimo() {
        return (Math.min(numero, Math.min(numero2, numero3)));
    }

    public float medio() {
        if (numero >= numero2 && numero >= numero3)
            media = numero2;
        if (numero2 >= numero3 && numero3 >= numero)
            media = numero3;
        if (numero3 >= numero && numero >= numero2)
            media = numero;
        return (media);
    }

        @Override
        public String toString () {
            return "NUMEROS A EVALUAR" +
                    "\n Numero 1:   " + this.numero
                    + "\n Numero 2 :  " + this.numero2
                    + "\n Numero 3:   " + this.numero3
                    + "\n EL MAYOR ES:    " + mayor()
                    + "\n EL MENOR ES:    " + minimo()
                    + "\n EL MEDIO ES:    " + medio();
        }
    }
import javax.swing.*;

public class Main {
    public static void main(String[] args) {
        Media c = new Media();

        c.numero = Float.parseFloat(JOptionPane.showInputDialog("INGRESE EL PRIMER NUMERO A EVALUAR;    "));
        c.numero2 = Float.parseFloat(JOptionPane.showInputDialog("INGRESE EL SEGUNDO NUMERO A EVALUAR:    "));
        c.numero3 = Float.parseFloat(JOptionPane.showInputDialog("INGRESE EL TERCER NUMERO A EVALUAR:    "));

        JOptionPane.showMessageDialog(null,c.toString());

    }
}
~~~ 
## Etapa 05. Depuración pruebas

Se verifica que la validación de los numeros mayor y menor sean las correctas y evitar se realize incorrecto, teniendo dentro de este mismo la comprbación del numero medio que queda entre los tres.


~~~ 
 public float medio() {
        if (numero >= numero2 && numero >= numero3)
            media = numero2;
        if (numero2 >= numero3 && numero3 >= numero)
            media = numero3;
        if (numero3 >= numero && numero >= numero2)
            media = numero;
        return (media);
    }
~~~

## Etapa 06. Documentación

El programa realizado tiene la inteción de ayudar de manera automatica a encontrar el numero medio que queda entre tres numeros ingresados, dando como salida final el numero mayor de los tres, el numero menor de los tres y el numero que queda en medio de esos mismos. Se emplean metodos de validación para poder encontrar los resultados.
