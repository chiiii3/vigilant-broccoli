# vigilant-broccoli
import java.util.Scanner;

/**
  *   In-class activity for Fall 2022.
  *
  *   @author Joseph Wolff && Fyodor Dsouza .
  *   @version 03/15/2022
  */
  
public class ApproximatePI
{
   /**
     *   final variable for side length
     *
     */

   public static final int SIDE_LENGTH = 300;
   
   /**
     *   final variable for radius
     *
     */
   
   public static final int RADIUS = SIDE_LENGTH / 2;
   
   
   /**
     *   The entry point for the program.
     *
     *   @param args The command-line arguments to the program.
     */
     public static void main(String [] args)
     {
     
     //Create a Scanner Object
     Scanner scnr = new Scanner(System.in);
     
     // Initialize an int numPoints
     int numPoints = 0;
     
     //Initialize an int n1
     int n1 = 0;
      
     //Initialize an int n2
     int n2 = 0;
     
     //Initalize a double variable percentage
     double percentage = 0.0;
     
     // Calls the inputNumberOfPoints method
     numPoints = inputNumberOfPoints();
     
     // Echo print inputNumberOfPoints
     System.out.println(numPoints);
     
     //Prompt the user for n1
     System.out.print("Enter the first integer: ");
     
     //Set n1 to user input
     n1 = scnr.nextInt();
     
     //Prompt the user for n2
     System.out.print("Enter the second integer: ");
     
     //Set n2 to user input
     n2 = scnr.nextInt();
     
     //Call the computePercentage
     percentage = computePercentage(n1, n2);
     
     //Echo Print computePercentage
     System.out.printf("%nThe percentage is: %.2f", percentage);
     
     
     
     
     
     }
     /**
       *    Prompts the user for the number of points to
       *    generate, inputs the value, and validates it to
       *    be greater than zero. Once a valid value has
       *    been input, the value is returned
       *
       *    @return The number of points to generate 
       */
     
     public static int inputNumberOfPoints()
     {
     // Creates new scanner variable
     Scanner scnr = new Scanner(System.in);
     
     // Initializes return variable for num points
     int numPoints = 0; 
     
     // Flag variable
     boolean flag = false;
     
     while (flag == false)   {
        // Prompt the user
        System.out.print("Enter the number of points(>0): ");
     
        // Sets num points to the users input 
        numPoints = scnr.nextInt();
        
        if (numPoints > 0)   {
            // Sets flag to true
            flag = true; 
        }
        else   {
           // ERROR!
           System.out.println("ERROR: Value must be greater than 0.");
        }
      }
      // Returns 
      return numPoints;
    }
    
    /**
      *  Computes the relationship of the first parameter
      *  to the second, expressed as a percentage. Once the
      *  percentage value has been calculated, the value is 
      *  returned to the calling method.
      *
      *  @param n1 The first integer.
      *  @param n2 The second integer.
      *  @return The value of (n1 / n2).
      */ 
    
    public static double computePercentage(int n1, int n2) 
    {
      //Initialze a double temp
      double temp = n1;
      
      //Initialize an double percentage
      double percentage = 0.0;
      
      //Calculate percentage
      percentage = temp / n2;
      
      
      
      //Return percentage
      return percentage;  
    }
    /**
      * Computes the distance between two points of (x1, x2)
      * (and y1, y2)
      *
      * @param x1 The first x coordinate
      * @param x2 The second x coordinate
      * @param y1 The first x coordinate
      * @param y2 The second x coordinate
      * @return The value of distance
      */
   
   
      public static double computeDistance(int x1, int y1, int x2, int y2)
      {
   
      // Initializes a return double for distance
      double distance = 0.0;
   
      // Computes the distance using points x1 x2 y1 y2
      distance = Math.sqrt(Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2));
   
      // return
      return distance;
   }
   }
        
      


     
