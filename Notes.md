

### Inicializando la aplicación

```sh
# Instalar la interfaz de línea de comandos expo-cli
# Legacy > npm install --global expo-cli

# Inicializar nuestro proyecto en un directorio `rate-repository-app`
npx create-expo-app rate-repository-app --template expo-template-blank@sdk-53
cd rate-repository-app
npx expo install react-native-web@~0.19.6 react-dom@18.2.0 @expo/metro-runtime@~3.1.1

# Upgrade sdk a versión 53 en caso de tener una versión más antigua
npx expo install expo@latest
npx expo install expo@^53.0.0

# Inicializar Metro Bundler y visitar en navegador la url: 
npm start
```

El paquete `Metro`es como webpack (javascript) o vite del ecosistema react native. 

### ESLint

Crear archivo de configuración [eslint.config.mjs](./rate-repository-app/eslint.config.mjs)

```sh
npm install --save-dev eslint @babel/eslint-parser eslint-plugin-react eslint-plugin-react-native
```

> [!WARNING] 
> Solo sí no existe el archivo de configuración eslint.config.mjs y sí se desea crear este a partir del archivo de configuración [.eslintrc.json](./rate-repository-app/.eslintrc.json).
> 
> La última version de ESLint no soporta .eslint.json configuración, por lo que es necesario migrar este (https://eslint.org/docs/latest/use/configure/migration-guide):
> 
> ```
> npm install @eslint/js @eslint/eslintrc -D
> npx @eslint/migrate-config .eslintrc.json 
> ```


Agregar la línea: `"lint": "eslint ./src/**/*.{js,jsx} App.js --no-error-on-unmatched-pattern"` en la sección de los `scripts` del archivo `package.json` 

### Debugging

```sh
npx react-devtools
```

Refs: 

- https://reactnative.dev/docs/debugging#accessing-the-in-app-developer-menu
- https://docs.expo.dev/debugging/runtime-issues/


