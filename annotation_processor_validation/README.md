## annotation processor debug  idea configure 

1. Create a Remote Run Configuration
![png](../image/2020-12-28_22-12.png)

2. Make sure the build process uses your port
 
```
Invoke Ctrl+Shift+A > Edit Custom VM Options…
Now add `-Dcompiler.process.debug.port=8000`, save, and restart IDEA.
```

3. Enable “Debug build process”
![png](../image/2020-12-28_22-16.png)
You’ll need to repeat this step every time you restart IDEA.

4.Try it out 

First, set a break point in your annotation processor’s code (the method overriding AbstractProcessor#init is an excellent choice).

![png](../image/2020-12-28_22-18.png)

Next, compile some code that will trigger your annotation processor.

![png](../image/2020-12-28_22-19.png)

The build process will pause, allowing you to attach the debugger:

Now start the Run configuration you added. javac will resume compilation.

![png](../image/2020-12-28_22-20.png)

Et voila, IDEA should now stop at the break point you’ve set.

if have provide not find 

check annoation configure 

![png](../image/2020-12-28_22-32.png)

