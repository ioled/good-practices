# Buenas prácticas de desarrollo en iOLED

## Control de versiones (Git)

Utilizamos git para el control de versiones junto con [Github](https://github.com/ioled)

### **Commits**

Los mensajes de los commit están basados en [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) y deben ser de la 
siguiente forma:

- Siempre en inglés
- Parten con la forma de: **tipo**, un **contexto** y una **descripción**

```
tipo(contexto): descripción
```

### **Tipo**

Los tipos nos ayudan a clasificar los commits y a hacer más fácil la búsqueda en caso de que algo salga mal. Los tipos más usados en iOLED son:

- **feat**: Nueva feture
- **fix**: La correción de un bug
- **docs**: Cambios en la documentación
- **style**: Cambios en el estilo

### **Contexto**

El contexto hace referencia al lugar del código o funcionalidad que afecta el commit. Se escribe usando kebab-case.

### **Descripción**

- sin punto (.) al final
- sin mayuscula al principio

### Ejemplo

Como ejemplo de estas recomendaciones el siguiente commit soluciona un bug en el método *applyLedConfig* en el firmware de la aplicación, en el cual no se estaba apagando el LED al aplicar porcentaje 0.

```
fix(applyLedConfig): fix problem when set percent in 0

The 'applyLedConfig' method don't turn off the LED when set percent in 0.

This commits add validation when set percen in 0.
```

--- 

### Branches y Pull-requests

Los fatures se hacen en un nuevo branch y hacemos un pull request hacia develop.

