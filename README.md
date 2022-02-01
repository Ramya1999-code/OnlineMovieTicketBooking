import java.util.Scanner;

public class MovieTicketBooking {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Demo d= new Demo();
		d.getname();
	}
	}
 class Demo{
		static Scanner sc = new Scanner(System.in);
		 static String [] movieList= {"1)Avengers End Game", "2)Shershah", "3)Doctor", "4)KGF ", "5)Thor"};
 public static void getname() {
	 String name;
	 System.out.println("Welcome PVR CINEMAS");
	 System.out.println("Enter your name: ");
	 name = sc.nextLine();
	 System.out.println("Hi "+name);
	 getmovie();
	 
	 
 }
 public static void getmovie() {
	
	 System.out.println("Please select the movie to watch: ");
	 for(int i=0; i<movieList.length; i++) {
		 System.out.println(movieList[i]);
		
	 }
	 int choice = sc.nextInt();
	 
	 System.out.println(movieList[choice-1]);  
	 getseat();
	 
 }
 
 public static void getseat() {
	 int n;
	 System.out.println("how many seat you want please Select");
	 n= sc.nextInt();
	 int [] arr = new int[n];
System.out.println("Which seat number you want choose it");
for ( int i=0; i<n; i++) {
	arr[i] =sc.nextInt();
	
}

int amount =n*150;// 1 ticket cost is 150
System.out.println("Total amount to pay: "+amount);
System.out.println("Please select your payment app to pay");

int app=1;
while(app==1) {
	System.out.println("1)Paytm");
	System.out.println("2)PayPal");
	System.out.println("3)PhonePe");
	System.out.println("4)Google Pay");
	int apps = sc.nextInt();
	switch(apps) {
	case 1:
		System.out.println("Welcome to Paytm app");
		break;
	case 2:
		System.out.println("Welcome to PayPal app");
		break;
	case 3:
		System.out.println("Welcome to PhonePe app");
		break;
	case 4:
		System.out.println("Welcome to GooglePay app");
		break;
	}
	break;
}
            System.out.println("Enter the amount ");
          int amountpay = sc.nextInt();
             if (amountpay == amount){
	System.out.println("Your payment is Succesfully");
	System.out.println("Your seat has been Successfully booked");
	System.out.println("Thank you");
             }
             else {
            	
            	 System.out.println("Your payment is Failed Please try Again");
             }
             
 }
 }



	

	
