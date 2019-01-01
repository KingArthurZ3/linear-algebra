# linear-algebra

This library provides implementations of vectors, lines, planes of nth dimensions, and also a linear systems of equations class. On a high level, the linear systems class can be used to solve for intersections and returns the intersection (if one exists), both as a unique point or as a parametrized equation. More detailed documentation for each classes methods can be found below.

### Vectors
<img src="https://github.com/KingArthurZ3/linear-algebra/blob/master/rsc/vectors.png" width="100%" height="30%" title="Vectors">

The vector object is initialized from a set of coordinates in n dimensions. A short list of some useful vector functions defined for it are listed below.

**dot(v)** - returns dot product between two vectors
**is_orthogonal_to(v)** - returns whether or not two vectors are orthogonal
**is_parallel_to(v)** - returns whether or not two vectors are parallel
**component_orthogonal_to(v)** - returns the component of vector perp to original vector
**angle(v)** - returns the angle between two vectors

### Lines

![network structure](https://github.com/KingArthurZ3/linear-algebra/blob/master/rsc/lines.png "lines")

The line object is initialized from a normal vector and constant for the line. A short list of useful line functions defined for it are listed below.

**is_parallel_with(l)** - returns whether or not two lines are parallel
**intersection_with(l)** - returns the intersection between two lines if it exists

### Planes

![network structure](https://github.com/KingArthurZ3/linear-algebra/blob/master/rsc/planes.png "planes")

The plane object is nearly identical to the lines object, requiring a normal vector and a constant term to initialize. Note: this plane object only works for three dimensional vectors, the hyperplanes object is valid for n dimensions

**is_parallel_to(p)** - returns whether or not two planes are parallel

### HyperPlanes

![network structure](https://github.com/KingArthurZ3/linear-algebra/blob/master/rsc/hyperplanes.png "hyperplanes")

The hyperplane object is identical to the planes object with the exception of being generalizable to n dimensions. The rest of the methods are identical to the planes object.

### Linear Systems

![network structure](https://github.com/KingArthurZ3/linear-algebra/blob/master/rsc/linsystems.png "linear systems")

The linear systems class computes the intersection points between an arbitrarily dimensioned system of linear equations using gaussian elimination. My implementation reduces the system of equations to triangular form, then solves the system in reduced row echelon form. Interesting methods can be found below.

**add_multiple_times_row_to_row(coefficient, row_to_add, row_to_be_added_to)** - adds a linear equation together n times to an original linear equation

**extract_direction_vectors_for_parametrization()** - computes the solution for a system of equations in n dimensions and extracts the direction vectors of the intersection

**raise_exception_if_contradictory_equation()** - determines if the system of equations cannot be solved for





















