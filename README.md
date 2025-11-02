# Algoritmos de Coordenação Pós-Quântica para Coexistência Multi-Standard em Redes IoT Móveis

## Descrição

Este repositório contém o pré-projeto de doutorado focado no desenvolvimento de algoritmos de coordenação para comunicação móvel que integram criptografia pós-quântica em arquiteturas multi-standard. A pesquisa investiga propriedades de coexistência, modelos matemáticos de canais com overhead criptográfico, técnicas de handover seguro e métodos de otimização energética para dispositivos IoT móveis.

## Objeto de Pesquisa

O objeto desta pesquisa são os **algoritmos de coordenação para comunicação móvel** que integram:
- Criptografia pós-quântica (ML-KEM, ML-DSA, SLH-DSA)
- Arquiteturas multi-standard (5G, LoRaWAN, NB-IoT)
- Propriedades de coexistência e coordenação distribuída
- Modelos matemáticos de canais com overhead criptográfico
- Técnicas de handover seguro e otimização energética

## Alinhamento com Temas do Edital

### Convivência entre Diferentes Sistemas de Comunicação
- Algoritmos de coexistência multi-standard 5G+LoRaWAN+NB-IoT
- Primeira solução algorítmica de coordenação distribuída com segurança pós-quântica

### Sustentabilidade e Equidade de Futuras Redes Sem Fio
- Algoritmos de otimização energética para comunicação verde com segurança quântica
- Algoritmos de power control adaptativos com energy harvesting

### Sensoriamento e Comunicação Integrados
- Algoritmos ISAC pós-quânticos com autenticação física
- Primeira integração algorítmica radar-comunicação resistente a ataques quânticos

## Metodologia

A metodologia é estruturada em quatro fases científicas para desenvolvimento sistemático dos algoritmos de coordenação pós-quântica, concebida como um ciclo de refinamento contínuo onde as fases são interdependentes. A modelagem teórica estabelece métricas e limites que guiam o desenvolvimento algorítmico, a implementação testa viabilidade prática sob restrições reais, e a validação experimental gera dados empíricos que refinam os modelos iniciais, fechando o ciclo de pesquisa.

### Fase 1: Modelagem Matemática de Canais (Semestres 1-2)
- Extensão de modelos de fading para overhead PQC variável
- Análise de capacidade Shannon com processamento criptográfico
- Caracterização estocástica de interferência entre protocolos
- Derivação de bounds teóricos para throughput com restrições energéticas

### Fase 2: Desenvolvimento de Algoritmos (Semestres 3-4)
- Algoritmos de handover seguro entre padrões com primitivas PQC
- Coordenação distribuída para alocação dinâmica de espectro
- Agregação de tráfego com verificação criptográfica
- Detecção e mitigação de interferência inter-standard

### Fase 3: Implementação e Otimização (Semestres 5-6)
- Implementação em plataformas multi-radio (ESP32 + módems)
- Codesign algoritmo-hardware para minimizar latência PQC
- Power control adaptativo baseado em battery harvesting
- Otimização cross-layer para eficiência energética

### Fase 4: Validação Experimental (Semestres 7-8)
- Testbed móvel com cenários de handover entre tecnologias
- Medições de interferência e coexistência em ambientes realísticos
- Análise de performance algorítmica
- Validação de modelos teóricos

### Verificação Formal
- **TLA+/Apalache**: Model checking para propriedades de safety e liveness
- **PRISM**: Análise probabilística de performance energética
- **Coq**: Verificação de propriedades de composição algorítmica (foco na integração, não nas primitivas base)
- **Escopo**: Propriedades da integração PQC, utilizando primitivas já validadas como base

## Resultados Esperados

### Teóricos
- Modelos matemáticos de canal e bounds de capacidade para comunicação PQC
- Primeira caracterização teórica de overhead criptográfico em sistemas móveis
- Limites fundamentais para trade-offs energia-throughput-segurança

### Algorítmicos
- Suite de algoritmos de coordenação multi-standard com segurança pós-quântica
- Handover adaptativo, alocação espectral distribuída, power control eficiente
- Primeira solução integrada para coexistência 5G+LoRaWAN+NB-IoT com PQC

### Práticos
- Implementação funcional em hardware multi-radio IoT
- Protótipos otimizados para ESP32 com módems comerciais
- Benchmarks de performance para comunicação móvel pós-quântica

### Científicos
- 8-10 publicações em venues A1/A2 (IEEE TWC, IEEE IoT Journal, IEEE Communications Magazine)
- Estabelecimento de nova linha de pesquisa em coordenação móvel pós-quântica
- Contribuições para padronização 6G através de 3GPP e ITU-R

## Estrutura do Repositório

```
├── README.md                    # Este arquivo
├── pre_projeto.tex             # Documento principal do pré-projeto
├── capa.sty                    # Formatação da capa UnB
├── bibliografia.bib            # 15 referências de alta qualidade
├── imagens/                    # Figuras e diagramas
│   ├── unb_bandeira.png       # Logo da UnB
│   └── arquitetura_algoritmo.png # Diagrama da arquitetura
└── includes/                   # Seções do documento
    ├── introducao.tex          # Introdução e lacunas da literatura
    ├── justificativa.tex       # Justificativa da pesquisa
    ├── objetivos.tex           # Objetivos geral e específicos
    ├── metodologia.tex         # Metodologia em 4 fases
    └── cronograma.tex          # Cronograma e resultados esperados
```

## Compilação

Para compilar o documento LaTeX:

```bash
pdflatex pre_projeto.tex
bibtex pre_projeto
pdflatex pre_projeto.tex
pdflatex pre_projeto.tex
```

## Referências Bibliográficas

O projeto utiliza **15 referências de alta qualidade**, incluindo:

### Venues de Prestígio (A1/A2):
- IEEE Transactions on Wireless Communications
- IEEE Internet of Things Journal  
- IEEE International Conference on Communications
- Computer Networks (Elsevier)
- Sensors (MDPI)

### Autores Renomados:
- **Marta Kwiatkowska** - Autoridade mundial em model checking (PRISM)
- **Theodore Rappaport** - Pioneiro em comunicações wireless
- **Claude Shannon** - Fundador da teoria da informação

### Distribuição Temática:
- **27%** Comunicações móveis e algoritmos
- **27%** Criptografia pós-quântica 
- **26%** Coexistência e coordenação
- **20%** Sustentabilidade energética

## ⚠️ Ajustes Implementados

Para atender ao limite de **7 páginas**:
- ✅ Margens ligeiramente reduzidas (2.3cm)
- ✅ Bibliografia reduzida para 15 referências essenciais
- ✅ Mantido todo o conteúdo técnico e rigor científico original
- ✅ Preservada a estrutura completa com todas as seções

## Linha de Pesquisa

**Comunicações Móveis** - Departamento de Engenharia Elétrica, UnB

## Palavras-chave

Algoritmos de Coordenação, Comunicações Móveis Pós-Quânticas, Coexistência Multi-Standard, Otimização Energética, Verificação Formal

## Autor

Fabricio Rodrigues Freire - Programa de Pós-Graduação em Engenharia Elétrica, UnB

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.
