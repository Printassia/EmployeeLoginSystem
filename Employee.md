# EmployeeLoginSystem
import java.util.Scanner;

public class Employee {

    String firstName, lastName,response;
    int empNo, department;
    int counter = 0;

    public void Info() {
        Scanner in = new Scanner(System.in);

        System.out.print("First Name:\t");
        this.firstName = in.next();
        System.out.print("Last Name:\t");
        this.lastName = in.next();
        System.out.print("Employee Number:");
        this.empNo = in.nextInt();
        System.out.println("Department codes:\n100:Information Technology\n200: Engineering\n" +
                "300: Accounting");
        System.out.println("Input your Department Code:\t");
        this.department = in.nextInt();
    }

    /**
     * public void setInfo(String firstName, String lastName, String department, int empNo){
     * Scanner in = new Scanner(System.in);
     * <p>
     * this.firstName = firstName;
     * this.lastName = lastName;
     * this.department = department;
     * this.empNo = empNo;
     * }
     */

    void display() {
        System.out.println("***KemTech Software KT, International, Software Engineering***");
        System.out.println("***Please Login***\n");
    }

    public void Count() {
        if (this.firstName != null && this.lastName != null){

            counter++;
        }
        else {
            System.out.println("Enter you firstname and lastname in the fields");
        }

        System.out.println("***Login Information Logged***");
        System.out.println("First Name: "        + firstName);
        System.out.println("Last Name: "         + lastName);
        System.out.println("Department: "        + department);
        System.out.println("Employee Number: "   + empNo);
        System.out.println("Counter: " + counter);


    }

    void exit(){
        Scanner input = new Scanner(System.in);
        System.out.println("Next Employee ? y/n");
        this.response = input.next();
        if (this.response.equalsIgnoreCase("n")){
            System.exit(0);

        }

        else if (this.response.equalsIgnoreCase("y")){
            boolean cont = true;
            while (cont){
                System.out.println("\n");
                display();
                Info();
                Count();
            }
        }

    }

}


