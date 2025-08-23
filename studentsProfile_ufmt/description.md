# Análise do perfil acadêmico/demográfico + histórico escolar dos discentes do curso de computação
 
# Seminário Integrado – Parte I: Testes Estatísticos

Utilizando os datasets em anexo (**perfil acadêmico/demográfico** + **histórico escolar**), cada trio (três alunos) deve realizar análises **descritivas**, **exploratórias** e **inferenciais**, além de aplicar **testes estatísticos** para validar hipóteses sobre **evasão** e **desempenho** dos estudantes do curso de **Ciência da Computação**.  

Este é o **primeiro de dois seminários integrados**:
- **Parte I:** Testes estatísticos  
- **Parte II:** Predição de evasão  

⚠️ **Observação:** É importante que pelo menos um membro do grupo tenha cursado a disciplina **Inteligência Artificial** ou possua **conhecimentos intermediários** no assunto.  

---

## 1. Perfil dos alunos
- Distribuição por sexo, raça, faixa etária, estado civil, nacionalidade.  
- Proporção de evasão vs conclusão por perfil demográfico.  
- Análise de correlação entre coeficiente de rendimento e evasão.  

---

## 2. Trajetória acadêmica
- Taxa média de aprovação/reprovação por disciplina.  
- Identificação de disciplinas gargalo (maior índice de reprovação).  
- Evolução do desempenho do aluno por período (notas e faltas).  
- Relação entre reprovações acumuladas e evasão.  

---

## 3. Comparação entre grupos
- Diferenças no coeficiente de rendimento por sexo, raça, tipo de ingresso.  
- Diferença entre evasão por forma de ingresso (ENEM, transferência, cotas).  

---

## Testes Estatísticos Recomendados

### Comparações de médias
- **t-Teste de Student (independente):** comparar coeficiente de rendimento médio entre evadidos e concluintes.  
- **ANOVA (ou Kruskal–Wallis, se não normal):** comparar rendimento entre diferentes tipos de ingresso ou estruturas curriculares.  

### Associação entre variáveis categóricas
- **Qui-quadrado de independência:** testar se evasão está associada a sexo, raça, tipo de ingresso, estado civil.  

### Correlação
- **Pearson:** correlação entre coeficiente e número de faltas.  
- **Spearman:** se a relação não for linear ou variáveis forem ordinais.  

### Comparação de distribuições
- **Mann-Whitney U:** comparar coeficientes entre dois grupos (ex.: evadidos vs concluintes) quando não há normalidade.  
- **Kolmogorov–Smirnov (K-S test):** comparar distribuição de notas entre evadidos e concluintes.  

### Modelagem estatística
- **Regressão logística:** prever evasão a partir de variáveis demográficas + acadêmicas.  
- **Análise de sobrevivência (Kaplan-Meier / Cox Regression):** modelar o tempo até a evasão.  

---

## 📌 Exemplos de hipóteses que podem ser testadas

- **"A taxa de evasão é maior entre alunos reprovados mais de 2 vezes em disciplinas obrigatórias do 1º ano."**  
  → Teste: Qui-quadrado + Regressão logística  

- **"O coeficiente de rendimento médio é diferente entre tipos de ingresso."**  
  → Teste: ANOVA / Kruskal-Wallis  

- **"O número de faltas tem correlação negativa significativa com o coeficiente."**  
  → Teste: Correlação de Pearson / Spearman  

- **"Alunos que são de fora do estado têm maior probabilidade de evasão que alunos locais."**  
  → Teste: Qui-quadrado ou Regressão logística  

- **"O tipo de ingresso (ENEM, vestibular, transferência, cotas, etc.) influencia a evasão."**  
  → Teste: Qui-quadrado  

- **"O coeficiente médio varia conforme o tipo de ingresso."**  
  → Teste: ANOVA / Kruskal-Wallis  

- **"O tempo até a evasão difere entre tipos de ingresso."**  
  → Teste: Análise de sobrevivência (Log-rank test, Kaplan-Meier)  

- **"Alunos reprovados por falta têm maior probabilidade de evasão que os reprovados por nota."**  
  → Teste: Qui-quadrado  

- **"Notas em disciplinas-chave (ex.: Cálculo I, Algoritmos) predizem evasão."**  
  → Teste: Regressão logística  

- **"Alunos que repetem disciplinas mais de duas vezes têm maior risco de evasão."**  
  → Teste: Qui-quadrado / Regressão logística  
