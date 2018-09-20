# Saya
CalculatePhoneBills
public class CalculatePhoneBill {
      public static void main(String[] args) {
	
	   Scanner scan = new Scanner (System.in);
	   System.out.println("Enter please number of received calls");
	   double numberOfCalls =scan.nextDouble();
	   
	   double firstCharge = 0.60*50;    //plus $0.60 per call for next 50 calls
	   double secondCharge = 0.50*50;   // plus $0.50 per call for the next 50 calls
	                                    // plus $0.40 per call for any call beyond 200 calls
	   double billForCalls = 200.00;  
	   
	   double bill1 = billForCalls+(numberOfCalls-100)*0.60;
	   double bill2 = billForCalls+firstCharge+(numberOfCalls-150)*0.50;
	   double bill3 = billForCalls+firstCharge+secondCharge+(numberOfCalls-200)*0.40;
	   
	  
	   if (numberOfCalls >= 0 && numberOfCalls <= 100) {
		   System.out.println("Your bill is : "+"$ "+ billForCalls);
		   
	   } else if(numberOfCalls >= 101 && numberOfCalls <= 150) {
		   System.out.println("Your bill is :" +"$ "+bill1);
		   
	   } else if (numberOfCalls >= 151 && numberOfCalls <= 200) {
		   System.out.println("Your bill is : "+"$ "+bill2);
		   
	   } else if (numberOfCalls >200) {
		   System.out.println("Your bill is :"+"$ "+bill3);
		   
	   } else  {
		   System.out.println("INVALID NUMBER OF CALLS");
	   }
	   scan.close();
}
}
