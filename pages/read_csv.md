type:: function
package:: tidyverse
language:: R

- ```R
  library(tidyverse)
  example_data <- read_csv("example_data.csv")
  View(example_data)
  ```
- import a [[csv file]] into an object
- By default, read_csv() converts blank cells to missing data (NA)
- ## arguments
	- `col_names = FALSE`
		- to specify that the first row does NOT contain column names
	- `skip = 2`
		- will skip the first 2 rows
		- You can set the number
		   to any number you want.
		- This is helpful if there is additional information in the first few rows of your data frame that are not actually part of the table.
	- `n_max = 100`
		- will only read in the first 100 rows
		- You can set the number to any number you want
		- This is helpful if you’re not sure how big a file is and just want to see part of it.