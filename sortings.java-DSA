import java.io.*;
import java.util.*;
class Main
{
    public static void mergesort(int arr[],int low,int high)
    {
        if(low<high)
        {
            int mid=(low+high)/2;
            mergesort(arr,low,mid);
            mergesort(arr,mid+1,high);
            merge(arr,low,mid,high);
        }
    }
    
    public static void merge(int arr[],int low,int mid,int high)
    {
        int i=low,j=mid+1,k=low;
         int temp[]=new int[arr.length];
         while(i<=mid && j<=high)
         {
             if(arr[i]<arr[j])
             {
                temp[k] = arr[i];
                i++;
                k++;
             }
             else//arr[i]>arr[j]
             {
                 temp[k] = arr[j];
                 j++;
                 k++;
             }
         }
         if(i>mid)
         {
             while(j<=high)
             {
                 temp[k]=arr[j];
                 j++;
                 k++;
             }
             
         }
         if(j>high)
         {
             while(i<=mid)
             {
                 temp[k] = arr[i];
                 i++;
                 k++;
             }
         }
         for(i=low;i<=high;i++)
         {
             arr[i]=temp[i];
         }
    }
    public static void main(String args[])
    {
        int arr[]={12,5,8,3,9,0};
        int n=arr.length;
       
        mergesort(arr,0,n-1);
        System.out.print("Array is: "+Arrays.toString(arr));
    }
}
