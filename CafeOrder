import java.io.FileWriter;
import java.io.IOException;
import java.text.DateFormat;
import java.text.NumberFormat;
import java.util.ArrayList;
import java.util.Scanner;
import java.util.InputMismatchException;
import java.util.Date;


public class CafeOrder{
        
        double espressoPrice = 3;
        double lattePrice = 4.75;
        double cappuccinoPrice = 4;
        double coldBrewPrice = 4;
        double totalPrice = 0;
        
        Scanner scnr = new Scanner(System.in);
        Scanner scnr1 = new Scanner(System.in);
        NumberFormat formatter = NumberFormat.getCurrencyInstance();
        
        double extraEspressoPrice = 1.50;
        double pannaPrice = 1.50;
        double oatMilkPrice = 1;
        double almondMilkPrice = 1;
        
        double tunaSandwichPrice = 11;
        double chickenSandwichPrice = 9;
        double burritoPrice = 10;
        double yogurtBowlPrice = 9;
        double avocadoToastPrice = 8;
       
        ArrayList<String> list = new ArrayList<String>();
        
        
           
   
            
        public CafeOrder(){
           
            Coffee();
            AddOns();
            Food();
            String name = printName();
            Date now = new Date();  
            DateFormat defaultDate = DateFormat.getDateTimeInstance(DateFormat.MEDIUM, DateFormat.MEDIUM);
            String time = defaultDate.format(now);
            System.out.print(defaultDate.format(now) + " " + name + ",");
            System.out.print(list.toString().replace("["," ").replace("]"," "));
            System.out.println(formatter.format(totalPrice));
            
        
               try {
            FileWriter writer = new FileWriter("order.txt", true);
            writer.write(defaultDate.format(now) + " " + name + ",");
            writer.write(list.toString().replace("["," ").replace("]"," ")); 
            writer.write(formatter.format(totalPrice));
            writer.write(" ");
            writer.close();
        } catch (IOException e) {
        }      
            
        
        }
    
    public void Coffee() {
        
        System.out.println("=== Select Coffee: ===");
        System.out.println("1 Espresso          " + formatter.format(espressoPrice));
        System.out.println("2 Latte             " + formatter.format(lattePrice));
        System.out.println("3 Cappuccino        " + formatter.format(cappuccinoPrice));
        System.out.println("4 Cold Brew         " + formatter.format(coldBrewPrice));
        System.out.print("Select a coffee [1, 4]: ");
        boolean flag = true;
        int coffeeOrder;
        
        while (flag) {
            
            try {
                coffeeOrder = scnr.nextInt();
                
                if (coffeeOrder == 1) {
                    totalPrice += espressoPrice;
                    list.add("Espresso");
                    flag = false;
                } 
               
                else if (coffeeOrder == 2) {
                    totalPrice += lattePrice;
                    list.add("Latte");
                    flag = false;
                } 
                
                else if (coffeeOrder == 3) {
                    totalPrice += cappuccinoPrice;
                    list.add("Cappuccino");
                    flag = false;
                } 
                
                else if (coffeeOrder == 4) {
                    totalPrice += coldBrewPrice;
                    list.add("Cold brew");
                    flag = false;
                } 
                
                else {
                    System.out.println("Error! Number must be between 1-4.");
                    System.out.println("Select a coffee [1, 4]: ");
                }
            } 
            catch (InputMismatchException e) {
                System.out.println("Error! Number must be between 1-4.");
                System.out.println("Select a coffee [1, 4]: ");
                scnr.next();
            }
        }
    }
        
    public void AddOns() {
        System.out.println("\n=== Select Add on: ===");
        System.out.println("1 Extra Espresso    " + formatter.format(extraEspressoPrice));
        System.out.println("2 Panna             " + formatter.format(pannaPrice));
        System.out.println("3 Oat Milk          " + formatter.format(oatMilkPrice));
        System.out.println("4 Almond Milk       " + formatter.format(almondMilkPrice));
        System.out.println("5 Quit Add on selection");
        System.out.print("Select Add Ons: [1,5]: ");
        boolean flag1 = true;
        
        while (flag1) {
            
            try{
            int addOnOrder = scnr.nextInt();
            
            switch (addOnOrder) {
                
                case 1:
                    totalPrice += extraEspressoPrice;
                    System.out.println("\n=== Select Add on: ===");
                    System.out.println("1 Extra Espresso    " + formatter.format(extraEspressoPrice));
                    System.out.println("2 Panna             " + formatter.format(pannaPrice));
                    System.out.println("3 Oat Milk          " + formatter.format(oatMilkPrice));
                    System.out.println("4 Almond Milk       " + formatter.format(almondMilkPrice));
                    System.out.println("5 Quit Add on selection");
                    System.out.print("Select Add Ons: [1,5]: ");
                    list.add("Extra espresso");
                    break;
                
                case 2:
                    totalPrice += pannaPrice;
                    System.out.println("\n=== Select Add on: ===");
                    System.out.println("1 Extra Espresso    " + formatter.format(extraEspressoPrice));
                    System.out.println("2 Panna             " + formatter.format(pannaPrice));
                    System.out.println("3 Oat Milk          " + formatter.format(oatMilkPrice));
                    System.out.println("4 Almond Milk       " + formatter.format(almondMilkPrice));
                    System.out.println("5 Quit Add on selection");
                    System.out.print("Select Add Ons: [1,5]: ");
                    list.add("Panna");
                    break;
                
                case 3:
                    totalPrice += oatMilkPrice;
                    System.out.println("\n=== Select Add on: ===");
                    System.out.println("1 Extra Espresso    " + formatter.format(extraEspressoPrice));
                    System.out.println("2 Panna             " + formatter.format(pannaPrice));
                    System.out.println("3 Oat Milk          " + formatter.format(oatMilkPrice));
                    System.out.println("4 Almond Milk       " + formatter.format(almondMilkPrice));
                    System.out.println("5 Quit Add on selection");
                    System.out.print("Select Add Ons: [1,5]: ");
                    list.add("Oat milk");
                    break;
                
                case 4:
                    totalPrice += almondMilkPrice;
                    System.out.println("\n=== Select Add on: ===");
                    System.out.println("1 Extra Espresso    " + formatter.format(extraEspressoPrice));
                    System.out.println("2 Panna             " + formatter.format(pannaPrice));
                    System.out.println("3 Oat Milk          " + formatter.format(oatMilkPrice));
                    System.out.println("4 Almond Milk       " + formatter.format(almondMilkPrice));
                    System.out.println("5 Quit Add on selection");
                    System.out.print("Select Add Ons: [1,5]: ");
                    list.add("Almond milk");
                    break;
                
                case 5:
                    totalPrice += 0;
                    flag1 = false;
                    break;
                default:
                    System.out.println("Error! Number must be a number between 1-5");
                    System.out.println("Select Add Ons: [1,5]: ");
                    break;
            }
            }
            catch (InputMismatchException e) {
                System.out.println("Error! Number must be between 1-5.");
                System.out.println("Select Add Ons: [1, 5]: ");
                scnr.next();
            }
        }
        }
        
    public void Food() {
        System.out.println("\n=== Select Food ===");
        System.out.println("1 Tuna Sandwich     " + formatter.format(tunaSandwichPrice));
        System.out.println("2 Chicken Sandwich  " + formatter.format(chickenSandwichPrice));
        System.out.println("3 Burrito           " + formatter.format(burritoPrice));
        System.out.println("4 Yogurt Bowl       " + formatter.format(yogurtBowlPrice));
        System.out.println("5 Avocado Toast     " + formatter.format(avocadoToastPrice));
        System.out.println("6 Quit Food selection");
        System.out.print("Select Food: [1, 6]: ");
        
        boolean flag2 = true;
        
        while (flag2) {
            
            try{
            int foodOrder = scnr.nextInt();
            
            switch (foodOrder) {
                
                case 1:
                    totalPrice += tunaSandwichPrice;
                    list.add("Tuna sandwich,");
                    flag2 = false;
                    break;
                
                case 2:
                    totalPrice += chickenSandwichPrice;
                    list.add("Chicken sandwich,");
                    flag2 = false;
                    break;
               
                case 3:
                    totalPrice += burritoPrice;
                    list.add("Burrito,");
                    flag2 = false;
                    break;
                
                case 4:
                    totalPrice += yogurtBowlPrice;
                    list.add("Yogurt bowl,");
                    flag2 = false;
                    break;
                
                case 5:
                    totalPrice += avocadoToastPrice;
                    list.add("Avocado toast,");
                    flag2 = false;
                    break;
                
                case 6:
                    totalPrice += 0;
                    flag2 = false;
                    break;
                default:
                    System.out.println("Error! Number must be a number between 1-6.");
                    System.out.print("Select Food: [1, 6]: ");
            }
            }
            catch (InputMismatchException e) {
                    System.out.println("Error! Number must be a number between 1-6.");
                    System.out.print("Select Food: [1, 6]: ");
                    scnr.next();
            }
            
        }
    }
    
    public String printName() {
        System.out.println("\nEnter customer's name: ");
        String customerName = scnr1.nextLine();
        return customerName;
    }
    
    
    }
