# apply vitest to new nestjs-app

## step

1. write "vitest.config.e2e.ts", "vitest.config.ts"

2. change "package.json" test scripts

3. npm i vitest @vitest/ui @vitest/coverage-v8 --save-dev (version should be compatibility)

4. npm i unplugin-swc --save-dev

## handle error

- error: "Error: unknown variant `ES2021`, expected one of `es3`, `es5`, `es2015`, `es2016`, `es2017`, `es2018`, `es2019`, `es2020`, `es2021`, `es2022`, `esnext` at line 1 column 263"

change tsconfig.json { "compilerOptions": { "target": "ES2021" -> "es2021" }}

- error: "test/app.e2e-spec.ts > AppController (e2e) > / (GET)
  TypeError: **vite_ssr_import_1** is not a function"

change "import \* as request from 'supertest';" -> import request from 'supertest';
