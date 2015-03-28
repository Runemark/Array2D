# Array2D
Generic, lightning-fast 2D matrix in Swift (runs laps around traditional 2D arrays)

Advantages:
* Really Fast

Disadvantages:
* Dimensions (rows, cols) must be known at time of initialization, and cannot be changed
* Must provide a default "fill" value of type <T> which will be used to populate the matrix
* Much slower at getting specific rows

Comparison to a traditional double array ([[Int]], [[Float]], [[Double]], etc.):
Standard Double Array (SDA) vs. Array2D (A2D)... fight!

Benchmark: 2-Dimensional Array of Bools with 1000 rows and 1000 columns. Times reported in seconds.

* SDA Init: 5.77422904968242
* A2D Init: 2.40751695632935 {2.3x faster}

Last Element: (row:999,col:999)

* SDA Access Last Element: 6.9737434387207e-06
* A2D Access Last Element: 2.9802322387695e-06 {2.3x faster}

* SDA Set Last Element: 5.69820404052734e-05
* A2D Set Last Element: 2.98023223876953e-06 {19.1x faster}

Last Row: (row:999)

* SDA Get Last Row: 2.0265579223632e-06
* A2D Get Last Row: 0.00067870020866394 {330x slower}

Last Col: (col:999)

* SDA Get Last Col: 0.00999301671981812
* A2D Get Last Col: 0.0068429708480835 {1.4x faster}

* SDA Full Iteration: 3.64821296930313
* A2D Full Iteration: 1.90631002187729 {1.9x faster}
