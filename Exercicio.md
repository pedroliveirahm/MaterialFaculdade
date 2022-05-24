### Resolução de questões da <a href="">ficha</a>

# 1
#include <iostream>
using namespace std;

int main()
{
    int numero;
    cout << "Digite um número inteiro : ";
    cin >> numero;
    cout << "O número inteiro escolhido foi : " << numero;
}
# 2
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int numero1, numero2, numero3;
    cout << "Olá, preciso que você digite 3 números inteiros :)" << endl;
    
    cout << "Digite o primeiro número inteiro : ";
    cin >> numero1;
    system("clear");
    
    cout << "Digite o segundo número inteiro : ";
    cin >> numero2;
    system("clear");
    
    cout << "Digite o terceiro número inteiro : ";
    cin >> numero3;
    system("clear");
    
    int calculo = numero1 + numero2 + numero3;
    
    cout << "O resultado da soma dos números inteiros escolhidos foi : " << calculo;
}
# 3
#include <iostream>
using namespace std;

int main() {
    int numero, sucessor, antecessor;
    cout << "Digite um número inteiro : ";
    cin >> numero;
    
    antecessor = numero - 1;
    cout << "O antecessor do número escolhido é : " << antecessor << endl;
    
    sucessor = numero + 1;
    cout << "O sucessor do número escolhido é : " << sucessor;
}
# 4
#include <iostream>
using namespace std;

int main() {
    float temperaturaCelsius, temperturaFahrenheit;
    
    cout << "Digite um número que será guardado em unidade de temperatura graus celsius : ";
    cin >> temperaturaCelsius;
    
    temperturaFahrenheit = (temperaturaCelsius * 9/5) + 32;
    cout << "A temperatura " << temperaturaCelsius << " em graus celsius equivale a " << temperturaFahrenheit << " em Fahrenheit";
}
# 5
#include <iostream>
using namespace std;

int main() {
    float velocidadeKmH, velocidadeMS;
    
    cout << "Digite um número que será guardado como velocidade na unidade Km/h : ";
    cin >> velocidadeKmH;
    
    velocidadeMS = velocidadeKmH / 3.6;
    cout << "A velocidade (" << velocidadeKmH << ") em km/h corresponde a (" << velocidadeMS << ") em m/s";
}
# 6
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    float nota1, nota2, nota3, nota4, mediaNotas;
    
    cout << "Bem vindo ao calculo da média das notas de um aluno" << endl;
    
    cout << "Informe a primeira nota do aluno : ";
    cin >> nota1;
    
    cout << "Informe a segunda nota do aluno : ";
    cin >> nota2;
    
    cout << "Informe a terceira nota do aluno : ";
    cin >> nota3;
    
    cout << "Informe a quarta nota do aluno : ";
    cin >> nota4;
    system("clear");
    
    mediaNotas = (nota1 + nota2 + nota3 + nota4) / 4;
    cout << "A média do aluno foi de : " << mediaNotas;
}
# 7
#include <iostream>
using namespace std;

int main() {
    float valorReal, valorDolar;
    
    cout << "Informe uma quantidade de dinheiro na cotação real : ";
    cin >> valorReal;
    
    valorDolar = valorReal * 4.82;
    cout << "O valor em reais (" << valorReal << ") corresponde a (" << valorDolar << ") em dolar"; 
}
# 8
#include <iostream>
using namespace std;

int main() {
    float raioCirculo, areaCirculo, pi = 3.14;
    
    cout << "Informe o raio do circulo (em metros) : ";
    cin >> raioCirculo;
    
    areaCirculo = pi * (raioCirculo * raioCirculo);
    cout << "A área do circulo em metros quadrados é : " << areaCirculo;
}
# 9
#include <iostream>
using namespace std;

int main() {
    float premio = 780000, ganhador1 = premio * 0.46, ganhador2 = premio * 0.32, ganhador3 = premio * 0.22;
    
    cout << "O premio do concurso foi avaliado em " << premio << " reais" << endl;
    cout << "O ganhador 1 receberá a fatia de 46%, correspondente a " << ganhador1 << " reais" << endl;
    cout << "O ganhador 2 receberá a fatia de 32%, correspondente a " << ganhador2 << " reais" << endl;
    cout << "O ganhador 3 receberá o restante, correspondente a " << ganhador3 << " reais" << endl;
}
# 10
#include <iostream>
using namespace std;

int main() {
    float numero;
    
    cout << "Digite um número : ";
    cin >> numero;
    
    if (numero > 0) {
        cout << "O número escolhido é positivo !" << endl << endl;
        if (numero > 0) {
            float raizquadrada = numero / numero;
            cout << "A raiz quadrado do número é : " << raizquadrada << endl;
            
            cout << "O número ao quadrado é : " << numero * numero;
        }
    }
    else cout << "O número é negativo";
}
# 11
#include <iostream>
using namespace std;

int main() {
    int numero;
    
    cout << "Digite um número - ";
    cin >> numero;
    
    if (numero % 2 == 0) {
        cout << "O número escolhido é par !" << endl;
        
        if(numero > 0) {
            cout << "O número também é positivo";
        } else cout << "O número também é negativo";
    } else {
        cout << "O número escolhido é ímpar !" << endl;
        
        if(numero > 0) {
            cout << "O número também é positivo";
        } else cout << "O número també mé negativo";
    }
}
# 12
#include <iostream>
using namespace std;

int main() {
    float nota1, nota2, media;
    
    cout << "Bem vindo ao calculador de média de um aluno, o qual 7 pontos eh a média de aprovação" << endl;
    
    cout << "Informe a primeira nota do aluno - ";
    cin >> nota1;
    if (nota1 < 0) cout << "A nota informada não pode ser negativa !" << endl;
    if (nota1 > 10) cout << "A nota informada não pode ser maior que 10.0 !" << endl;
    
    if(nota1 >= 0 && nota1 <= 10) {
        cout << "Informe a segunda nota do aluno - ";
        cin >> nota2;
        if (nota2 < 0) cout << "A nota informada não pode ser negativa !" << endl;
        if (nota2 > 10) cout << "A nota informada não pode ser maior que 10.0 !" << endl;
        
        if(nota2 >= 0 && nota2 <= 10) {
            media = (nota1 + nota2) / 2;
            if(media > 7) cout << "Parabéns ! a média das notas foi " << media << ". Aluno aprovado !";
            else cout << "Infelizmente o aluno não foi aprovado, pois sua média foi de " << media << " pontos";
        }
    }
}
# 13
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    float altura, pesoIdealHomem, pesoIdealMulher;
    char sexo;
    
    cout << "Bem vindo ao calculador de peso ideal através da sua altura e do seu peso" << endl;
    
    cout << "Agora informe sua altura (em metros) : ";
    cin >> altura;
    system("clear");
    
    if (altura > 0) {
        cout << "Informe seu sexo." << endl << "Se for masculino escreva 'M'" << endl << "Se for feminino escreva 'F'" << endl;
        cin >> sexo;
        
        if (sexo == 'M' || sexo == 'm' || sexo == 'F' || sexo == 'f') {
            
          pesoIdealHomem = (72.7 * altura) - 58;
            if (sexo == 'M' || sexo == 'm') cout << "Seu peso ideal é : " << pesoIdealHomem;
        
            pesoIdealMulher = (62.1 * altura) - 44.7;
            if (sexo == 'F' || sexo == 'f') cout << "Seu peso ideal é : " << pesoIdealMulher;
            
        } else cout << "Você informou o seu sexo incorretamente, repita o precesso corretamente !";
        
    } else cout << "Não existe algo ou alguém com altura negativa, repita o processo corretamente !";
}
# 14
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    float laboratorio, avaliacaoSemestral, exameFinal, mediaPonderada, pesos;
    
    cout << "Bem vindo ao calculador de média das avaliações e seus respectivos pesos" << endl << "laboratório : 2" 
    << endl << "avaliação semestral : 3" << endl << "exame final : 5" << endl;
    
    cout << "Informe a nota da avaliação do laboratório : ";
    cin >> laboratorio;
    system("clear");
    
    if (laboratorio >= 0 && laboratorio <= 10) {
        cout << "Informe a nota da avaliação semestral : ";
        cin >> avaliacaoSemestral;
        system("clear");
        if (avaliacaoSemestral >= 0 && avaliacaoSemestral <= 10) {
            cout << "Informe a nota da avaliação do exame final : ";
            cin >> exameFinal;
            system("clear");
            if(exameFinal >= 0 && exameFinal <= 10) {
                pesos = 10;
                mediaPonderada = ((laboratorio * 2) + (avaliacaoSemestral * 3) + (exameFinal * 5)) / pesos;
                cout << "A média ponderada do aluno foi de : " << mediaPonderada << endl;
                if (mediaPonderada < 3) {
                    cout << "Infelizmente o aluno foi reprovado !";
                } else if (mediaPonderada < 5) {
                    cout << "Ainda tem uma chance, você está de recuperação !";
                } else {
                    cout << "Parabéns, Você foi aprovado !";
                }
            } else {
                if (exameFinal < 0) cout << "A nota não pode ser negativa !";
                else if (exameFinal > 10) cout << "A nota não pode ser superior a 10.0 !";
            }
        } else {
            if (avaliacaoSemestral < 0)  cout << "A nota não pode ser negativa !";
            else if (laboratorio > 10) cout << "A nota não pode ser superior a 10.0 !";
        }
    } else {
        if (laboratorio < 0) cout << "A nota não pode ser negativa !";
        else if (laboratorio > 10) cout << "A nota não pode ser superior a 10.0 !";
    }
}
# 15
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    char pergunta1, pergunta2, pergunta3, pergunta4, pergunta5;
    int i = 0;
    
    cout << "Este é programa de investigação o qual deve ser 's' ou 'n'" << endl;

    cout << "Telefonou para a vítima? ";
    cin >> pergunta1;
    if (pergunta1 == 's') i++;
    
    cout << "Esteve no local do crime? ";
    cin >> pergunta2;
    if (pergunta2 == 's') i++;
    
    cout << "Mora perto da vítima? ";
    cin >> pergunta3;
    if (pergunta3 == 's') i++;
    
    cout << "Devia para a vítima? ";
    cin >> pergunta4;
    if (pergunta4 == 's') i++;
    
    cout << "Devia para a vítima? ";
    cin >> pergunta5;
    if (pergunta5 == 's') i++;
    system("clear");
    
    cout << "Conclusão do caso : " << endl;
    if (i < 1) cout << "O investigado é considerado inocente";
    if (i == 2) cout << "O investigado é considerado suspeito";
    if (i <= 4) cout << "O investigado é considerado cumplice";
    if (i == 5) cout << "O investigado é considerado culpado";
}
# 16
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int idade, tempoDeServico;
    
    cout << "Bem vindo ao calculador de aposentadoria" << endl 
    << "Iremos calcular se você possui o direito a partir da sua idade e tempo de serviço" << endl;
    
    cout << "Informe sua idade : ";
    cin >> idade;
    
    cout << "Informe seu tempo de serviço prestado (em anos) : ";
    cin >> tempoDeServico;
    system("clear");
    
    if (idade < tempoDeServico) cout << "Impossível você ter prestado serviço antes de ter nascido !" << endl 
    << "Refazer o questionário corretamente";
    else if (idade == 65 || tempoDeServico == 30) cout << "Parabéns você tem direito a aposentadoria !";
    else if (idade == 60 && tempoDeServico >= 25) cout << "Parabéns você tem direito a aposentadoria !";
    else cout << "Infelizmente o senhor ainda não tem o direito de se aposentar !";
}
# 17
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    float distancia, litrosGasolina, consumo;
    
    cout << "Bem vindo ao programa que faz a classificação economica do carro através do consumo (km/litro)" << endl;
    
    cout << "Informa a distância percorrida pelo carro (em km) : ";
    cin >> distancia;
    
    cout << "Informe a quantidade de gasolina consumida pelo carro (em litros) : ";
    cin >> litrosGasolina;
    system("clear");
    
    consumo = distancia / litrosGasolina;
    if (consumo < 8) cout << "O carro consome muita gasolina" << endl << "Venda-o rapidamente !";
    else if (consumo <= 12) cout << "O carro é classificado como econômico !";
    else if (consumo > 12) cout << "O carro é classificado como super econômico !";
    else cout << "Não existe carro com consumo negativo." << endl << "Refazer o programa com mais precisão !";
}
# 18
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int i = 1, i2 = 1, i3 = 1;
    
    for (i; i <= 100; i++) cout << i << " ";
    
    cout << endl << endl;
    
    while (i2 <= 100) {
        cout << i2 << " ";
        i2++;
    }
    
    cout << endl << endl;
    
    do {
        cout << i3 << " ";
        i3++;
    } while (i3 <= 100);
}
# 19
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    float valor; int i = 0;

    cout << "Digite 10 valores em sequência : " << endl;
    for (int stop = 1; stop <= 10; stop++) {
        cout << "Valor " << stop << " : ";
        cin >> valor;
        
        cout << valor + i << endl << endl;
        i = valor + i;
    }
}
# 20
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int i = 0, numero, media, stop;

    cout << "Digite 10 inteiros para que possa ser feita uma média : " << endl;
    
    for (stop = 1; stop <= 10; stop++) {
        cout << endl << "inteiro " << stop << " : ";
        cin >> numero;
        
        i = numero + i;
    }
    system("clear");
    if (stop = 10) {
            media = i / stop;
            cout << "A média aritmética foi de : " << media;
    }
}
# 21
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int i = 0, numero, media, stop;

    cout << "Digite 10 inteiros para que possa ser feita uma média : " << endl;
    
    for (stop = 1; stop <= 10; stop++) {
        cout << "inteiro " << stop << " : ";
        cin >> numero;
        
        if (numero > 0) {
            i = numero + i;
        }
        cout << i << endl << endl;
    }
    system("clear");
    if (stop = 10) {
            media = i / stop;
            cout << "A média aritmética dos números positivos foi de : " << media;
    }
}
# 22
#include <iostream>
using namespace std;

int main() {
    int numero;
    
    cout << "Digite um número para que possa ser dito os números ímpares na sequência existente : ";
    cin >> numero;
    
    for (int i = 1; i <= numero; i++) {
        if (i % 2 != 0) {
            cout << i << endl;
        }
    }
}
# 23
#include <iostream>
#include <stdlib.h>
using namespace std;

int main() {
    int numero;
    
    cout << "Digite um número para que possa ser impressa sua sequência de 0 até n em ordem crescente" << endl;
    cin >> numero;
    for(int i = 0; i <= numero; i++) {
        cout << i << " ";
    }
}
# 24
#include <iostream>
using namespace std;

int main() {
    int numero;
    
    cout << "Digite um número para que possa ser impressa sua sequência de 0 até n em ordem decrescente" << endl;
    cin >> numero;
    for(int i = numero; i >= 0; i--) {
        cout << i << " ";
    }
}
# 25

# 26
# 27


