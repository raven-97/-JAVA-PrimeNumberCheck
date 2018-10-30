import java.io.*;

public class Prime_Or_Not_PositiveIntegerCheck
{  	
	static private boolean Prime_Or_Not_PositiveIntegerCheck(int input)
	{
			int currentRemainder;
			boolean divisibleFLAG = false,
						  primeFLAG = false;
			
			if (input > 0 && input != 1)
			{ 
				for(int i = 2; i < input/2; i++)
				{
					currentRemainder = input % i;
					divisibleFLAG = (currentRemainder == 0) ? true : false;
					System.out.println("DIVISION TRACE: Divisible By " + i +": "+  divisibleFLAG);
					
					primeFLAG = (divisibleFLAG == false) ? true : false;
				}
				return primeFLAG;
			}
			else return false;
	}
	
	static private boolean isPrimeNumber(int number)
	{
		if(number  == 2 || number ==3){
			System.out.println("Prime Number!!!");
		}else{
			if(number % 2 == 0){
			System.out.println("Not a prime Number");
		}else if(number % 3 == 0 ){
			System.out.println("Not a prime Number");
		}else{
			System.out.println("Prime Number!!!");
		}
		}
		
	}
	
	public static void main(String args[])
	{
		System.out.print("\nEnter the positive whole number: ");
		//boolean output = Prime_Or_Not_PositiveIntegerCheck(Integer.parseInt(System.console().readLine()));
		//boolean output = isPrimeNumber(Integer.parseInt(System.console().readLine()));
		//System.out.print("\nThe number is a Prime Number: " + output + "\n");

 isPrimeNumber(Integer.parseInt(System.console().readLine()));		
	}
}
