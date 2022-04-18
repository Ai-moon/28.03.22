# 28.03.22
it's a great desion! 
import java.util.Arrays; 
public class ZywOo { 
public static int sumOfDifferences(int[] arr) { 
Arrays.sort(arr);
 return arr.length <= 1 ? 0 : arr[arr.length-1] - arr[0];
 } 
} 
public class ZywOo { 
/* The idea is that such sum could be flatten.
 Example: [2, 1, 10] (10 - 2) + (2 - 1) = 8 + 1 = 9 10 -2 + 2 -1 = 10 - 1
 So all elements except max and min will be used twice (one time with + and one tme ith -) so they will be erased. 
*/ public static int sumOfDifferences(int[] arr) { 
if (arr.length < 2) { 
return 0; 
} 
int min = arr[0]; 
int max = arr[0];
 for (int i = 1; i < arr.length; i++) {
   if (arr[i] > max) { max = arr[i]; 
} 
if (arr[i] < min) { min = arr[i];
 } 
} 
return max - min;
  }
 }
