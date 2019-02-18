import java.util.Random;
import java.util.Scanner;
public class Modeandmedian
{
public static void main (String[]args){
Scanner input = new Scanner(System.in);
Random random = new Random();    
int  i ,j,count,max,maxvalue,num,tmp;

i = 0;
j = 0;
tmp=0;
//numbers = 0;
count = 0;
//tmpcount=0;
//mode =0;
//maxcount =0;
max =10;
//mode2=0;
num=0;
int maxcount=0;
int maxValue = 0;
int numbers[] = new int[max];
//int mode[] = new int [max];
//int median[] =new int [max];

System.out.println ("input 10 nums");
for ( i = 0; i < numbers.length; i++){
num=input.nextInt();
//num=random.nextInt(max);
numbers [i] = num;
}
//------------------------------------------------------------------------------------------
for ( i = 0; i < numbers.length; i++){
count = 0;
for ( j = 0; j < numbers.length; j++){
if (numbers[j] == numbers[i]) {
count++;
    

}
 if (numbers[i] > numbers[j]) 
{
tmp = numbers[i];
numbers[i] = numbers[j];
numbers[j] = tmp;
}
}
if (count >= maxcount) {
maxValue = numbers[i];
maxcount = count;

}
}
System.out.println("The mode is :" + maxValue);

System.out.print("Ascending Order:");
for ( i = 0; i < max - 1; i++) 
{
 System.out.print(numbers[i] + ",");
}
System.out.print(numbers[max - 1]);
//System.out.println("The mode is :" + maxValue);
//Find the median 
//Arrays.sort(numbers);

if (numbers.length % 2 != 0){
System.out.println("The median is:" + numbers[numbers.length/2]); 
}else{
System.out.println("The median is:" + numbers[numbers.length/2] + numbers[numbers.length/2-1]/2);
}



}
}
