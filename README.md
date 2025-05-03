# EP-Multithreaded-QuickSort

# Sobre:
  O projeto é um programa em C que implementa o algoritmo de ordenação quicksort utilizando múltiplas threads. O objetivo principal é ordenar um arquivo binário com registros baseando-se apenas nas chaves dos registros. A quantidade de threads utilizadas no processo é definida pelo usuário ao executar o programa.


# Tarefas:
 TODO: Modularizar funções para simplificar o funcionamento do código.

# Principais funcionalidades:

### 1.Geração de Arquivos de Entrada:
  O arquivo ep_input_generator.c é responsável por criar arquivos binários de entrada com registros. Cada registro possui uma chave (4 bytes) e dados adicionais (96 bytes). O usuário pode escolher se as chaves estarão em ordem crescente, decrescente ou aleatória.

### 2.Ordenação Multithreaded:
  O arquivo principal, ep.c, implementa o quicksort multithreaded. Ele divide os registros do arquivo entre as threads, que ordenam suas respectivas seções. Após isso, as seções ordenadas são intercaladas para formar o arquivo final ordenado.

### 3.Verificação de Saída:
  O arquivo ep_output_verificator.c verifica se o arquivo de saída está corretamente ordenado. Ele percorre os registros e valida se as chaves estão em ordem crescente.

### 4.Cores no Terminal:
  O arquivo color.c define macros para exibir mensagens coloridas no terminal, facilitando a visualização de informações.


# Fluxo de Execução:

* O usuário gera um arquivo de entrada com ep_input_generator.c.
* O programa principal (ep.c) é executado para ordenar o arquivo gerado.
* O arquivo de saída é validado com ep_output_verificator.c.

# Formato de Execução:
./ep <arquivoDeEntrada> <arquivoDeSaida> <numeroDeThreads>


* <arquivoDeEntrada>: Caminho para o arquivo binário de entrada.
* <arquivoDeSaida>: Caminho para o arquivo binário de saída.
* <numeroDeThreads>: Número de threads a serem utilizadas.

# Objetivo:
O projeto demonstra o uso de programação paralela com threads para melhorar o desempenho de algoritmos de ordenação em arquivos grandes em um sistema Linux. Ele também explora o uso de mapeamento de memória (mmap) para manipular arquivos binários de forma eficiente.
