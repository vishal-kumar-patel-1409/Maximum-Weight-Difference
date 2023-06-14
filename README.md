# Maximum-Weight-Difference
Telling the Chef the maximum possible difference between the weight carried by him & his son

int MaximumWeightDifference(int[] arr,int N,int k)
{
    if(k>N/2)
    {
      k=N-k;
    }

  int sum1=0,sum2=0;

  Arrays.sort(arr);

  for(int i=0;i<k;i++)
  {
    sum1+=arr[i];
  }

  for(int i=k;i<N;i++)
  {
    sum2+=arr[i];
  }

return sum2-sum1;

}

