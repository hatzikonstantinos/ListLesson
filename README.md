# ListLesson
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Project/Maven2/JavaApp/src/main/java/${packagePath}/${mainClassName}.java to edit this template
 */

package com.mycompany.ebdomada;

import java.util.Arrays;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;

/**
 *
 * @author User
 */
public class ListLesson{

    public static void main(String[] args) {
         List<String> countries = Arrays.asList("Germany", "Panama", "Australia");
         
         for(int i=0; i<countries.size(); i++){
             System.out.println(countries.get(i));
         }
         for(String country : countries){
             System.out.println(country);
         }
         Iterator<String> countriesIterator = countries.iterator();
         
         while(countriesIterator.hasNext()){
             System.out.println(countriesIterator.next());
         }
         
         ListIterator<String> listIterator = countries.listIterator();
            
         while(listIterator.hasNext()){
             System.out.println(listIterator.next());
         }
         
         ListIterator backwardIterator;
         backwardIterator=countries.listIterator(countries.size());
         
         while(backwardIterator.hasPrevious()){
             System.out.println(backwardIterator.previous());
         }

         
         for(int i = countries.size(); i-- >0; ){
             System.out.println(countries.get(i));
         }
         
         countries.forEach(System.out::println);
    }
}
