# Dicas, anotações e recursos extras

A especificação do caso de uso (UCS) documenta o que o sistema faz do ***ponto de vista do usuário***. O Diagrama de Caso de Uso apresenta o conjunto de comportamentos e funcionalidades de um sistema. É considerado o diagrama primordial da UML, justamente por não exigir elevado grau de detalhamento. 

## Definições  

**Ator**: é um papel que tipicamente estimula/solicita ações/eventos do sistema e recebe um resultado. Pode ser uma pessoa, um timer, um hardware ou outro gatilho externo.  

**Caso de uso**: Descreve as operações que o sistema deve cumprir para cada usuário, desconsiderando a estrutura interna do sistema. Tipicamente descrito pelo nome (*verbo no infinitivo + substantivo*), atores envolvidos, condições prévias, pós-condição, fluxo padrão, fluxos alternativos, pontos de extensão e casos de uso incluídos. [Exemplo 1 (em inglês)](exemplo1_ucs_ingles.md)

**Regra de Negócio**: Uma diretiva específica, testável e sobre a qual se podem tomar decisões que está sob o controle da empresa/software e oferece suporte a uma política de negócios.

---
## Regras de Negócio
1. Pode ser traduzido em um código específico que valida os dados inseridos ou impõe o comportamento desejado do usuário.  
1. Descreva o que pode ou não ser feito em um cenário específico.  
1. Fornece os critérios, condições e exceções para um cenário.
1. Pode existir independentemente dos requisitos
1. Serve para aplicar uma política
1. Determina quando as informações podem mudar ou quando os valores são válidos



### Como escrever uma boa regra de negócio

- Nome: Dê a cada regra de negócios um identificador exclusivo. Faça com que seja significativo para o leitor.
- Descrição: Descreva a finalidade da regra de negócios. Use verbos ativos, remova texto ambíguo e se esforce para obter clareza. Use fluxogramas ou diagramas UML para descrever regras complexas.
- Exemplo: se possível, inclua um exemplo positivo e um exemplo negativo da regra.
- Fonte: Identifique a fonte da regra para que possa ser verificada. Pode ser legislação, norma, procedimento interno ou pessoa.
- Regras relacionadas: Identifique as regras de negócios relacionadas, se houver, para oferecer suporte à rastreabilidade. 

>Exemplos de regras de negócio  
>- Restrições
>- Validações obrigatórias
>- Procedimentos obrigatórios

---
## Inclusão vs Extensão vs Generalização de Caso de Uso

### Inclusão entre Casos de Uso   

Incluir é usado para **extrair fragmentos de caso de uso que são duplicados em vários casos de uso**. O caso de uso incluído **não pode ser independente e o caso de uso original não está completo sem o caso de uso incluído**. A inclusão deve ser usada com moderação e apenas nos casos em que a duplicação é significativa e existe intencionalmente (e não por coincidência).

>Exemplo:
O fluxo de eventos que ocorre no início de cada caso de uso de caixa eletrônico (quando o usuário coloca seu cartão do caixa eletrônico, insere seu PIN e é mostrado o menu principal) seria um bom candidato para include. 


A relação de inclusão pode ajudar a esclarecer um caso de uso da seguinte maneira:

1. Isolando e encapsulando detalhes complexos para que eles não obscureçam o sentido real do caso de uso.
1. Melhorando a consistência através da inclusão do comportamento dos diversos casos de uso.
1. Geralmente, mais de um caso de uso deve conter um caso de uso de inclusão para que valha a pena manter um caso de uso extra e a relação de inclusão.

Somente o caso de uso base tem conhecimento do relacionamento entre os dois casos de uso. Nenhum caso de uso de inclusão sabe o que está incluído em outros casos de uso.   

> Nota:   
No diagrama a seta aponta do caso base para o incluído. Lê se que o caso base inclui o caso incluído.


### Extensão entre Casos de Uso   

Extender é usado quando um caso de uso adiciona condicionalmente etapas a outro caso de uso. Se um caso de uso possuir segmentos de comportamento de **caráter opcional ou excepcional** que não inclua nada na compreensão da finalidade principal do caso de uso, fragmente-os em um novo caso de uso de extensão.  

Os subfluxos complexos e o comportamento opcional são os primeiros candidatos a um particionamento em casos de uso de extensão. Geralmente, esse comportamento pode ser bastante complexo e difícil de descrever: incluí-lo no fluxo de eventos de um caso de uso pode dificultar a visão do "comportamento" normal. A extração do comportamento deve melhorar a compreensão do modelo de casos de uso.

Importante: _O caso de uso base ainda está com seu sentido completo e pode ser compreendido por si só, sem que seja necessária nenhuma referência ao caso de uso de extensão._

Importante: _Descreva, em breves palavras, cada relação de extensão que você definiu. Defina as condições que devem ser atendidas para que a extensão ocorra. Certifique-se de que você definiu o ponto de extensão no caso de uso base em que a extensão deve ser inserida._


> Nota:   
No diagrama a seta aponta do caso extensão para o caso base. Lê se que o caso extensão extende o caso base.

### Generalização:
A Generalização é usada quando temos **um caso base que possui diferentes especializações e inclui comportamento ou sobrescreve o caso de uso base**.
> Exemplo:  
Pagar Fatura pode ser generalizado por Pagar com Boleto, Pagar com Cartão de Crédito ou Pagar em Espécie.  

> Nota:  
No diagrama a seta aponta do do caso mais especializado para o caso mais geral. Ex: Pagar com cartão aponta para pagar fatura.

## Outros Recursos

[OMG® Unified Modeling Language® (OMG UML®)Version 2.5.1](https://www.omg.org/spec/UML/2.5.1/PDF)

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

[GitHub Markup](https://github.com/github/markup/blob/master/README.md)
