# 📦 Plantilla Backend — Chatbot CV

Plantilla limpia con la estructura de **arquitectura hexagonal** lista para empezar a desarrollar.

## 🚀 Cómo correrlo

```bash
./gradlew bootRun
```

El servidor levanta en `http://localhost:8081`

## ✅ Probar que funciona

Hay un endpoint de prueba para verificar que el backend está vivo:

```
GET http://localhost:8081/api/hola
```

Debería responder: **"¡Hola Mundo! El backend está funcionando 🚀"**

## 📁 Estructura

```
src/main/java/com/chatbot/
│
├── ChatbotApplication.java              ← Punto de entrada
│
├── dominio/                              ← 🟢 Capa de dominio (vacía)
│   ├── modelo/                          
│   └── puerto/
│       ├── entrada/                     
│       └── salida/                      
│
├── aplicacion/                           ← 🟡 Capa de aplicación (vacía)
│   └── servicio/                        
│
└── infraestructura/                      ← 🔴 Capa de infraestructura
    ├── adaptador/
    │   ├── cliente/                     
    │   └── controlador/
    │       ├── ControladorPrueba.java   ← Controlador de prueba
    │       └── dto/                     
    └── configuracion/                   
```

## 📝 Próximos pasos

1. Crear el modelo `Mensaje` en `dominio/modelo/`
2. Crear el puerto de entrada `CasoUsoChatbot` en `dominio/puerto/entrada/`
3. Crear los puertos de salida en `dominio/puerto/salida/`
4. Implementar el servicio en `aplicacion/servicio/`
5. Implementar los adaptadores en `infraestructura/adaptador/`
6. Configurar Spring Security (CORS) en `infraestructura/configuracion/`

## 🛠️ Stack

- Java 21
- Spring Boot 3.3.5
- Spring WebFlux (reactivo)
- Spring Security
- Lombok
- Gradle
