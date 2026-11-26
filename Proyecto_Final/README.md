# Proyecto final: asistente RAG de Los Angeles Lakers

## ¿De qué trata?

Un asistente de inteligencia artificial que responde preguntas sobre los
jugadores de **Los Angeles Lakers en la temporada 2026-2027**, usando la
técnica **RAG**.

## Problema

- Para saber algo de un jugador hay que consultar varias páginas.
- Una IA convencional puede inventar datos o equivocarse sin decir de dónde
  saca la información.

## Solución

- Una base de conocimiento de **7 documentos**: la plantilla del equipo y
  fichas detalladas de **6 jugadores**.
- La IA consulta esos documentos antes de responder y **muestra de dónde
  obtuvo cada dato**.
- Si no encuentra el dato, **indica que no tiene suficiente información** en
  lugar de inventarlo.

## ¿Cómo funciona RAG?

RAG significa **generación aumentada por recuperación**:

1. **Recuperar:** se busca la información relevante en nuestros documentos.
2. **Generar:** esa información se le da a la IA para que redacte una
   respuesta fundamentada y con citas.

## Fuentes de información disponibles

| Fuente | Información que podemos obtener | Método |
|---|---|---|
| [NBA.com](https://www.nba.com) | Plantilla oficial, posiciones, estadísticas y trayectoria | API no oficial |
| [Basketball Reference](https://www.basketball-reference.com) | Estadísticas históricas, récords y rendimiento por temporada | HTML, sujeto a permisos |
| [RealGM](https://basketball.realgm.com) | Traspasos, draft, trayectoria y estadísticas | HTML |
| [Spotrac](https://www.spotrac.com/nba/) | Salarios, contratos y agentes libres | HTML |
| [BALLDONTLIE](https://www.balldontlie.io) | Jugadores, equipos, partidos y estadísticas | API JSON |
| [Wikidata](https://www.wikidata.org) | Biografías, nacionalidades, premios y datos personales | API JSON / SPARQL |
| [Lakers oficial](https://www.nba.com/lakers) | Noticias, entrevistas y comunicados oficiales | HTML |

> **Nota:** el corpus actual (los 7 documentos) se redactó a partir de
> artículos de **Wikipedia** en español e inglés (licencia CC BY-SA 4.0). Las
> fuentes de la tabla son opciones para ampliar o verificar la información.

## Tecnologías

Streamlit (interfaz) · FastAPI (API) · ChromaDB (base de vectores) ·
Google AI / Gemini (embeddings y respuestas)
