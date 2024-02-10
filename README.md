# Loja Online

Esta é uma representação do processo de compra em uma loja online, desde o início até a finalização do pedido.

## Fluxograma

```mermaid
graph TD;
    A(Início) --> B("Usuário (Cliente)");
    B --> C{"Navegar pela Loja Online?"};
    C -- Sim --> D("Selecionar Produtos");
    D --> E{"Mais Produtos?"};
    E -- Sim --> D;
    E -- Não --> F{"Adicionar ao Carrinho?"};
    F -- Sim --> G("Finalizar Compra");
    G -->|Informações de Pagamento válidas?| H(Pagamento);
    H --> I("Realiza o Pagamento");
    I --> J("Confirmação do Pedido");
    J --> K(Fim);
    C -- Não --> L("Sair da Loja");
    L --> M(Fim);
    F -- Não --> N("Continuar Navegando");
    N --> C;
    G --> O{"Deseja Adicionar Outros Produtos?"};
    O -- Sim --> D;
    O -- Não --> P("Finalizar Compra");
    P --> H;
