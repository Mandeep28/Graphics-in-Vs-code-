[![Author - Mandeep28](https://img.shields.io/badge/Author%20---%20Mandeep28-brightgreen)](https://opensource.org/licenses/)


## Setting up graphics library (graphics.h) in Visual Studio Code (c++)

Download the compiler (Because graphic.h library need a 32 bit compiler) - [click here](https://jmeubank.github.io/tdm-gcc/)


Download the graphic.h files -[click here](https://drive.google.com/file/d/16xZBvFXf7yFjxwTpuyevK1KPuLgUeZFh/view)

Open vs code , go to command palette (ctrl + shift + P), then go to C/C++ edit ui config 
Add compiler argument 
```
-lbgi
-lgdi32
-lcomdlg32
-luuid
-loleaut32
-lole32
```
Then go to code runner extension setting 

Then go to Code runner Execute Map and click on edit in setting json 

if "code-runner.executorMap " : {// some files } not include then include it and in "cpp" : "// some value",


replace the value with 
```
"cd $dir && g++ $fileName -o $fileNameWithoutExt -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32 && $dir$fileNameWithoutExt",
```
