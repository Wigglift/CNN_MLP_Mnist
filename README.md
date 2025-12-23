# CNNxMLP — Classificação do MNIST

Projeto desenvolvido para a eletiva de **Redes Neurais e Deep Learning** no **2º semestre de 2025**.

## 📌 Objetivo

Comparar **duas abordagens distintas de redes neurais** aplicadas ao mesmo problema:  
classificação de dígitos manuscritos usando o dataset **MNIST**.

A ideia aqui não é “inventar moda”, mas **entender na prática**:
- o que cada arquitetura assume sobre os dados  
- como essas suposições impactam desempenho e interpretabilidade  

## 🧠 Modelos Treinados

### 1️⃣ MLP (Multi-Layer Perceptron)

- Entrada: imagens do MNIST **flattened** (28x28 → 784 pixels)
- Cada pixel é tratado como uma feature independente
- Não preserva relações espaciais da imagem

**Limitação central:**  
O modelo não “entende” imagem — ele apenas aprende correlações numéricas entre pixels.

### 2️⃣ CNN (Convolutional Neural Network)

- Entrada: imagens no formato original (28x28)
- Uso de camadas convolucionais para:
  - detectar padrões locais (bordas, curvas, traços)
  - preservar a estrutura espacial da imagem
- Pooling para redução de dimensionalidade e generalização

**Vantagem estrutural:**  
A CNN impõe uma hipótese correta sobre o problema: **imagens têm padrões locais e hierárquicos**.

## 📊 Resultados

- O modelo **CNN apresentou desempenho significativamente superior** ao MLP
- Além da acurácia maior, o comportamento da CNN foi:
  - mais estável durante o treinamento
  - mais coerente na análise de erros
  - mais interpretável do ponto de vista conceitual

Isso não é coincidência.  
É consequência direta da **arquitetura estar alinhada com a natureza dos dados**.

## 🎯 Conclusão

- MLP funciona, mas força o problema errado sobre os dados
- CNN explora corretamente a estrutura espacial das imagens
- Arquitetura **importa tanto quanto os dados**

Este projeto reforça um ponto central em Deep Learning:  
> desempenho não vem só de mais parâmetros, mas de **boas hipóteses embutidas no modelo**

## 🛠️ Tecnologias Utilizadas

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Dataset MNIST

## 📚 Contexto Acadêmico

Projeto desenvolvido exclusivamente para fins educacionais, como parte da disciplina eletiva de **Redes Neurais e Deep Learning**.
