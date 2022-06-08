# coderByte_Roman-Numeral-Reduction
import java.util.*; 
import java.io.*;

class Main {

  public static String RomanNumeralReduction(String str) {
    // code goes here 
    int n = str.length();

    int number =0;

    String[] strArr= str.split("");
   // System.out.println(strArr);

    for(int i=0; i<n;i++){
     // System.out.println(strArr[i]);

      if(strArr[i].equals("I")){

        number = number +1;
      } else if(strArr[i].equals("V")){
        number = number +5;

      }  else if(strArr[i].equals("X")){
        number = number +10;

      } else if(strArr[i].equals("L")){
        number = number +50;
      }else if(strArr[i].equals("C")){
        number = number +100;
      }else if(strArr[i].equals("D")){
        number = number +500;
      } else if(strArr[i].equals("M")){
        number = number +1000;
      }

          }
       
          String romanNum ="";

          while(number>=1000){
           romanNum =romanNum+"M";
           number=number-1000;
          }
            while(number>=500){
            romanNum =romanNum+"D";
            number=number-500;
          }
          while(number>=100){
            romanNum =romanNum+"C";
            number=number-100;
          } while(number>=50){
            romanNum =romanNum+"L";
            number=number-50;
          } while(number>=10){
            romanNum =romanNum+"X";
            number=number-10;
          } while(number>=5){
            romanNum =romanNum+"V";
            number=number-5;
          }while(number>=1){
            romanNum =romanNum+"I";
            number=number-1;
          }

    return romanNum;
  }

  public static void main (String[] args) {  
    // keep this function call here     
    Scanner s = new Scanner(System.in);
    System.out.print(RomanNumeralReduction(s.nextLine())); 
  }

}
