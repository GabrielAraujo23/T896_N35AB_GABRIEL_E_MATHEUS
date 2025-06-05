# Detecção de Placas de Veículos (PDI)

Este repositório contém um Jupyter Notebook que demonstra um pipeline completo para:

1. **Alinhamento/Retoque de Placas Inclinadas**  
   - Uso de Canny para detecção de bordas  
   - Transformada de Hough (HoughLinesP) para identificar as linhas mais longas  
   - Cálculo do ângulo médio e rotação da imagem para “alinhar” a placa  

2. **Segmentação (Crop) da Placa**  
   - Conversão para tons de cinza, blur(Filtro Gaussiano) e binarização (thresholding)  
   - Extração de contornos (`findContours`)  
   - Filtragem de retângulos pelo aspect‐ratio, área e posição para isolar a placa  
   - Corte (`crop`) da região correspondente à placa  

Além disso, há exemplos aplicados a **duas imagens de carro** para que você possa comparar resultados lado a lado.

---

## 🚀 Pré‐Requisitos

- **Python 3.7+**  
- **Jupyter Notebook** (ou JupyterLab)  
- Bibliotecas Python:
  - `opencv-python`
  - `numpy`
  - `matplotlib`

Você pode instalar todas as dependências de uma só vez com:
```bash
pip install opencv-python numpy matplotlib
