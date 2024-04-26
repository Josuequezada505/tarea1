import java.util.InputMismatchException;
import java.util.Scanner;

public class trycatch {
    public static void main (String args []){

        int num1,num2,num3,menor1,menor2,mayor,sumamenores,diferencia;
        Scanner entrada = new Scanner (System.in);
try {
        System.out.println("INGRESE EL PRIMER NUMERO");
            num1 = entrada.nextInt();
        System.out.println("INGRESE EL SEGUNDO NUMERO");
            num2 = entrada.nextInt();   
         System.out.println("INGRESE EL TERCER NUMERO");
            num3 = entrada.nextInt(); 
         //sumar los 2 mas pequeños;
         if(num1<num2 && num1<num3){
            menor1=num1;
            if (num2 < num3){
                menor2=num2;
                mayor = num3;
            }
            else {menor2 =num3;
            mayor = num2;}

         } else if (num2 <num1 && num2< num3){
            menor1=num2;
            if (num1 < num3){
                menor2 = num1;
                mayor = num3;
            }
            else {menor2 = num3;
            mayor = num1;}
           } else {
            menor1= num3;
            if (num1 < num2){
                menor2= num1;
                mayor = num2;
            }
            else {menor2 =num2;
            mayor = num1;}
           }
         
            sumamenores = menor1+menor2;
            diferencia = mayor - menor2;
            System.out.println("La suma de los menores es"+sumamenores);
            System.out.println("La diferecnia de los mayores es"+diferencia);
            System.out.println("El mayor es"+ mayor);
         


       
    } catch (InputMismatchException ex) {
        System.out.println("Debe ingresar obligatoriamente un número entero.");
    }
    }

    
}
