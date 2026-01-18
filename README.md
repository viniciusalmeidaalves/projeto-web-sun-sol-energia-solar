# Sun Sol Energia Solar — Site Corporativo

Resumo rápido
------------
Aplicação web responsiva para apresentação de soluções em energia solar fotovoltaica, com páginas segmentadas por público-alvo (residência, empresa, fazenda), galeria de projetos e formulário de orçamento com PHPMailer.

Tecnologias
----------
- Frontend: HTML5, CSS3, JavaScript (jQuery, Bootstrap 4, Owl Carousel, AOS)  
- Backend: PHP 7+ (estruturado com PHPMailer para envio de emails)  
- Banco: MySQL / MariaDB (configurado em php/php.ini)  
- Dependências: PHPMailer, Composer, Bootstrap, Owl Carousel, jQuery UI
- Validação: reCAPTCHA (opcional)

Arquitetura geral
-----------------
- Entrada pública: index.html + páginas temáticas (empresa, projetos, orçamento)  
- Backend de processamento: php/orcamento.php (formulário de contato/orçamento)  
- Camada de email: php/class.phpmailer.php para envio de mensagens  
- Assets organizados por tipo: css/ (estilos), js/ (scripts), images/ (mídia)  
- Configuração PHP: php/php.ini (limites de tamanho, extensões)  
- OAuth2 (opcional): php/get_oauth_token.php (autenticação Google)

Principais arquivos e símbolos
------------------------------
- Homepage: index.html — apresentação geral com call-to-action  
- Segmentação por público:
  - parasuacasa.html — soluções para residências  
  - parasuaempresa.html — soluções corporativas  
  - parasuafazenda.html — soluções rurais  
- Institucional: empresa.html (sobre a empresa, parceiros)  
- Portfólio: projetos.html (galeria de projetos realizados)  
- Orçamento: orcamento.html (formulário de contato) → php/orcamento.php (processamento)  
- Estilos: css/style.css (custom), css/bootstrap.min.css (framework)  
- Scripts: js/main.js (lógica customizada), bibliotecas (AOS, FancyBox, Owl Carousel)  
- Email: php/class.phpmailer.php, php/PHPMailerAutoload.php

Fluxo de dados resumido
-----------------------
1. Usuário navega por index.html ou páginas temáticas  
2. Clica em "Solicitar Orçamento" → orcamento.html  
3. Preenche formulário (dados de contato, consumo, localização)  
4. Formulário envia para php/orcamento.php via POST  
5. Backend valida dados e utiliza php/class.phpmailer.php para:
   - Enviar email ao cliente (confirmação)  
   - Enviar email interno (nova solicitação para sales/suporte)  
6. Resposta retorna ao frontend com status (sucesso/erro)

## 🖼 Prévia do Projeto 
*Página inicial do projeto Sun Sol
![image](https://github.com/user-attachments/assets/aa2cfd87-ed05-4f50-9b23-1f3c78ec5d2e)

## 📁 Acesso ao projeto
1. [visualizar o projeto na web](https://projeto-web-sun-sol-energia-solar-q.vercel.app/)
