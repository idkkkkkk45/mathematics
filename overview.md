Subjects:

- numbers
- ratio
- factors - HCF/LCM
- probability
- statistics
- algebra
- geometry

# Numbers

An equality in mathematics means that the two sides are perfectly equal and interchangeäble.
That'll be important later: they are _exactly equivalent_, rather than being "nearly the same".

0.99... = 1.0

https://imgflip.com/memegenerator/They're-The-Same-Picture

1/3, 2/3, 3/3

# Ratios

Ratio is effectively division - one number divided by another - but is typically used to represent comparative scale.

For example, if you have a cat which is 3 times bigger than another cat, the ratio of the big cat to the small cat is 3:1, or (3/1).

- map scale
- fractions

# Factors

- HCF
- LCM

Decomposing a number into factors helps when simplifying. The decomposition process is called "factorising", and typically uses prime numbers:
numbers which have no factors (other than themselves).

For example, `6 = 2 * 3`, where 2 and 3 are both prime numbers. The prime numbers can be repeated in factorisation: `4 = 2 * 2`, or `12 = 2 * 2 * 3`.

The highest-commmon factor between two numbers is the multiple of all common factors.

For example, the HCF of `4` and `12`:

- `4 = 2 * 2`
- `12 = 2 * 2 * 3`
- common factors: `2 * 2` = 4

The lowest-common multiple is helpful when working with fractions:

```
1/3 + 1/6 + 1/2
```

The "least common denominator" is the smallest number you can use in the denominator for all those fractions.

You can find the LCM by factorising into primes, then taking the highest power of each prime.

For example, `2^3 * 3^1 * 5^2` and `2^1*5^3` would be `2^3 * 3^1 * 5^3 = 8 * 3 * 125 = 3000`.

Note that the "lowest-common multiple" is often a *big* number, and the "highest-common factor" is typically a *smaller* number, despite the "lowest" and "highest" names.

Used in: security and cryptography, RSA prime factors

# Probability

Used in: forecasting, AI

# Statistics

- median
- mode
- mean / average
- quartiles
- cumulative frequency

Used in: business

# Geometry

- geology - words about earth
- geometry - measuring earth
- geography - drawing earth
- geomancy - earth-based magic
- geolocation - finding things on earth
- geopositioning - finding where you are on earth
- geostationary - holding steady at a specific place

## Coördinates

Coördinates represent a position. On a flat, 2-dimensional object, that position can be described by two numbers:

- how far across
- how far down

Rather than writing out "across" and "down" every time, mathematicians use a single letter to represent these. The typical convention is to use `x` and `y`, since that leaves the last letter `z` for 3D (depth: how far into the distance something is).

The two numbers are grouped together to form a coördinate: a vector (a collection of numbers) representing a position.

- scalar - single number, e.g. "how big" something is (e.g. 1 metre, 5 metres, 10 kg - all scalars, all representing "size")
- vector - a group of scalars (numbers), one for each "dimension"

When we say something is "3D" or "3 dimensional", that means we have 3 values in the vector, because there are 3 directions possible: left/right, up/down, forward/backwards.

Coördinates can be defined by vectors. Vectors are also used for directions - if you draw a line from the origin (centre, or zero) to the vector coördinate, that's the direction you're going.

## Shapes

## Lines

Lines are infinite - the lines we draw are technically "line segments", they start and end.

A line has a gradient and an offset:

- gradient tells you how far up it goes as you go across
- offset is where the line crosses the axis

For example, a gradient of 2 means a ratio of 2:1 - that's 2 up for every 1 across.
An offset of 1 would mean at zero across, the point on the line is 1 up.

There are a few different equations you can use to define a line - in gradient and offset terms, this equation is common:

```
y = mx + c
```

where `m` is the gradient, and `c` the offset.

This doesn't work for a vertical line, though - there are an infinite number of points with the same value of `x`.

You could turn the equation around like this:

```
x = my + c
```

but this would have the same problem for horizontal lines.

A _general_ equation that works for any line is:

```
ax + by + c = 0
```

- for a horizontal line, `b = 0`
- for a vertical line, `x = 0`

If you have at least 2 points, you can derive the equation of the line from them, using simultaneous equations:

(2,3), (7, 4) and (12, 5)

```
y = mx + c
3 = 2m + c
4 = 7m + c (-)
(4-3) = (7-2)m
1 = 5m (/5)
m = 1/5
substitute m back in:
3 = 2 * (1/5) + c
3 - (2/5) = c
c = 13/5

y = (x + 13)/5
```

You can test that with another point on the line to confirm that it works:

```
y = (x + 13)/5
5 = (12 + 13)/5
5 = 25/5
5 = 5  ✓
```

## Squares

A square and a rectangle can both be represented by 2 congruent triangles.

A parallelogram is similar to a rectangle, but without the constraint of 90 degree angles. It's like a deck of cards with the top part pushed to one side.

### Perimeter

Single-dimensional.

Curve model for a roller-coaster - you can represent location by a single value: unless something has gone very wrong, each position along the track always has the same height/depth.

Used in: chemistry

### Area

2 dimensional.

Used in: chemistry, construction, fabrication, 3D modelling (texture mapping)

### Volume

3 dimensional.

Used in: physics

## Congruency

Harmony from the Latin "con-gruere", "come together" or "agree"

In mathematics, originally used to indicate that something "can be superposed", or put on top of something else: when two things have the same shape, they are congruent. You might need to turn them around, or make them bigger or smaller, but you don't need to alter the shape to make them match.

- scale
- rotate
- translate

Used in: 3D modelling

# Algebra

Algebra - الْجَبْر

- by الخوارزمي (Mohammed Musaa Al-Khawarizmi)
- who wrote الكتاب المختصر في حساب الجبر - the short book on agebraïc mathematics
- which gives us the words "algebra" ("putting things back together", rejoining broken pieces)
- and "algorithm" (process for doing so)
- https://www.jw.org/id/perpustakaan/majalah/g201505/al-khwarizmi-bapak-aljabar/

The "broken pieces" here are equations (things which are equal to each other)
and inequalities (things which are... not, but in specific ways).

Remember: an equality in mathematics means that the two sides are perfectly equal and interchangeäble.
That'll be important later: they are _exactly equivalent_, rather than being "nearly the same".

An inequality specifies a rule: although "not equal" is one case, it's more common to encounter
ranges such as "less than" or "greater than".

- think positive: things are simpler when they are positive, adding or multiplying for example.

Why? Some example danger areas:

- cannot divide by zero

so "divide both sides by x" only works when you know `x` cannot be zero.

- multiplication or division by negative numbers reverses an inequality

```
x > 2
-x > -2  ✗
```

Why doesn't this work? Try with a number - 3 for example:

```
3 > 2   ✓
-3 > -2 ✗
```
