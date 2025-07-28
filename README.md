# Backend E2E QA Testing 
Este repositorio contiene un conjunto de pruebas E2E (end-to-end) diseñadas para validar los endpoints del backend del sistema de clientes. Las pruebas fueron desarrolladas utilizando **Postman** y ejecutadas con **Newman**, generando reportes en formato HTML para facilitar el análisis de resultados.

##  Contenido del repositorio

Archivo                                                        
`reporte_final.json`= Colección de pruebas en formato Postman        
`reporte_final.env.json` = Entorno de variables para la colección Postman 
`reporte_backend.html` = Reporte en formato HTML generado por Newman    
`.gitignore`= Archivos y carpetas excluidos del repositorio  
`package.json` / `package-lock.json` = Configuración de dependencias de Node.js       


## Tecnologías utilizadas

- [Postman](https://www.postman.com/)
- [Newman](https://www.npmjs.com/package/newman)
- [Newman HTML Reporter](https://www.npmjs.com/package/newman-reporter-html)
- Node.js



## ¿Cómo ejecutar las pruebas?
### 1. Instalar dependencias

```bash
npm install

npx newman run reporte_final.json -e reporte_final.env.json -r html --reporter-html-export reporte_backend.html

## Notas
- Se ha configurado .gitignore para excluir la carpeta node_modules y otros archivos innecesarios del repositorio
- El proyecto está orientado a validar flujos como: login, consulta de clientes, creación, actualización y eliminación de clientes.
