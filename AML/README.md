# Primeiro laboratório: Ataque de Evasão com FGSM

Primeiro laboratório focado no conceito base de Adversarial Machine Learning (AML). Este projeto demonstra como realizar um ataque de evasão (Evasion Attack) de caixa-branca (White-box) contra um modelo de rede neural, enganando-o para que classifique imagens de forma incorreta.

O objetivo deste projeto é fornecer uma base prática para entender como pequenas perturbações matemáticas podem quebrar a lógica de inferência de um modelo.

## Conceitos Abordados

- **Adversarial Machine Learning (AML):** Exploração das vulnerabilidades estatísticas de modelos de IA.
- **Ataque de Evasão (Evasion Attack):** Manipulação da entrada (input) no momento da inferência para subverter o modelo.
- **Fast Gradient Sign Method (FGSM):** Uma técnica que usa os gradientes da rede neural para gerar ruído adversário.
- **Epsilon (força do ataque):** O orçamento de perturbação que define a intensidade da alteração na imagem.

## Pré-requisitos

Para rodar este notebook localmente, você precisará do Python 3.8 ou superior e das seguintes bibliotecas:

```bash
pip install tensorflow adversarial-robustness-toolbox matplotlib numpy jupyter
```

## O que esperar dos resultados

O notebook treinará rapidamente um modelo convolucional simples no dataset MNIST (dígitos escritos à mão). Em seguida, ele aplicará o ataque FGSM.

Na última célula, você verá um gráfico comparativo:

- Linha Superior: Imagens limpas e a classificação correta da IA.

- Linha Inferior: Imagens com o ruído adversário aplicado. Você notará que para o olho humano o número continua legível, mas a IA (indicada em texto vermelho) classifica o número incorretamente.
