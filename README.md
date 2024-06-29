# clrplt module
I'd wanted to write module which would help me to plot matrix
(like matplotlib for python do). So, I created this module.


## How to use
Add this line in your file to import module:

```
import "github.com/Aleksandr-qefy/clrplot"
```


To draw your matrix like structure it must implement methods of `Plotable` interface:
```
type Plotable interface {
	CoordsToNum(Coords) int
	GetMaxNum() int
	GetMinNum() int
	Height() int
	Width() int
}

type Coords struct {
	I int
	J int
}
```


Supposed, that every element in matrix at position (I, J) 
can be represented as int type value (I name them `Num`),
so module could plot it.


To speed up matrix drawing I use multiple algorithms
like binary search and memorization. 


## Use examples
Examples how to create new ColorMap you can see in [file](https://github.com/Aleksandr-qefy/clrplot/blob/main/colormaps.go).


I use this module to plot fractals in this [project](https://github.com/Aleksandr-qefy/go_algebra_fractals).
