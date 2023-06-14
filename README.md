# Maximum-Weight-Difference
Telling the Chef the maximum possible difference between the weight carried by him & his son

int MaximumWeightDifference(int[] arr,int N,int k)

{
                 
		 //Sorting using Bubble Sort

		for (int i = 1; i < N; i++) 
       {
			for (int j = 0; j < N-1; j++) 
              {
				if(arr[j] > arr[j+1]) 
                                {
					int temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp;
                                }
	      }
       }

    if(k>N/2)
    {
      k=N-k;
    }

  int sum1=0,sum2=0;

  // Sum upto k items
  for(int i=0;i<k;i++)
  {
    sum1+=arr[i];
  }

  // Sum of remaining items
  for(int i=k;i<N;i++)
  {
    sum2+=arr[i];
  }

  // Maximum Weight Difference
   return sum2-sum1;
   
   
   }


