# Numpy Array Operations

Trigonometric Functions:
    
    * numpy.radians()
    * numpy.sqrt()
    * numpy.tan()
    * numpy.sin()
    * numpy.cos()
    

## List of functions explained

    function1 = np.radians  
    function2 = np.sqrt
    function3 = np.tan
    function4 = np.sin
    function5 = np.cos

## Function 1 - np.radians

This mathematical function helps user to convert angles from **degree to radians**.

#### Example 1:

Connvert 18° to radians

#### Solution 1:


```python
radian_18 = np.radians(18)
```


```python
radian_18
```

#### Example 2:

Convert 20° and 60° to radians

#### Solution 2:


```python
radian_20 = np.radians(20)
```


```python
radian_60 = np.radians(60)
```


```python
radian_20
```

    0.3490658503988659


```python
radian_60
```

    1.0471975511965976


#### Example 3: - Breaking

Convert θ = 60° to radians

#### Solution 3:


```python
radian_60 = np.radians(θ)
```


## Function 2 - np.sqrt

This mathematical function returns the non-negative **square-root** of an array, element-wise.

#### Example 1:

The two sides of a right-angled triangle are given as shown in the figure. Find the third side.

<img src="/images/sqex1.jpg" />

#### Solution 1:

Given; Perpendicular = 15 cm

Base = b cm

Hypotenuse = 17 cm

As per the Pythagorean Theorem, we have;

$Perpendicular^2 + Base^2 = Hypotenuse^2$

⇒$15^2 + b^2 = 17^2$

⇒$b^2 = 17^2 – 15^2$


```python
b = np.sqrt(17**2 - 15**2)
```


```python
b
```

#### Example 2:

Given the side of a square to be 4 cm. Find the length of the diagonal.

<img src="/images/sqex2.jpg" />

#### Solution 2:

Given; Sides of a square = 4 cm

To Find- The length of diagonal ac.

Consider triangle abc (or can also be acd)

$(ab)^2 +(bc)^2 = (ac)^2$


```python
ab = bc = 4
```


```python
ac = np.sqrt(ab**2 + bc**2)
```


```python
round(ac, 2)
```

#### Example 3: - Breaking

Steve is turning half of his backyard into a chicken pen. His backyard is a 24 meter by 45 meter rectangle. He wants to put a chicken wire fence that stretches diagonally from one corner to the opposite corner.

How many meters of fencing will Steve need?

#### Solution 3:

x = 24, y = 45, z = ?

$z^2 = x^2 + y^2$


```python
x = 24
y = 45
```


```python
z = np.sqrt(x² + y²)
```


      File "<ipython-input-26-91241913fa05>", line 1
        z = np.sqrt(x² + y²)
                     ^
    SyntaxError: invalid character in identifier
    


## Function 3 - np.tan

This mathematical function computes **tangent** element-wise. Equivalent to np.sin(x)/np.cos(x) element-wise.

#### Example 1:

A person 100 meters from the base of a tree, observes that the angle between the ground and the top of the tree is 18 degrees. Estimate the height h of the tree to the nearest tenth of a meter.

<img src="/images/ex1.jpg" />

#### Solution 1:

Use the tangent: tan(18°) = h / 100

Hence, h = 100 * tan(18°)


```python
h = 100 * np.tan(radian_18)
```


```python
print("Height of the tree is {0} meter".format(round(h, 1)))
```

#### Example 2:

In the figure below AB and CD are perpendicular to BC and the size of angle ACB is 31°. Find the length of segment BD.

<img src="/images/ex2.jpg" />

#### Solution 2:

Use right triangle ABC to write: tan(31°) = 6 / BC

Hence, BC = 6 / tan(31°)


```python
radian_31 = np.radians(31)
```


```python
BC = 6 / np.tan(radian_31)
```


```python
BC
```

Use Pythagora's theorem in the right triangle BCD to write: $9^2 + BC^2 = BD^2$

$BD = \sqrt{9^2 + BC^2}$ 

$BD = \sqrt{9^2 + (\frac{6} {tan(31)})^2}$


```python
BD = np.sqrt((9**2) + (BC**2))
```


```python
print("Length of the BD is {0}".format(round(BD, 1)))
```

#### Example 3: - Breaking

An airplane is approaching point A along a straight line and at a constant altitude h. At 10:00 am, the angle of elevation of the airplane is 20° and at 10:01 it is 60°. What is the altitude h of the airplane if the speed of the airplane is constant and equal to 600 miles/hour? (round answer to 2 decimal places).

<img src="/images/ex3.jpg" />

#### Solution 3:

We first calculate distance d using the time and speed (1 minute = 1/60 hour)

Hence, d = 600 * (1 / 60) = 10 miles


```python
d = 600 / 60
```

We now express the tangent of the given angles of elevation

$tan(20°) = \frac{h}{(d + x)}$  and  $tan(60°) = \frac{h} {x}$

Hence, $x = \frac{h}{tan(20°)} - d$  and  $x = \frac{h} {tan(60°)}$


Eliminate x in the two equations above to find a relationship between h and d

Now, $\frac{h} {tan(60°)}$ = $\frac{h}{tan(20°)} - d$

$h = \frac{d} {\frac{1} {tan(20°)} - \frac{1} {tan(60°)}}$


```python
tan20 = np.tan20
```


```python
tan60 = np.tan60
``` 


```python
altitude = d / ((1/tan20)-(1/tan60))
```


```python
print("Altitude of the airplane is {0} miles".format(round(altitude, 1)))
```


## Function 4 - np.sin

This mathematical function is **Trigonometric sine**, element-wise. The sine is one of the fundamental functions of trigonometry.

#### Example 1:

A string of a kite is 100 meters long and it makes an angle of 60° with horizontal. Find the height of the kite, assuming that there is no slack in the string.

#### Solution 1:

<img src="/images/sinex1.png" />

Here AB represents height of kite from the ground, BC represents the distance of kite from the point of observation.

In the right triangle ABC the side which is opposite to angle 60 degree is known as opposite side (AB), the side which is opposite to 90 degree is called hypotenuse side (AC) and remaining side is called adjacent side (BC).

Now we need to find the height of the side AB.

$sinθ  =  \frac{Opposite side}{Hypotenuse side}$

$sin θ  =  \frac{AB}{AC}$

$sin 60°  =  \frac{AB}{100}$


```python
sin_60 = np.sin(radian_60)
```


```python
AB = sin_60 * 100
```


```python
AB
```

    86.60254037844386


```python
print("Height of kite from the ground is {0} meters".format(round(AB, 1)))
```

    Height of kite from the ground is 86.6 meters
    

#### Example 2:

<img src="/images/sinex2.png" />

Calculate the length of the side x, given that θ = 39°

#### Solution 2:

$sinθ  =  \frac{Opposite side}{Hypotenuse side}$

$sin39°  =  \frac{BC}{AB}$



```python
radian_39 = np.radians(39)
```


```python
sin_39 = round(np.sin(radian_39), 1)
```


```python
sin_39
```

    0.6


Hence, 
$0.6  =  \frac{12}{AB}$


```python
AB = 12 / sin_39
```


```python
AB
```

    20.0


Using Pythagoras’ theorem:

$ 20^2 = 12^2 + x^2 $

$ x = \sqrt{20^2 - 12^2} $


```python
x = np.sqrt(20**2 - 12**2)
```


```python
print("Length of x is {0} cm".format(x))
```

    Length of x is 16.0 cm
    

#### Example 3: - Breaking

what is the sine of −3 radians?

#### Solution 3:

−3 is less than 0 so let us add 2π radians

−3 + 2π = −3 + 6.283 = 3.283 radians


```python
sin(−3)
``` 


Now, sin(−3) = sin(3.283)


```python
sin(3.283)
```

## Function 5 - np.cos

This mathematical function is **Cosine** element-wise.

#### Example 1:

Find the distance "z"

<img src="/images/cosineex1.gif" />

#### Solution 1:

The letters are different! So we can easily substitute x for a, y for b and z for c

Here, a = x = 9.4, b = y = 6.5, and cos(c) = cos(z) = 131°

Now, $c^2 = a^2 + b^2 − 2ab \times cos(C)$

$c^2 = 9.4^2 + 6.5^2 − 2 \times 9.4 \times 6.5 \times cos(131°)$

$c = \sqrt{9.4^2 + 6.5^2 − 2 \times 9.4 \times 6.5 \times cos(131°)}$


```python
radian_131 = np.radians(131)
radian_131
```

    2.2863813201125716


```python
cos_131 = np.cos(radian_131)
cos_131
```

    -0.6560590289905072
    

```python
a = 9.4
```


```python
b = 6.5
```


```python
c = np.sqrt(a**2 + b**2 - (2 * a * b * cos_131 ))
```


```python
print("The distance z is {0}".format(c))
```

    The distance z is 14.518278594332042
    

#### Example 2:

Find the unknown side the following diagram:

<img src="/images/cosineex2.gif" />

#### Solution 2:

The triangle is right-angled, and in the question angles are given, so we need to use trigonometric ratios

$cos(50°) = \frac{y}{8}$


```python
radian_50 = np.radians(50)
```


```python
cos_50 = np.cos(radian_50)
```


```python
y = cos_50 * 8
```


```python
print("The side y is {0}".format(y))
```

    The side y is 5.142300877492315
    

#### Example 3 -Breaking


```python
np.cos({0, np.pi/2, np.pi})
```

```python
np.cos([0, np.pi/2, np.pi])
```


    array([ 1.000000e+00,  6.123234e-17, -1.000000e+00])





```python

```
