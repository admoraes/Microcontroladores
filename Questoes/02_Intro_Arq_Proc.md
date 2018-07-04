1. Quais as diferenças entre os barramentos de dados e de endereços?
Os barramentos de dados são bidirecionais, podendo ser utilizados tanto para envio quanto recebimento de dados. Além disso, este barramento representa o poder do processador.
Os barramentos de endereços são unidirecionais, sendo utilizados para apenas selecionar um determinado endereço de memória.

2. Quais são as diferenças entre as memórias RAM e ROM?
A memória RAM é uma memória volátil, ou seja, retém os dados apenas enquanto é alimentada. A memória ROM armazena os dados mesmo quando não está conectada a nenhuma fonte de alimentação.
Essas memórias também diferem quanto à velocidade e ao armazenamento. As memórias RAM são mais rápidas em relação as memórias ROM, mas armazenam menos informações que essas.

3. Considere o código abaixo:

```C
#include <stdio.h>
int main(void)
{
	int i;
	printf("Insira um número inteiro: ");
	scanf("%d", &i);
	if(i%2)
		printf("%d eh impar.\n");
	else
		printf("%d eh par.\n");
	return 0;
}
```

Para este código, responda: (a) A variável `i` é armazenada na memória RAM ou ROM? Por quê? (b) O programa compilado a partir deste código é armazenado na memória RAM ou ROM? Por quê?
(a) A variável i é armazenada na memória de dados (memória RAM), pois necessita de um acesso mais rápido durante a execução do programa.
(b) Os programas são armazenados na memória de programa (memória ROM). Isso ocorre porque o programa deve ficar gravado mesmo quando o dispositivo é desligado. Se os programas fossem armazenados na memória RAM teriam que ser carregados toda cada vez que o dispositivo fosse ligado.

4. Quais são as diferenças, vantagens e desvantagens das arquiteturas Harvard e Von Neumann?
A principal diferença entre as arquiteturas Harvad e Von Neumann é o acesso a memória. Na arquitetura de Von Neumann as memória RAM e ROM utilizam o mesmo barramento de dados e endereço. Por outro lado, a arquitetura Harvard utiliza um barramento de dados e endereço para a memória RAM e outro para a memória ROM.
Por conta disso, a arquitetura de Von Neumann tem a vantagem de ser menos complexa em relação a arquitetura Harvard, mas de ser mais lenta, pois na arquitetura harvard uma instrução pode ser executada enquanto também são buscadas informações na memória RAM.

5. Considere a variável inteira `i`, armazenando o valor `0x8051ABCD`. Se `i` é armazenada na memória a partir do endereço `0x0200`, como ficam este byte e os seguintes, considerando que a memória é: (a) Little-endian; (b) Big-endian. 
</br>
(a) Little-endian </br>
0x0200: 80 </br>
0x0201: 51 </br>
0x0202: AB </br>
0x0203: CD </br>
</br>
(b) Big-endian</br>
0x0200: CD </br>
0x0201: AB </br>
0x0202: 51 </br>
0x0203: 80 </br>
