package com.pom.map;

import java.util.Collection;
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Map.Entry;
import java.util.Set;

public class HashMapExample {
	//break;
	//continue;
	public static void main(String[] args) {
		HashMap h=new HashMap();  //16  0.75
		
		h.put(101, "pawan");
		h.put(102, "pooja");
		h.put(103, "Bhushan");
		h.put(104, "Harshal");
		h.put(105, "Bhushan");
		System.out.println(h); //[101=pawan, 102=pooja, 103=Bhushan, 104=Harshal]
		
		//to retrive key from hashmap
		Set result = h.keySet();
		System.out.println(result); //[101, 102, 103, 104]
		
		//to retrive value from hashmap
		Collection value = h.values();
		System.out.println(value); //[pawan, pooja, Bhushan, Harshal]
	
				//to retrive data as key value pair
		Set data = h.entrySet(); 	
		System.out.println(data);//[101=pawan, 102=pooja, 103=Bhushan, 104=Harshal]
		Iterator itr = data.iterator();	
		//hashNext()
		//next(); 
		
		/*
		 *  101 pawan
		 *  102 pooja 
		 *  103 Bhushan 
		 *  104 Harshal
		 */
		while(itr.hasNext()) {    
			   //101=pawan
			      Map.Entry<Integer,String> data1 = (Map.Entry)itr.next(); //typeCasting with map
			      System.out.println(data1.getKey()   + "   " +data1.getValue());
			      
			      if(!data1.getKey().equals(105) && data1.getValue().equals("Bhushan"))
			      {
			    	  data1.setValue("vivek");
			    	 
			      }
			      
		}

		System.out.println(h);
		
		
		
	}
	
	

}
