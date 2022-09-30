# Numerical Problems and Solutions

## 1. Given object A(2, 5), B(4, 2), C(6, -7) and D(10, 2) is translated with T(9, 0) and then scale about origin with scale factor S(2, 4) and then rotate about origin with an angle θ = 30°.

    Given,
    T(9, 0)
    S(2, 4)
    θ = 30°

    Net transformation = R(30°) ・ S(2, 4) ・ T(9, 0)

         [ cos30  -sin30  0 ][ 2  0  0 ][ 1  0  9 ]
    NT = [ sin30  cos30   0 ][ 0  4  0 ][ 0  1  0 ]
         [ 0      0       1 ][ 0  0  1 ][ 0  0  1 ]

         [ 0.866  -0.5    0 ][ 2  0  18 ]
    NT = [ 0.5     0.866  0 ][ 0  4  0  ]
         [ 0       0      1 ][ 0  0  1  ]

         [ 1.732  -2      15.588 ]
    NT = [ 1       3.464  9      ]
         [ 0       0      1      ]

    Let A', B', C', D' be the resultant point. So,

    A' = NT * A

         [ 1.732  -2      15.588 ][ 2 ]
    A' = [ 1       3.464  9      ][ 5 ]
         [ 0       0      1      ][ 1 ]

         [  9.052 ]
    A' = [ 28.32  ]
         [  1     ]

    B' = NT * B

         [ 1.732  -2      15.588 ][ 4 ]
    B' = [ 1       3.464  9      ][ 2 ]
         [ 0       0      1      ][ 1 ]

         [ 18.516 ]
    B' = [ 19.928 ]
         [  1     ]

    C' = NT * C

         [ 1.732  -2      15.588 ][  6 ]
    C' = [ 1       3.464  9      ][ -7 ]
         [ 0       0      1      ][  1 ]

         [ 39.98  ]
    C' = [ -9.248 ]
         [  1     ]

    D' = NT * D

         [ 1.732  -2      15.588 ][ 10 ]
    D' = [ 1       3.464  9      ][  2 ]
         [ 0       0      1      ][  1 ]

         [ 28.908 ]
    D' = [ 25.928 ]
         [  1     ]

## 2. Given object A(2, 6), B(8, 4), C(6, 5) is rotated by 45° about the point(2, 2).

    Given,
    T(2, 2)
    θ = 45°

    Net transformation = T(2, 2) ・ R(45°) ・ T(-2, -2)

         [ 1  0  2 ][ cos45  -sin45  0 ][ 1  0  -2 ]
    NT = [ 0  1  2 ][ sin45  cos45   0 ][ 0  1  -2 ]
         [ 0  0  1 ][ 0      0       1 ][ 0  0   1 ]

         [ 1  0  2 ][ 0.7071  -0.7071  0 ][ 1  0  -2 ]
    NT = [ 0  1  2 ][ 0.7071   0.7071  0 ][ 0  1  -2 ]
         [ 0  0  1 ][ 0        0       1 ][ 0  0   1 ]

         [ 1  0  2 ][ 0.7071  -0.7071   0      ]
    NT = [ 0  1  2 ][ 0.7071   0.7071  -2.8284 ]
         [ 0  0  1 ][ 0        0        1      ]

         [ 0.7071  -0.7071   2      ]
    NT = [ 0.7071   0.7071  -0.8284 ]
         [ 0        0        1      ]

## 3. Reflect a prism A(0, 0, 0), B(1, 1, 0), C(1, 2, 2), D(0, 2, 0) about yz plane which has been rotated previouslywith +90° about y axis.

    NT = Ryzplane ・ R(90°)y-axis

$$NT =\begin{bmatrix}
-1 & 0 & 0 & 0 \\
 0 & 1 & 0 & 0 \\
 0 & 0 & 1 & 0 \\
 0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
Cos90° & 0 & -Sin90° & 0 \\
0      & 1 &  0      & 0 \\
Sin90° & 0 &  Cos90° & 0 \\
0      & 0 &  0      & 1 \\
\end{bmatrix}$$

$$NT =\begin{bmatrix}
 0 & 0 & 1 & 0 \\
 0 & 1 & 0 & 0 \\
 1 & 0 & 0 & 0 \\
 0 & 0 & 0 & 1 \\
\end{bmatrix}$$

## 4. A pyramid defined by coordinates A(0, 0, 0), B(1, 0, 0), C(0,1, 0), D(0, 1, 0) is sclaed to double of its size about the point (0, 1, 0) then translate it to new position by translation vector (4, 5, 6) and finally rotated by angle(-45°) in clockwise about x axis. Find out the final point.

    NT for scaling = T(0, 1, 0) ・ S(2, 2, 2) ・ T(0, -1, 0)

$$NT = \begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
2 & 0 & 0 & 0 \\
0 & 2 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
1 & 0 & 0 &  0 \\
0 & 1 & 0 & -1 \\
0 & 0 & 1 &  0 \\
0 & 0 & 0 &  1 \\
\end{bmatrix}$$

$$NT = \begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
2 & 0 & 0 &  0 \\
0 & 2 & 0 & -2 \\
0 & 0 & 2 &  0 \\
0 & 0 & 0 &  1 \\
\end{bmatrix}$$

$$NT = \begin{bmatrix}
2 & 0 & 0 &  0 \\
0 & 2 & 0 & -1 \\
0 & 0 & 2 &  0 \\
0 & 0 & 0 &  1 \\
\end{bmatrix}$$

    Final NT = R(-45°) x T(4, 5, 6) x NTscale
$$Final NT =\begin{bmatrix}
1 &  0      &  0      & 0 \\
0 & -cos45° & -sin45° & 0 \\
0 & -sin45° & -cos45° & 0 \\
0 &  0      &  0      & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
1 & 0 & 0 & 4 \\
0 & 1 & 0 & 5 \\
0 & 0 & 1 & 6 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
2 & 0 & 0 &  0 \\
0 & 2 & 0 & -1 \\
0 & 0 & 2 &  0 \\
0 & 0 & 0 &  1 \\
\end{bmatrix}$$

$$NT = \begin{bmatrix}
1 &  0      &  0      & 0 \\
0 & -0.7071 & -0.7071 & 0 \\
0 & -0.7071 & -0.7071 & 0 \\
0 &  0      &  0      & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
2 & 0 & 0 & 4 \\
0 & 2 & 0 & 4 \\
0 & 0 & 2 & 6 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}$$

$$NT = \begin{bmatrix}
2 &  0      &  0      &  0     \\
0 & -1.4142 & -1.4142 & -7.071 \\
0 & -1.4142 & -1.4142 & -7.071 \\
0 &  0      &  0      &  1     \\
\end{bmatrix}$$