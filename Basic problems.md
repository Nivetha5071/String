 ##01.Without using len keyword
 ````java[]

#include <stdio.h>
int main() {
 char str[100];                           output:                                        
 scanf("%s",str);                            hello
 int i;                                      5
 for(i=0;str[i];i++);
    printf("%d",i);
    return 0;
}
````

##02.Valid parenthesis
````java[]
import java.util.*;

public class string1 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        while(str.contains("[]")||str.contains("()")||str.contains("{}")) {
        	str = str.replace("[]", "");
        	str = str.replace("()", "");
        	str = str.replace("{}", "");
        }
        if(str.length()==0) {
        	System.out.println("Valid");
        }else {
        	System.out.println("Invalid");
        }
	}

}
output:


{[]()}
Valid
````

##03.ValueOf()
````java[]

import java.util.*;
public class string2 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		//String str = sc.nextLine();
		char ch ='a';
		String str = "hello";
		str =""+ch;
		str= String.valueOf(ch);
		System.out.println(str);

	}

}
output:
a
````

##04.StingBuffer
````java[]
import java.util.*;

public class string1 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
       StringBuffer sb = new StringBuffer("hello");
       sb.append("hi");
       sb.deleteCharAt(3);
       sb.length();
       sb.insert(0,"heelo");
       System.out.print(sb.deleteCharAt(3));
        System.out.print(sb.reverse());
	}

}
output:
heeohelohi
````

##05.Trim()
````java[]
import java.util.*;

public class string1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String str = "hello" ;
        System.out.println(" " + str + " ");
        str = str.trim();  

        System.out.println("" + str + "");
    }
}
output:
 hello 
hello
````
##06.Write a program to count the number of upper-case characters in a given string
````java[]
Sample Input: 
BeauTIfull Life
Sample Output:
4

import java.io.*;
import java.util.*;
public class Solution {

    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("[^A-Z]","");
        System.out.print(str.length());
    }
}
output:
````

##07.Write a program to count the special characters in the given string

````java[]
Sample Input:
togy@#123
Sample Output:
2

import java.io.*;
import java.util.*;
public class Solution {

    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("[a-z0-9]","");
        System.out.print(str.length());
    }
}
````

## 08.Write a program to find the length of the string without using in-built function
````java[]
Sample Input: 
i like apple
Sample Output:
12

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        char[] arr = str.toCharArray();
        int i=0;
        try{
            for(i=0;;i++){
                char ch = arr[i];
            }
        }
        catch(Exception e){
            System.out.println(i);
        }
    }
}
````
##09.Write a program to replace all vowels with spaces
Sample Input
Replace all vowels 
Sample Output 
R pl c   ll v w ls 

````java[]
import java.io.*;
import java.util.*;
public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("['a','e','o','i','u']"," ");
        System.out.println(str);
    }
}
````

##10.Write a program to search for a character in a string
Sample Input1:
p
apple
Sample Output
Present
Sample Input2:
f
Myslate
Sample Output
Not Present
````java[]
import java.io.*;
import java.util.*;
public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);
        String str = sc.next();
       if (str.indexOf(ch) != -1){
            System.out.println("Present");
        }else{
            System.out.println("Not Present");
        }
    }
}
````
##W11.rite a program to accept the string and rotate the string n times

````java[]
import java.util.*;

public class RotateString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();     
        String str = sc.next();  
        int len = str.length();
        n = n % len; 
        String rotated = str.substring(n) + str.substring(0, n);
        System.out.println(rotated);
    }
}
````
##12.Write a program to accept the string from the user and display the string in the password format without making any change in the input array
````java[]
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("[a-zA-Z0-9]","*");
        str = str.replaceAll("[^a-zA-Z0-9]","*");
        System.out.println(str);
    }
}
````
##13.Write a program to convert the digits of the string into a single number
````java[]
mport java.util.*;

public class Solution {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        str = str.replaceAll("[^0-9]", "");
        if (str.isEmpty()) {
            System.out.println(0);
        } else {
            System.out.println(str);
        }
    }
}
````

##14.Write a program to reverse a given string without using in-built functions
````java[]
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        StringBuffer str1= new StringBuffer();
        str1.append(str);
        str1= str1.reverse();
        System.out.println(str1);
    }
}

````

##16.Write a program to reverse a string except the special characters
````java[]
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        char[] arr = str.toCharArray();
        int i = 0, j = arr.length - 1;

        while (i < j) {
            if (!Character.isLetter(arr[i])) {
                i++;
            } else if (!Character.isLetter(arr[j])) {
                j--;
            } else {
                // Swap letters
                char temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
                i++;
                j--;
            }
        }

        System.out.println(new String(arr));
    }
}
````
##17.To check whether the given is Anagram or not
````java[]
package STRING;
import java.util.*;
public class program3 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		String str1 = sc.nextLine();
		String str2 = sc.nextLine();
		int [] dp = new int[26];
		for(int i=0;i<str1.length();i++) {
			dp[str1.charAt(i)-'a']++;
		}
		for(int i=0;i<str1.length();i++) {
			dp[str2.charAt(i)-'a']--;
	}
		for(int i=0;i<26;i++) {
			if(dp[i]!=0) {
				System.out.println("Not an anagram");
				return;
			}
			
		}
		System.out.println("Anagram");

     }
}
````


