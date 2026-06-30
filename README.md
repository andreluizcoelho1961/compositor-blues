# Estúdio de Composição de Blues

Conjunto de agentes de IA para composição, crítica e produção de blues — do brainstorm à cifra final.

## Agentes

### `compositor-blues`
Compositor de blues afro-americano do pós-guerra. Conversa em português para brainstormar ideias e compõe letras originais em inglês, no espírito de Lil' Son Jackson, Muddy Waters, Jimmy Rogers e Magic Sam. Tem memória persistente entre sessões — trata cada conversa como parte de uma parceria criativa contínua.

### `critico-blues`
Estudioso da tradição do blues que avalia letras com honestidade e respeito. Analisa estrutura AAB, autenticidade temática, uso de metáfora e coerência narrativa — citando trechos específicos ao comentar.

### `suno-prompt`
Transforma letras compostas em prompts prontos para o Suno AI (plano Premier). Gera três saídas: Style Prompt, Lyrics formatadas com tags de seção, e Notas para o Studio com sugestões de pós-produção, stems para exportar e lembrete de exportação MIDI.

### `cifra-blues`
Gera cifras em formato brasileiro com extensões (C7, Am7, F7+, C7(13), D7/F#) a partir do MIDI exportado pelo Suno Studio. Organiza a cifra por seção, alinhada com a letra, e inclui observações harmônicas para os músicos.

## Fluxo de trabalho

```
compositor-blues → critico-blues → suno-prompt → cifra-blues
     ↓                  ↓               ↓              ↓
 letra.md          revisão         prompt Suno      cifra.md
```

1. **Composição** — brainstorm com o `compositor-blues`, letra salva em `letras/`
2. **Revisão** — `critico-blues` avalia e sugere melhorias
3. **Produção no Suno** — `suno-prompt` gera o style prompt e a letra formatada
4. **Cifra** — `cifra-blues` transcreve o MIDI exportado em cifra brasileira

## Letras

| Música | Data |
|---|---|
| [Flood Town Blues](letras/flood-town-blues.md) | 2026-06-30 |
