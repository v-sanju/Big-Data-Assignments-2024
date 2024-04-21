Big Data Analytics (CS661)
Assignment 1

Sanjeev Kumar 231110044
Govind Sharma 23111

Question 1:

	Python Package required: vtk
	Functions Used:
		1) marchingx(c, v1, v2, pid1, pid2,data) -> returns the intersection point on horizontal edge of a cell. c is the iso-value, v1 and v2 are the pressure values at the two ends of the edge, pid1 and pid2 are the point ids of the two ends of the edge.
		2) marchingy(c, v1, v2, pid1, pid2,data) -> returns the intersection point on verticle active edge of the cell.
		3) marching(data) -> takes all the points in data set and iterates all the cells sequentially and finds the iso-contour points calling above two functions as and when required. These iso-countour points and iso-contour lines as collected in two variable "points" and "lines". Once all the cells are traversed, these two variables are passed to vtkPolyData() object and returned to main() function.
		4) main() -> this loads the dataset and calls the marching(data) function. output of marching(data) function is then saved in a vtp file named "onecell.vtp".
	
	Instructions to visualize in PARAVIEW:
		1) load this onecell.vtp file in paraview and load actual dataset as well.
		2) apply contour filter on actual data set and turn off the visibility of actual data set.
		3) at same value of the iso-contour parameter, contour of actual data and onecell.vtp will almost coincide (differs for ambiguos cells only).
		4) For a new value of iso-contour, re_run the python script and refresh the onecell vtp in PARAVIEW.