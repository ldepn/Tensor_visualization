# Visualizing Second Order Tensor Fields
This tool computes the bi-linear interpolation of tensor component from four input tensors (either from data or input symbolically).
The eigenvector field is then drawn along with separatrices overlayed.

## Libraries Used
To run this code you must have OpenGL, specifically the GLUT toolkit: https://www.opengl.org/resources/libraries/glut/

## Symbollic Tensor Input
Test tensors can be input either symbollically or from existing tensor data.
For symbolic input the equations for each tensor component can be input starting on line 299 of separatrices.cpp, then you must uncomment lines 324 through 327 and comment out the numerical input below that. 
For example:
```
double a(double x){
    return -2.0*x+1;
}
double b(double y){
    return y;
}
double c(double x){
    return x*x;
}
```
For numerical input there are a few examples starting on line 321 generated by Abaqus.
The input looks like this:
```
tensor[0].set(-486250,-13189,-13189,-524850);
tensor[1].set(-501290,-2951,-2951,-466510);
tensor[2].set(-511890,11300,11300,-472760);
tensor[3].set(-495640,2649.20,2649.20,-533430);
```
Four tensors are set, one for each vertex of a unit square. For each of the four tensors the four components are defined such that the second third are always identical (so that the tensor is symmetric)
## Built With

* C++
* Xcode
* OpenGL/GLUT

## Authors

* **David Lovitz**- [DavidLovitz](https://github.com/DavidLovitz)
* **Xiaofei Gao**


## License

This project may not be used/reproduced/republished without consent of the authors

## Acknowledgments

* Xiaofei Gao
* Professor Yue Zhang
* Oregon State University
* Thierry Delmarcelle
