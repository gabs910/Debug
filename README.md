# Debug



****************************8Craps Game****************************************
-found no bug in this code


*****************************Dice Game*****************************************
-found no bugs



**************************The Bank Statement***********************************
-Balance in the output was not aligning by the decimal

-corrected it by changing

	System.out.printf("%-1s %-4s %-19s %-8s", getType(),getAccountId(),getDescription(),df.format(balance));
to:

	System.out.printf("%-1s %-4s %-19s %8s", getType(),getAccountId(),getDescription(),df.format(balance));


-Savings class displaying 0.0 for the interest rate when savings should always have an interest rate

-corrected it by deleting this constructor:

	public Savings() {
	this.setType("S");
		}
other constructors require that input a rate when creating an instance of the class


-checking class displaying null when created with no description, changing code to not allow
 checking class to be created without a description

-deleting this constructor:
	
	}
	
	public Checking(){
		this.setType("C");
	}


*************************RPN Calculator****************************************

-in the switch statement there was nothing to deal with the case of divivding by 0

-added code to deal with if you try to divide by 0:

		case "/":
			if(pop1!= 0){
			stk.push(pop2 / pop1);
			} else {
				System.out.println("Cannot divide by 0");
			}
			
			break;

-added if statement above to not allow dividing  by zero creates a problem later 
 
 in the program when the program executes and asks if you want to continue with operations
 
 if you divided by zero it will return "can't divide by zero" but will allow you to 
 
 do another operation causing the program to error out.

_fix:

  added a return statement which effectively terminates the running of the code 
  if condition is met.

	case "/":
		if(pop1!= 0){
		stk.push(pop2 / pop1);
		} else {
			System.out.println("Cannot divide by 0");
		  return;
		}
		break;

******************************Bowling Game*****************************************

-didn't fing any bugs in this one


