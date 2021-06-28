# String-
//how to Split a given String on the basis of Spaces

String s="hefshine is best"; 
		int count=1;
		for (int i = 0; i < s.length(); i++)
		{
			if (s.charAt(i)==' ')
			{
				count++;
			}
		}
		System.out.println(count);
		
		String arr[]=new String[count];
		
		int index=0;
		for (int i = 0; i < s.length(); i++)
		{
			String s1="";
			for (int j = i; j < s.length(); j++) 
			{
				if (s.charAt(j)==' ') 
				{
					arr[index++]=s1;
					i=j;
					break;	
				}
				else if(j==s.length()-1)
				{
					s1=s1+s.charAt(j);
					arr[index++]=s1;
					i=j;
					break;
				}
				else 
				{
					s1=s1+s.charAt(j);
				}
			}
		}
		System.out.println(Arrays.toString(arr));
