# learning-ruby

## Rails Generators

## Model

```bash
bin/rails g model User name:string age:integer
```

Cria:
- Model
- Migration
- Testes
- Fixtures

Arquivos comuns:

```plaintext
app/models/user.rb
db/migrate/xxxx_create_users.rb
```

## Controller

```bash
bin/rails g controller Products index show
```

Cria:
- Controller
- Views
- Helpers
- Testes
- Rotas

Arquivos comuns:

```plaintext
app/controllers/products_controller.rb
app/views/products/
```

---

## Mailer

```bash
bin/rails g mailer Product in_stock
```

Cria:
- Mailer
- Templates de email
- Preview
- Testes

Arquivos comuns:
```plaintext
app/mailers/product_mailer.rb
app/views/product_mailer/
```

---

## Migration

```bash
bin/rails g migration AddAdminToUsers admin:boolean
```

Cria:
- Apenas migration

Arquivos comuns:
```plaintext
db/migrate/xxxx_add_admin_to_users.rb
```

---

## Scaffold

```bash
bin/rails g scaffold Product name:string price:decimal
```

Cria:
- Model
- Migration
- Controller
- Views CRUD
- Rotas
- Testes

Arquivos comuns:
```plaintext
app/models/
app/controllers/
app/views/
db/migrate/
```

---

## Resource

```bash
bin/rails g resource Product name:string
```

Cria:
- Model
- Migration
- Controller
- Rotas

Menos completo que scaffold.

---

## Job

```bash
bin/rails g job SendEmail
```

Cria:
- Background job

Arquivos comuns:
```plaintext
app/jobs/send_email_job.rb
```

Uso:
```ruby
SendEmailJob.perform_later
```

---

## Channel

```bash
bin/rails g channel Chat
```

Cria:
- WebSocket channel
- Arquivos JS

Arquivos comuns:
```plaintext
app/channels/chat_channel.rb
app/javascript/channels/
```

---

## Helper

```bash
bin/rails g helper Products
```

Cria:
- Helper methods para views

Arquivos comuns:
```plaintext
app/helpers/products_helper.rb
```

---

## Concern

```bash
bin/rails g concern Trackable
```

Cria:
- Módulo reutilizável

Arquivos comuns:
```plaintext
app/models/concerns/
app/controllers/concerns/
```

---

## Stimulus

```bash
bin/rails g stimulus modal
```

Cria:
- Controller JavaScript Stimulus

Arquivos comuns:
```plaintext
app/javascript/controllers/modal_controller.js
```

---

## Authentication

```bash
bin/rails g authentication
```

Cria:
- Sistema básico de autenticação

Inclui:
- User model
- Sessions
- Password reset
- Login/logout

---

# Ver generators disponíveis

```bash
bin/rails g
```

---

# Ajuda de um generator

```bash
bin/rails g model --help

## Padrão RESTful ruby on rails

| Método HTTP | URL                | Action  |
| ----------- | ------------------ | ------- |
| GET         | /products          | index   |
| GET         | /products/new      | new     |
| POST        | /products          | create  |
| GET         | /products/:id      | show    |
| GET         | /products/:id/edit | edit    |
| PATCH/PUT   | /products/:id      | update  |
| DELETE      | /products/:id      | destroy |
