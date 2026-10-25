# PayView

Plataforma de vendas de produtos digitais: criação de produtos, checkout, vendas, afiliados, área de membros (produtor e aluno), controle de acessos e financeiro.

> **Versão de demonstração.** Roda 100% no navegador (HTML, CSS e JavaScript puros), sem servidor. Os dados ficam salvos no `localStorage` de cada navegador. Não há pagamento real nem login seguro.

## Estrutura

```
payview/
├── index.html      # página principal
├── css/style.css   # estilos (tema claro e escuro)
├── js/app.js       # toda a lógica do app
├── .nojekyll
├── .gitignore
└── README.md
```

## Rodar no computador

Abra o `index.html` no navegador. Para um servidor local:

```bash
python3 -m http.server 8000
```

Depois acesse http://localhost:8000.

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex.: `payview`).
2. Envie os arquivos:
   ```bash
   git init
   git add .
   git commit -m "PayView: primeira versão"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/payview.git
   git push -u origin main
   ```
3. No repositório, abra **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`, e salve.
5. Em alguns minutos o site fica em `https://SEU-USUARIO.github.io/payview/`.

## Funcionalidades

- **Criar produto:** preço em R$ com máscara, tipo de acesso (vitalício, mensal, trimestral, anual ou prazo fixo), garantia, parcelas e formas de pagamento.
- **Checkout:** cor e botão personalizáveis, order bump, cupons; exige nome completo, idade e e-mail.
- **Vendas, Afiliados e Financeiro:** lista de transações, comissões por produto, saldo e saques.
- **Área de membros:** o produtor edita módulos e aulas e pode visualizar como aluno; o aluno entra com o e-mail da compra, assiste, conclui aulas, comenta e recebe certificado.
- **Acessos:** expiração automática, renovação automática (simulada), suspensão e edição da data por cliente.

## Próximos passos para produção

Para vender de verdade é preciso um backend com autenticação, banco de dados e um gateway de pagamento (Pix, cartão e boleto), além de hospedagem de vídeos.
