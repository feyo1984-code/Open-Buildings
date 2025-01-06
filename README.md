# Mapas de Kernel - Municípios Operados pela Sabesp

Este repositório contém os dados e a metodologia utilizada para criar mapas de Kernel para identificar áreas rurais adensadas no Estado de São Paulo, com foco nos municípios atendidos pela Companhia de Saneamento do Estado de São Paulo (Sabesp).

## Metodologia

A seguir, descrevemos a metodologia utilizada para gerar os mapas de Kernel e identificar as áreas rurais mais densamente povoadas:

### 1. Criação das ROIs (Regiões de Interesse)
- As camadas do Estado de São Paulo foram obtidas em formato Shapefile a partir do Sistema Nacional de Cadastro Ambiental Rural (SICAR).
- As áreas urbanas foram removidas utilizando a operação de Diferença Simétrica em ferramentas como QGIS ou ARCGIS Pro.
- Foi aplicada a ferramenta *Dissolve* para manter apenas as áreas rurais.

### 2. Recorte por Municípios Operados pela Sabesp
- As áreas rurais foram filtradas para selecionar somente os municípios operados pela Sabesp.

### 3. Extração de Vetores das Edificações
- Foi utilizado o Open Footprint Dataset no Google Earth Engine (GEE) para vetorizar as edificações nas áreas rurais atendidas pela Sabesp.

### 4. Centralização das Edificações
- Os centroides das edificações foram calculados utilizando QGIS ou ARCGIS Pro para análises espaciais.

### 5. Mapas de Kernel
- Mapas de Kernel foram gerados para criar mapas de calor, identificando áreas mais densamente povoadas.

### 6. Vetorização de Dados Contínuos
- Os dados contínuos dos mapas de Kernel foram transformados em dados discretos para permitir a classificação das áreas.

### 7. Identificação de Áreas Alvo
- Áreas com classificação próxima a 10 foram identificadas como zonas rurais densamente povoadas, prioritárias para a universalização do saneamento.

### 8. Delimitação de Áreas
- A Sabesp pode utilizar as classes-alvo para definir as zonas prioritárias para a implantação de projetos de saneamento.

