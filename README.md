# teach2give-quiz
//Design a function that reverses the digits of an integer. For example, 50 should become 5 and -12 should become -21.
           #include <stdio.h>
           #include <stdbool.h>
           int reverseDgts(int x);
           int main() {
             int num1 = 50;
             int num2 =-12;
             printf("reversed %d is %d\n, num1, reversedDgts(num1));
              printf("reversed %d is %d\n, num2, reversedDgts(num2));
              return 0;
              }
              int reverseDgts(int x) {
              int reversed = 0;
              bool is negative = x <0;
              if(is negative) {
              x=-x;
              }
              while(x !=0){
              reversed = reversed * 10+x%10;
              x /=10;
              if(is negative){
              reversed = -reversed;
              }
              return reversed;
              }



              //Write a recursive function to calculate the factorial of a number
                      #include <stdio.h>
                      int factorial(int x);
                      int main() {
                      int num = 5;
                      printf(" %d is %d\n", num, factorial(num));
                      return 0;
                      }
                      int factorial(int x){
                      if(n <=1){
                      return 1;
                      }
                      return x * factorial(x-1);
                      }




                      //Design a function that takes a string or sequence of characters as input and returns the character that appears most frequently.
                                      //Eg 11189 => '1'
                                      //hello => l

                                      #include <stdio.h>
                                      char mostFrequentChar(const char* str) {
                                      int counts[256] = {0};
                                      char maxChar = '\0';
                                      int maxCount = 0;                                          
                                      const char* ptr = str;
                                      while (*ptr) {
                                      counts[*ptr]++;
                                      if (counts[*ptr] > maxCount) {
                                      maxCount = counts[*ptr];
                                      maxChar = *ptr;
                                              }
                                         ptr++;
                                            }                                          
                                        return maxChar;
                                          }                                          
                                          int main() {
                                           char str1[] = "11189";
                                              char str2[] = "hello";                                            
                                              char mostFrequent1 = mostFrequentChar(str1);
                                              char mostFrequent2 = mostFrequentChar(str2);                                            
                                              printf("Most frequent character in '%s': %c\n", str1, mostFrequent1);
                                              printf("Most frequent character in '%s': %c\n", str2, mostFrequent2);                                            
                                              return 0;
                                                       }


//Design a function that determines whether a given string is a pangram. A pangram is a sentence or phrase containing every letter of the alphabet atleast once. Punctuation and case are typically ignored. For example, the string "The quick brown fox jumps over the lazy dog" is a pangram, while "Hello, world!" is not.

                            #include <stdio.h>
                            #include <ctype.h>
                            #include <stdbool.h>        
                            bool isPangram(const char *str);                            
                            int main() {
                            const char *str1 = "The quick brown fox jumps over the lazy dog";
                            const char *str2 = "Hello, world!";                                
                            printf("Is the string \"%s\" a pangram? %s\n", str1, isPangram(str1) ? "Yes" : "No");
                            printf("Is the string \"%s\" a pangram? %s\n", str2, isPangram(str2) ? "Yes" : "No");                                
                                return 0;
                            }                          
                            bool isPangram(const char *str) {
                            int alphabet[26] = {0}; // Array to keep track of letter counts
                            int index;                            
                            for (int i = 0; str[i] != '\0'; i++) {
                            if (isalpha(str[i])) {
                              index = tolower(str[i]) - 'a';
                              alphabet[index] = 1;
                                    }
                                    }                           
                            for (int i = 0; i < 26; i++) {
                            if (alphabet[i] == 0) {
                              return false;
                                    }
                                      }                           
                          return true;
                }




//Design a function that takes a list of integers as input. The function should return True if the list contains two consecutive threes (3 next to a 3) anywhere within the list. Otherwise, it should return False. For example, the function should return True for [1, 3, 3] and False for [1, 3, 1, 3].

                                          #include <stdio.h>
                                          #include <stdbool.h>                                    
                                          bool hasConsecutiveThrees(const int *arr, int size);                                          
                                          int main() {
                                          int arr1[] = {1, 3, 3};
                                          int arr2[] = {1, 3, 1, 3};                                              
                                              printf("is there two consecutive threes? %s\n", hasConsecutiveThrees(arr1, sizeof(arr1) / sizeof(arr1[0])) ? 
                                              "Yes" : "No");
                                              printf("is there two consecutive threes? %s\n", hasConsecutiveThrees(arr2, sizeof(arr2) / sizeof(arr2[0])) ? 
                                              "Yes" : "No");                                              
                                              return 0;
                                               }                                          
                                          bool hasConsecutiveThrees(const int *arr, int size) {
                                          for (int i = 0; i < size - 1; i++) {
                                          if (arr[i] == 3 && arr[i + 1] == 3) {
                                           return true;
                                                  }
                                                  }
                                          return false;
                                          }



Master Yoda, a renowned Jedi Master from the Star Wars universe, is known for his unique way of speaking. He often reverses the order of words in his sentences. For example, instead of saying "I am home" he might say "Home am I" Design a function that takes a sentence as input and returns a new sentence with the words reversed in the same order that Master Yoda would use.

                                #include <stdio.h>
                                #include <string.h>                               
                                void reverseSentence(char *sentence);                                
                                int main() {
                                char sentence[] = "I am home";                                 
                                printf("Original sentence: %s\n", sentence);
                                reverseSentence(sentence);
                                printf("Yoda-style sentence: %s\n", sentence);                                    
                                    return 0;
                                          }                             
                                void reverseSentence(char *sentence) {
                                char *word, *temp = strdup(sentence);
                                strcpy(sentence, "");
                                 while ((word = strtok(temp, " ")) != NULL) {
                                strcat(sentence, word);
                                  strcat(sentence, " ");
                                temp = NULL;
                                    }
                                sentence[strlen(sentence) - 1] = '\0';
                                }




                                                               //THANK YOU



                
                                          
                                                                      
                                                                                                                
                                                                      
                                                                                          
