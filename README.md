# YetzFlash — Gerenciar Plataforma (UX-673)

Protótipo interativo, em um único arquivo, do fluxo **Gerenciar Plataforma** do YetzFlash,
implementado a partir do design no Figma ([UX-673](https://www.figma.com/design/4SFJVoNr2LGVlMKDB4H1IP/YetzFlash?node-id=10919-4652)).

## Abrir

Abra [`flash.html`](flash.html) direto no navegador. Não há build nem dependências —
todos os assets (logos, ilustrações) estão embutidos em base64 e as fontes vêm do Google Fonts.

## O que está implementado

- **Seletor de tipo de configuração** — alterna entre *Modo de Manutenção* e *Termos e Condições*,
  trocando formulário e pré-visualização.
- **Modo de Manutenção**
  - Campos de início/fim, *Texto Padrão* × *Texto Personalizado* (habilita título + editor rich-text).
  - Barra de formatação (negrito, itálico, sublinhado, tachado, listas, link).
  - Pré-visualização Desktop e Mobile atualizando em tempo real (título, corpo, previsão de retorno).
- **Termos e Condições**
  - Versão vigente + links, upload de arquivo (validação de 5 MB, exibe nome/tamanho, botão de remover).
  - Justificativa com contador (mínimo 30 caracteres) que habilita *Publicar nova versão*.
  - Preview do modal de aceite (Desktop) e bottom sheet (Mobile), com scroll dos termos e checkbox.
  - Ao publicar, a "Versão vigente" é atualizada e o formulário é resetado.
- **Modal de confirmação** "Configurações salvas com sucesso" ao salvar/publicar.

## Estrutura

- `flash.html` — build final, self-contained (assets em base64). É o arquivo para abrir.
- `flash.template.html` — fonte com placeholders `%%ASSET%%`; os assets são injetados na geração do build.
