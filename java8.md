# JAVA 8 features

- Lambda API/Expression
- Stream API




## Lambda expression? 
 - anonymous function -> no name,no modifier, no return type

 ### use of lambda expression
 - reduces the line of code
 - sequential and parallel execution suppport by passing behaviour as an argument in methods.
 - to call API's very effectivevly
 - to write more readable, Maintainable and concise code.
 

 <mark>lambda expression can be used only with funcitional interfaces<mark>

 with the introduce of lambda expression,the **funtional programming** in java is enabled.

### important rules of lambda
- if body contains only one statement ,then curly braces is optional.
- java compiler infer the type of variable passed in argument, hence type is optional.


## functional Interface?
- an interface with only one abstract method
- ex Runnable, Callable, Comparable etc

- `to call lambda  and use it, we require functional interface`

- `Lambda is used to implement functiona interface in simple and short manner`

## implementation ways of funtional interface
- creating class and implementing it
- using anonymous class
- using lambda expression


`using lambda threads can also be created`

```
  Runnable thread1 = () -> {
            try {
                for (int i = 0; i < 10; i++) {
                    System.out.println(i);

                    Thread.sleep(1000);
                }
            }catch (InterruptedException e) {
                e.printStackTrace();
            }
        };
        Runnable thread2 = () -> {
            try {
                for (int i = 0; i < 10; i++) {
                    System.out.println("multiply" + i*i);

                    Thread.sleep(2000);
                }
            }catch (InterruptedException e) {
                e.printStackTrace();
            }
        };

        Thread t = new Thread(thread1);
        Thread t2 = new Thread(thread2);
        t.setName("JOHN");
        t2.setName("JANE");
        t.start();
        t2.start();
        System.out.println("main thread ends here");

```
<mark>If an interface has more than two methods, it's usually better to avoid using a lambda expression because lambda expressions are intended to be used for single-method interfaces (functional interfaces).</mark>