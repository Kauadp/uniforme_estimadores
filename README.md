# 📊 Estimadores para a Distribuição Uniforme Discreta

Projeto desenvolvido para a disciplina de Estatística II, com foco na dedução, simulação e comparação de dois estimadores clássicos do parâmetro da distribuição uniforme discreta: **Método dos Momentos (MM)** e **Máxima Verossimilhança (MV)**.

---

## 🎯 Objetivo

- Deduzir os estimadores analiticamente
- Implementar simulações no R para avaliar o desempenho de cada estimador
- Comparar **viés**, **erro quadrático médio (REQM)** e **amplitude dos intervalos de confiança** em diferentes cenários

---

## 🧠 Metodologia

Foram realizadas simulações considerando três cenários distintos para o valor de θ: `θ = 5`, `10` e `100`, com amostras de tamanhos variados (n = θ/2, θ, 2θ). Para cada caso, foram geradas 10.000 amostras da distribuição uniforme discreta.

As métricas avaliadas foram:
- **Viés**: diferença entre o valor estimado e o verdadeiro
- **REQM**: mede a variância e o erro quadrático
- **Intervalos de confiança**: média das amplitudes de IC para 95%

---


## 📈 Resultados

### 🔹 Estimador por Método dos Momentos

- Estimador simples e direto: $\hat{θ}_{MM} = 2\bar{X} - 1$
- Maior viés e REQM em amostras pequenas
- Comportamento melhora com o aumento da amostra
- Boa consistência a partir de $n \geq 2\theta$

### 🔹 Estimador por Máxima Verossimilhança

- Estimador não centrado: $\hat{θ}_{MV} = \max(X_1, ..., X_n)$
- Rápida convergência para o verdadeiro $\theta$ com o aumento da amostra
- Menor viés e REQM em praticamente todos os cenários
- Mais sensível a amostras pequenas quando $\theta$ é grande

---

## ⚖️ Conclusão Comparativa

Os resultados das simulações mostram que:

- O **estimador de máxima verossimilhança (EMV)** se mostrou **mais eficiente** na maioria dos casos, com menor viés e REQM, especialmente quando o tamanho da amostra é adequado em relação a $\theta$.
- O **método dos momentos (MM)**, apesar de ser mais simples e computacionalmente leve, apresentou **maior variabilidade e viés** em cenários com menos informação.
- Ambos os estimadores são **consistentes**, mas o EMV oferece uma melhor performance geral, sendo preferível em aplicações práticas com tamanho amostral suficiente.

---

## 👨‍💻 Autor

Kauã D. — Estudante de Estatística  
Este projeto foi desenvolvido como parte de um trabalho acadêmico e adaptado para portfólio no GitHub.

---

## 📂 Observação

Os arquivos `.csv` contendo as tabelas de resultados estão disponíveis na pasta `data/`.  



