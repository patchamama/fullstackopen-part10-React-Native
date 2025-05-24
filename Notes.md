

### Inicializando la aplicación

```sh
# Instalar la interfaz de línea de comandos expo-cli
# Legacy > npm install --global expo-cli

# Inicializar nuestro proyecto en un directorio `rate-repository-app`
npx create-expo-app rate-repository-app --template expo-template-blank@sdk-50no 
cd rate-repository-app
npx expo install react-native-web@~0.19.6 react-dom@18.2.0 @expo/metro-runtime@~3.1.1
```

El paquete `Metro`es como webpack (javascript) o vite del ecosistema react native. 