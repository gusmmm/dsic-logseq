- layer by layer
- function ggplot()
- data inside function
	- ggplot(data=penguins)
- mapping argument
	- defines how variables in your dataset are mapped to visual properties of your plot
	- [[aesthetics]]
		- mapping is always paired with [[aes()]] function
			- the x and y arguments specify the variables for each axis
		- ggplot(data = penguins,
		              mapping = aes(x = flipper_length_mm, y = body_mass_g))
		- ![image.png](../assets/image_1672157347287_0.png)
	- geom
		- the geometrical object used to represent the data
		- these geometric objects are made available in ggplot2 with functions that start with geom_
		- #bar_chart  use bar geoms geom_bar()
		- #line_chart use line geoms geom_line()
		- #boxplot use boxplot geoms geom_boxplot()
		- #scatterplot break the trend; they use the point geom [[geom_point()]]
		- add the geom argument with a + after aes()
		- ggplot(data = penguins,
		              mapping = aes(x = flipper_length_mm, y = body_mass_g)) +
		              geom_point()
			- ![image.png](../assets/image_1672157903777_0.png)
		- add a smooth curve displaying the relationship between the variables with [[geom_smooth()]]
			- ggplot(data = penguins,
			              mapping = aes(x = flipper_length_mm, y = body_mass_g, color = species)) +
			              geom_point() +
			              geom_smooth()
			- ![image.png](../assets/image_1672158604287_0.png)
			- a line for each specie in the data set
		- add color and shape to the points
			- ggplot(data = penguins,
			              mapping = aes(x = flipper_length_mm, y = body_mass_g)) +
			              geom_point(mapping = aes(color = species, shape = species)) +
			              geom_smooth()
			- ![image.png](../assets/image_1672159168707_0.png)
			- a single line for the whole data set
		- improve the #label of the plot with [[labs()]]
			- ggplot(penguins, 
			         aes(x = flipper_length_mm, y = body_mass_g)) +
			         geom_point(aes(color = species, shape = species)) +
			         geom_smooth() +
			         labs(
			                 title = "Body mass and flipper length",
			                 subtitle = "Dimensions for Adelie, Chinstrap, and Gentoo Penguins",
			                 x = "Flipper length (mm)", 
			                 y = "Body mass (g)",
			                color = "Species", 
			                shape = "Species"
			    )
			- ![image.png](../assets/image_1672159760615_0.png)
-