
//Sistema Embutido - O Lugar Certo Para o Conhecimento
//www.sistemaembutido.com.br
//https://www.facebook.com/sistemaembutido/
//Acesse o nosso site para ver muitos outros projetos!!

//Acionamento de um servo com potenciometro



#include <Servo.h>

Servo servo1; //Cria um objeto servo

void setup() {
servo1.attach(5); // indica que o servo esta vinculado a porta 5

}

void loop() {
int angle= analogRead(0);               //le o valor do potenciomentro
angle=map(angle, 0, 1023, 0, 180);      // Indica os valores de 0 a 180 do potenciometro
servo1.write(angle);                    // Escreve o angulo para o servo
delay(1);                               //aguarda para o servo atingir a posiçao

}
