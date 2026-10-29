# Projeto_Caldora
O **Projeto Caldora** é uma iniciativa sem fins lucrativos focada no aprendizado e na evolução prática. Nosso objetivo é criar e colaborar em projetos de desenvolvimento, transformando teoria em conhecimento real enquanto construímos juntos!

## Direitos Autorais e Licença

Este projeto é distribuído sob os termos que protegem a sua propriedade intelectual, permitindo a colaboração e o aprendizado aberto, mas com restrições claras de uso:

Permissão de Aproveitamento Parcial: Você tem permissão para utilizar trechos isolados do código-fonte, elementos de estilização, componentes visuais ou lógicas específicas para ajudar na construção, melhoria ou estética de outros projetos educacionais ou pessoais.

Proibição de Cópia Completa: Não é permitida a cópia integral, redistribuição comercial ou clonagem de todo o repositório para a criação de serviços idênticos ou concorrentes sem autorização prévia.

Obrigação de Créditos: Qualquer reutilização de partes do código ou da interface deve obrigatoriamente incluir os créditos visíveis ao projeto original Caldora e aos seus autores iniciais.

## Sobre o Projeto

O Caldora resolve contas desde operações aritméticas simples até equações avançadas. Os cálculos e o reconhecimento de imagem funcionam inteiramente no navegador do usuário, para garantir total privacidade e velocidade instantânea.

## Principais Funcionalidades

#### Calculadora Básica:
Interface intuitiva semelhante à de smartphones, com suporte a sugestões de símbolos e funções.

#### Calculadora Avançada (Captura de Tela):
Permite selecionar uma área da tela (via Screen Capture API) para reconhecer expressões matemáticas instantaneamente através de OCR local (Tesseract.js), permitindo que o usuário revise e corrija a expressão antes do cálculo.

#### Catálogo de Fórmulas:
Lista de fórmulas matemáticas (como a de Bhaskara) acompanhadas de explicações simples e exemplos resolvidos passo a passo.

#### Histórico Local:
Armazenamento seguro e privado no navegador (via IndexedDB) para consulta rápida de contas anteriores, sem exigir login.

## Stack Tecnológica

O projeto foi construído priorizando alta performance, baixo consumo de recursos e execução 100% no cliente:

#### Back-End:
Python com Flask, servido por Gunicorn em produção. Responsável por servir as páginas e os arquivos estáticos.

#### Front-End:
HTML com Jinja2, JavaScript em módulos ES e Vite.

#### Estilização:
Tailwind CSS, compilado no build.

#### Renderização Matemática:
KaTeX.

#### Motor de Cálculo:
Math.js e Módulo de Resolução Determinística em JavaScript.

#### Reconhecimento de Imagem (OCR):
Tesseract.js compilado para WebAssembly (Wasm), executado em Web Worker.

#### Armazenamento:
IndexedDB (com idb) e LocalStorage, este último apenas para preferências.

#### Segurança e Desempenho:
Flask-Talisman, Flask-Compress e Flask-Limiter. O site também funciona como PWA, com service worker e manifesto.

## Privacidade e Segurança

O Caldora foi projetado sob a premissa de privacidade total:

As imagens capturadas para o reconhecimento de fórmulas são processadas na memória RAM do dispositivo e descartadas imediatamente, sem armazenamento permanente ou envio para servidores externos.

O histórico de navegação e cálculos permanece restrito ao armazenamento local do seu navegador, podendo ser apagado pelo usuário a qualquer momento.
