Aluno: Ítalo Fernandes Mendes Costa
Matrícula: 2021052414
Curso: BICT – UFMA
Disciplina: Laboratório de Programação
Professor: Rondineli Seba Salomão


📌 Descrição do Problema
O presente trabalho tem como objetivo o desenvolvimento de um sistema de gerenciamento de estacionamento rotativo, inspirado em modelos reais utilizados em centros urbanos e estabelecimentos comerciais.
Nesse tipo de sistema, os veículos são tarifados de acordo com o tempo de permanência no estacionamento. Além disso, existem regras adicionais, como aplicação de descontos por longos períodos e multas para permanência excessiva.

O sistema proposto deve ser capaz de:
Identificar o tipo de veículo
Calcular o valor com base no tempo de permanência
Aplicar regras de desconto e multa
Exibir um resumo completo do atendimento

📌 Modelagem do Sistema
Análise do Problema
O funcionamento do sistema segue uma lógica simples e sequencial:
Inicialmente, o usuário informa os dados do veículo, como placa, tipo e tempo de permanência. Em seguida, o sistema determina o valor por hora com base no tipo do veículo.
Após isso, é realizado o cálculo do valor base. Em seguida, o sistema verifica se o tempo de permanência atende aos critérios para aplicação de desconto ou multa.

Por fim, o sistema apresenta ao usuário todas as informações calculadas das Variáveis
Variável	Tipo	Finalidade
placa	char[]	Armazena a placa do veículo
tipo	inteiro	Identifique o tipo do veículo
tempo	flutuador	Tempo de chuva
valorHora	flutuador	Valor cobrado por hora
valorBase	flutuador	Valor inicial calculado
desconto	flutuador	Valor do desconto aplicado
multa	flutuador	Valor da multa.
valorFinal	flutuador	Valor total a ser pago
Regras de
O sistema considera os seguintes tipos de veículos:
Carro → R$ 5,00 por hora
Moto → R$ 3,00 por hora
Caminhonete → R$ 8,00 por hora
Extra:
Permanência de até 1 hora → cobrança do valor mínimo (1 hora)
Permanência acima de 5 horas → desconto de 10%
Permanência acima de 10 horas → multa adicional de R$ 20,00
Fluxo Lógico
O processamento do sistema ocorre na seguinte ordem:
- Entrada de dados (placa, tipo e tempo)
Definição do valor por hora utilizando estrutura switch-case
Cálculo do valor base utilizando estrutura if/else
Verificação de desconto (tempo > 5 horas)
Verificação de multa (tempo > 10 horas)
Cálculo do valor final
Exibição dos resultados

📌 Explicação 
O programa foi desenvolvido utilizando linguagem C, respeitando as restrições propostas (sem uso de laços de repetição e funções além da função principal).
Inicialmente, são declaradas variáveis para armazenar os dados do veículo e os valores utilizados nos cálculos.
A entrada de dados é realizada através da função scanf, onde o usuário informa a placa, o tipo do veículo e o tempo de permanência.
A definição do valor por hora é feita por meio da estrutura switch-case, garantindo organização e clareza na escolha do tipo de veículo.
O cálculo do valor base utiliza uma estrutura condicional if/else, garantindo a cobrança mínima de uma hora.
Em seguida, outras estruturas condicionais são utilizadas para verificar a aplicação de desconto e multa, conforme o tempo informado.
Por fim, o valor final é calculado e todos os dados são exibidos ao usuário utilizando a função printf.

📌 Como Compilar e Executar
Para compilar o programa, utilize o seguinte comando no terminal:
bash gcc main.c -o estacionamento
Para executar o programa:
bash ./estacionamento
📌 Exemplo de Entrada e Saída
Entrada
Placa: ABC1234
Tipo: 1
Tempo: 6
Às vezes, isso acontece por si só.
===== RESUMO =====
Placa: ABC1234
Tipo: Carro
Tempo: 6,00 horas
Valor Base: R$ 30,00
Desconto: R$ 3,00
Multa: R$ 0,00
Valor Final: R$ 27,00
📌 Considerações Financeiras
O desenvolvimento deste sistema permitiu a aplicação dos conceitos fundamentais da linguagem C, como uso de variáveis, operações e estruturas condicionais.
Além disso, contribuiu para o desenvolvimento do raciocínio lógico e da capacidade de modelagem de problemas reais.
