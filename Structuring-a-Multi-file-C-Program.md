# Structuring a Multi-File C Program

## Writing a Good main() Function

This is a short summary of the article ["How to write a good C main function"](https://opensource.com/article/19/5/how-write-good-c-main-function). It tries to address the following questions:

* How to structure a C file and write a ```main()``` function
* How to best process command line arguments

Typical structure of a ```main()``` function in a C program:

```C
/* main.c */
int main(int argc, char *argv[]) {

}
```

**What is the main()?**  
Every C program MUST have only one ```main()``` function and program execution begins at the ```main()```. The ```main()``` function has two arguments that traditionally are called ```argc``` and ```argv``` and always returns a signed integer.  ```main()``` returns a 0 (zero) on success and -1 (negative one) on failure.

| Argument | Name            | Description                   |
|----------|-----------------|-------------------------------|
| argc     | argument count  | Length of the argument vector |
| argv     | argument vector | Array of char pointers        |