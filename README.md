# Sieve
creates a Sieve of Eratosthanes to find prime numbers

import java.util.Arrays;

/**
 *	Construct a Sieve of Eratosthanes to find the prime numbers < N.
 *
 *	@author Erika Ochoa
 *	@version 2015.06.05
 */
public class Sieve
{
    public static final int N = 1_000;

    public static void main(String[] args)
    {
        //System.out.println(Arrays.toString(primes(N)));
        int[] primes = primes(N);
        System.out.println(primes[9]);
    }

    public static int[] primes(int n)
    {
        int [] sieve = new int[N];//  Build a sieve: an array of n int elements.
        //TODO

        for(n = 0; n < sieve.length; ++n){
            sieve[n] = n ;//  Initialize the sieve where each element contains its index.
        }//TODO
        
        
        //  Create a counter variable to count the number of primes < n.
        //TODO
        int counter = 0;// this will be the amount of primes
        //  Using the sieve, find the primes < n.
        //	When done scanning, the sieve array will contain elements that
        //	have a value of 0 meaning that it is not a prime
        //	or a value equal to its index meaning that it is a prime
        //	(numbers < 2 are not prime and their values are irrelevant).
        //TODO
        int[] primes = new int[counter]; // right now it has no values
        for(n = 0; n < sieve.length; ++n){
            for(int i = 0; i <= n; ++i){
                //compare i to sieve[n]
                if( )//if not prime
                {
                    sieve[n]=0;
                    break;
                }
            }
                    int number = sieve[n];
            if(number )
        }    


            //  If k is not a prime, skip it.
            //TODO
            //  k is a known prime.
            //	Clear the elements (set their values to 0) of all
            //	multiples of k (starting at 2 * k).
            //TODO
            //  Increment the count of known primes.
            //TODO
        

        //  Copy the known primes into a new array named primes,
        //	single array of a fixed size (the count).

        //	Build the new array of the correct size.
        //TODO
        //  Starting at 2 find the elements of the sieve that are prime
        //	(not 0) (use index k).
        //TODO
        //  Copy the primes into the primes array (use index j).
        //TODO
            //  Skip sieve elements that are 0 (not primes)
            //TODO
            //  For each prime in the sieve, move it to the primes array.
            //TODO
        
            return sieve;//return primes;
    }
}

