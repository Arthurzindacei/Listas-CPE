/*Projeto codificado pelo Monitor 
Monitor  : Sebastião Flávio Ribeiro de Morais   	      
Disciplina: CPE - COMPUTAÇÃO PARA ENGENHARIA
Professor: Wesin Ribeiro Alves
Data: 27/06/2024

Lista de exercícios sobre Arquivos

Nome do Programa: LeituraDeArquivo

Objetivo:

Demonstração de como ler um tipo de arquivo texto. No caso aqui, a leitura será
de um arquivo com extensão .cpp (programa em C++)

*/

//biblioteca padrão do c++
#include <iostream>

//biblioteca para abertura/leitura e escrita em arquivos
#include <fstream>

//permite utilizar a instrução sleep()
#include <unistd.h>

//Permite eliminar a instrução std:: 
using namespace std;

string sRegistro;

int main(){
    
    //criando a variável para leitura do arquivo
    ifstream vArquivo;//este modo é apenas para leitura

    //abrindo o arquivo ListaRamaisQuestao2
    vArquivo.open("main.cpp", ios::in);

    //verifica se o arquivo foi aberto
    if (!vArquivo.is_open()) {//vArquivo.fail() <=> vArquivo.is_open()
        cout << "\n===================================================";
        cout << "\nO arquivo não foi aberto. O programa será abortado!";
        cout << "\n===================================================\n";        
        vArquivo.close(); //fechando o arquivo
        sleep(2);
        return 2;
    }
   
    system("clear");
    
    //lendo linha a linha até o fim do arquivo
    while (getline(vArquivo, sRegistro)){

        //mostrando a linha lida na console
        cout << sRegistro << "\n";
    }
    
    //fechando o arquivo
    vArquivo.close();

    return 0;
}
