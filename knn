#include "datos.h"
int col;
int filas = 0;
float promedio = 0;
float distancia = 0;
float datos_entrada[5] = {5.2,3.5,1.5,0.2,1};
int k = 3;
int i =0;
int j =0;
float dist_menores[2][3];
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  for(;i<k;i++){
    dist_menores[0][i] = 4000+i;
    dist_menores[1][i] = 0;
  }
  i=0;
}

void loop() {
  // put your main code here, to run repeatedly:
  for(;filas<90;filas++){
    for(int col = 0;col<4;col++){
      //Serial.print(matriz[fila][col]);
      promedio = promedio+pow((datos_entrada[col]-matriz[filas][col]),2);
    }
    //Serial.println();
    distancia = sqrt(promedio);
    if(distancia<dist_menores[0][k-1]){
      dist_menores[0][k-1]=distancia;
      for (int i = k-1;i>0;i--){
        float aux = dist_menores[0][i];
        float aux2 = dist_menores[1][i];
        
          if(aux<dist_menores[0][i-1] ){
            dist_menores[0][i]=dist_menores[0][i-1];
            dist_menores[0][i-1] = aux;
            dist_menores[1][i]=dist_menores[0][i-1];
            dist_menores[1][i-1] = aux2; 
          }
        
      }  
    }
    for (int j = 0 ; j<k; j++){
      Serial.println(dist_menores[0][j]);  
    }
    //Serial.println(promedio);
    promedio = 0;
  }
  //for (int i = 0 ; i<k; k++){
    //Serial.println(dist_menores[0][i]);  
  //}
