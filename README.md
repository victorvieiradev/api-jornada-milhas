# Loja Online

Esta é uma representação do processo de compra em uma loja online, desde o início até a finalização do pedido.

## Fluxograma

```mermaid
graph TD;
    A(Início) --> B("Recebimento do Pedido");
    B --> C{"Pedido Completo?"};
    C -- Sim --> D("Validação do Estoque");
    D --> E{"Produtos Disponíveis?"};
    E -- Sim --> F("Validação do Pagamento");
    F --> G{"Pagamento Confirmado?"};
    G -- Sim --> H("Preparação do Pedido");
    H --> I("Envio do Pedido");
    I --> J(Fim);
    G -- Não --> K("Cancelar Pedido");
    K --> L(Fim);
    E -- Não --> M("Notificar Cliente");
    M --> N("Cancelar Pedido");
    N --> O(Fim);
    C -- Não --> P("Notificar Cliente");
    P --> N;
