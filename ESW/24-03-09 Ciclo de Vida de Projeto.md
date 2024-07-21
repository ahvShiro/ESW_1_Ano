#ESW 

> [!important] Projeto
> Empreendimento TEMPORÁRIO para a criação de um produto ou serviço ÚNICO

> [!note] Ciclo de vida
> Processo pelo qual um projeto passa, desde o seu começo quanto sua finalização
```mermaid
flowchart LR 
	id1[Início] --> id2[Fase 1] --> id3[Fase 2] --> id4[Fase n] --> id5[Final]
```
# Ciclo de Vida Tradicional
- Cada fase acontece ***sequencialmente***
```mermaid
flowchart LR 
	id1[Elicitação] --> id2[Análise] --> id3[Construção] --> id[Testes] --> id5[Implementação]
```
- Mais lento
- Melhor para projetos pequenos
# Ciclo de Vida Iterativo-Incremental
- Cada fase acontece ***concorrentemente***

```mermaid
flowchart TD
subgraph "Iteração 3"
	id1[Elicitação] --> 
	id2[Análise] --> 
	id3[Construção] --> 
	id[Testes] --> 
	id5[Implementação]
end

subgraph "Iteração 2"
	id6[Elicitação] --> 
	id7[Análise] --> 
	id8[Construção] --> 
	id9[Testes] --> 
	id10[Implementação]
end

subgraph "Iteração 1"
	id11[Elicitação] --> 
	id12[Análise] --> 
	id13[Construção] --> 
	id14[Testes] --> 
	id15[Implementação]
end
```
- Ciclo de vida mais rápido
- Mais dinâmico
- Ideal para ambientes burocráticos
