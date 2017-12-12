# MP7
Rap Name Generator
import java.util.Scanner;

public class NameGenerator {

	String prefix;
	
	String middle;
	
	String suffix;
	
	public NameGenerator(String first, String second, String last) {
		this.prefix = first;
		this.middle = second;
		this.suffix = last;
		
	}
	
	public String getRapName() {
		return this.prefix + " " + this.middle + " " + this.suffix;
	}



 public static String generator(String firstName, int birthday, String favoriteAnimal) {
        firstName = firstName.toLowerCase();

        favoriteAnimal = favoriteAnimal.toLowerCase();
         String rapNamePrefix = "";
         String rapNameMiddle = "";
         String rapNameLast = "";
                if (birthday == 1 || birthday == 4 || birthday == 6 || birthday == 11 ) {
                        rapNamePrefix += "lil";

                } else if (birthday ==  2|| birthday == 5 || birthday == 7 || birthday == 12 ) {
                        rapNamePrefix += "young";

                } else {
                        rapNamePrefix += "supa";
                }

                if((int) (firstName.charAt(2)) <= 100) {
                        rapNameMiddle += " " + favoriteAnimal +  "y ";
                } else if ((int) (firstName.charAt(2)) <= 104 && (int) (firstName.charAt(2)) > 100) {
                        rapNameMiddle += " fetti-Chini";
                } else if ((int) (firstName.charAt(2)) <= 108 && (int) (firstName.charAt(2)) > 104) {
                        rapNameMiddle += " poKemon";
                } else if ((int) (firstName.charAt(2)) <= 112 && (int) (firstName.charAt(2)) > 108) {
                        rapNameMiddle += " " + favoriteAnimal +  "man ";
                } else if ((int) (firstName.charAt(2)) <= 116 && (int) (firstName.charAt(2)) > 112) {
                        rapNameMiddle += " guaccy-mollie";
                } else if ((int) (firstName.charAt(2)) <= 122 && (int) (firstName.charAt(2)) > 116) {
                        rapNameMiddle += " grecian potato";
                } else {
                        rapNameMiddle += "cheater";
                }
                if((int) (favoriteAnimal.charAt(2)) <= 100) {
                        rapNameLast += " eata ";
                } else if ((int) (favoriteAnimal.charAt(1)) <= 104 && (int) (favoriteAnimal.charAt(1)) > 100) {
                        rapNameLast += " fighta";
                } else if ((int) (favoriteAnimal.charAt(1)) <= 108 && (int) (favoriteAnimal.charAt(1)) > 104) {
                        rapNameLast += " the rapper ";
                } else if ((int) (favoriteAnimal.charAt(1)) <= 112 && (int) (favoriteAnimal.charAt(1)) > 108) {
                        rapNameLast += " playa ";
                } else if ((int) (favoriteAnimal.charAt(1)) <= 116 && (int) (favoriteAnimal.charAt(1)) > 112) {
                        rapNameLast += " killa ";
                } else if ((int) (favoriteAnimal.charAt(1)) <= 122 && (int) (favoriteAnimal.charAt(1)) > 116) {
                        rapNameLast += " the creater ";
                } else {
                        rapNameLast += " balla ";
                }

        NameGenerator createdName = new NameGenerator(rapNamePrefix, rapNameMiddle, rapNameLast);
        return createdName.getRapName();



                  
}

				public static void main(final String[] unused) {
                        Scanner inputScanner = new Scanner(System.in);

                        System.out.println("Please enter your first name:");
                        String firstName = inputScanner.nextLine();

                        System.out.println("Please enter your favorite Animal:");
                        String favoriteAnimal = inputScanner.nextLine();

                        System.out.println("Please enter your birth month as an integer 1-12:");
                        int birthday = inputScanner.nextInt();






                       System.out.println(String.format("Your rap name is: " + generator(firstName, birthday, favoriteAnimal)));


                        inputScanner.close();
                   }




        }
