# Quiz-11.0



/*
 *  #Quiz
 *  Created by George.16 on 4/23/15.
 *  Copyright (c) 2015 George.16. All rights reserved.
 *  Main: Read text files from C++
 *  #TC1017
 *  Referencia: xxxxxxxxxxxxxxxxxxx
 *
 */
#include <iostream>
#include <unistd.h>
#include <string>
#include <fstream> // permite que un programa lea un textfile

using namespace std;

int nike(int w){
    int a[500] = {0}, x, sum = 0, div = 0, input[w], r = 0, total = 0 ;

fstream textfile; // no se que hace eso :O

textfile.open("Num.txt"); // lee el escrito

for(int i = 0; i<w; i++){ // 2418 strings
    
    textfile >> input[i]; // el dato en el lugar i es seleccionado en input[i]
    
    a[i] = input[i]; // el dato es guardado en la variable
    cout << input[i] << endl;

}
    
    for(int i = 0; i < w; i++){
        
        sum = a[i] + sum;
        div = div + 1;
        
    }
    
    cout << "The total of the values = "<< sum << endl;
    cout << "The number of values (same as number of lines btw) = "<< div << endl;
    cout << "The arithmetic mean (average) of the values = " << sum/div << endl;

    for(int i = 0;i < w; i++){
        
        total = total + (a[i] - r)^2;
        
    }
    
    sum = total / div;
    x = (sum)^(1/2);
    
    cout << "The standard deviation of the values = "<< x << endl;
    

    return 0;
}

int main(){
    int w;
    
    cout << "Cuantos Numeros tiene tu archivo" << endl;
    cin >> w;
    
    nike(w);
    
    return 0;
}
