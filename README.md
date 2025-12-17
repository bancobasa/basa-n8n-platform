# Basa n8n Platform

Plataforma de automatización de workflows n8n para Banco Basa.

## 🛠️ Herramientas incluidas

- **n8n**: Plataforma de automatización de workflows de código abierto

## 🚀 Despliegue

Esta herramienta se despliega automáticamente via ArgoCD desde este repositorio.

## 📁 Estructura

```
└── apps/n8n/
    ├── Chart.yaml          # Helm chart wrapper
    ├── values.yaml         # Configuración de n8n
    └── templates/          # Templates adicionales (opcional)
└── applications/
    └── n8n.yaml           # ArgoCD Application
```

## 🔄 GitOps Flow

1. Cambios en este repo → GitHub
2. ArgoCD detecta cambios automáticamente  
3. Sincronización automática a Kubernetes
4. n8n actualizado en el cluster

## 📋 Configuración

n8n se configura con:
- **Chart Version**: 1.16.11 (community-charts)
- **App Version**: 2.0.2
- **Namespace**: n8n
- **Ingress**: n8n-testing.bancobasa.com.py
- **Persistence**: 10Gi (gp2)

## 🌐 Acceso

Una vez desplegado, n8n estará disponible en:
- **URL**: https://n8n-testing.bancobasa.com.py
- **Namespace**: n8n

## 🔧 Personalización

Para modificar la configuración, edita `apps/n8n/values.yaml` y haz commit. ArgoCD sincronizará automáticamente los cambios.
