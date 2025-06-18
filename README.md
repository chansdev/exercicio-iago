# exercicio-iago

## 1
```c
#include <stdio.h>

int main() {
    
    int a, b, soma;
    printf("Digita um numero ai pra ve as soma deles:\n");
    scanf("%d", &a);
    scanf("%d", &b);
    
    soma = a + b;
    
    printf("\nSoma: %d", soma);

    return 0;
}
```

## 2
```c
#include <stdio.h>

int main() {
    
    int a;
    printf("Digita um numero ai pra ve se ele é impar:\n");
    scanf("%d", &a);
    
    if (a % 2 == 0) {
        printf("O numero é par visse");
    } else {
        printf("O numero é impar visse");
    }

    return 0;
}
```

## 3
```c
#include <stdio.h>

int main() {
    
    int a, i;
    printf("Digita um numero ai pra ve o fatorial dele:\n");
    scanf("%d", &a);
    
    i = a - 1;
    
    while (i > 0) {
        a = a * i;
        i--;
    }
    
    printf("valor: %d", a);

    return 0;
}
```

## 4
```c
#include <stdio.h>

int main() {
    
    int a, b, c, d, e, f, media;
    printf("Digita uns numero ai pra ve a media deles:\n");
    scanf("%d\n", &a);
    scanf("%d\n", &b);
    scanf("%d\n", &c);
    scanf("%d\n", &d);
    scanf("%d\n", &e);
    scanf("%d\n", &f);
    
    media = (a + b + c + d + e + f) / 6;
    
    printf("Media: %d", media);

    return 0;
}
```

## 5
```c
#include <stdio.h>

int main() {
    int ano;
    printf("Digita um ano ai pra ver se ele é bissexto:\n");
    scanf("%d\n", &ano);
    
    if ((ano % 4 == 0 && ano % 100 != 0) || (ano % 400 == 0)) {
        printf("O ano %d é bissexto", ano);
    } else {
        printf("O ano %d n é bissexto", ano);
    }
    

    return 0;
}
```

## 6
```
#include <stdio.h>
#include <math.h>

int main() {
    int n, i = 0, x;
    printf("Digite um numero pra ver se ele é uma potencia de 2:\n");
    scanf("%d", &n);
    
    while (x < n) {
        x = exp2(i);
        i++;
    }
    
    if (n == x) {
        printf("Esse numero é uma potencia de 2");
    } else {
        printf("Esse numero nao é uma potencia de 2");
    }

    return 0;
}
```

## 7
```c
#include <stdio.h>

int main() {
    int n1, n2, n3;
    printf("Fale 3 numeros para saber o maior V\n");
    printf("O primeiro: ");
    scanf("%d", &n1);
    printf("O segundo: ");
    scanf("%d", &n2);
    printf("O terceiro: ");
    scanf("%d", &n3);
    
    if (n1 > n2 && n1 > n3) {
        printf("%d é o maior numero", n1);
    } else if (n2 > n3) {
        printf("%d é o maior numero", n2);
    } else {
        printf("%d é o maior numero", n3);
    }
}
```

## 8
```c
#include <stdio.h>
#include <math.h>

int main() {
    float n, raiz;
    printf("Diga um nuemro para ver a raiz quadrada dele:\t");
    scanf("%f", &n);
    
    raiz = sqrt(n);
    printf("A raiz quadrada de %.2f é: %.2f", n, raiz);
}
```

## 9
_Transformar string em int (char - '0')

## 10
```c
#include <stdio.h>

int main() {
    float l1, l2, l3;
    printf("Digite o tamanho dos lados do triangulo pra saber a sua classe: \t");
    scanf("%f", &l1);
    scanf("%f", &l2);
    scanf("%f", &l3);
    
    if ((l1 == l2 && l1 != l3) || (l1 == l3 && l1 != l2) || (l2 == l3 && l2 != l1)) {
        printf("É isocelis");
    } else if (l1 == l2 && l1 == l3) {
        printf("É equilatero");
    } else {
        printf("É escaleno");
    }
    
}
```

## 25
```c
#include <stdio.h>

int main() {
    
    int a = 0, auxiliar, b = 1, n;
    printf("Digita um numero ai pra sabe se ele ta na sequencia de fibonacci:\n");
    scanf("%d", &n);
    
    while (auxiliar < n) {
        auxiliar = a + b;
        a = b;
        b = auxiliar;
        printf("%d\n", auxiliar);
    }
    
    if (auxiliar == n) {
        printf("Esse numero ta na sequencia de fibonacci visse");
    } else {
        printf("Esse numero nao ta na sequencia de fibonacci visse");
    }

    return 0;
}
```

## 27
```c
#include <stdio.h>
#include <math.h>

int main() {
    int preco, precoFinal;
    printf("Digite um preço pra saber qual vai ser o falor dele com juros\n");
    scanf("%d", &preco);
    
    if (preco < 100) {
        precoFinal = preco + (preco * 0.1);
    } else {
        precoFinal = preco + (preco * 0.2);
    }
    
    printf("Preco final: %d", precoFinal);

    return 0;
}
```

## 28
```c
#include <stdio.h>

int main() {
    float preco, valorFinal;
    int forma;
    printf("Digite o preço do produto comprado:\n");
    scanf("%f", &preco);
    
    printf("Formas de pagamento V\n 1: A vista\t2: Duas vezes\t3: de 3 até 10 vezes\n Digite forma que deseja:\n");
    scanf("%d", &forma);
    
    switch (forma) {
        case 1: 
        valorFinal = preco - (preco * 0.1);
        printf("Valor final: %f", valorFinal);
        break;
        
        case 2:
        printf("Valor final: %f", preco);
        break;
        
        case 3:
        if (preco > 100) {
            int qtd;
            printf("Você vai pagar por quantos meses? (de 3 a 10).");
            scanf("%d", &qtd);
            valorFinal = preco + (qtd * (preco * 0.03));
            printf("Preço final: %.2f", valorFinal);
        } else {
            printf("Desculpe, mas o preço não é suficiente para escolher essa opção... Reinicie o sistema.");
        }
        break;
    }
    

    return 0;
}
```

## 34
```c
#include <stdio.h>

int main() {
    char nome[100]; 
    char idade[100];
    char endereco[100]; 
    char numero[100];
    printf("Nome:");
    scanf("%s", &nome);
    printf("Idade:");
    scanf("%s", &idade);
    printf("Endereco (underline ao invez de espaço):");
    scanf("%s", &endereco);
    printf("Numero:");
    scanf("%s", &numero);
    
    printf("Seu nome é %s, você tem %s anos, mora na rua %s e seu telefone é %s", nome, idade, endereco, numero);
}

![image](https://github.com/user-attachments/assets/ae645183-c5d1-43a4-a11d-280553c933b9)
```

## 52
```c
#include <stdio.h>

int main() {
    float nota, notas = 0, media, i = 0;
    printf("Digite suas notas: \t\n");
    
    while (nota >= 0) {
        scanf("%f", &nota);
        
        if (nota >= 0) {
        notas += nota;
        
        i++;
        }
    }
    
    media = notas / i;
    
    printf("Media: %.2f", media);
    return 0;
}
```
