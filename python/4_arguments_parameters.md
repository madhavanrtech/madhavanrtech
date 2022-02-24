# Arguments

Arguments are used to pass values between programs, subroutines or functions. When an argument is used to customize a program, it is called a parameter.

```
import sys

def main():
    print("Number of arguments:", len(sys.argv), "arguments.")
    print("Argument List:", str(sys.argv))

if __name__=="__main__":
    main()

```

run by passing the arguments

```
python arguments.py madhavan raj champ
```