# Configuración del proyecto

1. Instala el paquete gh-pages como dependencia de desarrollo:
```
npm install gh-pages --save-dev
```

2. En el archivo vite.config.js, agrega la configuración de base:
```
export default defineConfig({
  plugins: [react()],
  base: '/nombre-de-tu-repositorio/'
})
```
Reemplaza "nombre-de-tu-repositorio" con el nombre real de tu repositorio en GitHub.
Para porfolio se recomienda que sea la raíz de tu perfil. Por lo que habría que poner base: ''
# Modificación del package.json
3. Añade los siguientes scripts en tu package.json:
```
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d dist"
}
```
Estos scripts automatizarán el proceso de build y deploy.

# Despliegue
Ejecuta el comando de deploy:
```
npm run deploy
```
Este comando construirá tu proyecto y lo publicará en la rama gh-pages de tu repositorio

# Configuración final en GitHub
4. Ve a la configuración de tu repositorio en GitHub.
5. En la sección "Pages", selecciona la rama "gh-pages" como fuente para GitHub Pages.
6. Espera unos minutos y tu aplicación estará disponible en:
https://tu-usuario.github.io/nombre-de-tu-repositorio/
