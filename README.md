# ESLint Básico - Projeto Exemplo

Exemplo de configuração do ESLint - http://eslint.org

## Setup

Instalar dependências:

```
npm install
```

Executar o ESLint:

linha de comando:

```
./node_modules/.bin/eslint *.js
```

script NPM:

```
npm run lint
```

Gulp:

```
gulp lint
```

## Instalar o ESLint em um projeto

Adicionar a dependência:

```
npm i --save-dev eslint
```

Inicializar o arquivo de configuração (.eslintrc.json ou .eslintrc.js):

```
./node_modules/.bin/eslint --init
```

e responder as perguntas para criar a configuração inicial.

## Script NPM ou task Gulp

### Script NPM

Adicionar no package.json, seção "scripts":

```
"lint": "eslint *.js"
```

### Task Gulp

Adicinar plugin:

```
npm i --save-dev gulp-eslint
```

Adicionar task no gulpfile.js:

```javascript
var gulp = require('gulp')
var eslint = require('gulp-eslint')
  
gulp.task('lint', function () {
  return gulp.src('*.js')
    .pipe(eslint())
    .pipe(eslint.format())
    .pipe(eslint.failAfterError())
})
```
