# HackerRank
#https://www.hackerrank.com/challenges/pairs
#Given N integers, count the number of pairs of integers whose difference is K .
#Solution using 2 pointer mechanism.


import java.io.*;
import java.util.*;
import java.util.Arrays;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner obj=new Scanner(System.in);
        int n=obj.nextInt();
        int k=obj.nextInt();
        int[] a =new int[n];
        int count=0;
        for(int i=0;i<n;i++)
            a[i]=obj.nextInt();
        Arrays.sort(a);
        int i=0,j=1;
        while(j<n){
            int diff=a[j]-a[i];
            if(diff==k)
               { count++;
                  i++;
                j++;
               }
            if(diff>k)
                i++;
            if(diff<k)
            j++;
       
            } 
         System.out.println(count);
    }
}
