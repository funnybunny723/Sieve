# Sieve
creates a Sieve of Eratosthanes to find prime numbers

import java.util.Arrays;


public class metry {
    public static final int N = 1000;
   
    public static int[] sieve(int n){
       int[] sieve = new int[N];
       for(n = 0; n < N; ++n){
            sieve[n] = n;
        }return sieve;//System.out.println(Arrays.toString(sieve));
    }//created the array of all numbers including zero to 999
    
    public static boolean isDivisibleBy(int l, int m){
        if(l % m == 0){
            return true;
        }return false;
    }
    
    public static int[] checkPrimes(int [] sieve,int n){
      int[] checkPrimes = sieve;
        int counter = 0;//the length of the prime array
        for(n = 2; n < N; n++){ //goes through the array starting at 2
            int num = checkPrimes[n];
            if(num != 0){
                for(int k = n + 1 ; k < N; k++){ //k are the numbers after n
                    int next = checkPrimes[k];
                    if(isDivisibleBy(num,next)){ // checks if that number is divisable by n
                        checkPrimes[k] = 0;//if the number is not prime reassign to 0
                    }
                }
            }
        }
        for(n = 2; n < N; n++){
            while(sieve[n] != 0){
                counter ++;
            }
        }return checkPrimes;  
    }
    public static int[] primes(int[] checkPrimes,int counter){
        
        int[] primes = new int[counter];
        for(int j = 0; j < counter; ++j){
            if(checkPrimes[j] > 1){
                for(int a = 0; a < counter; ++a){
                primes[a] = checkPrimes[j];
                }
            }System.out.println(counter);
        }return primes;
    }   
 
    public static void main(String[] args){
        System.out.println(Arrays.toString(primes));
    }
}
