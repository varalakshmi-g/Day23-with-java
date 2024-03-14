# Day23-with-java

Hey all, Today I practiced and learned 
import java.util.Scanner;

class Day22 {
     static int[] mergeArrays(int[] ar1, int[] ar2)
     {
        int i = 0, j = 0, k = 0;
        int[] res = new int[ ar1.length + ar2.length ];
        
        while (i<ar1.length && j<ar2.length)
        {
            if (ar2[j] <= ar1[i])
            {
                res[k] = ar2[i];
                k++;
                j++;
            }
            else
            {
                res[k] = ar1[i];
                k++;
                i++;
            }
        }
        while (j < ar2.length) 
        {
            res[k] = ar2[j];
            k++;
            j++;
        }
        while (i< ar1.length)
        {
            res[k] = ar1[i];
            k++;
            i++;
        }
        public static void main(String[] args)
    {
        Scanner scan = new Scanner(System.in);
        int n1 = scan.nextInt();
        int[] ar1 = new int[n1];
        for(int i = 0; i < ar1.length; i++)
        {
            ar1[i] = scan.nextInt();
        }
        int n2 = scan.nextInt();
        int[] ar2 = new int[n2];
        for(int i = 0; i < ar2.length; i++)
        {
            ar2[i] = scan.nextInt();
        }
        int[] res = mergeArrays(ar1, ar2);
        for(int i = 0; i < res.length; i++)
        {
             System.out.print(res[i] + " ");
        }
    }
}



    

