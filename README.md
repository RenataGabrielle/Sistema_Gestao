
# Sistema de Gestão - E-commerce de Skin Care

Este projeto é um sistema de gestão para um e-commerce de produtos de skin care, desenvolvido em Java utilizando Swing para a interface gráfica. Ele permite aos usuários visualizar produtos, gerenciar um carrinho de compras, registrar clientes e finalizar compras.

<img src ="https://github.com/RenataGabrielle/TrabalhoFinal-LP_POO/assets/163059025/27ed2e99-006f-40df-80ac-5488920c6a00" >


## Estrutura do Projeto

```
sistema-gestao/
├── src/
│   ├── model/
│   │   ├── Produto.java
│   │   ├── Cliente.java
│   │   ├── Funcionario.java
│   │   ├── Pagamento.java
│   │   ├── Pedido.java
│   │   ├── Venda.java
│   │   ├── Financeiro.java
│   │   ├── Estoque.java
│   │   ├── Fornecedor.java
│   │   ├── Usuario.java
│   ├── dao/
│   │   ├── DatabaseConnection.java
│   │   ├── ProdutoDAO.java
│   │   ├── ClienteDAO.java
│   │   ├── FuncionarioDAO.java
│   │   ├── PagamentoDAO.java
│   │   ├── PedidoDAO.java
│   │   ├── VendaDAO.java
│   │   ├── FinanceiroDAO.java
│   │   ├── EstoqueDAO.java
│   │   ├── FornecedorDAO.java
│   │   ├── UsuarioDAO.java
│   ├── ui/
│   │   ├── TelaPrincipal.java
│   │   ├── TelaLogin.java
│   │   ├── TelaCadastro.java
│   │   ├── TelaCarrinho.java
│   │   ├── TelaPagamento.java
│   │   ├── Main.java
│   ├── utils/
│   │   ├── Carrinho.java
└── pom.xml (se estiver usando Maven)
```

## Funcionalidades

### Tela Principal (Vitrine de Produtos)

- Exibe uma vitrine de produtos de skin care com imagem, descrição e preço.
- Permite adicionar produtos ao carrinho de compras.

### Tela de Login

- Permite que os usuários façam login no sistema.

### Tela de Cadastro

- Permite que novos usuários se registrem no sistema.

### Tela do Carrinho de Compras

- Lista os produtos adicionados ao carrinho.
- Exibe o preço total.
- Permite finalizar a compra ou voltar à vitrine.

### Tela de Pagamento

- Permite selecionar o método de pagamento (boleto, Pix, cartão de crédito, cartão de débito).
- Finaliza a compra.

## Configuração do Banco de Dados

Certifique-se de configurar o banco de dados corretamente. Atualize o arquivo `DatabaseConnection.java` com as credenciais do seu banco de dados:

```java
package dao;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class DatabaseConnection {
    private static final String URL = "jdbc:mysql://localhost:3306/sistema_gestao";
    private static final String USER = "root";
    private static final String PASSWORD = "password";

    public static Connection getConnection() throws SQLException {
        return DriverManager.getConnection(URL, USER, PASSWORD);
    }
}
```

## Executando o Projeto

1. Clone este repositório.
2. Importe o projeto em sua IDE preferida.
3. Configure a conexão com o banco de dados no arquivo `DatabaseConnection.java`.
4. Execute a classe `Main.java` para iniciar o sistema.

## Exemplo de Diagrama de Classe

<img src="https://github.com/RenataGabrielle/IsaeRenata/assets/163059025/149c1506-6e10-4f85-940b-641f84cd96f3"> 

## Contribuição

Para contribuir com este projeto:

1. Faça um fork deste repositório.
2. Crie uma nova branch (`git checkout -b feature/sua-feature`).
3. Commit suas mudanças (`git commit -am 'Adiciona nova feature'`).
4. Push para a branch (`git push origin feature/sua-feature`).
5. Crie um novo Pull Request.

