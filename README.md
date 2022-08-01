# GPA-Calculator
/*
Dileep kumar 
*/
GPA calculator using java language


import java.util.Scanner;

class GPA {
     public static void main(String[] Dileep_kumar) {
        Scanner scan = new Scanner(System.in);
        Scanner input = new Scanner(System.in);

        int size;
        int sumCreditGpa = 0;
        double creditGpa ;
        double totalCreditHours=0;
	double GPA=0;

        System.out.println("Enter the number of Subjects");
        size = scan.nextInt();
        String [] sub = new String[size];

        System.out.println("TAKING THE NAME OF THE SUBJECTS\n");
        for (int i = 0; i < size; i++) {
            System.out.println("Enter the name of the Subject " + (i + 1));
            sub[i] =input.nextLine();
        }
        double [] creditHours = new double[size];


        System.out.println("TAKING THE CREDIT HOURS OF THE SUBJECTS\n");
       // double [] gpa = new double[size];
        for (int i = 0; i < size; i++) {

            System.out.println("Enter the Credit hours of " + sub[i]);
            creditHours[i] = input.nextInt();
            totalCreditHours+=creditHours[i];
        }
		
		
		double p[]= new double[size];
		for (int i=0; i<size;i++)
		{
		System.out.println("Enter the percentage of the  "+sub[i]);
		p[i]=input.nextDouble();
		if (p[i]>=93 && p[i]<=100)
		{
			GPA=4;
		}
		else if (p[i]>=87 && p[i]<=92)
		{
			GPA=3.67;
		}
		else if (p[i]>=82 && p[i]<=86)
		{
			GPA=3.33;
		}
		else if (p[i]>=77 && p[i]<=81)
		{
			GPA=3.0;
		}
		else if (p[i]>=72 && p[i]<=76)
		{
			GPA=2.67;
		}
		else if (p[i]>=68 && p[i]<=71)
		{
			GPA=2.3;
		}
		else if (p[i]>=64 && p[i]<=67)
		{
			GPA=2.0;
		}
		else if (p[i]>=60 && p[i]<=63)
		{
			GPA=1.67;
			
		}
		else if (p[i]>=0 && p[i]<=59)
		{
			GPA=0.00;
			
		}
		}
        System.out.println();
	System.out.println();
	System.out.println();

	System.out.println("********************************************");

	System.out.println("Subject\t\tPercent\t\tCredit Hours");
for (int i = 0; i < size; i++) {
            creditGpa=creditHours[i]*GPA;
            sumCreditGpa +=creditGpa;
              System.out.println(sub[i]+"\t\t"+p[i]+"\t\t"+creditHours[i]);
        }
        System.out.println("********************************************");
	System.out.println();
	System.out.println();

        System.out.println("GPA is \n"+ sumCreditGpa /totalCreditHours);  
        	
        
}}

