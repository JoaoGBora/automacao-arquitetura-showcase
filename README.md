# Automação com IA para Escritório de Arquitetura

> 🔒 Código privado. Esta página descreve o escopo.

## 1. Gerador de briefing de cliente
A partir das respostas da entrevista com o cliente, a IA monta um **briefing de projeto pronto para apresentar**:
- Aplica a identidade visual do escritório
- Pesquisa tendências e itens em alta
- Sugere referências visuais alinhadas ao gosto do cliente

## 2. Detalhamento de projeto a partir do CAD
Pipeline que lê plantas exportadas do AutoCAD em **DXF** e gera:
- **Memorial descritivo** detalhado
- **Tabela de esquadrias** (portas e janelas) automática
- Modelo 3D inicial no **SketchUp**, a partir da planta 2D e de uma planilha de alturas e níveis

## Arquitetura
```
Planta DXF + planilha de níveis ─► Leitura da geometria (Python) ─► Memorial + tabelas
                                                │
                                                └─► SketchUp (conector MCP) ─► modelo 3D
```

## Tecnologias
Claude (agentes e skills) · Python (leitura de DXF) · Excel · SketchUp MCP
