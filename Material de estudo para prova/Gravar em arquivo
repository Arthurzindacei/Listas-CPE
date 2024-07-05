/*Projeto codificado pelo Monitor 
Monitor  : Sebastião Flávio Ribeiro de Morais   	      
Disciplina: CPE - COMPUTAÇÃO PARA ENGENHARIA
Professor: Wesin Ribeiro Alves
Data: 03/07/2024

Lista de exercícios sobre Arquivos

Nome do Programa: GravarEmArquivo

Objetivo:

Demonstração de como Gravar e ler em um arquivo texto a partir de uma struct. 

*/

//biblioteca padrão do c++
#include <iostream>

//biblioteca para abertura/leitura e escrita em arquivos
#include <fstream>

//permite utilizar a instrução sleep()
#include <unistd.h>

//Permite eliminar a instrução std:: 
using namespace std;

struct Arquivo{
    int iMatricula;
    string sNome;
};

int main(){
    
    //criando uma variável do tipo struct arquivo
    Arquivo vArquivo;
    
    //criando a variável para o arquivo
    fstream vArqSaida;//este modo é de leitura e Gravação

    //abrindo o arquivo para criação
    vArqSaida.open("C:\\Lixo\\Turma01.txt", ios::out);

    //verifica se o arquivo já existe
    if (!vArqSaida.is_open()) {//vArquivo.fail() <=> vArquivo.is_open()
        cout << "\n===============================================";
        cout << "\nO arquivo já existe. O programa será abortado!";
        cout << "\n===============================================\n";        
        vArqSaida.close(); //fechando o arquivo
        sleep(2);
        abort();
    }
   
    system("clear");
    
    cout << "Para finalizar a entrada de Dados no Arquivo digite 0.\n"; 
        int iM;
    while(true){
        cout << "\nMatrícula = ";
        cin >> vArquivo.iMatricula;
        
        if (vArquivo.iMatricula == 0){break;}//fim dos trabalhos
        
        cout << "\nNome      = ";
        cin >> vArquivo.sNome;
        
        //gravando no arquivo - o endl fecha a linha dentro do arquivo
        vArqSaida << vArquivo.iMatricula << " " << vArquivo.sNome << endl;         
 
    } 

    //fechando o arquivo
    vArqSaida.close();
    
    //abrindo o arquivo para leitura somente
    vArqSaida.open("C:\\Lixo\\Turma01.txt", ios::in);

   cout << "\n\n===============================================";        
   cout << "\n         Listagem do Arquivo de Dados"; 
   cout << "\n===============================================\n";
   
    //lendo o registro do arquivo e carregando a struc
    while (vArqSaida >> vArquivo.iMatricula >> vArquivo.sNome){

        //mostrando os dados lidos do arquivo na console
        cout << vArquivo.iMatricula << " - " << vArquivo.sNome << "\n";

    }

    //fechando o arquivo
    vArqSaida.close();
    
    return 0;
}
