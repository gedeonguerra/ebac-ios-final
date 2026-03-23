# EBAC iOS Tests - Módulo 29

Suíte de testes E2E para o app EBAC Store (iOS) usando WebdriverIO + Appium + SauceLabs.

## Fluxo testado

1. Login com credenciais válidas
2. Navegar para a aba Browse
3. Selecionar o primeiro produto da lista
4. Adicionar ao carrinho
5. Adicionar endereço (se não existir)
6. Ir para pagamento
7. Confirmar Cash on Delivery
8. Finalizar com Checkout
9. Validar tela "Order Success" com "Transaction successful!"

## Stack

- WebdriverIO v8
- Appium v2 + XCUITest
- SauceLabs (iOS Simulator)
- Mocha
- Page Object Model

## Como executar

### Pré-requisitos

1. Conta no [SauceLabs](https://saucelabs.com)
2. Upload do `LojaEBAC-sim.zip` em [App Management](https://app.saucelabs.com/app-management)
3. Criar arquivo `.env` na raiz do projeto:

```
SAUCE_USERNAME=seu-usuario
SAUCE_ACCESS_KEY=sua-access-key
```

### Instalação e execução

```bash
npm install
npm run test:sauce:ios
```

## Estrutura

```
ebac-ios-tests/
├── .env                          # Credenciais (não versionar)
├── .env.example                  # Modelo do .env
├── .gitignore
├── package.json
├── wdio.conf.js
└── test/
    ├── pageobjects/
    │   ├── login.page.js
    │   ├── home.page.js
    │   ├── product.page.js
    │   └── cart.page.js
    └── specs/
        └── checkout.spec.js
```
