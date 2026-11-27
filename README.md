# 🦍 Wi-Fi Grátis — Pegadinha do QR Code

Uma página web interativa criada para ser usada como pegadinha ("troll") através de QR Codes impressos. Quando alguém escaneia o código esperando acessar uma rede Wi-Fi gratuita, é redirecionado automaticamente para uma tela cheia com a imagem de um gorila fazendo gesto obsceno, acompanhada de efeitos visuais e táteis para surpreender a vítima.

---

## 🎯 Como Funciona a Pegadinha

1. Você hospeda este projeto online (ex: GitHub Pages, Vercel, Netlify).
2. Gera um **QR Code** apontando para o link do site.
3. Imprime o QR Code com um aviso chamativo (ex: *"Escaneie para conectar no Wi-Fi Grátis"*) e cola em um local visível.
4. Assim que a pessoa aponta a câmera e abre o link, a página dispara automaticamente todos os efeitos de impacto.

---

## ✨ Funcionalidades e Efeitos

* **Isca no Título:** A aba do navegador exibe *"Wi-Fi Grátis - Acesso Livre"* para manter o disfarce até o carregamento.
* **Flash na Tela:** Um clarão branco imediato (`flash-bang`) assim que a página abre.
* **Tremor (Screen Shake):** A tela inteira vibra intensamente por 2 segundos para causar susto.
* **Vibração no Celular:** Utiliza a API `navigator.vibrate` para fazer o smartphone vibrar em duas rodadas de pulsos fortes (compatível com dispositivos Android).
* **Chuva de Confetes:** Dispara 60 partículas coloridas animadas em duas ondas.
* **Texto de Impacto:** Exibe a palavra **"TROUXA!"** com animação de salto e contorno neon vermelho posicionada sobre a imagem.
* **Bloqueio de Gestos Mobile:** Impede zoom, rolagem e o efeito de "elástico" (`overscroll`) no celular para prender a atenção na tela.

---

## 📁 Estrutura de Pastas

Para que a imagem de fundo funcione corretamente, mantenha a seguinte organização de arquivos:

```text
├── index.html          # Código principal da página (HTML, CSS e JS)
├── README.md           # Documentação do projeto
└── imagem/
    └── gorila.png      # Imagem do gorila exibida em tela cheia
```

> **Nota:** Certifique-se de que o arquivo da imagem se chame exatamente `gorila.png` e esteja dentro da pasta `imagem/`, caso contrário a tela ficará apenas preta.

---

## 🚀 Como Usar / Hospedar

### 1. Testando Localmente
Basta abrir o arquivo `index.html` diretamente em qualquer navegador ou usar a extensão **Live Server** no VS Code.

### 2. Colocando no Ar (Gratuito)
Para que o QR Code funcione no celular de outras pessoas, o site precisa estar na internet:
1. Crie um repositório no **GitHub** e envie o `index.html` e a pasta `imagem/`.
2. Vá em **Settings > Pages** no repositório e ative o **GitHub Pages** na branch `main`.
3. Copie o link gerado (ex: `https://github.io`).
4. Use qualquer gerador de QR Code gratuito na internet para transformar esse link em uma imagem imprimível.

---

## 🎨 Personalização Rápida

* **Posição do texto:** No CSS, dentro da classe `.troll-overlay`, altere o valor de `padding-top: 40vh;` para subir ou descer o texto *"TROUXA!"* conforme o enquadramento da sua imagem.
* **Mensagem:** Altere o texto dentro de `<div class="troll-text">TROUXA!</div>` para a palavra ou frase que preferir.

---

## ⚠️ Aviso

Este projeto foi desenvolvido exclusivamente para fins de entretenimento e humor entre amigos. Utilize com bom senso.
