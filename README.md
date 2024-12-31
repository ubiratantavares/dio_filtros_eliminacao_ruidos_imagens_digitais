# DIO - Filtros de Eliminação de ruídos em imagens digitais

Segue uma proposta estruturada para abordar **Filtros de Eliminação de Ruídos em Imagens Digitais** e seus tópicos relacionados. 

## **Tratamento de Ruídos em Imagens Digitais**

O tratamento de ruídos em imagens digitais é essencial para melhorar a qualidade visual e garantir resultados mais precisos em análises ou processamento subsequente. Ruídos como *sal e pimenta*, gaussianos e speckle podem degradar imagens, dificultando a interpretação. Abaixo estão os principais filtros utilizados.

### **1. Filtro Gaussiano**

O filtro gaussiano é um método linear utilizado para suavizar imagens e reduzir ruídos de alta frequência. Ele aplica um kernel com pesos distribuídos conforme uma função gaussiana, o que preserva melhor as bordas comparado ao filtro de média.

- **Características**:

  - Suaviza gradualmente.

  - Reduz ruídos uniformes.

  - Excelente para ruído Gaussiano.

- **Exemplo de kernel (3x3)**:

  \[
  \frac{1}{16}
  \begin{bmatrix}
  1 & 2 & 1 \\
  2 & 4 & 2 \\
  1 & 2 & 1 \\
  \end{bmatrix}
  \]

### **2. Filtro da Mediana**

O filtro da mediana é não-linear e substitui cada pixel pelo valor mediano de uma janela ao redor. É altamente eficaz para ruídos *sal e pimenta* sem borrar significativamente os detalhes.

- **Características**:

  - Preserva bordas.

  - Eficiente contra ruídos impulsivos.

  - Ideal para imagens binárias e naturais.

### **3. Filtro de Média**

O filtro de média é um método linear que calcula a média aritmética dos pixels vizinhos em uma janela. Ele reduz o ruído suavizando a imagem, mas tende a borrar bordas.

- **Características**:

  - Simples e rápido.

  - Bom para redução de ruídos leves.

  - Não preserva bordas.

- **Exemplo de kernel (3x3)**:

  \[
  \frac{1}{9}
  \begin{bmatrix}
  1 & 1 & 1 \\
  1 & 1 & 1 \\
  1 & 1 & 1 \\
  \end{bmatrix}
  \]

## **Filtros para Imagens Digitais**

Filtros podem ser utilizados não apenas para remoção de ruídos, mas também para destacar detalhes, alterar o contraste ou transformar características estruturais das imagens.

### **1. Filtros**

- **Passa-Baixa**: Remove altas frequências, ideal para suavização.

- **Passa-Alta**: Realça bordas e detalhes finos.

- **Filtro de Sobel/Prewitt**: Detecta bordas ao computar gradientes locais.

### **2. Contrastes**

- **Equalização de Histograma**: Redistribui a intensidade para melhorar o contraste.

- **Realce Local**: Ajusta o contraste em pequenas regiões da imagem.

### **3. Transformação**

- **Transformada de Fourier**: Converte a imagem para o domínio da frequência para análise e manipulação de componentes de frequência.

- **Wavelets**: Oferece uma análise multi-resolução, útil em compactação e remoção de ruídos.

### **4. Morfologia**

Filtros morfológicos operam sobre a estrutura de uma imagem, geralmente binária, para remover ruídos ou destacar formas.

- **Erosão**: Reduz objetos pequenos ou ruídos isolados.

- **Dilatação**: Expande regiões de interesse.

- **Abertura**: Remove ruídos pequenos mantendo formas maiores.

- **Fechamento**: Preenche lacunas em objetos conectados.

Essa organização cobre aspectos fundamentais e avançados dos filtros em imagens digitais. Caso deseje aprofundar em algum tópico ou incluir exemplos práticos em Python, posso ajudar.
