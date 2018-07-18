import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Average_Calculator{
    List<Float> myList = new ArrayList<Float>();
    public void createList() {

        int counter = 0;
        boolean cond = true;

        while(cond == true)

        {
            System.out.println("Type a number to test!");
            Scanner inp = new Scanner(System.in);
            float x = inp.nextFloat();
            System.out.println(x);
            if (x == 0) {
                cond = false;
                System.out.println(cond);
                counter = counter +1;
            }
            else{
                myList.add(x);
            }
        }

    }
    public float findAverage(){
        float counter = 0;
        float sum = 0;
        for(float number : myList){
            sum = number + sum;
            counter = counter+1;
        }
        float average = sum / counter;
        return average;
}
    public static void main(String[]args){
        Average_Calculator myNumbers = new Average_Calculator();
        myNumbers.createList();
        float y = myNumbers.findAverage();
        System.out.println(y);


    }
}
