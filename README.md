# loging-and-calculater
package passwords;
import java.util.Scanner;

public class cal {

public double equle(double x,double y) {
	return x+y;
}


public double minus(double x,double y) {
	return x-y;
}


public double multi(double x,double y) {
	return x*y;
}


public double div(double x,double y) {
	return x/y;
}
}

public class main {

public static void main(String[] args) {
	char ch;
	cal cl=new cal();
	Scanner scr2=new Scanner(System.in);
	
	while(true) {
		
do{
	Scanner scr=new Scanner(System.in);
	System.out.println("Enter user name:");
	String username=scr.nextLine();
	System.out.println("Enter password:");
	String password=scr.nextLine();
	
	if(username.equals("Naduka0916") && password.equals("IT21820182")) {
		System.out.println("Welcome user!!");
		
		break;
	}
	else {
		System.out.println("error");
	}
	System.out.println("Do you want to continue??? (y foe yes N for no)");
	ch=scr.next().charAt(0);
}
while(ch =='y'||ch== 'Y');
break;
}

System.out.println("What ndo you need to do today??");
System.out.println("If you want to user usd to lkr cal type 'money ex'\nIf you want to user calculator type 'cal':");
String input=scr2.nextLine();
if(input.equals("money_ex")||input.equals("Money_Ex")) {
	double usd;
	
	System.out.println("Enter your usd value:");
	usd=scr2.nextDouble();
	double usdToLkr=usd*350;
	System.out.println("your usd to Lkr is:"+usdToLkr);
	
}
else if(input.equals("cal")){
	System.out.println("1 for equl\n2 for minus\n3 for multiple\n4 for divide");
	System.out.println("select your calculation type:");
	int option=scr2.nextInt();
	
	switch(option) {
	
	case 1:
		System.out.println("entet your 1st number:");
		double num1=scr2.nextDouble();
		System.out.println("enter your 2nd number:");
		double num2=scr2.nextDouble();
		double resulteql=cl.equle(num1, num2);
		System.out.println("result is:"+resulteql);
		
		break;
		
	case 2:
		System.out.println("entet your 1st number:");
		double num3=scr2.nextDouble();
		System.out.println("enter your 2nd number:");
		double num4=scr2.nextDouble();
		double resultminus=cl.minus(num3, num4);
		System.out.println("result is:"+resultminus);
		
		break;
	case 3:
		System.out.println("entet your 1st number:");
		double num5=scr2.nextDouble();
		System.out.println("enter your 2nd number:");
		double num6=scr2.nextDouble();
		double resultmulti=cl.multi(num5, num6);
		System.out.println("result is:"+resultmulti);
		
		break;
		
	case 4:
		System.out.println("entet your 1st number:");
		double num7=scr2.nextDouble();
		System.out.println("enter your 2nd number:");
		double num8=scr2.nextDouble();
		double resultdivide=cl.div(num7, num8);
		System.out.println("result is:"+resultdivide);
		
		break;
	}
}

else {
	System.out.println("Unknown data type!!!");
}
}
