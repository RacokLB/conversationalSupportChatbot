🤖 Conversational SupportChatBot (RAG + Ollama + n8n)

🚀 Optimización de Soporte para Seguros Médicos mediante IA y Automatización
Este repositorio contiene un flujo de trabajo (workflow) avanzado desarrollado en n8n que implementa un Agente de IA conversacional diseñado para gestionar consultas sobre pólizas de seguros médicos del Consejo Nacional Electoral (CNE).

📋 Descripción del Proyecto
El sistema utiliza una arquitectura de Generación Aumentada por Recuperación (RAG) para garantizar que las respuestas del bot no solo sean naturales, sino técnicamente precisas y basadas exclusivamente en la documentación oficial de la póliza.

🛠️ Stack Tecnológico
Orquestador: n8n.

IA Local: Ollama (Modelo Llama 3.1:8b).

Base de Datos Vectorial: Supabase (Vector Store).

Procesamiento de Texto: Recursive Character Text Splitter.

Embeddings: bge-m3:567m (para alta eficiencia en búsquedas relacionales).

Canales: Telegram (Interfaz de usuario) y Google Drive (Ingesta de documentos).

⚙️ Características Principales
Arquitectura RAG (Retrieval-Augmented Generation): El bot consulta una base de datos de vectores en Supabase para recuperar fragmentos relevantes de la póliza antes de generar una respuesta, eliminando alucinaciones.

Procesamiento de Documentos Automático: Incluye un disparador de Google Drive que detecta nuevos archivos PDF, los fragmenta (chunking) y los indexa automáticamente en la base de datos vectorial.

Memoria Contextual: Implementación de nodos de memoria para mantener el hilo de la conversación y entender referencias previas del usuario.

Escalamiento Inteligente (Human-in-the-loop): Lógica condicional (If/Switch) integrada para detectar errores de salida o consultas complejas, notificando automáticamente a un agente humano vía Telegram.

Privacidad y Costo: Al utilizar Ollama de forma local, el sistema garantiza la privacidad de los datos sensibles de los trabajadores y reduce a cero los costos de tokens por inferencia.

🛠️ Configuración e Instalación
n8n: Importa el archivo .json incluido en este repositorio.

Ollama: Asegúrate de tener Ollama corriendo localmente con los modelos llama3.1 y el modelo de embeddings configurado.

Supabase: Crea una tabla de vectores y configura tus credenciales en el nodo de Supabase Vector Store.

Telegram: Crea un bot a través de @BotFather y añade el token en el nodo "Telegram Trigger".

Google Drive: Configura las credenciales de Google Cloud para la ingesta de documentos.

📊 Impacto y Resultados
Disponibilidad: Soporte técnico y administrativo 24/7.

Eficiencia: Reducción del tiempo de respuesta para consultas de cobertura médica de minutos a segundos.

Fiabilidad: Reducción de errores de interpretación mediante el uso de embeddings relacionales para búsquedas precisas.

Desarrollado por: Victor Batista
Full Stack & Automation Engineer especializado en optimización de procesos.
