# Sistem-de-alarma

1. Tema proiectului
Acest proiect reprezinta o implementare minimala a unui sistem de alarm iar pentru implementarea acestuia am folosit un microcontroller Arduino Uno.
Pe langa placa de dezvoltare, am mai folosit urmatoarele componente: senzor PIR(necesar pentru detectia miscarii), un buzzer(cu rolul de a produce semnalul sonor in 
cazul in care se detecteaza o miscare), un ecran LCD(afiseaza parola introdusa precum si statusul sistemului), o tastatura(necesara pentru a introduce parola), 2
potentiometre(unul pentru a regla intensitatea sunetului si celalalt pentru intensitatea ecranului), breadboard(necesar pentru a interconecta componentele) precum si
fire de legatura. 

2. Dezvoltarea software a programului
Dupa implementarea partii hardware a proiectului, m-am ocupat de dezvoltarea partii software a acestuia prin utilizarea limbajului de programare C++ si a mediului de
lucru Arduino IDE.
Astfel, in scrierea codului am utilizat diverse biblioteci pentru a reduce din complexitatea programului si anume:
- LiquidCristal: am utilizat aceasta biblioteca pentru a mi se permite controlul ecranului LCD pe care l-am utilizat cu scopul de a afisa parola introdusa cat si
informatii despre starea sistemului
-Keypad: in cadrul proiectului am utilizat o tastatura cu 16 taste dispuse sub forma de matrice cu dimensiunea de 4x4, iar pentru a putea controla acest tip de tastatura
a fost necesar sa includ in program biblioteca keypad.h

3. Functionarea proiectului
Initial sistemul de alarma este dezactivat afisandu-se pe ecran un mesaj in acest sens iar pentru activarea acestuai este necesara apasarea tastei * . Odata apasat acest
buton, se observa ca mesajul de pe ecranul LCD se schimba si ni se cere sa se introduca o parola pentru ca sistemul sa se dezactiveze. Tot in acest moment, daca senzorul
detecteaza o miscare, aceasta este "preluata" de catre buzzer iar rezultatul apelarii functiei handlerBuzzer() pentru cazul in care sistemul este activat, va fi generarea
unui semnal sonor similar unui semnal de alarma. Dupa ce se introduce parola corecta formata din 4 cifre si insotita de tasta # la final, sistemul de alarma va fi 
dezactivat si va ramane asa pana cand se va apasa din nou tasta *.

4. Resurse bibliografice
https://howtomechatronics.com/
https://www.circuitbasics.com/how-to-set-up-a-keypad-on-an-arduino/
https://docs.arduino.cc/learn/electronics/lcd-displays
