# Recursion

* How to calculate n! using a single function

## Coding Practice #1
    // Calculate the value of a number raised to a power
    int pow(int num, int power){
      if(power == 0){
        return 1;
      }else{
        return num * pow(num, power-1);
      }
    }
