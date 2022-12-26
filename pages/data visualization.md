- use ##ggplot2 https://r4ds.hadley.nz/data-visualize.html
- demo dataset #palmerpenguins #penguins_dataset
	- library(palmerpenguins)
- check how the data frame looks
	- penguins
- get a glimpse or view of the data frame
	- glimpse(penguins)
	- view(penguins)
- create a ggplot
	- it's created layer by layer
	- it begins with the function ggplot()
	- then add the data ggplot(data=penguins)
		- #error_message in #rstudio
			- Warning message:
			  In grSoftVersion() :
			    unable to load shared object '/usr/local/lib/R/modules//R_X11.so':
			    libXt.so.6: cannot open shared object file: No such file or directory
			- #solution https://notes.rmhogervorst.nl/post/2020/09/23/solving-libxt-so-6-cannot-open-shared-object-in-grdevices-grsoftversion/
-