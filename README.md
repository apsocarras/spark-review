# _spark-review_

#### By _**Alejandro Socarras**_

#### _Unit 3, Chapter 14 Code Review_

## Description

Practicing Spark Dataframe API 

## Assignment Instructions: 

Set Up the Data

* Read the coffee data CSV file into a Spark DataFrame.

* All the columns should be floats except for the 'Date' and 'Currency' columns.

Columns from Aggregate Functions

* Add a column to the DataFrame where the values are the difference between 'Open' and 'Close'.

* Add a column to the DataFrame where the values are the difference between 'High' and 'Low'.

* Add a column to the DataFrame where the values are 'True' if the volume for that day was 100 or above, and otherwise 'False'.

* Once you have a column for the difference between 'Open' and 'Close', add another column that contains the absolute values of the numbers in that column.
        Note: Absolute value is how far a number is from zero; it ignores whether a number is positive or negative. The Python standard library has a built-in function for this.

* Compute a column called net_sales which is the average of opening, high, low, and closing cost times the volume: net_sales = avg(opening, high, low, closing price) * volume

Stats

* Find the average of the values in the column that has the absolute values of the difference between 'Open' and 'Close'.

*  Get the count of values where the 'Volume' was less than 100.

* Find the average 'Open' value.

* Get the highest 'High' value.

Write File

* Save your DataFrame (including the four added columns) to /data as a parquet file. Exclude the /data directory from Git.

* Use Matplotlib to create a visualization (i.e. a chart) using the coffee data.

* Include code to write the Parquet file to BigQuery 
  
###  Setup/Install (Bash)

```bash
# Make/change to new project directory in desired location
mkdir </path/for/your/new/directory> && cd "$_"

# Clone repo
git clone https://github.com/apsocarras/spark-review.git 

# Create and activate a virtual environment
virtualenv -p python3.7 venv # repo written using 3.7 
source venv/bin/activate

# Pip install required packages
pip install -r requirements.txt

# Install dataset 
cd data/ 
sh get_data.sh # requires gsutil 
```
## Known Bugs

_No known bugs._

## License

_[MIT License](https://opensource.org/licenses/MIT)_

Copyright (c) _2.10.23_ Alejandro Socarras

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


