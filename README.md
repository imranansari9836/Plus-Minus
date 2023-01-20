import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

class Result {

    /*
     * Complete the 'plusMinus' function below.
     *
     * The function accepts INTEGER_ARRAY arr as parameter.
     */

    public static void plusMinus(List<Integer> arr) {
    // Write your code here
    float pos=0;
    float neg=0;
    float zero=0;
    for(int i=0;i<arr.size();i++)
    {
        if(arr.get(i)>0)//1>0
        {
            pos++;//2
        }
        else if(arr.get(i)<0)//1<0
        {
            neg++;//2
        }
        else if(arr.get(i)==0)
        {
            zero++;//1
        }
    }
    pos=pos/arr.size();//2/5
    neg=neg/arr.size();//2/5
    zero=zero/arr.size();//1/5
    System.out.println(pos);//0.400000
     System.out.println(neg);//0.400000
      System.out.println(zero);//0.200000
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        String[] arrTemp = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        List<Integer> arr = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int arrItem = Integer.parseInt(arrTemp[i]);
            arr.add(arrItem);
        }

        Result.plusMinus(arr);

        bufferedReader.close();
    }
}
