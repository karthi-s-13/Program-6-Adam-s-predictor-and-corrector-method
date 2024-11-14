# Program 6: Adam's predictor and corrector method

<br>

## Question:

<br>

Find $$y(1.4)$$ , given that $$\frac{dy}{dx} = x^2 (1 + y) , y(1) = 1 , y(1.1) = 1.233 , y(1.2) = 1.548$$ , and $$y(1.3) = 1.979$$ using Adam’s predictor and corrector method.

<br>

## Aim:

<br>

To find approximate solution of first order differential equation by using Adam's predictor and corrector method

<br>

## Algorithm:

<br>

Step 1: Define the function $$f(x,y) = (x * * 2 ) * ( 1 + y )$$

<br>

Step 2: Get the values of $$x_0, y_0, x, y, x_2, y_2, x_3$$ and $$y_3$$

<br>

Step 3: Compute $$h = x_1 - x_0$$

<br>

Step 4: Compute $$y_{4}^{(p)} = y_3 + \frac{h}{24} * (55f (x_3, y_3) - 59f(x_2, y_2) + 27f(x_1, y_1) - 9f (x_0, y_0))$$

<br>

  - $$x_4 = x_3 + h$$

<br>

Step 5: Compute $$y_{4}^{(c)} = y_3 + \frac{h}{24} * (9f(x_4, y_{4}^{(p)} + 19f (x_3, y_3) - 5f(x_2, y_2) + f(x_1, y_1))$$

<br>

Step 6: Print the value of $$y_{4}^{(c)}$$

<br>

## Program:

<br>

```
def f (x, y):
 return x**2*(1+y)
x0=float (input ("Enter x0: "))
y0=float (input ("Enter y0: "))
x1=float (input ("Enter x1: "))
y1=float (input ("Enter y1: "))
x2=float (input ("Enter x2: "))
y2=float (input ("Enter y2: "))
x3=float (input ("Enter x3: "))
y3=float (input ("Enter y3: "))
h =0.1
y4p=y3+(h/24) *(55*f (x3, y3)-59*f (x2, y2) +37*f (x1, y1)-9*f (x0,
y0))
x4=x3+h
y4c=y3+(h/24) *(9*f (x4, y4p) +19*f (x3, y3)-5*f (x2, y2) +f (x1, y1))
print ("Approximate soln is %0.4f"%y4c) 
```

<br>

## Output:

<br>

Enter x0: 1

<br>

Enter y0: 1

<br>

Enter x1: 1.1

<br>

Enter y1: 1.233

<br>

Enter x2: 1.2

<br>

Enter y2: 1.548

<br>

Enter x3: 1.3

<br>

Enter y3: 1.979

<br>

Approximate solution is 2.5749 

<br>

## Result:

<br>

The solution of first order differential equation is obtained by using Adam's predictor and corrector method.
