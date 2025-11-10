# Relatório de Observações - Atividade de Threads

## Informações do Aluno
- **Nome:** Pedro Ricardo dos Santos Gomes
- **Matrícula:** 20242014040014
- **Data:** 10/11/2025

## Ambiente de Execução

- [X] Executado localmente
- [ ] Executado em Docker/Fedora

**Sistema Operacional:** Codespace  
**Processador:** _[Ex: Intel Core i5, AMD Ryzen, etc.]_  
**Número de Cores:** 2 Cores

---

## Execução 1

### Resultados Observados

**Thread CPU (Thread 1):**
- Tempo de execução: 0.32 segundos
- Soma dos primos: 37550402023
- Ordem de conclusão: 3ª (1ª, 2ª ou 3ª)

**Thread I/O (Thread 2):**
- Tempo de execução: 0.02 segundos
- Linhas processadas: 10000
- Ordem de conclusão: 1ª (1ª, 2ª ou 3ª)

**Thread Mista (Thread 3):**
- Tempo de execução: 0.03 segundos
- Total de cálculos: 3482527859448382464
- Ordem de conclusão: 2ª (1ª, 2ª ou 3ª)

**Tempo Total do Programa:** 0.37 segundos

### Observações sobre a Saída

Descreva como as mensagens das threads apareceram no console:
Os threads aparecem intercalando em execução de suas operações.


---

## Execução 2 (Repetir para comparação)

### Resultados Observados

**Thread CPU (Thread 1):**
- Tempo de execução: 0.29 segundos
- Ordem de conclusão: 3ª (1ª, 2ª ou 3ª)

**Thread I/O (Thread 2):**
- Tempo de execução: 0.01 segundos
- Ordem de conclusão: 1ª (1ª, 2ª ou 3ª)

**Thread Mista (Thread 3):**
- Tempo de execução: 0.01 segundos
- Ordem de conclusão: 2ª (1ª, 2ª ou 3ª)

**Tempo Total do Programa:** 0.31 segundos

### Diferenças entre Execuções

Na segunda execução teve diferença de 6 segundos a menos que a primeira, a ordem foi igual.

---

## Análise e Conclusões

### 1. Qual thread terminou primeiro? Por quê?

A thread 2 terminou primeiro por conta de pedir muito da CPU, então o sistema "acelera" sua execução para não ter pausas na sua execução.

### 2. Por que os tempos de execução variam entre diferentes execuções?

Pois não há fatores que priorizem uma execução específica, então dependendo da execução um thread pode ser mais rápido.

### 3. Como o sistema operacional gerencia a execução das threads?

Durante a execução o sistema operacional decide a ordem e prioridades de execução, assim, intercalando entre execução dos threads.

### 4. Qual seria o impacto de aumentar o número de threads?

Se tiver mais núcleos ou mesma quantidade de threads, os threads poderam rodar paralelamente, assim, rodando mais rápido, entretanto, se tiver mais threads que núcleos, os núcleos teram que intercalar os threads, causando intervalos entre execuções dos threads.

### 5. O que aconteceria se executássemos as mesmas operações sequencialmente?

O sistema teria que esperar concluir a execução de uma operação para ir para a outra, deixando uma parte ociosa enquanto a outra executa uma determinado operação.

---

## Experimentos Adicionais (Opcional)

### Modificação 1: Aumentar NUM_ITERACOES

**Alteração realizada:** Mudei NUM_ITERACOES de 1000000 para 6000000

**Resultado observado:**
- Tempo da Thread CPU: 0.29 segundos
- Impacto no tempo total: ficou 0.02 segundo acima da segunda execução e 0.04 segundos abaixo da primeira.

**Conclusão:** Não teve impacto na execução.

### Modificação 2: Adicionar mais threads

**Alteração realizada:** Criei uma thread CPU e uma I/O

**Resultado observado:**
- Comportamento: Demorou mais a execução.
- Impacto na performance: O tempo almentou para 6 segundos.

**Conclusão:** Muitos threads podem fazer a execução ficar lenta se tiver poucos núcleos.

---

## Conceitos Aprendidos

Liste os principais conceitos de sistemas operacionais que você compreendeu melhor com esta atividade:

1. Como funciona o escalonamento no uso dos threads.
2. Como o uso de um tipo de operação pode impactar no uso de GPU do sistema.
3. Como a quantidade de núcleos impacta na quantidade de threads.
4. Como criar threads usando C.

---

## Dificuldades Encontradas

Descreva quaisquer problemas que enfrentou durante a atividade e como os resolveu:

Entender alguns conceitos, como o paralelismo de threads e como mexer no código em C.

---

## Comentários Finais

Atividade proveitosa para o aprendizado de sistemas operacionais e o que está por trás de seu funcionamento.

---

**Data de Conclusão:** 10/11/2025  
**Assinatura:** Pedro Ricardo dos Santos Gomes
