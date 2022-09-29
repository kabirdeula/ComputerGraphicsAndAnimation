# Unit 02 : Two Dimensional and Three Dimensional Transformations

## Homogeneous Coordinate

### 1. Homogeneous representation for translation.

Therefore, P' = T(tx, ty)P

For inverse translation: T⁻¹(tx, ty) = T(-tx, -ty)

    [ x' ]   [ 1  0  x ] [ x ]
    [ y' ] = [ 0  1  y ] [ y ]
    [ h' ]   [ 0  0  1 ] [ h ]

Where h = 1

### 2. Homogeneous representation for rotation.

Therefore, P' = R(θ)P

For inverse rotation clockwise: R⁻¹(θ) = R(-θ) 

    [ x' ]   [ Cosθ  -Sinθ  0 ] [ x ]
    [ y' ] = [ Sinθ   Cosθ  0 ] [ y ]
    [ h' ]   [ 0      0     1 ] [ h ]

### 3. Homogeneous representation for scaling.

Therefore, P' = S(sx, sy)P

For inverse scaling: S⁻¹(sx, sy) = S(1/sx, 1/sy)

    [ x' ]   [ Sx  0  x ] [ x ]
    [ y' ] = [ 0  Sy  y ] [ y ]
    [ h' ]   [ 0   0  1 ] [ h ]