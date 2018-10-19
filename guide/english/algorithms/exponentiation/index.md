---
title: Exponentiation
---
## Exponentiation

Given two integers a and n, write a function to compute a^n.

#### Code

Algorithmic Paradigm: Divide and conquer.

```C
int power(int x, unsigned int y) { 
    if (y == 0) 
        return 1; 
    else if (y%2 == 0) 
        return power(x, y/2)*power(x, y/2); 
    else
        return x*power(x, y/2)*power(x, y/2); 
} 
```
Time Complexity: O(n) | Space Complexity: O(1)

####  Optimized Solution: O(logn)

```C
int power(int x, unsigned int y) { 
    int temp; 
    if( y == 0) 
        return 1; 
    temp = power(x, y/2); 
    if (y%2 == 0) 
        return temp*temp; 
    else
        return x*temp*temp; 
} 
```

## Modular Exponentiation

Given three numbers x, y and p, compute (x^y) % p

-Iterative version.
```C
int power(int x, unsigned int y, int p) { 
    int res = 1;  
    x = x % p; 
    while (y > 0) {  
        if (y & 1) 
            res = (res*x) % p; 
  
        // y must be even now 
        y = y>>1; 
        x = (x*x) % p;   
    } 
    return res; 
} 
```
Time Complexity: O(Log y).

-Recursive version.
```C++

int power(int a,unsigned int b,int p){
    if(!b){             //check if b==0 or not
        return 1;
    }
    if(b&1){            //check if b is odd.
        return (a%p * power((a*a)%p,(b-1)/2,p)%p)%p;
    }
    return power((a*a)%p,b/2,p)%p;
}
```
