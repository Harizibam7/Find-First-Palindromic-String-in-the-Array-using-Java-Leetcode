# Find-First-Palindromic-String-in-the-Array-using-Java-Leetcode

      class Solution {
          public String reverse(String word){
              String temp = word;
              String ch = "";
              for(int i =temp.length()-1; i>=0;i--){
                  ch +=temp.charAt(i);
              }
              System.out.println(ch);
              return ch;
          }
          public String firstPalindrome(String[] words) {
              String result = "";
              for(String word : words){
                  String reverseword = reverse(word);
                  if(reverseword.equals(word)){
                      result = word;
                      break;
                  }
              }
              return result; 
          }
      }
