[![Author - Mandeep28](https://img.shields.io/badge/Author%20---%20Mandeep28-brightgreen)](https://opensource.org/licenses/)


## Setting up graphics library (graphics.h) in Visual Studio Code (c++)

Download the compiler (Because graphic.h library need a 32 bit compiler) - [click here](https://jmeubank.github.io/tdm-gcc/)

Download the graphic.h files -[click here](https://drive.google.com/file/d/16xZBvFXf7yFjxwTpuyevK1KPuLgUeZFh/view)

 Get all the files needed `graphics.h`, `winbgim.h` and `libbgi.a`

- Copy `graphics.h` and `winbgim.h` files to `TDM-GCC-32/include` folder.

location might be **("C:/TDM-GCC-32/include/")**

- Copy `libbgi.a` to file to `TDM-GCC-32/lib` folder.

location might be **("C:/TDM-GCC-32/lib")**



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
Then go to code runner extension setting (if not install code runner extension please install it ) 

Then go to Code runner Execute Map and click on edit in setting json 

if "code-runner.executorMap " : {// some files } not include then include it and in "cpp" : "// some value",


replace the value with 
```
"cd $dir && g++ $fileName -o $fileNameWithoutExt -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32 && $dir$fileNameWithoutExt",
```
After setting up all thing make a file with any name example - "example.cpp" and paste the code given below (note that this is only for testing that all the thing you setup is perfect or not )
```
//create a file name it example.cpp inside src or any other name with .cpp extension

#include <graphics.h>

int main(){
    int gdrive = DETECT;
    int gmode;

    initgraph(&gdrive, &gmode, NULL);
    // you can also pass NULL for third parameter if you did above setup successfully
    // example: initgraph(&gd, &gm, NULL);

    arc(200, 200, 0, 360, 100);
    arc(150, 150, 0, 360, 20);
    arc(250, 150, 0, 360, 20);

    arc(200, 200, 0, 360, 5);
    arc(200, 250, 180, 360, 30);

    getch();
    closegraph();
}

```

Then run the code - Output will be look like this 👇👇


<img width="959" alt="Screenshot_20230213_114103" src="https://user-images.githubusercontent.com/95164601/218538691-0d4f8de3-6aaf-4ec0-a1e1-352e197cbd3b.png">

<h3> 🤝🏻 &nbsp;Connect with Me </h3>

<p align="center">
<a href="https://www.linkedin.com/in/mandeep2002/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Mandeep%20Singh-blue?style=flat-square&logo=linkedin"></a>
<a href="https://www.instagram.com/mandeep_singh.28/"><img alt="Instagram" src="https://img.shields.io/badge/Instagram-mandeep_singh.28-blue?style=flat-square&logo=instagram"></a>
<a href="mailto: mandeepsingh13524@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-mandeepsingh13524@gmail.com-blue?style=flat-square&logo=gmail"></a>
</p>

⭐️ From [Mandeep28](https://github.com/Mandeep28)
