# 🚀 APICatalogo com ASP.NET Core

Nesta semana, coloquei a mão na massa e desenvolvi uma API simples — mas muito útil — para gerenciar **produtos** e **categorias**.  
O objetivo? Praticar os fundamentos da construção de uma API RESTful usando **ASP.NET Core** com **Entity Framework Core**.

---

## 📦 Funcionalidades

Implementei os endpoints básicos para duas entidades:

- ✅ **Categorias**
- ✅ **Produtos**

Com suporte a operações completas:

- `GET` - Listar todos e buscar por ID
- `POST` - Cadastrar novos registros
- `PUT` - Atualizar informações existentes
- `DELETE` - Remover registros

---

## 🔧 Tecnologias utilizadas

- ASP.NET Core (Web API)
- Entity Framework Core
- SQL Server (via DbContext)
- Anotações de validação com `DataAnnotations`

---

## 🧩 Estrutura do projeto

- Controllers organizando as rotas:
  - `CategoriasController`
  - `ProdutosController`
- Models com validações:
  - `Categoria`
  - `Produto`
- Relacionamento 1:N (uma categoria pode ter vários produtos)
- Uso de rotas nomeadas para facilitar o retorno de recursos criados

### Exemplo de rota com `CreatedAtRoute`:

```csharp
return new CreatedAtRouteResult("ObterProduto", new { id = produto.ProdutoId }, produto);
