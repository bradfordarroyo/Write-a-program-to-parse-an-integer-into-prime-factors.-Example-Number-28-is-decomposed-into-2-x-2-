# Write-a-program-to-parse-an-integer-into-prime-factors.-Example-Number-28-is-decomposed-into-2-x-2-
Write a program to parse an integer into prime factors. Example: Number 28 is decomposed into 2 x 2 x 7
package bai04;
import java.util.Scanner;
public class Main {
 
    
    public static void phanTich(int n){
        int i=2;
        while(n>1){
            if(cachamchung.checkSNT(i)){
                if(n%i==0){
                    System.out.print(i+".");
                    n/=i;
                }
                else i++;
            }
            else i++;
        }
    }
    public static int enter(){
        Scanner input= new Scanner(System.in);
        boolean check= false;
        int n=0;
        while(!check){
            System.out.print(" ");
            try{
                n= input.nextInt();
                check= true;
            }catch(Exception e){
                System.out.println("You must log in! or log in again...");
                input.nextLine();
            }
        }
        return(n);
    }
    public static void main(String[] args) {
        System.out.print("Tap n");
        int n= enter();
        System.out.print("n= " );
        phanTich(n);
    }
 
}
