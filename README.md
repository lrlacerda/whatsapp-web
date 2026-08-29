# 💬 WhatsApp Web Clone

Clone de estudo da interface do **WhatsApp Web**, feito em **HTML, CSS e JavaScript puro** (sem frameworks ou build tools) para praticar layout, componentização de CSS e manipulação do DOM. É um projeto pessoal de aprendizado, sem qualquer vínculo com o WhatsApp/Meta — reproduz apenas a interface visual, com dados fixos de exemplo (não há envio real de mensagens nem backend funcional).

## Funcionalidades

- Layout de duas colunas nos moldes do WhatsApp Web: lista de conversas à esquerda e janela de conversa à direita
- Cabeçalho de perfil com foto, ícones de status, novo chat e menu
- Campo de busca de conversas (sem lógica de filtro implementada)
- Lista de contatos com foto, nome e horário da última mensagem
- Janela de conversa com mensagens enviadas/recebidas estilizadas de forma diferente (balões verdes e brancos)
- Campo de digitação de mensagem no rodapé da conversa
- Comportamento **responsivo**: em telas menores que 992px, tocar em um contato abre a tela de conversa em tela cheia, com botão de voltar para a lista

> Os arquivos `js/app.js` e `js/script.js` contêm um protótipo de tela de login com busca de usuários via `fetch` a uma API local (`http://localhost:5000/usuarios`), mas não estão referenciados em `index.html` e não fazem parte do fluxo atual da aplicação.

## Tecnologias

| Tecnologia | Uso |
|---|---|
| HTML5 | Estrutura da interface |
| CSS3 | Estilização e responsividade |
| JavaScript (vanilla) | Interação (abrir/fechar conversa no mobile) |
| Font Awesome | Ícones |
| Google Fonts (Barlow, Dosis) | Tipografia |

## Estrutura do projeto

```
index.html                  # Página principal
css/                          # Estilos globais
js/                            # Scripts de protótipo (não usados no index.html atual)
componentes/                    # Um CSS/HTML/JS por componente da interface
├── header/, headerperfil/       # Cabeçalhos
├── leftcol/, personitem/          # Lista de conversas
├── rightcol/, talkheader/          # Coluna e cabeçalho da conversa ativa
├── talkbox/, talkimessage/,         # Área de mensagens (recebidas/enviadas)
│   talkyoumessage/
├── talkfooter/                        # Campo de digitação
├── messagecontainer/, searchmessage/    # Container e busca de conversas
image/, fonts/                             # Assets estáticos
```

## Como executar

Não há dependências ou build — é um site estático. Basta abrir o `index.html` diretamente no navegador ou servir a pasta com um servidor estático simples, por exemplo:

```bash
npx serve .
# ou
python3 -m http.server
```
