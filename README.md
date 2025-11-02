
# Caracterização de Primitivas de Segurança Física no Domínio Terahertz para Redes 6G

## Sobre o Projeto

Este repositório contém o **pré-projeto de doutorado** que investiga primitivas de segurança da camada física (Physical Layer Security - PLS) para comunicações em redes 6G operando na faixa de Terahertz (THz). A pesquisa propõe metodologias inovadoras para geração de chaves secretas e autenticação de dispositivos explorando as propriedades únicas de propagação do canal THz, especialmente a absorção molecular atmosférica.

### Objetivo Principal

Desenvolver e validar por meio de simulação computacional uma metodologia para caracterização e extração de primitivas de segurança física (geração de chaves e autenticação) baseadas nas propriedades únicas de propagação do canal no domínio Terahertz.

### Área de Concentração

- **Programa**: Pós-Graduação em Engenharia Elétrica (PPGEE-FT/UnB)
- **Área**: Telecomunicações e Redes de Comunicação
- **Linha de Pesquisa**: Comunicações Móveis
- **Nível**: Doutorado Acadêmico
- **Duração**: 48 meses

---

## Estrutura do Repositório

```
.
├── pre_projeto.tex              # Documento principal LaTeX
├── capa.sty                     # Estilo customizado para capa
├── bibliografia.bib             # Referências bibliográficas
├── includes/                    # Seções do documento
│   ├── introducao.tex          # Contextualização e problema de pesquisa
│   ├── referencial_teorico.tex # Estado da arte e fundamentação
│   ├── justificativa.tex       # Relevância científica e aplicada
│   ├── objetivos.tex           # Objetivos geral e específicos
│   ├── metodologia.tex         # Abordagem metodológica
│   └── cronograma.tex          # Planejamento temporal (48 meses)
├── imagens/                     # Diretório para figuras (se houver)
└── README.md                    # Este arquivo
```

---

## Conceitos-Chave

### Physical Layer Security (PLS)
Abordagem de segurança que explora as características físicas do canal de comunicação (reciprocidade, variabilidade temporal, decorrelação espacial) para garantir confidencialidade e autenticação, complementando ou substituindo criptografia tradicional.

### Domínio Terahertz (THz)
Faixa de frequência entre 0,1-10 THz, candidata para redes 6G devido à vasta largura de banda. Caracterizada por:
- Alta perda de propagação
- Absorção molecular seletiva (H₂O, O₂)
- Enlaces dominados por linha de visada (LoS)
- Alta sensibilidade atmosférica

### Geração de Chaves Secretas (SKG)
Processo de extração de material criptográfico a partir das medições do canal sem fio, explorando sua reciprocidade e aleatoriedade para estabelecer chaves compartilhadas entre dispositivos legítimos.

### Physical Unclonable Function (PUF)
Uso da resposta ao impulso do canal (CIR) como "impressão digital" única para autenticação de dispositivos, explorando a sensibilidade espacial extrema do canal THz.

---

## Contribuições Científicas Esperadas

1. **Modelagem de Canal THz**: Quantificação numérica da entropia disponível da absorção molecular atmosférica como fonte de aleatoriedade
2. **Protocolo SKG Inovador**: Desenvolvimento de algoritmos de geração de chaves que exploram variações temporais da absorção molecular (não apenas multipercurso)
3. **Mecanismo de Autenticação**: Proposta de detector baseado em fingerprinting CIR com limiares de decisão otimizados para detecção de spoofing
4. **Análise de Trade-offs**: Caracterização quantitativa entre taxa de chave, segurança (entropia) e overhead de sinalização

---

## Tecnologias e Ferramentas

### Modelagem e Simulação
- **Python 3.10+**: SciPy, NumPy, Scikit-learn
- **Simulação de Canal**: Sionna, Wireless InSite (ray-tracing 3D)
- **Base de Dados**: HITRAN 2020 (espectroscopia molecular)
- **Padrões**: ITU-R P.676-12 (atenuação atmosférica)

### Análise Estatística
- Monte Carlo (10⁵ iterações por cenário)
- Testes ANOVA para validação paramétrica
- Intervalos de confiança 95%

### Documentação
- LaTeX (abntex2)
- BibTeX (gestão de referências)

---

## Requisitos para Compilação

### Sistema Operacional
- Linux (recomendado: Ubuntu 20.04+)
- Windows (com MiKTeX ou TeX Live)
- macOS (com MacTeX)

### Distribuição LaTeX
```bash
# Ubuntu/Debian
sudo apt-get install texlive-full texlive-lang-portuguese

# Pacotes essenciais
sudo apt-get install texlive-bibtex-extra biber
```

### Pacotes LaTeX Necessários
- `abntex2` (classe de documento)
- `abntex2cite` (citações ABNT)
- `inputenc`, `babel` (suporte UTF-8 e português)
- `amsmath`, `amssymb` (matemática)
- `graphicx`, `tikz`, `pgfplots` (figuras)
- `hyperref` (links)

---

## Como Compilar

### Compilação Completa (com bibliografia)
```bash
pdflatex pre_projeto.tex
bibtex pre_projeto
pdflatex pre_projeto.tex
pdflatex pre_projeto.tex
```

### Usando Makefile (alternativa)
```bash
# Criar Makefile
cat > Makefile << 'EOF'
all:
	pdflatex pre_projeto.tex
	bibtex pre_projeto
	pdflatex pre_projeto.tex
	pdflatex pre_projeto.tex

clean:
	rm -f *.aux *.log *.bbl *.blg *.toc *.out *.lof *.lot *.fls *.fdb_latexmk
EOF

# Compilar
make

# Limpar arquivos auxiliares
make clean
```

### Usando latexmk (recomendado)
```bash
latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" pre_projeto.tex
```

---

## Referências Principais

### Trabalhos Seminais
- **Shannon (1949)**: Teoria da informação e sigilo perfeito
- **Wyner (1975)**: Canal de escuta (wiretap channel)
- **Maurer (1993)**: Acordo de chaves por discussão pública

### Estado da Arte em PLS
- **Mukherjee et al. (2014)**: Survey sobre PLS em redes multiusuário
- **Nguyen et al. (2022)**: PLS em banda THz
- **Basat et al. (2023)**: Segurança em 6G

### Específico para THz
- **Rappaport et al. (2019)**: Comunicações acima de 100 GHz
- **Ma et al. (2018)**: Segurança em enlaces THz
- **Fang et al. (2022)**: Canais seguros usando atenuação atmosférica

> **Total**: 30+ referências de alto impacto (IEEE, Nature, periódicos A1-B1)

---

## Cronograma de Execução

| Semestre | Atividades Principais |
|----------|----------------------|
| **S1** | Revisão bibliográfica sistemática, projeto detalhado |
| **S2** | Modelagem de canal THz (absorção molecular + ray-tracing) |
| **S3-S4** | Desenvolvimento de protocolos SKG e autenticação, qualificação |
| **S5** | Simulações Monte Carlo, análise de trade-offs |
| **S6** | Submissão 2º artigo, início redação tese |
| **S7** | Consolidação da tese, revisões de artigos |
| **S8** | Defesa final |

**Metas de Publicação**:
- 1 artigo em conferência internacional (ano 2)
- 2 artigos em periódicos Qualis A1/A2 (anos 3-4)

---

## Autor

**Fabricio Rodrigues Freire**
- Universidade de Brasília (UnB)
- Email: fabricio.freire@redes.unb.br

### Orientação
- **Orientador**: [Nome a ser definido]
- **Programa**: PPGEE - Faculdade de Tecnologia (FT)

---

## Lacunas Científicas Endereçadas

Esta pesquisa preenche duas lacunas críticas identificadas na literatura:

1. **Ausência de SKG para canais LoS-dominantes**: Técnicas existentes dependem de multipercurso rico, inadequadas para THz
2. **Não exploração de dinâmica atmosférica**: Trabalhos prévios usam absorção molecular para atenuação espacial estática, não para variabilidade temporal como fonte de entropia

---

## Licença

Este projeto acadêmico está disponível para fins educacionais e de pesquisa. Para uso ou citação:

```bibtex
@phdthesis{Freire2025,
  author = {Fabricio Rodrigues Freire},
  title = {Caracterização de Primitivas de Segurança Física no Domínio Terahertz para Redes 6G},
  school = {Universidade de Brasília},
  year = {2025},
  type = {Pré-projeto de Doutorado}
}
```

---

## Contribuições

Este é um projeto de pesquisa individual para doutorado. Sugestões e discussões científicas são bem-vindas via:
- Issues neste repositório
- Contato direto com o autor
- Grupos de pesquisa em telecomunicações da UnB

---

## Status do Projeto

**EM DESENVOLVIMENTO** - Pré-projeto submetido para avaliação (2025)

### Próximos Passos
- Aprovação no processo seletivo PPGEE/UnB
- Definição de orientador
- Cursamento de disciplinas obrigatórias (12 créditos)
- Início das simulações (Fase I)

---

## Destaques Técnicos

### Inovações Metodológicas
- Modelagem linha-a-linha da absorção molecular (HITRAN 2020)  
- Ray-tracing 3D para cenários indoor/outdoor realistas  
- Quantização adaptativa multi-nível para SKG  
- Detector Neyman-Pearson otimizado para PUF THz  
- Protocolo Cascade adaptado para CIR esparso  

### Métricas de Avaliação
- **Taxa de Geração de Chaves (KGR)**: bits/s/Hz
- **Taxa de Discordância (KDR)**: P[K_A ≠ K_B]
- **Probabilidade de Detecção (P_d)**: autenticação
- **Informação Mútua**: I(K_A; K_B) - I(K_A; K_E)

---

## Suporte e Contato

Para questões técnicas sobre o documento LaTeX ou conteúdo científico:

- **Issues**: Use a aba "Issues" deste repositório
- **Email institucional**: [a ser definido após aprovação]
- **Grupo de Pesquisa**: GTEL/UnB (a confirmar)

---

<div align="center">

**Universidade de Brasília**  
*Faculdade de Tecnologia*  
*Programa de Pós-Graduação em Engenharia Elétrica*

---

[![UnB](https://img.shields.io/badge/UnB-Universidade%20de%20Bras%C3%ADlia-blue)](https://www.unb.br)
[![LaTeX](https://img.shields.io/badge/LaTeX-Project-008080?logo=latex)](https://www.latex-project.org/)
[![License](https://img.shields.io/badge/License-Academic-green)](LICENSE)

*Última atualização: Novembro 2025*

</div>
