 ##Without using len keyword
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
##Valid parenthesis
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

##ValueOf()
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

##StingBuffer()
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

##Trim()
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

