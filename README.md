# Detección de Imágenes Sintéticas (IA vs. Real) mediante Descriptores Clásicos y Redes Convolucionales

**Asignatura:** Procesamiento de Imágenes Digitales (PID)  
**Titulación:** Grado en Ingeniería Informática - Tecnologías Informáticas  
**Institución:** Escuela Técnica Superior de Ingeniería Informática (ETSII) - Universidad de Sevilla  

---

## Descripción del Proyecto

Este repositorio contiene el código fuente, notebooks experimentales y scripts de evaluación de un estudio comparativo experimental centrado en la detección de imágenes generadas por Inteligencia Artificial frente a fotografías reales. 

El objetivo principal es analizar la evolución de la capacidad de detección y el equilibrio entre precisión técnica (*Accuracy, Precision, Recall, F1-Score*) y coste computacional a medida que aumentamos el nivel de abstracción sobre los datos, utilizando el dataset **CIFAKE** (100.000 imágenes RGB de 32×32 píxeles equilibradas entre capturas reales y síntesis de Stable Diffusion v1.4)[cite: 4].

---

## Metodología (3 Niveles Progresivos)

1. **Tier 1 — Baseline (Red Neuronal Densa / MLP):** Aplanamiento directo de la imagen en un vector unidimensional sin filtrado espacial previo para establecer la cota inferior de rendimiento[cite: 5].
2. **Tier 2 — PID Tradicional (HOG + LBP + SVM):** Extracción manual de características mediante histogramas de gradientes orientados (*HOG*) para estructura geométrica y patrones binarios locales (*LBP*) para micro-textura superficial, clasificados mediante una Máquina de Vectores de Soporte (*SVM*)[cite: 5].
3. **Tier 3 — Deep Learning (CNN):** Arquitectura de Red Neuronal Convolucional implementada en PyTorch donde los filtros de extracción espacial se aprenden automáticamente mediante retropropagación[cite: 6].

