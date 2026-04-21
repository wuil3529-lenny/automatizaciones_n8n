# 06 - Generador de Copys para Telegram

Este flujo de n8n implementa un asistente avanzado de copywriting para Telegram, utilizando **Gemini 2.5 Flash** para la generación de contenido y detección de intenciones.

## Características Principales
- **Detección de Intenciones con IA**: El sistema analiza el lenguaje natural del usuario para determinar qué comando ejecutar.
- **Configuración Dinámica (/setup)**: Permite cargar un notebook de marketing desde Google Drive para extraer el estilo, tono y patrones de escritura del cliente.
- **Generación de Copys Personalizados (/copy)**: Crea contenido siguiendo exactamente el patrón extraído del cliente.
- **Planificación Diaria (/copy_hoy)**: Genera automáticamente el copy correspondiente al tema del día según el plan diario del cliente.
- **Persistencia en Supabase**: Guarda la información de los clientes y las estadísticas de los copys generados para seguimiento y análisis.

## Comandos Disponibles
- `/setup [file_id]` - Configura el perfil del cliente cargando un notebook desde GDrive.
- `/copy [tema]` - Genera un copy sobre un tema específico.
- `/copy_hoy` - Genera el copy programado para el día de hoy.
- `/stats` - Muestra estadísticas de uso y rendimiento.
- `/pattern` - Muestra el patrón de escritura extraído y activo.
- `/help` - Muestra la ayuda y comandos disponibles.
- `/reset` - Reinicia la configuración del usuario.

## Integraciones
- **Telegram Bot API**: Interfaz de usuario.
- **Google Gemini API**: Motor de inteligencia artificial.
- **Google Drive**: Almacenamiento de notebooks de referencia.
- **Supabase**: Base de datos para perfiles de clientes y métricas.
