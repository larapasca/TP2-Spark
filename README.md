# TP2 — Sistema de Recomendación de Música

Sistema de recomendación de artistas musicales usando ALS sobre el dataset Last.fm 360K.

**Grupo:** Lara Pascaretta - Agustina Kohan Miller - Stefania Ranucci
**Materia:** Analítica de Big Data con Spark 

---

## Cómo reproducir

**Entorno:** Google Colab (no requiere nada instalado localmente).

1. Abrir `TP_Recomendacion.ipynb` en Google Colab
2. Ejecutar todas las celdas de arriba a abajo
3. El dataset se descarga automáticamente desde Internet Archive (543MB)
4. El notebook completo tarda aproximadamente 3 horas en ejecutarse con runtime T4 (no tuvimos acceso a la GPU)

No hace falta descargar ni subir ningún archivo manualmente.

---

## Sección bonus (Sección 9)

La sección de recomendaciones personalizadas requiere una API key gratuita de Last.fm:

1. Crear cuenta en last.fm y generar una API key en last.fm/api/account/create
2. Al llegar a la celda 9.1, ingresar la key cuando aparezca el prompt (no queda guardada en el notebook)

---

## Dataset

**Last.fm 360K** — upf.edu/web/mtg/lastfm360k
- 359,349 usuarios, 160,168 artistas, 17,559,530 interacciones
- Subconjunto usado: 22,125 usuarios - 25,128 artistas - 809,540 interacciones

---

## Estructura del notebook

| Sección | Contenido |
|---------|-----------|
| 1–2 | Setup, descarga y configuración de Spark |
| 3 | EDA |
| 4 | Preprocesamiento, features, indexación, Parquet |
| 5 | Modelo ALS — hiperparámetros y curva de entrenamiento |
| 6 | Evaluación — Precision@10, Recall@10, NDCG@10, PCA |
| 7 | Limitaciones de ALS |
| 8 | Escalabilidad |
| 9 | Bonus — recomendaciones personalizadas vía API de Last.fm |
| 10 | Comparación ALS vs BPR |
