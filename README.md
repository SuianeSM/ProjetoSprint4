# 📡 Megaline Insights: Quem Gera Mais Receita — Surf ou Ultimate?

## Sobre o Projeto
Este projeto é uma análise prática e descomplicada dos planos pré-pagos da Megaline. A missão é simples: descobrir qual plano — **Surf** ou **Ultimate** — traz mais receita por usuário, usando dados de 500 clientes ao longo de 2018.

## 🎯 Objetivo Principal
Limpar, organizar e analisar os dados para entender o comportamento dos usuários e comparar a receita média entre os planos. De quebra, verificar se a galera de **NY–NJ** gasta diferente do resto do país.

## 📌 O Que Foi Feito

### **1. Limpeza de Dados**
- Tratamento de nulos e duplicados.
- Padronização de datas e unidades (minutos, GB).
- Arredondamentos conforme regras da Megaline:
  - cada chamada → arredondada pra cima;
  - dados do mês → soma em MB → arredondado pra cima em GB.

### **2. Cálculo da Receita Mensal**
Para cada usuário e mês:
- Contagem de minutos, SMS e GB usados.
- Cálculo de excedentes.
- Aplicação das regras de preço de cada plano.
- Receita final = preço mensal + excedentes.

### **3. Análise Exploratória**
- Distribuição de uso (minutos, SMS, dados).
- Estatísticas como média, variância e desvio padrão.
- Histogramas para visualizar padrões.

### **4. Testes de Hipótese**
- Surf vs Ultimate: média de receita é diferente?
- NY–NJ vs outras regiões: gastam diferente?
- Métodos usados: teste t ou Mann–Whitney, dependendo da distribuição.

## 📂 Dados Utilizados
A base inclui informações de 500 clientes: região, plano e uso mensal de chamadas, mensagens e dados.

## 🚀 Resultado Esperado
Ao final, você terá:
- uma base limpa e pronta pra análise;
- visualizações simples e diretas;
- comparações entre planos e regiões;
- conclusão sobre qual plano é mais lucrativo, em média.

Simples, direto ao ponto e pronto pra evoluir se você quiser expandir depois.

** Conclusão **
Analisando os valores dos planos já era possível perceber uma grande diferença na receita e em ambos os testes de hipóteses confirmam que os planos possuem diferenças significativas tanto quando comparando por usuários, tanto quando comparando por região. O plano Surf embora seja mais barato não tem uma boa franquia e os excedentes são caros tornando a receita muito variável para a operadora. Já o Ultimate mesmo com custo mais alto é mais compensativo devido a franquia e aos excedentes mais baratos. Em geral, somente analisando a receita utilizando gráficos não era possível identificar qual plano é mais vantajoso e até em alguns casos era possível verificar comportamentos semelhantes. Com isso, percebe-se a importância da realização dos testes de hipóteses
