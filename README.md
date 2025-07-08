# 🪸 Coral Reefs Classifier - CNN2

> Classificação automática de recifes de coral em três categorias: `bleached` (branqueado), `healthy` (saudável) e `partially` (parcialmente branqueado), utilizando redes neurais convolucionais com PyTorch.

---

## 📁 Dataset

- **Fonte**: [Roboflow - CoralReefs v1](https://universe.roboflow.com/ufrn-tx5b5/coralreefs-sdvu2)
- **Total de imagens**: 429
- **Formato**: `.jpg`, organizadas por pastas (ImageFolder)
- **Classes**:
  - `bleached`
  - `healthy`
  - `partially`

---

## 🧠 Arquitetura

Modelo baseado na classe `Architecture` fornecida pelo professor:

- 2 camadas convolucionais + `ReLU` + `MaxPool`
- `Dropout(p=0.3)`
- 2 camadas lineares
- Função de perda: `CrossEntropyLoss`
- Otimizador: `Adam (lr=3e-4)`

---

## ⚙️ Pré-processamento

- Redimensionamento para **28×28**
- Normalização automática `[0.0–1.0]`
- Conversão para `Tensor`
- Divisão:
  - 70% treino
  - 20% validação
  - 10% teste

---

## 📊 Resultados

### ✅ Acurácia no conjunto de teste


### 📈 Gráfico de Perdas

![Gráfico de Perdas](https://github.com/user-attachments/assets/7b8152a7-a839-4cef-b7b6-d96142d3d3cb)


- Linha azul: perda de treino  
- Linha vermelha: perda de validação  
- Escala logarítmica no eixo Y

### 📉 Matriz de Confusão

![Matriz de Confusão]([./confusion_matrix.png](https://github.com/user-attachments/assets/4b5541b7-f767-4a3c-ab3e-30201982d360))

---

## 📚 Conclusão

- O modelo teve bom desempenho nas classes `healthy` e `bleached`
- A classe `partially` foi a mais desafiadora, apresentando alta taxa de confusão
- A rede se mostrou promissora para tarefas reais com imagens subaquáticas

---

## 🧪 Próximos passos

- Testar normalização por canal (`make_normalizer`)
- Ajustar a arquitetura e dropout
- Explorar `lr_range_test` para encontrar a melhor taxa de aprendizado
- Visualizar filtros e ativações internas da rede

---

## 🧩 Requisitos

- Python 3.11
- PyTorch
- torchvision
- scikit-learn
- matplotlib

---

## 👨‍🏫 Trabalho acadêmico

Este projeto foi desenvolvido como parte da disciplina de **Aprendizado de Máquina**, utilizando código base fornecido pelo professor no notebook `week11`.

---
