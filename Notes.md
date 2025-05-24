

### Inicializando la aplicación

```sh
# Instalar la interfaz de línea de comandos expo-cli
# Legacy > npm install --global expo-cli

# Inicializar nuestro proyecto en un directorio `rate-repository-app`
npx create-expo-app rate-repository-app --template expo-template-blank@sdk-50no 
cd rate-repository-app
npx expo install react-native-web@~0.19.6 react-dom@18.2.0 @expo/metro-runtime@~3.1.1

# Inicializar Metro Bundler y visitar en navegador la url: 
npm start
```

El paquete `Metro`es como webpack (javascript) o vite del ecosistema react native. 

### ESLint

```sh
npm install --save-dev eslint @babel/eslint-parser eslint-plugin-react eslint-plugin-react-native

# La última version de ESLint no soporta .eslint.json configuración, por lo que es necesario migrar este (https://eslint.org/docs/latest/use/configure/migration-guide):
npm install @eslint/js @eslint/eslintrc -D
npx @eslint/migrate-config .eslintrc.json 
```

### Debugging

```sh
npx react-devtools
```

Refs: 

- https://reactnative.dev/docs/debugging#accessing-the-in-app-developer-menu
- https://docs.expo.dev/debugging/runtime-issues/


