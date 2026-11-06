# MeuFinanceiro PWA — teste iPhone

Protótipo web instalável inspirado na beta Android 0.6 Debug 3. O ZIP Android original **não foi alterado**. Não é conversão binária de Java/Android: é uma implementação web separada com funções equivalentes para teste.

## Publicar e instalar

1. Extraia o ZIP.
2. Publique **todo o conteúdo da pasta**, mantendo a estrutura, em uma hospedagem HTTPS estática (por exemplo, GitHub Pages ou Netlify). Não envie arquivos com dados pessoais.
3. Abra o endereço HTTPS no **Safari do iPhone**.
4. Compartilhar → Adicionar à Tela de Início → Adicionar.
5. Abra pelo ícone instalado. Depois da primeira carga, o service worker permite abrir sem rede em condições normais.

**Abrir `index.html` diretamente como arquivo não é suficiente para instalar o PWA.** Este pacote não contém link hospedado nem aplicativo IPA.

## Funcionalidades de teste

- Abas Início, Movimentações, Cartões, Histórico e Ajustes.
- Saldo, entradas, saídas, contas pendentes e faturas.
- Débito, crédito, conta pendente, parcelas distribuídas em meses e total ajustado com juros.
- Cartões com limites, barra de utilização e pagamento integral da fatura do mês com débito ou outro cartão.
- Conciliação do saldo, saldo inicial, backup JSON e importação manual.
- Dados somente no armazenamento local do navegador/dispositivo; nenhuma sincronização.

## Limitações importantes

- **Não há widget nativo de iOS.**
- Por padrão, a primeira parcela cai no mês seguinte; há escolha manual de mês atual ou +2 meses. O fechamento cadastrado é informativo nesta versão, ainda não calcula automaticamente a data da primeira fatura.
- Pagamento integral da fatura corrente; sem pagamentos parciais ou estornos automáticos.
- Dados de Android não são importados automaticamente.
- `localStorage` pode ser limpo pelo usuário ou pelo sistema. Faça backup JSON com frequência e evite navegação privada.
- O pacote passou por verificação sintática do JavaScript e validação de arquivos, **não por teste real em iPhone**.
- Teste com valores fictícios antes de usar como registro financeiro definitivo.
