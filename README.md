## Teste Liberfly

O projeto possui docker mas pode ser iniciado diretamente pelo serve do artisan.

Preencha os dados no .env local para criar o banco e dados

Faça a instalação do composer e npm

```bash
composer install
npm install
```

Rode o seed para ter uma base de teste
### Seed
```bash
php artisan migrate --seed
```

### Formas de iniciar o projeto

### Docker

```bash
// construir a imagem
docker build -t liberflydocker . 

// iniciar o container
docker run -p 80:80 liberflydocker
```

### Artisan
```bash
php artisan serve
```

### PEST

Estou utilizando o PEST para realizar os testes. Criei alguns metodos de testes de integração com dados fake do factory. 
Teste em autenticação, perfil, jogador e time. Apenas para exemplificar algumas habilidades.

Verifique os testes na pasta test/Feature

```bash
./vendor/bin/pest
```

### POSTMAN
O collection e o environment estão na raiz do projeto, para testar via API também.

### OBSERVAÇÕES E CONSIDERAÇÕES
- Decidi adicionar um diagrama de entidade relaciomento para facilitar a visualização da modelagem do banco usando o **[mermaid](https://mermaid.js.org/)**;

- O projeto roda no docker usando o nginx;

- Utilizei a autenticação para o usuário que controlará o CRUD do sistema;

- O site possui um seed para começar os testes;

- O site está responsivo;

- UTilizei o framework **[tailwindcss](https://tailwindcss.com/)** paa o front;