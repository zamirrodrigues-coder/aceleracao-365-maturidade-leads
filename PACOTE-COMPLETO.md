# Aceleração 365: Módulo Maturidade da Geração de Leads, Pacote Completo

**Data:** 11 de novembro de 2026
**De:** Zamir Rodrigues
**Para:** Lauro Kunzler, que valida, e a Claude que trabalha no código do app Aceleração 365.
**Estado:** PROPOSTA para validação. O conteúdo das telas foi homologado pelo Zamir, tela a tela, num exemplo clicável fora do app. A forma de levar ao app ainda não foi aprovada por ninguém.

---

## Parte 0. Leia Primeiro

### 0.1. O Que É

- Um tema novo do Bloco Marketing da Jornada: "Maturidade da Geração de Leads".
- O aluno percorre o caminho que o cliente faz até chegar à empresa, um caminho por vez. São quatro passos:
  - objetivo, pilar e canal;
  - as oito etapas, cada uma explicada e respondida;
  - em cada etapa, a leitura na hora do que os dados dele mostram;
  - no fim, o nível de maturidade, o próximo passo e o que vai ao mentor.
- Princípio do Zamir: toda tela entrega algo ao aluno na hora. O mentor recebe como consequência. Tela que só coleta dado para o mentor não entra.

### 0.2. O Que Está Neste Repositório

| Arquivo | O que é |
|---|---|
| `PACOTE-COMPLETO.md` | Este documento. Parte 0 (instruções), Parte 1 (o pacote do módulo) e Parte 2 (o registro completo do conteúdo validado) |
| `exemplo/Aceleracao-365-Exemplo-Maturidade-Geracao-de-Leads.html` | O exemplo clicável. É a referência de comportamento e a fonte de todo texto literal das telas. Abre direto no navegador |
| `prova/prova-do-exemplo.js` | A prova: 587 conferências sobre o exemplo. É o critério de aceite |
| `referencias/fluxograma-da-jornada.html` | O fluxograma da jornada de maturidade, aprovado |
| `referencias/modelo-jornada-fluxo-adequado.html` | O modelo aprovado da tela final como jornada |

Nas Partes 1 e 2, "você" é o Zamir, porque o texto foi escrito para ele. Os nomes de arquivo citados ali são os originais dele. O registro (Parte 2) é a peça `Conteudo-Validado`, o exemplo e a prova são os desta tabela. Pareceres e cópias de versões antigas citados no registro ficaram fora: são histórico.

### 0.3. O Que Se Pede ao Lauro

Validar o pacote antes de qualquer construção. Três perguntas:
- O conteúdo cabe no app como tema da Jornada?
- A proposta de subida (Parte 1) faz sentido para o código do app?
- As decisões em aberto (0.6) têm resposta do lado do app?

### 0.4. Regras para a Claude do App

1. **Comece pelo código do app, sem construir nada.**
   - Leia a arquitetura e localize onde os temas da Jornada vivem.
   - Veja como um tema guarda as respostas e como o mentor recebe o que o aluno faz.
   - O módulo entra como os outros temas. Não crie fluxo paralelo nem duplique estrutura que já existe.
2. **O exemplo é a referência.**
   - Todo texto de tela sai dele, literal.
   - O Zamir homologou cada tela. Nenhum texto muda sem o ok dele.
   - Se o app pedir outro texto, leve a proposta e espere.
3. **A prova é o critério de aceite.**
   - Ela vira teste automatizado do app, com os mesmos casos e os mesmos textos esperados.
   - Os 587 passam antes do ambiente de teste.
   - O que ela não cobre está na Parte 1, seção 9, e vira teste novo.
4. **Regras do produto que valem em toda tela:**
   - sem travessão em prosa;
   - títulos e rótulos em Title Case;
   - número sempre com máscara: ponto no milhar e vírgula no decimal, no campo e no texto;
   - termo técnico visível, com "?" ao lado;
   - respostas da mais completa para a menos completa, com "Não sei" por último.
5. **Segurança:**
   - o aluno vê só o que é dele;
   - o mentor vê só os seus alunos;
   - a permissão é conferida no servidor, e nenhum segredo vai no código.
6. **Dados:** toda mudança de dados é versionada e tem volta. "Não sei" e "Não acompanho" são estados explícitos, diferentes de vazio.
7. **Conta real intacta:** durante o teste, nada de "Salvar e enviar ao mentor" nem de envio de formulário em conta de aluno real.
8. **Ambiente de teste antes. Produção só com autorização do Zamir.**

### 0.5. Mapa do Exemplo: Onde Mora Cada Conteúdo

Tudo fica no único `<script>` do HTML. As linhas abaixo são do arquivo deste repositório.

| Constante ou função | Linha | O que guarda |
|---|---|---|
| `OBJ` | 246 | Os dois objetivos: Receita Nova e Expansão |
| `PILAR` | 263 | Os cinco pilares, com a lista de canais de cada um |
| `CANAL` | 331 | Os 32 canais: nome e conteúdo de cada um |
| `COMUM` | 466 | Textos comuns das Etapas 5 a 8 |
| `ORDEM`, `AQUISICAO`, `TOTAL`, `NOME` | 481 a 484 | Ordem dos pilares, os quatro de aquisição e as oito etapas |
| `LEIGO`, `EM`, `POR`, `DE` | 485 a 496 | O pilar na linguagem do dono e as formas "pelo Inbound" e "do Inbound" |
| `CONCEITO` | 502 | A explicação de cada etapa |
| `FICHA_PILAR`, `LEITURA_PILAR` | 514 e 522 | A ficha e a leitura de cada pilar |
| `FICHA_CANAL` | 530 | A ficha dos canais |
| `FICHA_CONV` | 623 | A Etapa 4 de cada pilar, no nível simples |
| `DADOS` | 679 | A Etapa 3 de cada canal no nível do Google: perguntas, respostas, leituras, situação, passos, pontos para o atendimento e o que vai ao mentor |
| `PORTAS`, `PORTA_OPS` | 1.597 e 1.627 | As portas da ficha do Google e as respostas do teste |
| `ADS`, `META`, `SEO_OPS`, `GEO_OPS`, `AVAL_OPS`, `PONTO_OPS`, `OFERTA_OPS`, `IND_OPS`, `PROG_OPS`, `PAR_OPS` | 1.629 a 1.790 | As opções de resposta de cada canal |
| `CONV` | 1.800 | A Etapa 4 de cada canal no nível do Google e o campo de CRM da Etapa 5 |
| `TESTE_CONTATO`, `PROX_ACAO`, `PROX_LER`, `CRITERIO`, `RELATORIO`, `DECISAO` | 2.491 a 2.567 | As conferências das Etapas 5 a 8 |
| `FLUXO` | 2.651 | Os textos de cada objetivo: rótulos, perguntas e frases das etapas |
| `NIVEL` | 2.901 | Os cinco níveis |
| `NOTA_*`, `CONTA_*`, `PAINEL_GOOGLE` | 2.910 a 2.930 | Os avisos de fonte do Onde Conferir |
| `TERMO` | 2.931 | As folhas do "?" e do Onde Conferir |
| `HERDA` | 3.291 | As etapas cujas respostas valem para a empresa toda e passam ao caminho seguinte |
| `TAXA` | 3.293 | Os canais que mostram o retorno "X em cada 10" |
| `medida`, `situacao`, `statusEtapa`, `proximo` | 3.480, 3.497, 2.534 e 4.064 | A conta do nível, a situação de cada etapa e o próximo passo |
| `devolutiva` | 3.895 | A leitura na hora, em cada etapa |
| `telaHome`, `telaInicio`, `telaEtapa`, `telaFim`, `telaFinal`, `telaBiblioteca` | 3.930 a 4.414 | As telas |
| `cartaoPasso`, `cartaoMentor` | 4.114 e 4.148 | O cartão do próximo passo e o que vai ao atendimento |
| `DONO`, `DONO_FRASE`, `ACAO`, `RELATORIO_TEM` | 4.304 a 4.313 | Os nomes do dono e as frases da tela final |

**Atalhos do exemplo:**
- `#/d/1?e=<JSON>` abre uma tela já com respostas.
- `?termo=<id>` abre uma folha do "?".
- O exemplo não guarda nada. As respostas vivem só na memória da página.

### 0.6. Decisões em Aberto

Elas não podem ser tomadas pela Claude do app. Vão ao Zamir e ao Lauro, uma por vez:
1. **A classe de risco da mudança.** A proposta é Crítico: cada aluno é uma empresa, o mentor vê vários alunos, e o módulo pede faturamento, meta e ticket.
2. **O Raio-X:**
   - no app, ele é o Tema 25, com seis canais e o botão "Salvar e enviar ao mentor";
   - no exemplo, ele saiu, e a pergunta da origem dos clientes foi para a Etapa 2;
   - falta decidir se o tema sai, fica ou se funde.
3. **O que o app guarda e o que o mentor recebe, e quando.**
   - O que guarda inclui o histórico por ciclo de 90 dias, para comparar os ciclos.
   - O Painel do Mentor não foi visto: a conta usada no estudo não tem permissão, e o bloqueio não foi contornado.
4. **Onde mora a conta do nível.** No exemplo, ela roda na página. No app, o que vai ao mentor precisa sair de uma conta conferida no servidor.
5. **O nível simples:** se Revendas, Marketplaces, Outbound, Branding, Base e a Expansão, ainda sem homologação, sobem como estão.
6. **Os caminhos de Onde Conferir de Meta, SEO, GEO e Avaliações:** vieram das páginas de ajuda e nunca foram vistos numa conta real.
7. **Os 57 acréscimos da seção 7 do registro:** ainda passam pela validação do Zamir.

### 0.7. Como Rodar a Prova

Na pasta do repositório:

```bash
node prova/prova-do-exemplo.js
```

- **O que sai no fim:** "587 conferências. TODAS PASSARAM".
- **Como ela trabalha:** carrega o script do exemplo com um documento falso, abre cada tela com respostas definidas e confere o texto que a tela mostra.
- **O que ela não faz:** não grava nada.
- **Tipo de prova:** comportamento executado.

### 0.8. O Que Ficou Fora

- **Nome de cliente e de outros projetos.** Os dois Exemplos Reais, o da ficha do Google e o do Google Ads, usam números de contas reais. Eles ficaram sem nome e sem valor em reais.
- **Lições de outro CRM.** Onde o conteúdo usa a lição, ela aparece como "CRM em operação", só como regra e sem número.
- **Histórico de trabalho:** pareceres, cópias antigas do exemplo e notas de sessão.

---

## Parte 1. O Pacote do Módulo (Proposta)

### 1. O Que Sobe

- Um tema no Bloco Marketing da Jornada: "Maturidade da Geração de Leads".
- Dois objetivos: Receita Nova e Expansão.
- Cinco pilares e 32 canais: Inbound (8), Outbound (7), Branding (7), Indicação e Parcerias (5) e Base de Clientes (5 ações, só na Expansão).
- Oito etapas e cinco níveis.
- Profundidade de hoje:
  - **11 canais no nível do Google:** os 8 do Inbound, mais Indicação de Clientes, Programa de Indicação e Parceiros de Negócio;
  - **21 canais no nível simples** (seção 4): Outbound, Branding, Revendas, Marketplaces e as 5 ações da Base;
  - **Expansão:** validada em bloco, sem homologação tela a tela (seção 5).

### 2. As Telas

| # | Tela | Rota no exemplo | O que faz |
|---|---|---|---|
| 1 | Jornada | `#/` | Botão do tema no Bloco Marketing, com a contagem de caminhos feitos |
| 2 | Início | `#/inicio` | Como Funciona (sete itens), Começar ou Percorrer mais um caminho, Ver o fluxo adequado, Explorar pilares e canais |
| 3 | Etapa 1, Objetivo | `#/d/1` | Escolhe Receita Nova ou Expansão. Pede o número de hoje e a meta. Sem meta, abre Vamos Calcular Juntos, com o ticket que no app vem da Ficha do Negócio |
| 4 | Etapa 2, Pilar | `#/d/2` | Receita Nova: escolhe um dos quatro pilares de aquisição. Expansão: a Base de Clientes |
| 5 | Etapa 3, Canal | `#/d/3` | Abertura da seção 6.7, lista de canais do pilar e as perguntas do canal |
| 6 | Etapas 4 a 8 | `#/d/4` a `#/d/8` | Uma tela por etapa |
| 7 | Fim do Caminho | `#/d/fim` | Nível declarado, origem, Onde a Rota Quebra, mapa das oito etapas, Seu Próximo Passo, funil, O Que Vai para o Atendimento e E Agora? |
| 8 | Seu Fluxo Adequado | `#/d/final` | A tela final como jornada (seção 6.18) |
| 9 | Pilares e Canais | `#/biblioteca` | A biblioteca, sem nota |

**Toda tela de etapa tem quatro partes:**
- **A ficha:** O Que Esta Etapa Faz, Por Que Ela Importa, Exemplo Real (só onde houve conta vista), O Entregável e Como Fazer.
- **Seus Dados:** a pergunta, o apoio, os termos com "?", as respostas e os campos de número com a marca medido ou estimado e o "Não sei".
- **O Que os Seus Dados Mostram:** a leitura na hora.
- **O avanço:** segue para a próxima etapa, ou manda conferir e voltar.

**Folhas que abrem por cima:** o "?" de cada termo, o Onde Conferir de cada pergunta e as duas folhas do GEO (Onde Cada IA Busca e O Que Não Precisa).

### 3. As Etapas

Receita Nova. O que põe a etapa de pé, pelas seções 2 e 6.10 a 6.14:

| Etapa | De pé quando | Números da etapa |
|---|---|---|
| 1. Objetivo | Há uma meta mensal de clientes novos, informada ou calculada junto | Clientes novos por mês e meta |
| 2. Pilar | Há o levantamento cliente por cliente, ou a origem sai do CRM | Clientes do pilar e sem origem conhecida |
| 3. Canal | Os pontos do canal estão em dia (seção 4 deste pacote) | A medida própria do canal |
| 4. Conversão | O teste da porta do canal passa. No nível simples, a frase descrita de pé | Os do canal, e o tempo de resposta opcional |
| 5. Lead | Todo contato entra no CRM, com origem e responsável, e o teste do contato novo passa | Contatos por mês e quantos têm origem e responsável |
| 6. Relacionamento | Cadência com a próxima ação no CRM, e todos os contatos em aberto com data | Contatos em aberto e MQL por mês |
| 7. Lead Qualificado | Critério escrito com etapa no CRM, dizendo o que é MQL e o que é SQL | SQL por mês |
| 8. Medir e Ajustar | Relatório do CRM com contatos, MQL, SQL e clientes por canal, e uma decisão no último mês | Quantos números do caminho são medidos |

**Expansão:** as oito etapas da seção 5. Ela não tem o teste do contato, as conferências das Etapas 6 a 8 nem o MQL e o SQL. Os textos dela não passaram pela homologação.

### 4. As Perguntas de Cada Canal

#### 4.1. Nível do Google (11 canais)

| Canal | Etapa 3: perguntas que decidem o "de pé" | Etapa 3: perguntas que só informam | Etapa 4: o teste | Etapa 5: campo no CRM | Registro |
|---|---|---|---|---|---|
| Google Meu Negócio | Perfil sem pendência, publicação no último mês, nenhuma avaliação sem resposta | Pessoas que viram a ficha nos três últimos meses completos e o percentual sobre o ano passado | Interações, porta principal e o teste da porta: Chamadas, Orientações, Site ou Outro botão | Não tem | 6.8 e 6.10 |
| Google Ads | Rodou o mês inteiro, e os dez termos com mais cliques são de quem procura o que você vende | Motivo da parada, investimento e cliques | A página que mais recebeu cliques, no celular, sem pesquisar o anúncio. A conversão principal só informa | Origem Google Ads | 6.19 |
| Anúncio Meta | Rodou o mês inteiro, e a coluna Resultados conta conversas ou cadastros | Motivo da parada, valor usado e resultados | Conforme o destino: a conversa no número que a empresa atende, o cadastro atendido no mesmo dia ou a página | Origem Meta | 6.20 |
| SEO | Há buscas pelo que você vende, sem o nome da empresa, e a página do serviço principal está no Google | Impressões e cliques sem as buscas pelo nome | A página que mais recebeu cliques, no celular | Origem SEO | 6.21 |
| GEO, trilha própria | Robôs de busca liberados, site incluído nos recursos de IA, serviço principal em texto, empresa no Google e no Bing Places | Ficha igual ao site (vira ajuste), robôs de treino, visitas do Assistente de IA, relatório de IA, citações no Copilot e o teste de perguntar a uma IA | A página que a IA citou, ou a inicial, no celular | Origem GEO | 6.22 e 6.28 |
| Avaliações do Google | Nenhuma prática que o Google não permite, link a todo cliente atendido, avaliação nova nos três últimos meses e nenhuma sem resposta | Nota, total e as notas 1 ou 2 entre as cinco mais recentes. Sem corte | A mesma porta da ficha | Não tem | 6.23 |
| Oferta de Entrada | Oferta escrita com o que a pessoa recebe, o preço e o prazo, à vista no canal que mais traz contato, com próximo passo de data e responsável | Quantos aceitaram e quantos compraram, nos três últimos meses completos | Pedir a oferta como cliente e comparar com o que ela promete | Não tem: a oferta é marca, não origem | 6.24 |
| Ponto Físico | A fachada diz o que vende, o contato está à vista, e o nome e o horário batem com a ficha | Preço na vitrine (vira ajuste) e pessoas novas que passaram na frente | A foto da fachada mostrada a quem não conhece, e o contato à vista usado de outro celular. Vale o pior | Não tem | 6.25 |
| Indicação de Clientes | Texto pronto com o que a empresa faz e como falar com ela, e o pedido nos cinco últimos clientes sem reclamação | Indicações nos três últimos meses completos e o obrigado a quem indicou | O teste do indicado | Origem Indicação, com quem indicou | 6.26 |
| Programa de Indicação | Regra escrita completa ou sorteio autorizado, regra mandada a toda a base e prêmios entregues no prazo | Indicações pelo programa | O teste do indicado | Não tem: a origem é Indicação | 6.27 |
| Parceiros de Negócio | Não trocar lista de clientes, lista de parceiros por escrito e acordo com o jeito de indicar | Parceiros que indicaram e indicações recebidas | O teste do indicado por um parceiro | Origem Parceiro | 6.29 |

Todo número com origem no painel da ferramenta vem sem a marca medido ou estimado. Os outros levam a marca.

#### 4.2. Nível Simples (21 canais)

- **A pergunta:** "Como você faz isto hoje?", com quatro respostas. Na tela, de cima para baixo: a frase "De pé", a frase "Faço, sem rotina", "Não faço" e "Não sei".
- **A medida própria:** a do último mês, ou o estado de hoje (contas na lista, revendas ativas, nota na plataforma), como na seção 4.
- **A Etapa 4:** a frase descrita da conversão do pilar. No Outbound, por exemplo, ela se chama Resposta do Contato. Essas frases ainda passam pela sua validação (seção 7, item 1).
- **Os canais:**
  - **Outbound:** Disparo de E-mail, Disparo de WhatsApp, Ligação, Abordagem em Redes Sociais, Porta em Porta, ABM (Contas-Alvo) e Feiras e Eventos.
  - **Branding:** Blog, Podcast, YouTube, Instagram, LinkedIn do Dono, Comunidades e Imprensa e Prêmios.
  - **Indicação e Parcerias:** Revendas e Representantes, com o levantamento feito e sem esqueleto, e Marketplaces.
  - **Base:** Oferta de Venda Adicional, Oferta de Venda Cruzada, Campanha de Recompra, Reativação de Inativos e Pós-Venda.

### 5. Regras de Leitura e de Nível

- **Situação de cada etapa:** de pé, em parte, falta ou não sei. Alguns canais têm também "pode esperar" e "não se aplica", como no registro.
- **O nível:** até onde a rota está de pé, na ordem. Os cortes estão nas Etapas 2, 3, 5 e 8 (seção 1.2).
- **"Não sei" e "Não testei":** levam a conferir e voltar à mesma etapa. Nenhuma tela fica sem saída.
- **CRM sem rotina:** vale "em parte".
- **Os números:** informam e levantam pontos para o atendimento. Não mudam o nível nem a rota.
- **As janelas** (seção 6.1):
  - o que a empresa colhe é a média mensal dos últimos três meses;
  - o que ela faz no canal é o último mês, ou os três últimos meses completos onde o registro diz;
  - estado é como está hoje.
- **A marca de origem:** medido, estimado ou não acompanho.
- **Etapas 1 e 2:** são da empresa e passam para o caminho seguinte. O teste da Etapa 5 e as conferências das Etapas 6 a 8 também.
- **A origem:**
  - cada cliente conta uma vez, pelo caminho por onde conheceu a empresa;
  - se ele citar dois, vale o primeiro;
  - quem não tem origem conhecida entra como "não sei de onde veio";
  - o mapa fecha com o total da Etapa 1.
- **Ordem das respostas:** da mais completa para a menos completa, com "Não sei" por último.
- **Máscara:** milhar com ponto e decimal com vírgula, no campo e no texto. O percentual tem o sinal fixo.
- **Nome do pilar:** cada pergunta e cada leitura dizem o pilar, como "pelo Inbound".
- **Termos técnicos:** ficam visíveis, cada um com "?".
- **O nível tem dois momentos:** declarado na hora e confirmado no atendimento, com o entregável de cada etapa.
- **A rota proposta:**
  - começa pelo caminho de nível mais alto;
  - no empate, segue o canal de pé até mais longe, da Etapa 3 em diante;
  - no empate de verdade, a escolha fica para o atendimento.
- **Estrutura e resultado:** cinco leituras (seção 3.2). São Estrutura com Resultado, Estrutura sem Resultado, Resultado sem Estrutura, Começo e Falta o Número.
- **O funil:** mostra a conversão do caminho e o retorno do canal. O ponto vai ao atendimento quando mais da metade para num trecho.

### 6. Próximo Passo e Avisos de Política

**O próximo passo**
- É a primeira etapa da rota que ainda não está de pé. Não muda por um número de memória.
- É o mesmo cartão no Fim do Caminho e na tela final. Ele traz:
  - a etapa e a ação do dono;
  - o motivo, que é a leitura da resposta dada;
  - "Esta semana", com a tarefa;
  - "Leve ao mentor", com o entregável;
  - "Em paralelo, se quiser", com no máximo dois ajustes, na ordem de cada canal;
  - e "Depois".
- O passo da base da empresa aparece uma vez, sem repetir por caminho.

**Os avisos de política na tela.** Todos têm fonte lida. Os de lei dizem "não é parecer jurídico".

| Aviso | Fonte | Canal |
|---|---|---|
| A empresa só chama quem deu o número e aceitou. No lugar, vai o texto que o cliente encaminha | Política de Mensagens do WhatsApp Business, seção 1 | Indicação de Clientes e Parceiros |
| Troca de lista de clientes entre empresas pede base legal | LGPD | Parceiros |
| Sorteio pede autorização prévia. O passo é parar ou pedir a autorização, e o prêmio em bens tem imposto na fonte | Lei 5.768/1971 e Lei 8.981/1995 | Programa de Indicação |
| A oferta obriga a empresa, e a informação precisa ser clara | Código de Defesa do Consumidor, arts. 30, 31, 35 e 37 | Oferta de Entrada e Programa |
| Não pode haver incentivo, pedido seletivo, meta para a equipe nem pressão no local | Política de avaliações do Google | Avaliações |
| Preço na vitrine, e conferir a regra da prefeitura antes de trocar a placa | Lei 10.962/2004 e Decreto 5.903/2006 | Ponto Físico |
| Comissão e retenção se conferem com o contador | Lei 7.450/1985, art. 53, sem vigência confirmada | Parceiros |

Cada caminho de Onde Conferir termina dizendo de onde ele veio e "Os nomes podem mudar". Só o da ficha do Google foi visto numa tela. Os outros vieram das páginas de ajuda ou da lei.

### 7. O Que Vai ao Atendimento

É o cartão O Que Vai para o Atendimento, no Fim do Caminho.
- **Sempre:** o nível declarado, a situação do canal, os números do canal e da conversão com a origem de cada um, e as Provas para o Mentor Conferir (o entregável de cada etapa de pé).
- **Na Receita Nova, conforme as respostas:**
  - o teste do contato novo e os contatos com origem e responsável;
  - o campo de CRM do canal e quem se interessa e não compra por mês;
  - os contatos em aberto e a próxima ação com data;
  - o que o critério diz, o que o relatório mostra e a última decisão;
  - quantos números do caminho são medidos.
- **Pontos para o Atendimento:** sempre como pergunta. Nenhuma frase afirma a causa.
- **Decisão Que Esses Dados Apoiam:** começa pelo próximo passo quando ele não é o canal.
- **Rodapé da tela final:** "No aplicativo, o mentor recebe o diagnóstico completo e confirma o próximo passo no atendimento, antes de ele entrar no Plano de 90 Dias."
- **Seu princípio, de 05/11:** tela que só coleta dado para o mentor não entra. O mentor recebe como consequência do que o aluno faz.
- **O que este pacote não diz:** como e quando isso chega ao mentor no app. É a segunda decisão da seção 10.

### 8. A Tela Final

Pela seção 6.18, com um bloco por objetivo percorrido:
- a barra das oito etapas, com "Você está na Etapa X de 8";
- **01 Sua Meta:** a meta primeiro, depois o número de hoje na média dos últimos três meses, com a marca de estimativa, e quanto falta por mês;
- **02 O Que Você Já Tem:** uma linha por etapa de pé ou em parte, o nível e "X de pé, Y em parte";
- **03 O Que Pede Atenção:** as três primeiras etapas que não estão de pé, com o nome do dono e "comece aqui" na primeira;
- **04 Seu Próximo Passo:** o único destaque dourado. Com dois caminhos, a frase da comparação abre o cartão;
- **Meu Diagnóstico Completo**, fechado: a origem dos clientes, os caminhos percorridos, as oito etapas com o que falta, a leitura das duas medidas e a nota Como o App Chega a Isto;
- os botões Avaliar Outro Caminho e Voltar à Jornada.

### 9. Critério de Aceite: a Prova Agrupada

Rodada hoje, 11/11/2026. São 587 conferências, e todas passaram. Tipo de prova: comportamento executado. O roteiro carrega o código do exemplo, abre cada tela com respostas definidas e confere o texto mostrado.

| # | O que o app precisa provar | Grupos da prova | Conferências |
|---|---|---|---|
| A | Medição: janelas, mapa de origem fechando com o total, máscaras, nome do pilar, conversão e retorno, número e ponto coerentes | Janelas, Mapa de Origem, Máscara dos Milhares, Máscara de Percentual, Nome do Pilar, Coerência, Conversão do Caminho | 31 |
| B | Nível e rota: CRM como padrão, rota que não muda por número, cruzamento, toda tela com saída, ordem das respostas, abertura da Etapa 3 e os 32 canais sem escala de opinião | Registro (dois grupos), A Rota Não Muda, Cruzamento, Toda Tela Tem Saída, Ordem das Respostas, Abertura da Etapa 3, Todos os Canais | 19 |
| C | Ficha do Google: três fatos, procura à parte, Onde Conferir e o teste da porta | Ficha do Google, Onde Conferir, Tela 3 Corrigida, Tela 4 | 53 |
| D | Etapas 5 a 8 da Receita Nova: teste do contato, próxima ação, MQL e SQL, relatório e decisão | Tela 5, Tela 6, MQL e SQL, Tela 8 | 81 |
| E | Fim do Caminho e tela final: causa do nível, quebra, desempate, ajustes em paralelo e os quatro blocos | Fim do Caminho, Fluxo Adequado, Parecer Externo, Tela Final como Jornada | 38 |
| F | Os sete canais do Inbound além da ficha | Google Ads 31, Anúncio Meta 33, SEO 24, GEO 29, Avaliações 29, Oferta 24, Ponto Físico 29 | 199 |
| G | Indicação e Parcerias | Indicação de Clientes 26, Programa 21, Parceiros 21 | 68 |
| H | Expansão | Expansão | 2 |
| I | Os textos que saíram não voltam | Textos que Saíram | 96 |
| | **Total** | | **587** |

**Proposta para o app**
- A prova vira teste automatizado do app, com os mesmos casos e os mesmos textos esperados.
- Os 587 passam antes do ambiente de teste.

**O que a prova não cobre hoje.** Vira teste novo, a decidir no Gate 1.
- A Expansão, com só 2 conferências.
- Os 21 canais simples, cobertos por 1 conferência agregada.
- Gravação, permissão, isolamento entre alunos e envio ao mentor: nenhuma conferência, porque o exemplo não guarda nada. As respostas vivem só na memória da página.
- A tela vista no celular do app real.
- Três linhas de exibição da prova não acham o texto que procuram: "Custo por contato", "A origem dos clientes está só na memória" e "A meta é". Não são conferências e não falham. Vale limpar na passagem para o teste automatizado.

### 10. Decisões dos Próximos Turnos

São levadas uma por vez, cada uma com a minha recomendação:
1. **O Raio-X:** no app real, ele é o Tema 25. No exemplo, ele saiu, e a pergunta da origem foi para a Etapa 2.
2. **O que o app guarda e o que o mentor recebe.** O Painel do Mentor está bloqueado e não será contornado.
3. **O nível simples:** se Revendas, Marketplaces, Outbound, Branding, Base e a Expansão sem homologação sobem como estão.
4. **Os caminhos de Onde Conferir nunca vistos numa conta real:** Meta, SEO, GEO e Avaliações vieram só das páginas de ajuda.
5. **Os acréscimos pendentes da seção 7:** são 57 itens.

### 11. Gate 0: Onde Está

- **Classe proposta:** Crítico. Cada aluno é uma empresa, o mentor vê vários alunos, e o módulo pede faturamento, meta e ticket. A classe é decisão sua.
- **Arquitetura** (`arquitetura-modular`): BLOQUEADO.
  - O código do app não está neste computador.
  - Sem ele, não há como localizar a arquitetura, o módulo dono, os componentes que se reaproveitam e quem consome cada parte.
- **Dados** (`modelagem-de-dados`): pendente do código. Vai cobrar quatro pontos:
  - onde ficam as respostas por caminho;
  - o histórico por ciclo de 90 dias, já que a comparação entre ciclos depende do app;
  - "Não sei" e "Não acompanho" como estado explícito, diferente de vazio;
  - a marca medido ou estimado junto de cada número.
- **Segurança e tenant** (`seguranca-e-tenant`): pendente do código. Vai cobrar quatro pontos:
  - o aluno vê só o que é dele;
  - o mentor vê só os seus alunos;
  - a permissão é conferida no servidor;
  - e fica decidido onde mora a conta do nível, que hoje é calculada na própria página.
- **Telas** (`componentizacao-ui`): pendente do código.
  - O exemplo copiou classes da folha de estilo do app real: block, lesson, chip, btn, pill e eyebrow.
  - Componentes a conferir se já existem: a folha do "?", o Onde Conferir, o campo de número com máscara, o cartão do próximo passo e a barra das oito etapas.
- **Texto** (`revisao-linguistica-anti-ia`): o texto já passou pela sua homologação. Ao subir, nenhum texto muda sem o seu gate. O código novo passa pela varredura de travessão e de Title Case.
  - Ponto para essa varredura: no cartão do próximo passo, "Esta semana", "Leve ao mentor" e "Em paralelo, se quiser" estão em caixa de frase. Se contam como rótulo, a troca volta a você.
- **Trava até o seu ok:** nada do exemplo vai ao app, e o app real segue em somente leitura.

---

## Parte 2. O Registro Completo do Conteúdo Validado

## Aceleração 365: Conteúdo Validado do Tema de Marketing

**Data:** 6 de novembro de 2026
**Solicitante:** Zamir Rodrigues
**Origem:** as suas validações nesta sessão, em 6 de novembro.
**Natureza:** registro do que você validou no chat. Atualizado depois do racional de medição e de registro, que você aprovou com "Sim, aplicar". O exemplo clicável foi refeito com este conteúdo e está em homologação tela a tela.

**Como ler.** Cada seção diz qual foi a sua resposta. Onde o racional de medição e de registro mudou um texto validado antes, a tabela já traz o texto novo, e a seção 6.4 lista o que foi substituído. As frases das respostas e as medidas são rascunho meu, validado por você em bloco. Nada aqui foi visto por um mentor.

---

### 1. A Base: Como o Nível e a Rota Ficam

**Sua resposta: "Sim, é isso".**

A correção que originou esta base: o tema não pode abrir mão de indicar o nível de maturidade nem de gerar a rota em fluxograma, sem ponto sem saída.

#### 1.1. O Nível

O nível continua sendo até onde a rota está de pé. Muda o que decide se uma etapa está de pé.

| O que os testes mostraram | Como fica |
|---|---|
| Trocar "Mais ou menos" por "Sim" mudava o nível | Cada etapa é respondida por uma frase que descreve o que existe na empresa. Sai a escala de opinião |
| Um caminho com sete etapas de pé caía para o nível 2 | O nível continua seguindo a rota. O mapa das oito etapas aparece junto, e o texto diz onde a rota quebra e o que já está de pé depois |
| O nível vinha só do que o aluno declarava | Dois momentos: nível declarado, na hora, e nível confirmado, no atendimento, com o entregável de cada etapa em mãos |
| Os cortes 2, 3, 5 e 8 pareciam régua sem base | São a definição dos trechos da rota, e ficam escritos |
| O nível era uma foto só | Vira o indicador de evolução: medido de novo a cada ciclo |

#### 1.2. Os Cinco Níveis

| Nível | A rota está de pé até | O que falta |
|---|---|---|
| 1. Improviso | Antes da Etapa 2 | A meta ou a origem dos clientes |
| 2. Direção | Etapa 2, Pilar | Pôr o canal de pé, com rotina |
| 3. Presença | Etapa 3, Canal | Transformar interesse em contato registrado |
| 4. Captação | Etapa 5, Lead | Relacionamento, critério e medição |
| 5. Gestão | Etapa 8, Medir e Ajustar | Nada: o caminho inteiro está de pé e é medido |

#### 1.3. A Rota

| Ponto | O que acontece | Para onde vai |
|---|---|---|
| 1. Início | Escolhe o objetivo | Ponto 2 |
| 2. Pilar e Canal | Escolhe um caminho por vez | Ponto 3 |
| 3. Etapas | Aprende, responde e vê a leitura | Próxima etapa. Se a resposta for "não sei": conferir e voltar à mesma etapa |
| 4. Fim do Caminho | Nível, mapa das oito etapas, próximo passo e pontos para o mentor | Ponto 5 |
| 5. Outro Caminho? | Sim | Volta ao ponto 2, com o caminho feito marcado |
| | Não | Ponto 6 |
| 6. Fluxo Adequado | Caminhos lado a lado e a rota proposta | Ponto 7 |
| 7. Atendimento | Mentor e empresário confirmam o nível pelas provas e combinam a rota | Ponto 8 |
| 8. Execução | Faz o próximo passo combinado | Ponto 9 |
| 9. Medir de Novo | Reavalia as etapas e os números, a cada ciclo de 90 dias | Volta ao ponto 4, com o nível atualizado, ou encerra o ciclo |

**Duas regras da rota**

- O próximo passo sai do mapa: é a primeira etapa da rota que ainda não está de pé. Isso não muda por um número de memória.
- Quando os números apontam para fora do marketing, como muito contato e pouca venda, isso entra como ponto para o atendimento. A rota não para.

**O desenho.** Está em `docs/Aceleracao-365-Fluxograma-da-Jornada-de-Maturidade-2026-11-06.html`. Sua resposta: "Sim, está certo". Depois do "Sim, aplicar", as provas das Etapas 2, 5, 6, 7 e 8 no desenho passaram a falar em levantamento e CRM. O fluxo não mudou.

#### 1.4. O Que Sai de Verdade

- A amostra dos dez últimos clientes e a estimativa de clientes por mês tirada dela.
- A frase que afirmava a causa da perda.
- A troca de rota por um número de memória.
- A escolha do caminho inicial pela contagem dos dez.
- A escala de opinião "Sim, Mais ou menos, Não" nas etapas e nos canais.
- A anotação solta como padrão de registro. O padrão passa a ser o CRM, como na seção 6.3.

---

### 2. As Oito Etapas da Receita Nova

**Suas respostas: "Sim, desenhar", para as etapas, e "Sim, aplicar", para o racional de medição e de registro.**

Exemplo de canal: Inbound, com Google Meu Negócio. Em negrito, a resposta que põe a etapa de pé. As etapas têm também "Não sei", que leva a conferir e voltar. Na Etapa 2, a primeira frase já é "Não sei de onde vêm".

| Etapa | Pergunta | Respostas descritas | Entregável, que serve de prova no atendimento |
|---|---|---|---|
| 1. Objetivo | Quantos clientes novos você precisa por mês? | **Um número**, informado ou calculado junto | Uma meta mensal de clientes novos, escrita |
| 2. Pilar | Você sabe por onde chegaram os clientes novos dos últimos três meses? | Não sei de onde vêm / Sei de cabeça / **Tenho o levantamento, cliente por cliente** / **Tiro do CRM a origem de cada cliente** | O levantamento da origem dos clientes novos dos últimos três meses, cliente por cliente, ou o relatório de origem do CRM |
| 3. Canal | Três fatos conferidos no painel do Google, como na seção 6.8 | Em dia: **Não pede mais**, **No último mês** e **Nenhuma** ou **Não tenho avaliações** | A ficha sem pendência no Google, com publicação no último mês e sem avaliação por responder |
| 4. Conversão | Teste da porta principal, como na seção 6.10 | A resposta depende da porta marcada | O teste da sua porta principal, feito no celular, com o resultado |
| 5. Lead | O que acontece com o contato de quem se interessa? | Não é registrado / Fica na conversa, em caderno ou em planilha / Tenho CRM, mas nem todo contato entra / **Todo contato entra no CRM, com origem e responsável** | Todo contato no CRM, com origem e responsável. A prova é o relatório de contatos por origem |
| 6. Relacionamento | O que você faz com quem se interessou e não comprou? | Espero a pessoa voltar / Volto a falar quando lembro / Tenho uma cadência, mas não registro no CRM / **Sigo uma cadência, com a próxima ação registrada no CRM** | Uma cadência de contato escrita, com a próxima ação de cada contato registrada no CRM |
| 7. Lead Qualificado | Como você sabe quem está pronto para comprar? | Trato todos igual / Separo pela experiência / Tenho critério escrito, mas não marco no CRM / **Tenho critério escrito, e o CRM tem a etapa de pronto para comprar** | Um critério escrito de pronto para comprar, e a etapa correspondente no funil do CRM |
| 8. Medir e Ajustar | Como você acompanha o que cada canal traz? | Não acompanho / Olho de vez em quando / Confiro todo mês, em planilha ou de cabeça / **Tiro do CRM, todo mês, o relatório por canal e decido com ele** | O relatório mensal por canal, tirado do CRM: o que foi investido e o que ele trouxe |

**O que muda em cada etapa**

- Etapa 1: fica como está.
- Etapa 2: fica de pé quando existe o levantamento, cliente por cliente, ou quando a origem sai do CRM.
- Etapa 3: já está neste formato nos oito canais do Inbound. No Google Meu Negócio, a situação vem de três fatos conferidos no painel, como na seção 6.8.
- Etapa 4: na ficha do Google, a conversão é escrita por canal, como na seção 6.10. Nos outros canais, a pergunta de opinião dá lugar à descrição do que existe.
- Etapas 5 a 8: de pé é o que está no CRM, com rotina. CRM sem rotina vale "em parte".

**O que toda etapa devolve**

- Na hora, para o aluno: o que a resposta dele significa e o passo que leva à resposta seguinte.
- Para o atendimento: a resposta marcada, o entregável para o mentor confirmar e os números da etapa, com a origem de cada um.

**Os números e a janela de cada um**

| Número | Etapa | Janela | Papel |
|---|---|---|---|
| Clientes novos por mês e meta | 1 | Média mensal dos últimos três meses | Mostra a distância da meta |
| Desses, quantos chegam por este caminho | 2 | A mesma amostra da Etapa 1 | Mapa de origem, que fecha com o total |
| Quantos por mês sem origem conhecida | 2 | A mesma amostra da Etapa 1 | Entram como "não sei de onde veio" |
| Medida própria do canal | 3 | Último mês. Na ficha do Google, três últimos meses completos | Mostra o que foi feito e o que voltou |
| Contatos por mês | 5 | Média mensal dos últimos três meses | Mostra quanto chega |
| Prontos para comprar por mês | 7 | Média mensal dos últimos três meses | Mostra quanto amadurece |

Cada número leva a marca de origem: medido, estimado ou não acompanho. A exceção é a ficha do Google, em que o número só existe no painel. Eles informam e levantam pontos para o atendimento. Não mudam o nível nem a rota.

---

### 3. As Cinco Decisões

| Ponto | Sua resposta | Decisão |
|---|---|---|
| 1. Critério da rota proposta | "A, nível mais alto" | A rota proposta começa pelo caminho de nível mais alto |
| 2. Cliente que passou por dois caminhos | "A, como conheceu" | Cada cliente conta uma vez, pelo caminho por onde conheceu a empresa |
| 3. Respostas dos outros 24 canais | "Sim, validado" | Frase descrita e medida própria, como na seção 4 |
| 4. Cruzamento entre estrutura e resultado | "A, manter" | As leituras ficam, com base nova, como na seção 3.2 |
| 5. Caminho da Expansão | "Sim, validado" | Mesmo tratamento da Receita Nova, como na seção 5 |

#### 3.1. Complementos dos Pontos 1 e 2

**Ponto 1**

- A origem dos clientes aparece ao lado de cada caminho, como informação.
- No empate de nível, vale o texto que o exemplo já tem: começar pelo caminho que dá para manter com rotina.
- A rota continua sendo proposta. Quem confirma é o atendimento com o mentor.

**Ponto 2**

- Vale a resposta do próprio cliente sobre como conheceu a empresa.
- Quando ele citar dois caminhos, vale o primeiro que disser.
- Cliente de origem desconhecida entra como "não sei de onde veio". Ele não é repartido entre os caminhos, e a conta fecha com o total de clientes novos por mês informado na Etapa 1.

#### 3.2. O Cruzamento entre Estrutura e Resultado

- **Resultado:** "na meta" quando a média mensal dos últimos três meses alcança a meta que o próprio aluno definiu. Sai o corte de 80%.
- **Estrutura:** "adiantada" a partir do nível Captação. Motivo: é quando os contatos passam a ficar registrados no CRM, e só então dá para ligar o resultado ao caminho.
- **Qual nível entra na conta:** o do caminho mais adiantado.
- **Textos:** descrevem a situação e terminam com a pergunta que vai para o atendimento.

| Leitura | Quando aparece | O que diz |
|---|---|---|
| Estrutura com Resultado | Estrutura adiantada e clientes na meta | O caminho está de pé e o número de clientes está na meta. Para o atendimento: crescer no que funciona ou abrir um caminho novo? |
| Estrutura sem Resultado | Estrutura adiantada e clientes abaixo da meta | O caminho está de pé, e o número de clientes ainda não chegou à meta. Para o atendimento: o que explica a diferença? |
| Resultado sem Estrutura | Estrutura no começo e clientes na meta | O número de clientes está na meta, mas o caminho ainda não está de pé. Para o atendimento: de onde vem esse resultado, e como fazer para ele se repetir? |
| Começo | Estrutura no começo e clientes abaixo da meta | O caminho ainda não está de pé, e o número de clientes está abaixo da meta. O próximo passo mostra por onde começar |
| Falta o Número | Sem o número de clientes por mês ou sem a meta | Fica como está: não saber já é um resultado, e o primeiro passo é registrar |

Os nomes "Previsível" e "Esforço sem Retorno" deram lugar a "Estrutura com Resultado" e "Estrutura sem Resultado".

---

### 4. Os Outros 24 Canais

**Sua resposta: "Sim, validado".**

Em todos, a pergunta é "Como você faz isto hoje?". As respostas são quatro: "Não faço", a frase da coluna "Faço, sem rotina", a frase da coluna "De pé" e "Não sei". A coluna "De pé" usa o entregável que o exemplo já tem.

A medida própria é do último mês. O que é estado vai como está hoje: contas na lista, parceiros ativos, revendas ativas e nota na plataforma.

#### 4.1. Outbound

| Canal | Faço, sem rotina | De pé | Medida própria, no último mês |
|---|---|---|---|
| Disparo de E-mail | Envio de vez em quando, para quem aparece | Tenho lista com o perfil certo e uma sequência de e-mails | E-mails enviados e respostas |
| Disparo de WhatsApp | Mando quando lembro, sem lista | Tenho lista de quem já tem relação com a empresa e um roteiro de primeira mensagem | Mensagens enviadas e respostas |
| Ligação | Ligo quando sobra tempo | Tenho roteiro curto e um número de ligações por dia | Ligações feitas e conversas |
| Abordagem em Redes Sociais | Chamo um ou outro perfil, sem lista | Tenho lista de perfis e rotina de interação e mensagem | Perfis abordados e respostas |
| Porta em Porta | Visito quando passo perto | Tenho região definida, roteiro de visita e material para deixar | Visitas feitas e conversas com quem decide |
| ABM (Contas-Alvo) | Sei quais empresas quero, sem plano para cada uma | Tenho a lista de contas, quem decide em cada uma e um plano por conta | Contas na lista e contas com conversa aberta |
| Feiras e Eventos | Vou a eventos sem meta e sem retorno combinado | Tenho calendário, meta de contatos e retorno a todos em até dois dias | Contatos trazidos do último evento e quantos tiveram retorno |

#### 4.2. Branding

| Canal | Faço, sem rotina | De pé | Medida própria, no último mês |
|---|---|---|---|
| Blog | Publico quando dá | Publico um texto por mês que responde a uma dúvida real do cliente | Textos publicados e visitas |
| Podcast | Gravei alguns episódios, sem dia certo | Publico episódios com dia e duração fixos | Episódios publicados e ouvintes por episódio |
| YouTube | Tenho vídeos soltos | Publico com frequência definida, um vídeo para cada dúvida do cliente | Vídeos publicados e visualizações |
| Instagram | Tenho perfil, mas parado ou sem dizer o que faço | O perfil mostra o que faço, para quem e uma prova, e é atualizado toda semana | Publicações e mensagens recebidas pelo perfil |
| LinkedIn do Dono | Publico de vez em quando | Publico toda semana no meu perfil | Publicações e conversas iniciadas por lá |
| Comunidades | Tenho um grupo, mas parado | O grupo é ativo, com conteúdo útil e encontros | Participantes ativos |
| Imprensa e Prêmios | Já apareci, mas não divulguei nem busco de novo | Busco aparições e divulgo cada uma nas redes | Aparições nos últimos doze meses |

#### 4.3. Indicação e Parcerias

| Canal | Faço, sem rotina | De pé | Medida própria, no último mês |
|---|---|---|---|
| Indicação de Clientes | Recebo indicação, mas não peço | Peço a todo cliente satisfeito, com um texto pronto para encaminhar | Pedidos feitos e indicações recebidas |
| Programa de Indicação | Dou um agrado a quem indica, sem regra divulgada | Tenho programa com regra simples, divulgado para toda a base | Indicações recebidas pelo programa |
| Parceiros de Negócio | Um ou outro parceiro indica, sem combinado | Tenho lista de parceiros e um acordo de como um indica o outro | Parceiros ativos e indicações recebidas |
| Revendas e Representantes | Tenho quem revenda, sem material nem combinado por escrito | As revendas têm material, treinamento e comissão combinada por escrito | Revendas ativas e vendas feitas por elas |
| Marketplaces | Estou na plataforma, com anúncio simples | Tenho anúncios com foto, título e descrição caprichados onde o meu cliente compra | Pedidos e nota na plataforma |

#### 4.4. Base de Clientes

| Canal | Faço, sem rotina | De pé | Medida própria, no último mês |
|---|---|---|---|
| Oferta de Venda Adicional | Ofereço quando o cliente pergunta | Tenho a opção superior definida e o momento certo de oferecer | Ofertas feitas e aceitas |
| Oferta de Venda Cruzada | Ofereço complemento quando lembro | Tenho a lista do que se compra junto e combinações prontas | Ofertas feitas e aceitas |
| Campanha de Recompra | Lembro um ou outro cliente | Tenho lembrete programado para antes da data em que o cliente costuma precisar de novo | Clientes lembrados e clientes que compraram de novo |
| Reativação de Inativos | Chamo cliente antigo quando o movimento cai | Tenho a lista de inativos e uma ação de retorno que se repete | Inativos chamados e clientes que voltaram |
| Pós-Venda | Faço contato só quando há problema | Faço contato com todo cliente poucos dias depois da entrega | Contatos feitos e problemas encontrados |

Cada canal tem um ou dois números: o que foi feito e o que voltou. Eles levam a marca de origem e informam sem decidir nível nem rota. Em 13 canais, o segundo número é parte do primeiro, e a análise mostra o retorno do canal, como "2 em cada 10".

---

### 5. O Caminho da Expansão

**Suas respostas: "Sim, validado", para o caminho, e "Sim, aplicar", para o racional de medição e de registro.**

A Expansão é o caminho de vender mais para quem já é cliente. Tem as mesmas oito etapas e os mesmos cinco níveis.

| Etapa | Pergunta | Respostas descritas | Entregável, que serve de prova |
|---|---|---|---|
| 1. Objetivo | Quantas vendas por mês você quer fazer para quem já é cliente? | **Um número**, informado ou calculado junto | Uma meta mensal de vendas para quem já é cliente, escrita |
| 2. Pilar: Base de Clientes | Onde estão os contatos dos seus clientes? | Não tenho os contatos reunidos / Estão espalhados: celular, caderno, planilha / Tenho CRM, mas a base está incompleta / **Estão no CRM, com contato e data da última compra** | A base de clientes no CRM, com contato e data da última compra |
| 3. Canal: ação da base | Como você faz isto hoje? | As cinco ações da seção 4.4 | O entregável de cada ação |
| 4. Conversão | Como o cliente responde quando você faz uma oferta? | Não faço oferta direta / Faço, e ele precisa ligar ou passar na loja para fechar / **Faço uma oferta por vez, e ele aceita respondendo com uma palavra** | Uma oferta por vez, aceita com uma palavra |
| 5. Lead | O que você faz quando um cliente mostra interesse em comprar de novo? | Não registro / Guardo de cabeça ou na conversa / Tenho CRM, mas nem todo interesse entra / **Registro no CRM, com a data e o que ele quis** | O interesse de cada cliente registrado no CRM, com a data e o que ele quis |
| 6. Relacionamento | Como você mantém contato com quem já comprou? | Só falo quando ele me procura / Falo de vez em quando, quase sempre com oferta / Tenho uma cadência, mas não registro no CRM / **Sigo uma cadência mensal, com a próxima ação registrada no CRM** | Uma cadência mensal com a base, alternando conteúdo útil e oferta, com a próxima ação registrada no CRM |
| 7. Lead Qualificado | Como você sabe qual cliente está na hora de comprar de novo? | Espero ele voltar / Tenho uma noção, de cabeça / Sei o intervalo entre compras, mas não tiro a lista do CRM / **O CRM mostra quem já passou do intervalo normal entre duas compras** | O intervalo normal entre duas compras e, no CRM, a lista de quem já passou dele |
| 8. Medir e Ajustar | Como você acompanha as vendas para quem já era cliente? | Não separo cliente novo de cliente que voltou / Olho de vez em quando, sem registro / Confiro todo mês, em planilha ou de cabeça / **Tiro do CRM, todo mês, as vendas para a base e a ação que trouxe cada uma** | O relatório mensal do CRM: vendas para a base e a ação que trouxe cada uma |

**Como as decisões valem aqui**

- Ponto 1: a rota proposta começa pela ação de nível mais alto.
- Ponto 2: não se aplica. O retrato da Expansão é o tamanho da base de clientes.
- Ponto 4: vale igual. O resultado é o número de vendas para a base em relação à meta.
- Fluxograma: é o mesmo desenho. Muda só a prova da Etapa 2, que passa a ser a base de clientes no CRM.

**Os números da Expansão e a janela de cada um**

| Número | Etapa | Janela | Papel |
|---|---|---|---|
| Vendas para a base por mês e meta | 1 | Média mensal dos últimos três meses | Mostra a distância da meta |
| Quantos clientes há na base | 2 | Como está hoje | Retrato do tamanho da base |
| Medida própria da ação | 3 | Último mês | Mostra o que foi feito e o que voltou |
| Clientes que respondem por mês | 5 | Média mensal dos últimos três meses | Mostra quanto interesse aparece |
| Prontos para comprar de novo por mês | 7 | Média mensal dos últimos três meses | Mostra quanto amadurece |

---

### 6. O Racional de Medição e de Registro

**Sua resposta: "Sim, aplicar".**

Origem: na homologação da Tela 2, você mandou trocar os dez últimos clientes pela janela do mês, pediu um racional sistêmico de medição e pediu o registro no padrão de CRM, com a minha análise como mentor antes de aplicar.

#### 6.1. Medição: a Janela de Cada Número

| O que se mede | Janela | Exemplos | Motivo |
|---|---|---|---|
| O que a empresa colhe | Média mensal dos últimos três meses | Clientes novos, origem dos clientes, contatos e prontos para comprar | Um mês sozinho oscila. Três meses é o ciclo do Plano de 90 Dias |
| O que a empresa faz no canal | Último mês | Atividade, retorno e investimento do canal | Mostra a rotina atual do canal |
| Estado | Como está hoje | Tamanho da base, nota e quantidade de avaliações | É retrato, e não fluxo |

Duas regras fecham o racional:

- A origem dos clientes usa a mesma amostra do total da Etapa 1. Por isso o mapa de origem fecha com o total.
- Tudo é medido de novo a cada ciclo de 90 dias.
- Exceção aprovada depois, nas seções 6.8 e 6.10: as pessoas que viram a ficha do Google e as interações são lidas nos três últimos meses completos, com o percentual do Google sobre o ano passado.

#### 6.2. Os Resultados Que a Análise Entrega

| Resultado | De onde sai | Como aparece |
|---|---|---|
| Distância da meta | Clientes por mês e meta | "Faltam 12 por mês para chegar à meta" |
| Mapa de origem | Etapa 1 e Etapa 2 de cada caminho | "7 de 18" por caminho, com "não sei de onde veio" à parte |
| Conversão do caminho | Contatos, prontos e clientes do pilar | "De contato a pronto, 4 em cada 10; de pronto a cliente, 9 em cada 10" |
| Retorno do canal | As duas medidas do canal | "Retorno do canal: 2 em cada 10" |
| Evolução por ciclo | Medição a cada 90 dias | No exemplo, aparece só como aviso. A comparação entre ciclos depende do aplicativo |

Os resultados informam e levantam pontos para o atendimento. Não mudam o nível nem a rota.

#### 6.3. Registro: o CRM como Padrão

- O CRM é definido pela função, e não pela marca: um lugar só, em que cada contato tem origem, etapa, responsável, datas, próxima ação e histórico.
- Nas Etapas 5 a 8, de pé é o que está no CRM, com rotina.
- CRM sem rotina vale "em parte".
- Na Etapa 2, o levantamento cliente por cliente também vale como de pé. Foi recomendação minha, que você aceitou. O CRM é a melhor prova.
- "Medido" é o número que saiu do CRM ou do painel de uma ferramenta. "Estimado" é o número que veio de memória.

#### 6.4. O Que Foi Substituído

| Antes | Agora |
|---|---|
| Os dez últimos clientes como amostra da origem | Os clientes novos dos últimos três meses, a mesma amostra da Etapa 1 |
| "Tenho anotado, cliente por cliente" | "Tenho o levantamento, cliente por cliente" e "Tiro do CRM a origem de cada cliente". O "Tenho" foi ajuste seu na Tela 2: antes estava "Fiz" |
| Lista única de contatos, na Etapa 5 | Todo contato no CRM, com origem e responsável |
| Sequência de mensagens, na Etapa 6 | Cadência escrita, com a próxima ação registrada no CRM |
| Critério escrito, na Etapa 7 | Critério escrito e etapa de pronto para comprar no CRM |
| Conferência mensal por canal, anotada, na Etapa 8 | Relatório mensal por canal, tirado do CRM |
| Perguntas de número sem janela | Cada número com a sua janela, como na seção 6.1 |

#### 6.5. Apresentação dos Números

**Seu pedido na Tela 1: "ajuste os numeros para pegar mascara dos milhares ex 7.500". Sua resposta depois de ver: "aprovado, pode passar proximo".**

- Todo campo de número mostra a máscara enquanto a pessoa digita: ponto nos milhares e vírgula nos decimais.
- Todo número que a tela devolve segue a mesma máscara, como "meta de 1.200 por mês".
- O número guardado não muda. A máscara é só a forma de mostrar.
- Percentual, por pedido seu na Tela 3: o campo mostra o sinal de % fixo, como o R$ do dinheiro. O sinal digitado não entra, e saiu o texto "Digite só o número, sem o sinal".
- Regra que você mandou guardar: "sempre use as máscaras nos números".

#### 6.6. Nome do Pilar nas Perguntas e Leituras

**Seu pedido na Tela 2: "precisa especificar melhor, veio por onde? indique pelo seu inbound (ajuste para trazer o nome que ele indicou)".**

- Toda pergunta e toda leitura de número diz o nome do pilar que o aluno escolheu, no lugar de "este caminho" e "este pilar".
- Exemplo: "Desses Clientes Novos por Mês, Quantos Chegam pelo Inbound?".
- "Este caminho" continua só onde o texto fala do percurso feito, como em "Você chegou ao fim deste caminho".

#### 6.7. Abertura da Etapa 3

**Seu pedido na Tela 3:** deixar explícito que a escolha é de um canal por vez e que quem usa mais de um volta para escolher outro, ou finaliza. Você pediu a minha análise da frase, com ajuste de concordância e de lógica.

- Receita Nova: "No Inbound temos estes canais. Escolha um deles para percorrer agora. Se você usa mais de um, não se preocupe: no fim deste caminho, você volta e escolhe outro, ou finaliza."
- Expansão: "Na Base de Clientes temos estas ações. Escolha uma delas para percorrer agora. Se você faz mais de uma, não se preocupe: no fim deste caminho, você volta e escolhe outra, ou finaliza."
- Ajustes meus na sua frase: "fluxo" virou "caminho", porque "fluxo" é o nome do resultado final. "Retornará para escolher ou finalizar" virou "volta e escolhe outro, ou finaliza", para a frase não dizer que é preciso voltar para finalizar.

#### 6.8. A Ficha do Google

**Suas respostas: "Sim, três meses", para a janela, e "Sim, aplicar", para o modelo.**

Origem: o parecer `docs/Aceleracao-365-Parecer-da-Ficha-do-Google-2026-11-06.md`, feito em outra sessão a seu pedido, mais cinco ajustes meus. O pedido que deu origem ao parecer: perguntas objetivas, que mostrem se está crescendo em qualquer tipo, faturamento e tamanho de negócio.

**As cinco perguntas**

| # | Pergunta | Respostas |
|---|---|---|
| 1 | O Google ainda pede algo para completar o seu perfil? | **Não pede mais** / Ainda pede / Não tenho ficha / Não sei |
| 2 | Quando foi a sua última publicação na ficha? | **No último mês** / Há mais tempo / Nunca publiquei / Não sei |
| 3 | Alguma avaliação está sem resposta? | **Nenhuma** / **Não tenho avaliações** / Tenho sem resposta / Não sei |
| 4 | Quantas Pessoas Viram a Ficha nos Três Últimos Meses Completos? (corrigido na seção 6.10) | Número / Não sei |
| 5 | Sobre o Ano Passado (compactado na seção 6.10) | Subiu, com o percentual / Caiu, com o percentual / O Google não mostra |

- Apoio da pergunta 1: "No painel da sua empresa no Google, clique em Força do Perfil. Se o Google abrir instruções do que preencher, ele ainda pede."
- Apoio da pergunta 4: "Hoje são agosto, setembro e outubro. O mês atual fica de fora, porque ainda não terminou. No painel, abra Desempenho e escolha esses meses no Período." O app calcula os meses pela data do dia.

**Onde conferir, por pedido seu na Tela 3**

Cada pergunta tem um ponto de interrogação que abre o caminho para achar a informação no Google.

| Pergunta | Caminho que o ponto de interrogação mostra |
|---|---|
| 1. Perfil | Entrar com a conta que administra a ficha, pesquisar o nome da empresa e, no painel "Sua empresa no Google", clicar em Força do Perfil |
| 2. Última publicação | No painel, clicar em Posts e ver a data da mais recente em "Suas postagens" |
| 3. Avaliações | No painel, clicar em Ler avaliações e abrir a aba Não respondido |
| 4. Pessoas que viram | No painel, clicar em Desempenho, escolher em Período só os três últimos meses completos e copiar o número de pessoas em "Como as pessoas descobriram sua empresa" |
| 5. Percentual | Com o período escolhido, ver o percentual logo abaixo do total |

Cada caminho termina com o aviso: "Caminho visto no Google pelo computador, em novembro de 2026. Os nomes podem mudar."

**A ficha, que decide o "de pé" da etapa**

| Situação | Quando |
|---|---|
| De pé | Os três fatos em dia |
| Em parte | Algum fato em falta |
| Falta | Não tem ficha |
| Não sei | Nenhum em falta, mas algum por conferir. A rota manda conferir e voltar |

**A procura, que só informa**

| Pessoas que viram nos três meses | Crescendo | Estável | Caindo |
|---|---|---|---|
| 200 ou mais | Acima de +10% | De -10% a +10% | Abaixo de -10% |
| De 30 a 199 | Acima de +20% | De -20% a +20% | Abaixo de -20% |

Com menos de 30 pessoas, a tela diz "pouco volume". Sem percentual do Google, o número vira a base do próximo ciclo.

**O que saiu**

- As opções "Completa e com novidade toda semana", "Completa, mas parada" e "Incompleta".
- As frases "Ficha parada chama menos atenção do que a do vizinho" e "continua trazendo contato", na leitura deste canal.
- A marca medido ou estimado, neste canal.
- No canal Avaliações do Google, o trecho "e resposta a todas" do entregável.

**Limites da prova**

- O comportamento do painel do Google foi visto em uma ficha só, em um dia.
- A ajuda do Google confirma o caminho pela Força do Perfil. Ela não diz o que uma ficha completa mostra.
- Se o Google pedir item que não serve ao negócio, o mentor decide no atendimento.

**Pontos de coerência que não apliquei**

- O "Por Que Ele Importa" do canal ainda diz "Ficha incompleta ou parada passa a imagem de empresa fechada".
- No Fim do Caminho, o texto geral do canal em parte ainda diz "ainda não tem rotina".
- A leitura geral dos outros 24 canais ainda diz "continua trazendo contato".

#### 6.9. Ordem das Respostas

**Seu pedido na Tela 3: "ajuste o racional das respostas sempre da ordem do mais completo ou idela, até menos completo e menos ideal".**

- Em toda pergunta, as respostas aparecem da mais completa ou ideal para a menos completa. "Não sei" fica por último.
- Vale para as etapas, para os 32 canais e para a Expansão.
- Quando duas respostas valem igual para o nível, vem antes a que traz a melhor prova, como "Tiro do CRM a origem de cada cliente" antes de "Tenho o levantamento, cliente por cliente".
- Nas tabelas das seções 2 e 5 deste documento, as frases estão listadas da menos completa para a mais completa. Na tela, a ordem é a inversa.

#### 6.10. A Etapa 4 da Ficha do Google e a Correção da Etapa 3

**Sua resposta: "Sim, aplicar", sobre a lista de 23 itens.**

Origem: o parecer `docs/Aceleracao-365-Parecer-da-Etapa-4-Conversao-2026-11-06.md`, feito em outra sessão a seu pedido, com o retorno do CRM em operação e sete ajustes meus.

**A correção da Etapa 3.** Interação já é conversão, e procura é quem viu a ficha. As perguntas 4 e 5 passam a ser as pessoas que viram a ficha e o percentual do Google sobre elas. Os três fatos não mudam.

**A Etapa 4.** A conversão passa a ser escrita por canal. Por enquanto, só no Google Meu Negócio.

| # | Pergunta | Resposta |
|---|---|---|
| 1 | Quantas Interações a Ficha Teve nos Três Últimos Meses Completos? | Número e percentual do Google, com Subiu ou Caiu |
| 2 | Qual porta teve o maior número nestes meses? | Chamadas / Orientações / Cliques no website / Outro botão / Não sei |
| 3 | O teste da porta marcada | Tabela abaixo |

| Porta | Teste | Respostas |
|---|---|---|
| Chamadas | Ligue de outro celular para o número da ficha, em horário de atendimento | **Uma pessoa atendeu** / Ninguém atendeu / O número não funciona / Não testei |
| Orientações | Trace a rota no celular até a sua empresa | **Levou à entrada certa, e a foto da fachada mostra onde é** / Levou, mas não há foto da fachada / Levou ao lugar errado / Não testei |
| Cliques no website | Toque em Site na ficha, pelo celular | **Cheguei ao contato com um toque, no número ou formulário que a empresa atende** / Precisei procurar / Não abriu ou foi para outro número / Não testei |
| Outro botão | Toque nesse botão na ficha, pelo celular | **Cheguei a quem atende** / Travou no caminho / Não testei |

**Regras**

- De pé é a porta principal passar no teste. Em negrito, a resposta que põe de pé.
- "Não testei" e "Não sei" levam a conferir e voltar.
- O número de interações e a conta de quantos agiram informam. Não decidem nível nem rota.
- Na porta do site e em Outro botão, com o teste aprovado, aparece o tempo até uma pessoa responder: máscara "min", opcional, sem régua. Saudação automática não conta.
- A leitura mostra cerca de quantos agiram em cada 100 que viram, comparado ao ano passado, a porta principal, por onde começar e a pergunta para o atendimento.
- A busca "restaurantes" e qualquer número do CRM em operação ficam fora da tela.

**A forma, por sua resposta "Sim, compactar"**

- Os quatro dados ficam, porque cada um entrega algo. O que se repetia era o jeito de perguntar.
- A comparação vira o rótulo "Sobre o Ano Passado", com os botões na mesma linha e o campo "Percentual" logo abaixo, nas duas telas.
- O apoio da Tela 4 passa a ser "Os mesmos meses da etapa anterior."
- Quando a Tela 4 traz a comparação, só a pergunta dela vai para o atendimento.

**O que a ajuda do Google confirma (texto presente, lido em 06/11/2026)**

- Chat e histórico de ligações acabaram em 31/07/2024.
- "Chamadas" conta o clique no botão, e não a ligação concluída.
- Na visualização, uma pessoa é contada uma vez por dia. Por isso a conta de cada 100 é aproximação.
- Mensagens e Agendamentos também existem como métricas, o que justifica a porta Outro botão.

**O que não está provado**

- Tudo o que veio do painel foi visto em uma ficha, em um dia. A ajuda do Google não fala do percentual sobre o ano passado.
- Nenhum teste foi feito com dono de empresa, e os nomes dos botões no celular não foram vistos em um celular.
- As lições do CRM em operação para as Etapas 2, 5, 6 e 8 ficam na seção 5 do parecer, para quando cada etapa chegar.

#### 6.11. A Etapa 5 na Receita Nova

**Sua resposta: "Sim, aplicar".**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | O que acontece com o contato de quem se interessa? | As quatro frases da seção 2 e Não sei | Todos |
| 2 | Mande uma mensagem de outro número, como um cliente novo. No dia seguinte, procure esse contato no CRM. O que aconteceu? | **Entrou, com origem e responsável** / Entrou, mas falta origem ou responsável / Não entrou / Não testei | Quem tem CRM |
| 3 | Quantos contatos novos chegam por mês pelo pilar? | Número, com marca de origem | Todos |
| 4 | Desses, quantos têm origem e responsável no CRM? | Número ou Não sei | Quem tem CRM |

**Regras**

- De pé é a frase "Todo contato entra no CRM" com o teste aprovado.
- CRM sem rotina continua em parte, mesmo com o teste aprovado.
- "Não testei" leva a conferir e voltar.
- O teste é da empresa: vale em todos os caminhos.
- Os números informam. Não decidem nível nem rota.
- A leitura avisa quando a conta sai de número estimado.
- Na ficha do Google, a pergunta para o atendimento liga a Tela 4 à Tela 5: "A ficha teve cerca de 120 interações por mês, e você conta 20 contatos no Inbound. Quem pediu rota e apareceu virou contato?"
- Saíram "se perde em poucos dias" e "chegam e se perdem".

**O que não está provado**

- O teste vem de defeitos vistos em um CRM, e nunca foi feito com dono de empresa.
- A Expansão continua como estava na seção 5.

#### 6.12. A Etapa 6 na Receita Nova

**Sua resposta: "Sim, aplicar".**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | O que você faz com quem se interessou e não comprou? | As quatro frases da seção 2 e Não sei | Todos |
| 2 | Abra no CRM os contatos em aberto. Quantos têm próxima ação com data? | **Todos** / A maioria / Poucos ou nenhum / Não consigo ver essa lista / Não sei | Quem tem CRM ou marcou que registra nele |
| 3 | Quantos contatos estão em aberto hoje? | Número ou Não sei, como está hoje | Quem tem CRM ou marcou que registra nele |

**Regras**

- De pé é a frase "Sigo uma cadência, com a próxima ação registrada no CRM" com a resposta "Todos".
- Cadência fora do CRM continua em parte.
- "Não sei" leva a conferir e voltar.
- A conferência e o número são da empresa: valem em todos os caminhos.
- O número informa. Não decide nível nem rota.
- A leitura mostra quantas pessoas por mês se interessam e não compram, com os números das Etapas 2 e 5, e o ticket como valor de cada uma que voltar. O valor não é promessa de venda.
- Saíram "A maioria não compra no primeiro contato", "Quem volta a falar fica com a venda" e "Quem não recebe retorno compra de quem lembrou primeiro".

**O que não está provado**

- A lição de que contato parado não aparece como perda vem de um CRM, e não de uma amostra do mercado.
- A pergunta da próxima ação nunca foi feita com dono de empresa.
- A Expansão continua como estava na seção 5.

#### 6.13. MQL na Etapa 6 e SQL na Etapa 7

**Seu pedido: "aqui nestas duas etapas temos que falar de MQL e SQL". Suas respostas: "Sim, 6 e 7" e "pode executar".**

| Etapa | Ao sair dela, a pessoa é | O que isso quer dizer |
|---|---|---|
| 5. Lead | Lead | Contato registrado, com origem e responsável |
| 6. Relacionamento | MQL, lead qualificado pelo marketing | Tem o perfil do cliente e mostrou interesse |
| 7. Lead Qualificado | SQL, lead qualificado para vendas | Quem vende confirmou: quer comprar, pode decidir e pediu preço ou prazo |

**Tela 6:** entra "Quantos Desses Contatos Viram MQL por Mês?", na média dos três últimos meses, com marca de origem.

**Tela 7**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Como você sabe quem está pronto para comprar? | As quatro frases da seção 2 e Não sei | Todos |
| 2 | Abra o critério escrito. O que ele diz? | **O que é MQL e o que é SQL** / Só o que é MQL / Só o que é SQL / Não achei o critério escrito / Não sei | Quem marcou critério escrito |
| 3 | Quantos Viram SQL por Mês? | Número, com marca de origem | Todos |

**Regras**

- De pé é a frase do critério com etapa no CRM, e o critério dizendo o que é MQL e o que é SQL.
- "Não sei" leva a conferir e voltar.
- Os números informam. Não decidem nível nem rota.
- A leitura mostra o funil e divide quem não compra pelos trechos. O ponto para o atendimento aponta o trecho em que mais da metade para.
- O entregável passa a ser "Um critério escrito de MQL e de SQL, e as duas etapas no funil do CRM".
- As siglas aparecem com ponto de interrogação, e o nome em português fica na explicação.
- Por pedido seu, o significado de MQL e de SQL também está na primeira frase de "O Que Esta Etapa Faz", nas duas telas.
- Nos dados, o número de prontos para comprar passa a ser o de SQL.

**O que não está provado**

- As definições são as usuais do mercado, de conhecimento meu, sem fonte conferida e sem o método dos mentores.
- A conferência do critério nunca foi feita com dono de empresa.
- Na Expansão, nada mudou. Ela ainda diz "Os outros ainda não estão na hora", frase que saiu da Receita Nova.

#### 6.14. A Etapa 8 na Receita Nova

Aplicada com a sua aprovação em 06/11/2026 ("Sim, aplicar") e aceita na homologação em 07/11/2026 ("Aceito, seguir").

- As quatro respostas continuam, da mais completa para a menos, com "Não sei" por último.
- Quem marca "Tiro do CRM" ou "Confiro todo mês" abre o relatório e responde duas perguntas: "Abra o relatório do último mês. O que ele mostra?" e "Qual foi a última decisão tirada desse relatório?".
- A etapa só fica de pé com a frase do CRM, o relatório com contatos, MQL, SQL e clientes por canal, e uma decisão no último mês. "Não sei" leva a conferir e voltar.
- A leitura conta quantos números do caminho foram medidos e quantos são estimativa. Isso informa e não muda o nível nem a rota.
- O Como Fazer passa a dizer MQL e SQL no lugar de "os prontos", com três passos novos: definir o número antes de olhar, registrar o motivo ao encerrar e não contar venda desfeita como cliente.
- Para o atendimento, quem tem o relatório leva "Qual número foi combinado para cada canal antes de olhar o relatório?". Quem tem o relatório ou CRM leva "Toda semana entram contatos com a marca do canal?".
- O entregável passa a ser o que cada canal trouxe, do contato ao cliente, e a decisão do mês. Saiu "o que foi investido", que a tela não pergunta.
- Saiu "O que não é medido não melhora", também da explicação da etapa.
- O fluxograma passa a dizer "prova: relatório do CRM por canal, com decisão".

**O que não está provado**

- Os passos novos e as duas perguntas para o atendimento vêm dos defeitos de um CRM em operação. Não são referência de mercado e nunca foram testados com dono de empresa.
- A conferência do relatório nunca foi feita com dono de empresa, e o nome da área de relatórios muda de um CRM para outro.
- "O número depende de alguém montar a conta, e por isso atrasa ou falha" é frase anterior a esta rodada, sem prova.
- A Expansão segue sem a conferência do relatório. Ela só herdou a explicação da etapa, que é comum aos dois caminhos.

#### 6.15. O Fim do Caminho

Aplicado com a sua aprovação em 07/11/2026 ("Sim, aplicar") e aceito na homologação no mesmo dia ("Aceito, seguir").

- A frase do nível diz a causa desta empresa. Persona: "Você tem meta, mas o pilar ainda não está de pé." Sem meta: "Falta a meta." No Nível 2, sai "com rotina". No Nível 4, a frase diz só o que falta de verdade, por exemplo "Falta a medição".
- Onde a Rota Quebra diz como estão as etapas depois da quebra, em faixas: "Depois dela, as Etapas 3 a 8 estão em parte." Diz também se o nível sobe ou se só a rota avança quando a etapa da quebra ficar de pé, conforme os cortes do nível.
- A decisão do atendimento começa pelo próximo passo quando ele não é o canal: "Confirmar o próximo passo, a Etapa 2 (Pilar). Depois, decidir o que cuidar primeiro na ficha...". Quando a quebra é no canal, fica a decisão do canal.
- O motivo do próximo passo em etapa em parte passa a ser a leitura da resposta dada. Saíram "Esta etapa existe, mas ainda não tem rotina" e "O canal existe, mas ainda não tem rotina". Na ficha do Google, o motivo é a leitura dos três pontos; em canal com rotina e sem medir, "O canal tem rotina, mas o resultado ainda não é medido".
- Nada disso muda o nível nem a rota.

**O que não está provado**

- A troca do motivo vale também para a Expansão, porque a função é a mesma. As leituras da Expansão não passaram por esta homologação.
- A definição geral dos níveis, que abre no ponto de interrogação, não mudou.

#### 6.16. O Fluxo Adequado

Aplicado com a sua aprovação em 07/11/2026 ("Sim, aplicar"). Aguarda o aceite na homologação.

- O mapa de origem marca os números estimados. Persona: "Os 18 por mês e os 7 do Inbound são estimativa." Número medido não recebe marca.
- O mapa conta por pilar. A linha do resto passa a "Pilares que você ainda não percorreu", e a nota diz "a parte de cada pilar nos clientes novos por mês. Cada cliente conta no pilar por onde conheceu a empresa."
- O aviso de soma acima do total passa a "Somando os pilares", na tela final e na Etapa 2, porque nas duas a soma é por pilar.
- O cartão do caminho diz que o número é do pilar inteiro: "Inbound: 7 de 18 clientes por mês", no lugar de "origem: 7 de 18 por mês".
- O subtítulo com um caminho passa a "Com dois ou mais, o app compara os caminhos e diz qual vem primeiro."
- Nada disso muda o nível, a rota, a leitura nem o próximo passo.

**O que não está provado**

- A tela com dois caminhos ou mais não foi vista nesta persona. A frase de empate, "Comece pelo que você consegue manter com rotina", fica para o lote dos outros canais.
- A nota "Como o app chega a isto" continua longa. Fica para a rodada de design.

#### 6.17. Sugestões do Parecer Externo no Fluxo Adequado

Aplicado com a sua aprovação em 07/11/2026 ("siga as sugestões"), depois do parecer do ChatGPT (`docs/Aceleracao-365-Parecer-Externo-ChatGPT-Fluxo-Adequado-2026-11-07.md`) e da minha validação dele. Aguarda o aceite na homologação.

**1. Etapas 1 e 2 como base da empresa**
- As respostas já eram herdadas pelo caminho novo. O que mudou é a comparação: o nível continua pela sequência, mas o empate de nível se resolve pelo canal de pé até mais longe, da Etapa 3 em diante.
- Frase do desempate: "Os caminhos estão no mesmo nível. No canal, X está de pé até mais longe, e a rota segue por ele."
- Empate de verdade, no nível e no canal: "A escolha fica para o atendimento, com o mentor." Saiu "Comece pelo que você consegue manter com rotina".
- O passo da base da empresa aparece uma vez, sem repetir por caminho, e sem "No caminho X".
- O ponto de interrogação do Fluxo Adequado e a nota "Como o app chega a isto" dizem a regra do empate.

**2. Ajustes simples em paralelo**
- No máximo dois, tirados dos fatos já levantados: primeiro o teste da porta, depois as avaliações sem resposta, o perfil e a publicação.
- Não entram os da etapa que já é o próximo passo.
- Texto: "Ajustes Simples em Paralelo: ... Eles não mudam o próximo passo nem o nível."
- Persona: a foto da fachada e as avaliações sem resposta.
- Aparece também no Fim do Caminho, porque o próximo passo é o mesmo componente.

**3. Tela final em três blocos**
- **Onde Você Está:** o resultado com a marca de estimativa, o mapa de origem, a base da empresa, a leitura das duas medidas e a nota.
- **Cartão do caminho:** "1 de pé, 7 em parte", no lugar de "1 de 8 etapas de pé".
- **O Que Falta:**
  - uma linha por bloco que não está de pé (Base da Empresa, Canal, Contatos e Medição), tirada das respostas e das conferências;
  - o mapa das oito etapas abre em "Ver as Oito Etapas".
- **Seu Próximo Passo:** o passo, o motivo, o entregável, a tarefa, "Depois: Etapas 3 (Canal) e 4 (Conversão)" e os ajustes em paralelo.
- **Saíram:** o bloco "A Rota Proposta" e o título "De Onde Vêm os Seus Clientes".
- **Linha do resto no mapa de origem:** passou a "Fora do Inbound, por diferença", ou "Fora dos pilares percorridos, por diferença". Isso substitui o "Pilares que você ainda não percorreu" da seção 6.16.
- **Motivo da Etapa 2:** "Esta etapa vem antes do canal: sem saber de onde vem cada cliente, não dá para saber onde vale pôr esforço." Saiu a frase da prova, porque o entregável logo abaixo já diz.
- **Tarefa da Etapa 2:** "Comece o levantamento dos clientes novos dos últimos três meses, cliente por cliente, e registre como cada um conheceu a empresa. Quem você não souber, registre como não identificado."
- Nada disso muda o nível nem o próximo passo da persona.

**Escolhas minhas que passam pela sua validação**
- Os quatro blocos do O Que Falta e a ordem de prioridade dos ajustes.
- O nome "Seu Próximo Passo" ficou no lugar de "Por Onde Começar", para ser igual ao do Fim do Caminho.
- A frase do motivo da Etapa 2 e a do empate de verdade.

**O que não está provado**
- A tela não foi testada com dono de empresa nem com mentor.
- O caso de dois caminhos foi visto com um segundo caminho montado por mim (Indicação de Clientes), e não com respostas reais.
- As taxas do funil no Fim do Caminho ("6 em cada 10") continuam sem a ressalva de estimativa. Fica como ajuste menor.

#### 6.18. A Tela Final como Jornada

Aplicado com a sua aprovação em 07/11/2026 ("Sim, aplicar a jornada"), depois de você achar a tela "muito confusa" e pedir "quase que uma jornada". O ChatGPT avaliou o seu print, que era da versão antiga. Pela minha medição, a versão de três blocos tinha ficado mais longa: 571 palavras, contra 372. O modelo aprovado está em `docs/Aceleracao-365-Modelo-Jornada-Fluxo-Adequado-2026-11-07.html`. Esta seção substitui a apresentação da 6.17. As regras da 6.17 continuam valendo: a base da empresa, o desempate e os ajustes em paralelo.

**Primeira camada, em linguagem do dono**
- **Barra das oito etapas:** com "Você está na Etapa 2 de 8".
- **01 Sua Meta:** o número de hoje, com a marca de estimativa, a meta e "Faltam 12 clientes novos por mês".
- **02 O Que Você Já Tem:**
  - abre com "Você já começou." e lista uma linha por etapa de pé ou em parte, dizendo o que existe;
  - a etapa fica sem linha quando a resposta não sustenta o que existe;
  - embaixo, o nível ("Nível 1 de 5 · Improviso") e "1 de pé, 7 em parte".
- **03 O Que Pede Atenção:**
  - as três primeiras etapas que não estão de pé, na ordem da rota, com o nome do dono ("De onde vêm os clientes", "Sua ficha no Google", "Porta de entrada");
  - a primeira leva "comece aqui", e as demais aparecem como "Mais 4 pontos no diagnóstico completo".
- **04 Seu Próximo Passo:**
  - é o único destaque dourado;
  - começa pela etapa do método e pela ação do dono ("Descubra de onde vêm os seus clientes");
  - traz o motivo, "Esta semana", "Leve ao mentor" (o entregável), "Em paralelo, se quiser" e "Depois";
  - com dois caminhos, a frase da comparação abre o cartão.
- **Botões:** "Avaliar outro caminho" e "Voltar à Jornada". Saíram "Percorrer mais um caminho" e "Explorar pilares e canais".

**Segunda camada, Meu Diagnóstico Completo (fechada)**
- A origem dos clientes, com a marca de estimativa e "Fora do Inbound, por diferença".
- O caminho ou os caminhos percorridos.
- As oito etapas com o que falta em cada uma, e a leitura das duas medidas.
- A nota "Como o app chega a isto".

**Mudou também no Fim do Caminho**
- O próximo passo é o mesmo componente e ganhou o mesmo formato.
- O motivo da Etapa 2 ficou "Antes de decidir onde pôr esforço, confira de onde vem cada cliente. Hoje isso está só na memória."
- Saiu a nota "No aplicativo, este passo vira a rota proposta" do cartão. Na tela final, ela foi para a linha de rodapé.

**Escolhas minhas que passam pela sua validação**
- Os nomes do dono para as oito etapas: Sua meta, De onde vêm os clientes, o nome do canal, Porta de entrada, Registro dos contatos, Retorno aos contatos, Quem está pronto para comprar e Medir e decidir.
- O título de ação de cada etapa.
- As frases de "O Que Você Já Tem".
- A leitura das duas medidas ficou na segunda camada. Ela foi decisão sua, e você decide se volta para a primeira.

**Aceite**
- Você aceitou a tela validando no celular, em 07/11/2026: "Demais ficou ótimo... Aprovado com esta correção".
- A correção, já aplicada, foi o ponto 1: no 01 Sua Meta, a meta vem primeiro e o número de hoje depois, com o rótulo "na média dos últimos três meses".
- O registro está em `docs/Aceleracao-365-Pontos-da-Validacao-no-Celular-2026-11-07.md`.
- Com isso, fecha o fluxo do Google Meu Negócio.

**O que não está provado**
- A tela não foi testada com dono de empresa nem com mentor.
- A largura de 900 px sugerida pelo ChatGPT não foi aplicada, porque o exemplo é de celular.

#### 6.19. O Canal Google Ads

Aplicado em 07/11/2026 com o seu "Sim" sobre o esqueleto em tabela, com os quatro acréscimos do CRM em operação que eu recomendei. É o primeiro canal do lote que leva os outros canais ao nível do Google Meu Negócio. Aceito por você na homologação, pelas fotos, em 07/11/2026 ("Ok").

**Fontes e tipo de prova**
- **Texto presente na ajuda do Google Ads, lida em 07/11:**
  - os caminhos de Termos de Pesquisa, de Páginas de Destino e de Metas, Conversões e Resumo;
  - a ação principal entra na coluna Conversões e nos lances, e a secundária não;
  - no pré-pagamento, o anúncio para quando o saldo acaba;
  - o relatório de termos mostra só os termos usados por um número significativo de pessoas;
  - o Google pede para não pesquisar o próprio anúncio e indica a ferramenta de visualização.
- **Tela observada na conta lida em 05/11:** as colunas do painel, as ações de clique marcadas como principais, o anúncio reprovado e a conta parada sem saldo.
- **Aprendizados do CRM em operação:** vêm da régua aplicada a essa conta e da seção 5 do parecer da Etapa 4. Nenhum número do CRM em operação vai para a tela.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Os seus anúncios no Google rodaram no último mês completo? | **Rodaram o mês inteiro** / Pararam em alguns dias / Não rodaram, mas já anunciei / Nunca anunciei no Google / Não sei | Todos |
| 2 | Por que você parou? | Ficou caro / Vinha contato que não comprava / Faltou tempo para cuidar / Não sei | Quem parou |
| 3 | Abra os termos de pesquisa do último mês e leia os dez com mais cliques. Eles são de quem procura o que você vende? | **Todos são** / Alguns não têm a ver / A maioria não tem a ver / Não sei | Quem rodou |
| 4 | Quanto Você Investiu nos Três Últimos Meses Completos? | Número / Não sei | Quem rodou |
| 5 | Quantos Cliques os Anúncios Tiveram Nesses Meses? | Número / Não sei | Quem rodou |

- **De pé:** as duas respostas em negrito. Em parte quando um dos dois pontos falha. Falta para quem parou ("parou") e para quem nunca anunciou ("não usa"). "Não sei" leva a conferir e voltar.
- **Números:** investimento e cliques vêm do painel, sem a marca de medido ou estimado. Mostram o custo por clique, informam e não decidem nível nem rota.
- **Entregável:** "O anúncio no ar o mês inteiro, com os termos de pesquisa do último mês revisados."
- **Para o atendimento:** a pergunta dos termos ou da parada. O motivo de ter parado vira pergunta, e saíram as três frases que afirmavam causa.

**Etapa 4, Conversão**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | O que a sua conta conta como conversão principal? | Contato registrado no CRM / Formulário enviado ou ligação / Toque em botão de WhatsApp, telefone ou rota / Nenhuma conversão configurada / Não sei | Quem rodou |
| 2 | Quantas ações de conversão estão marcadas como Principal? | Uma só / Mais de uma / Não sei | Quem tem conversão configurada |
| 3 | Quantas Conversões a Conta Registrou nos Três Últimos Meses Completos? | Número / Não sei | Quem tem conversão configurada |
| 4 | Abra no celular, pelo endereço e sem pesquisar o anúncio, a página que mais recebeu cliques. O que aconteceu? | **Cheguei ao contato com um toque, no número ou formulário que a empresa atende** / Precisei procurar / Não abriu ou foi para outro número / Não testei | Todos. Quem não roda testa a página para onde o anúncio levaria, com a resposta "Não tenho essa página" |
| 5 | Quanto Tempo Levou Até Uma Pessoa Responder? | Minutos / Ninguém respondeu até agora | Teste aprovado, opcional |

- **De pé:** o teste da página aprovado, como na ficha do Google. A conversão principal e os números informam.
- **Leitura:** quantos em cada 100 cliques viraram conversão, o custo por conversão, o que a conversão conta e o aviso de mais de uma ação principal.
- **Para o atendimento:**
  - Com toque em botão: "Quantas viraram conversa de verdade?"
  - Sem conversão configurada: "Como você sabe hoje o que o anúncio traz?"
  - Com contato de verdade e ticket conhecido: "De cada quantas conversões sai uma venda?"
- **Exemplo Real:** é a conta lida em 05/11, anônima e sem valor em reais.

**Etapa 5, só no caminho do Google Ads e para quem tem CRM:** entra o campo "Desses, Quantos Entraram no CRM com a Origem Google Ads?". A pergunta para o atendimento cruza as conversões por mês com esse número: "Onde ficaram as outras 6?" na persona.

**Tela final:** o dono lê "Seus anúncios no Google" e "Cuide dos seus anúncios no Google". Os ajustes em paralelo seguem esta ordem: o conserto da página, as buscas que não têm a ver, as ações principais e a parada, no máximo dois.

**Prova:** 301 conferências, todas passaram. São 28 novas do Google Ads, e o Anúncio Meta continua no molde antigo até a vez dele.

**A frase do empate na tela final.** Aplicada em 07/11/2026 com a sua resposta "siga sua sugestão":
- No empate de verdade entre caminhos, o bloco 02 diz "No caminho X, o primeiro que você percorreu:", e não mais "por onde a rota segue". Antes, a frase contradizia "A escolha fica para o atendimento".
- Sem empate, a frase continua "por onde a rota segue".
- Para a frase ser sempre verdadeira, saiu o desempate pela quantidade de etapas de pé. No empate de verdade, a ordem é a dos caminhos percorridos.
- Nível, rota e próximo passo não mudam.
- Prova com 304 conferências, todas passaram.

**O que não está provado**
- Os caminhos de onde conferir vêm da ajuda do Google, e não de uma tela vista. A leitura "dia sem custo é dia sem anúncio", no gráfico, é minha.
- A duração mínima de ligação que conta como conversão é definida pela conta. O padrão não foi confirmado.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.20. O Canal Anúncio Meta

Aplicado em 07/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o segundo canal do lote. Aceito por você na homologação, pelas fotos, em 07/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- **Texto presente na ajuda da Meta, lida em 07/11, em português e sem login.** Doze itens conferidos:
  - as colunas Valor usado, Resultados e Veiculação;
  - o anúncio para quando o saldo pré-pago acaba e pausa quando o pagamento falha;
  - a coluna Resultados conta o que a meta escolhida pede;
  - conversa iniciada é a primeira mensagem, ou a primeira depois de sete dias sem conversa;
  - os cadastros ficam na Central de Leads e só podem ser baixados até 90 dias depois do envio;
  - a Biblioteca de Anúncios é aberta a qualquer pessoa.
- **Correções de nome tiradas da ajuda:** "Turbinar" no lugar de "Impulsionar", o objetivo "Leads" e a métrica "Valor usado".
- **Aprendizados do CRM em operação, como regra, sem nenhum número dele na tela:**
  - a conversa do anúncio vai direto ao WhatsApp, e o contato só existe no CRM se alguém registrar;
  - anúncio que leva a número fora do atendimento perde o contato;
  - o cadastro do formulário fica na Meta;
  - o bloqueador de anúncio tira do CRM o contato que chega pelo site.
- **Nenhuma conta Meta foi vista.** Por isso o canal não tem Exemplo Real.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Os seus anúncios no Instagram ou no Facebook rodaram no último mês completo? | **Rodaram o mês inteiro** / Pararam em alguns dias / Não rodaram, mas já anunciei / Nunca anunciei no Instagram nem no Facebook / Não sei | Todos |
| 2 | Por que você parou? | Ficou caro / Vinha contato que não comprava / Faltou tempo para cuidar / Não sei | Quem parou |
| 3 | Na coluna Resultados do último mês, o que o painel está contando? | **Conversas iniciadas ou cadastros** / Cliques no link / Engajamento, visualizações ou alcance / Não sei | Quem rodou |
| 4 | Quanto Você Investiu nos Três Últimos Meses Completos? | Valor em R$ / Não sei | Quem rodou |
| 5 | Quantos Resultados os Anúncios Tiveram Nesses Meses? | Número / Não sei | Quem rodou |

- **De pé:** as duas respostas em negrito. Fica em parte quando um dos dois pontos falha. Fica em falta para quem parou ("parou") e para quem nunca anunciou ("não usa"). "Não sei" leva a conferir e voltar.
- **Apoio:** "Post turbinado também conta."
- **Números:** mostram o custo pelo nome do resultado, por exemplo "cada conversa ou cadastro custou cerca de R$ 18,00". Informam e não decidem.
- **Entregável:** "O anúncio no ar o mês inteiro, contando conversas ou cadastros."
- **Para o atendimento:** a pergunta do que o painel conta, ou a da parada. O motivo de ter parado vira pergunta.

**Etapa 4, Conversão**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Para onde o anúncio leva quem toca no botão? | WhatsApp / Direct ou Messenger / Formulário de cadastro da Meta / Site / Não sei | Quem rodou. Quem não roda responde para onde levaria, sem o formulário e com "Ainda não sei" |
| 2 | De outro celular, como cliente novo, mande uma mensagem para o WhatsApp que o anúncio usa. Onde a conversa abriu? | **No número que a empresa atende** / No celular pessoal de alguém da empresa / Em outro número, ou não abriu / Não testei | WhatsApp. No Direct e no Messenger, o teste fala de perfil |
| 3 | Abra a Central de Leads e pegue o cadastro mais recente. Quem atende já falou com essa pessoa? | **Sim, no mesmo dia** / Sim, depois de um dia ou mais / Ainda não / Não sei | Formulário |
| 4 | Abra no celular, pelo endereço, a página para onde o anúncio leva. O que aconteceu? | As mesmas respostas do Google Ads | Site |
| 5 | Quanto Tempo Levou Até Uma Pessoa Responder? | Minutos / Ninguém respondeu até agora | Teste da conversa ou da página aprovado, opcional |

- **De pé:** o teste aprovado.
- **Leitura:** a Meta conta quem iniciou a conversa, e só o CRM mostra se ela virou contato registrado. No formulário, entra o prazo de 90 dias da Central de Leads.
- **Para o atendimento:**
  - No WhatsApp: "Quantas tiveram resposta de uma pessoa?"
  - No formulário atrasado: "Quem baixa os cadastros da Central de Leads, e de quanto em quanto tempo?"
  - Com o destino funcionando e a venda média conhecida: "De cada quantos resultados sai uma venda?"

**Etapa 5, só no caminho do Anúncio Meta e para quem tem CRM:**
- Entra o campo "Desses, Quantos Entraram no CRM com a Origem Meta?".
- A pergunta para o atendimento cruza os resultados por mês com esse número. Na persona fica assim: "Onde ficaram os outros 5?"

**Tela final:**
- O dono lê "Seus anúncios no Instagram e no Facebook" e "Cuide dos seus anúncios no Instagram e no Facebook".
- Os ajustes em paralelo seguem esta ordem: o conserto do destino, a troca da meta e a parada. São no máximo dois.

**O que saiu junto**
- **O molde antigo do anúncio**, que só o Anúncio Meta usava.
- **A frase "O canal tem rotina, mas o resultado ainda não é medido"**, que só esse molde usava. Nenhum canal chegava mais a ela.
- **O código que antes falava só em Google Ads:**
  - a leitura do campo do CRM na Etapa 5;
  - a medida do mesmo campo no atendimento.

  Os dois passaram a servir aos dois anúncios, e o Google Ads continua igual.

**Prova:** 340 conferências, todas passaram. São 33 novas do Anúncio Meta e 3 de textos que saíram. Duas conferências antigas que usavam o molde antigo foram trocadas pelo novo.

**O que não está provado**
- Os caminhos de onde conferir vêm da ajuda da Meta, e não de uma tela vista.
- A leitura "dia sem valor usado é dia sem anúncio" é minha.
- A ajuda não confirma dois pontos:
  - que a coluna Resultados mostra o nome do resultado;
  - que o número do WhatsApp aparece no Local da conversão.
- Três regras são minhas:
  - "Cliques no link" vale falta;
  - "Celular pessoal" vale em parte;
  - "No mesmo dia" é o de pé do formulário.
- As dicas do Como Fazer da Etapa 3 ficaram como estavam, porque não estavam no esqueleto.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.21. O Canal SEO

Aplicado em 07/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o terceiro canal do lote. Aceito por você na homologação, pelas fotos, em 07/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- **Texto presente na ajuda do Google, lida em 07/11, em português e sem login:**
  - o Relatório de Performance, com Cliques e Impressões;
  - o filtro "Consultas sem" e o "Sem marca";
  - as consultas que ficam de fora para proteger a privacidade;
  - a Inspeção de URL e a solicitação de indexação, que leva de um dia a duas semanas e não tem garantia;
  - o título único da página, que pode trazer o lugar;
  - o prazo de semanas para avaliar uma mudança;
  - o resultado da busca, que varia com o lugar, o aparelho e o histórico.
- **Aprendizados do CRM em operação, como regra e sem número:**
  - com bloqueador de anúncio, o contato do site pode não entrar no CRM;
  - a origem vale pelo que está registrado.
- **Nenhuma conta foi vista.** Por isso o canal não tem Exemplo Real.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Você consegue ver o seu site no Search Console do Google? | Sim, tenho acesso / Tenho site, mas não tenho o Search Console / Não tenho site / Não sei | Todos |
| 2 | Com o filtro Consultas sem o nome da empresa, leia as dez consultas com mais cliques dos três últimos meses completos. Há buscas pelo que você vende? | **Sim, há buscas pelo que eu vendo** / Não, são de outros assuntos / Não aparece consulta sem o nome da empresa / Não sei | Quem tem acesso |
| 3 | Cole na Inspeção de URL o endereço da página do seu serviço principal. O que aparece? | **O URL está no Google** / O URL não está no Google / Não tenho página para esse serviço / Não sei | Quem tem acesso |
| 4 | Quantas Vezes o Site Apareceu nos Três Últimos Meses Completos, sem as Buscas pelo Nome? | Número / Não sei | Quem tem acesso |
| 5 | Quantos Cliques o Site Teve Nesses Meses, sem as Buscas pelo Nome? | Número / Não sei | Quem tem acesso |

- **De pé:** as duas respostas em negrito. Fica em parte quando uma das duas falha.
- **Sem o Search Console:** o canal fica "não sei", com a tarefa de adicionar o site e voltar.
- **Sem site:** "Este Canal Pode Esperar", como antes.
- **Números:** impressões e cliques mostram quantos em cada 100 viraram clique. Informam e não decidem.
- **Saiu o teste de procurar o próprio site.** Com ele saíram também a contagem dos contatos do site no último mês e o apoio "Faça o teste sem digitar o nome da empresa".
- **Entraram:** as quatro dicas novas e o entregável "A página do serviço principal no Google, recebendo cliques de quem procura o que você vende".

**Etapa 4, Conversão**
- **O teste:** a página que mais recebeu cliques é testada no celular. Quem não tem o Search Console testa a página do serviço principal, e para esse caso existe a resposta "Não tenho essa página".
- **De pé:** o teste aprovado.
- **Tempo de resposta:** é opcional e aparece só com o teste aprovado.
- **Leitura:** "O Search Console mostra quem clicou, e não quem falou com você."
- **Como Fazer:** a guia Páginas ordenada por Cliques, o número lido dígito a dígito, o teste fora do horário e o teste em aba anônima.

**Etapa 5, só no caminho do SEO e para quem tem CRM**
- Entra o campo "Desses, Quantos Entraram no CRM com a Origem SEO?".
- Com cliques e nenhum contato com essa origem, a pergunta para o atendimento é "Quem chega pela busca está virando contato?".

**Tela final:** o dono lê "Seu site no Google" e "Cuide do seu site no Google".

**Ficaram de fora, como no esqueleto**
- **O Analytics:** os números dele não batem com os do Search Console, e o cruzamento confiável é o do CRM.
- **A velocidade do site:** em site com pouca visita, o relatório costuma vir sem dados.

**Prova:** 367 conferências, todas passaram. São 24 novas do SEO e 3 de textos que saíram. As conferências que usavam o SEO como canal sem conversão própria passaram a usar o GEO.

**O que não está provado**
- O caminho no menu lateral do Search Console não está escrito na ajuda.
- A regra "uma página por serviço" não aparece no guia do Google.
- Quem não tem o Search Console ficar com "não sei" é escolha minha.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.22. O Canal GEO

Aplicado em 08/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o quarto canal do lote, e você o aceitou pelas fotos em 08/11 ("Ok, aceito").

**Fontes e tipo de prova**
- **Texto presente em fontes oficiais, lidas em 07/11:**
  - **Google:** as Visões Gerais criadas por IA e o Modo IA não pedem nada além do SEO, a página precisa estar no índice e o Perfil da Empresa deve estar atualizado.
  - **Gemini:** usa as informações públicas do Google Maps.
  - **OpenAI, Perplexity e Anthropic:** o robô de busca de cada uma (OAI-SearchBot, PerplexityBot e Claude-SearchBot) precisa estar liberado no robots.txt.
  - **Microsoft:** o Copilot usa a mesma base do Bing.
  - **Analytics:** tem o canal "Assistente de IA" desde 13/05/2026.
  - **ChatGPT:** a resposta muda com a localização, as memórias e o jeito de perguntar.
  - **Google, OpenAI e Microsoft:** não há garantia de aparecer.
- **Aprendizados do CRM em operação, como regra e sem número:** o bloqueador de anúncio, na Etapa 4, e a origem registrada no CRM, na Etapa 5.
- **Nenhuma conta foi vista.** Por isso o canal não tem Exemplo Real.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Abra no navegador o endereço do seu site seguido de /robots.txt. O arquivo bloqueia algum robô de busca das inteligências artificiais? | **Não bloqueia nenhum, ou o arquivo não existe** / Bloqueia algum deles / Não tenho site / Não sei | Todos |
| 2 | Compare a sua ficha no Google com o seu site. Nome, telefone, endereço e horário são iguais? | **Tudo igual** / Há diferença em algum / Não tenho ficha no Google / Não sei | Quem tem site |
| 3 | Quantas Visitas o Canal Assistente de IA Teve nos Três Últimos Meses Completos? | Número / Não sei | Quem tem site |
| 4 | Pergunte ao ChatGPT e ao Gemini pelo seu serviço na sua cidade, sem o nome da empresa. A empresa apareceu? | Apareceu, com a informação certa / Apareceu com informação errada / Não apareceu / Não testei | Quem tem site |

- **De pé:** as duas respostas em negrito. Fica em parte quando uma das duas falha.
- **Sem site:** "Este Canal Pode Esperar", porque a ficha no Google vem antes.
- **O que informa:** as visitas e o teste de perguntar a uma IA. Não decidem nível nem rota.
- **Para o atendimento:** "Quem decidiu bloquear, e por quê?" e "O que a IA disse de errado, e onde essa informação está publicada?".
- **Entregável:** "O site aberto aos robôs das IAs, com as mesmas informações da ficha no Google."
- **Saiu:** o aviso "Este canal não pede número", que o canal Assistente de IA tornou errado, e o teste de perguntar a uma IA como ponto que decide.
- **Entraram:** as quatro dicas novas.

**Etapa 4, Conversão**
- O dono abre no celular a página que a IA citou, ou a página inicial, e tenta falar com a empresa.
- As respostas são as mesmas do SEO.
- **De pé:** o teste aprovado.
- **Tempo de resposta:** é opcional e aparece só com o teste aprovado.

**Etapa 5, só no caminho do GEO e para quem tem CRM**
- Entra o campo "Desses, Quantos Entraram no CRM com a Origem GEO?".
- Com visitas de IA e nenhum contato com essa origem, a pergunta para o atendimento é "Quem chega pelas IAs está virando contato?".

**Tela final:** o dono lê "Sua empresa nas respostas de IA" e "Cuide de como as IAs encontram a sua empresa".

**Ficou de fora, como no esqueleto:** o relatório AI Performance, do Bing Webmaster Tools. Entra só como nota no Onde Conferir.

**Prova:** 394 conferências, todas passaram. São 24 novas do GEO e 3 de textos que saíram. As conferências que usavam o GEO como canal sem conversão própria passaram a usar as Avaliações do Google.

**O que não está provado**
- O bloqueio feito pelo CDN não aparece no robots.txt, e o dono não consegue conferir isso sozinho.
- A comparação entre a ficha e o site como ponto que decide é escolha minha. Nenhuma fonte diz que a igualdade decide a citação.
- Nenhuma página oficial no ar confirma o parâmetro de origem que o ChatGPT acrescentaria aos links.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.23. O Canal Avaliações do Google

Aplicado em 08/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o quinto canal do lote, e você o aceitou pelas fotos em 08/11 ("Ok, aceito").

**Fontes e tipo de prova**
- **Texto presente, na ajuda oficial do Google em português, lida em 08/11:**
  - O link e o QR Code ficam em Ler avaliações, Receba mais avaliações. O QR Code só é gerado no navegador do computador.
  - Toda resposta passa por análise, e a empresa precisa estar verificada para responder.
  - A nota é a média das classificações publicadas, e uma avaliação nova pode levar até duas semanas para mudar a nota.
  - Mais avaliações e notas positivas melhoram a classificação local. Responder ajuda a empresa a se destacar.
  - A política não permite incentivo, conflito de interesses, pressão no local, pedido seletivo de avaliação positiva e pedir à equipe um número determinado de avaliações.
  - Quem descumpre pode perder as avaliações e ficar um período sem receber novas.
  - Avaliação ruim verdadeira não é removida.
- **Regra lida, por ausência:** a ajuda não confirma visão de avaliações novas por período, e a lista de métricas de Desempenho não traz avaliações.
- **Tela observada, sem login, no Google Maps de um lugar público:** total por estrela, botão Classificar avaliações e data como "uma semana atrás". O menu de ordem pediu login e não foi visto.
- Nenhuma conta foi vista, e o canal fica sem Exemplo Real.

**Etapa 3, Canal**
- **Quatro pontos decidem o "de pé":** nenhuma prática que o Google não permite, o link a todo cliente atendido, avaliação nova nos três últimos meses e nenhuma avaliação sem resposta.
- **Só informam:** a nota, o total e quantas das cinco mais recentes têm 1 ou 2 estrelas. Não há corte de nota nem de total.
- **O total é a base do próximo ciclo,** porque o Google não mostra quantas avaliações chegaram por mês.
- **Em parte:** algum dos quatro pontos falha. **Falta:** "Não pedimos". **Sem ficha:** o canal pode esperar, e a ficha vem primeiro.
- **Ordem do próximo passo:** parar a prática proibida, mandar o link a todo cliente atendido, conferir se o link está chegando e responder às avaliações.
- **Para o atendimento:** com 1 ou 2 estrelas entre as cinco mais recentes, "Do que esses clientes reclamam?".

**Saiu da tela**
- A dica "Defina uma meta de avaliações novas por mês", que a política não permite cobrar da equipe.
- A dica "logo depois de uma boa entrega", que abre risco de pedido seletivo.
- O corte de 20 avaliações para reputação de pé e o corte de nota 4, sem fonte.
- As frases sobre o cliente insatisfeito que mais avalia, a avaliação antiga que pesa menos e a nota baixa que espalha o problema, sem fonte.

**Etapa 4, Conversão**
- Teste da porta principal da ficha, com as mesmas portas do Google Meu Negócio. Não pede de novo os números da ficha.
- **De pé:** o teste aprovado.
- Quem já percorreu a ficha encontra marcadas a avaliação sem resposta, a porta e o teste, com o aviso de que pode mudar.

**Etapa 5:** sem campo de origem no CRM, como na ficha, porque o Google não separa quem agiu por causa das avaliações.

**Tela final:** o dono lê "Suas avaliações no Google" e "Peça avaliação a todo cliente atendido".

**Ficou de fora, como no esqueleto:** avaliações novas por mês, origem "Avaliações" no CRM, denúncia de avaliação e Exemplo Real.

**Prova:** 431 conferências, todas passaram. São 29 novas das Avaliações, com 3 de comportamento executado por clique, e 8 de textos que saíram. As conferências que usavam as Avaliações como canal sem conversão própria passaram a usar a Oferta de Entrada.

**O que não está provado**
- As opções do menu Classificar, porque o Maps pediu login. O texto diz só "escolha as mais recentes".
- O botão Receba mais avaliações vem da ajuda, sem tela vista.
- "A todo cliente" é declaração do dono. A data da avaliação mais recente é a prova indireta.
- Tratar "só a quem ficou satisfeito" como pedido seletivo é leitura minha da frase do Google.
- O corte de três meses e a leitura das cinco mais recentes são escolhas minhas.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.24. O Canal Oferta de Entrada

Aplicado em 08/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o sexto canal do lote, e você o aceitou pelas fotos em 08/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- O canal não tem painel de ferramenta. Os números vêm do CRM, ou são marcados como estimados.
- **Regra lida, no Código de Defesa do Consumidor, no site do Planalto, em 08/11:**
  - **Art. 30:** a oferta suficientemente precisa, por qualquer meio, obriga a empresa.
  - **Art. 31:** a informação precisa ser clara sobre características, preço, garantia e prazos.
  - **Art. 35:** se a empresa recusar, o consumidor pode exigir o cumprimento, aceitar equivalente ou rescindir.
  - **Art. 37:** omitir dado essencial é publicidade enganosa.
- A tela avisa que a leitura não é parecer jurídico.

**Etapa 3, Canal**
- **Três pontos decidem o "de pé":** a oferta por escrito, com o que a pessoa recebe, o preço e o prazo; à vista logo de cara no canal em que mais chega contato; e com o próximo passo marcado, com data e responsável.
- **Só informam:** quantas pessoas aceitaram nos três últimos meses completos e quantas já fizeram a compra principal, com a marca de medido ou estimado. Não há corte.
- **Em parte:** algum dos três pontos falha. **Sem oferta:** o canal pode esperar.
- **Ordem do próximo passo:** escrever a oferta, deixá-la à vista e definir o próximo passo.
- **Para o atendimento:** se ninguém aceitou, "A oferta está chegando às pessoas certas?". Se alguém aceitou e não comprou, "Quem aceitou e não comprou era o público certo? Quanto custa entregar cada oferta?".

**Saiu da tela**
- O corte de metade e as frases "atrai curioso" e "gente com perfil de cliente", que afirmavam causa.
- "Oferta parada não abre conversa" e "pedir a compra completa afasta", sem prova.
- A janela do último mês, porque quem aceitou há poucos dias ainda não teve tempo de comprar.

**Etapa 4, Conversão**
- O dono pede a oferta como cliente e compara a resposta com o que a oferta promete.
- **De pé:** o pedido funciona e a resposta confere. **Em parte:** a resposta não confere ou ninguém respondeu. **Falta:** não achou onde pedir.
- **Tempo de resposta:** é opcional e aparece só com o teste aprovado.

**Etapa 5:** sem campo de origem no CRM. A oferta não é origem: quem aceita veio de um canal, e a oferta é uma marca a mais no contato.

**Tela final:** o dono lê "Sua oferta de entrada" e "Escreva e mostre a sua oferta de entrada".

**Ficou de fora, como no esqueleto:** o tipo de oferta, o custo de entregar a oferta como número, a venda casada e Exemplo Real.

**Prova:** 461 conferências, todas passaram. São 24 novas da Oferta e 6 de textos que saíram. As conferências que usavam a Oferta como canal sem conversão própria passaram a usar o Ponto Físico.

**O que não está provado**
- Escolher "o que recebe, preço e prazo" como os três itens é seleção minha dentro do art. 31.
- "Logo de cara" e "próximo passo com data e responsável" são critérios meus.
- A leitura do Código não é parecer jurídico.
- Ficou do texto anterior, sem fonte, a frase "Oferta de entrada faz sentido quando a compra principal é cara ou demorada de decidir".
- Nada foi testado com dono de empresa nem com mentor.

#### 6.25. O Canal Ponto Físico

Aplicado em 08/11/2026, com o seu pedido de fazer os últimos ajustes e fechar o lote, sobre o esqueleto em tabela. É o sétimo canal do lote e o último do Inbound, e você o aceitou pelas fotos em 08/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- O canal não tem painel de ferramenta. A foto e os testes são feitos de fora da empresa, e o número vem do CRM ou é marcado como estimado.
- **Texto presente, nas ajudas oficiais em português, em 08/11:** WhatsApp Business (link curto e QR Code) e Google (diretrizes da ficha, horário especial e horários de pico).
- **Regra lida, em 08/11:**
  - Lei 10.962/2004, art. 2º, I, e Decreto 5.903/2006, para o preço na vitrine.
  - Lei 14.223/2006 de São Paulo, arts. 6º e 13, só como exemplo de regra de placa.
- A tela avisa que a leitura das leis não é parecer jurídico.

**Etapa 3, Canal**
- **Três pontos decidem o "de pé":** a fachada diz o que a empresa vende, em letra que dá para ler da rua; o telefone, o WhatsApp ou o QR Code está à vista de quem passa; e o nome e o horário da porta conferem com a ficha no Google.
- **Só informam:** o preço na vitrine, que vira ajuste em paralelo, e as pessoas novas que disseram ter conhecido a empresa passando na frente nos três últimos meses completos, com a marca de medido ou estimado.
- **Em parte:** algum dos três pontos falha. **Falta:** não tem placa nem letreiro. **Pode esperar:** a entrada não dá para a rua. **Não se aplica:** não tem ponto aberto ao público.
- **Quando a fachada precisa mudar:** a tela manda conferir a regra da prefeitura antes de trocar a placa.
- **Para o atendimento:** "O problema é atrair quem passa ou aproveitar quem entra?" e, se ninguém disse ter vindo por aqui, "A rua tem movimento do seu público?".

**Saiu da tela**
- "Entende na hora", opinião de quem vê a própria fachada todo dia.
- "Quantas pessoas entram por dia sem ter marcado?", que mistura quem já conhece com quem é novo.
- A nota geral da chegada na Etapa 4, trocada pelos testes.

**Etapa 4, Conversão**
- **Dois testes feitos de fora decidem:** a foto da fachada mostrada a quem não conhece a empresa, e o uso do contato à vista, da calçada e de outro celular. A situação é a do pior dos dois.
- **Sem contato à vista:** o segundo teste não aparece, e a etapa fica em falta.
- **Só informam:** o tempo de resposta, opcional, e quem recebe na porta, que vira pergunta para o atendimento.

**Tela final:** o dono lê "Sua fachada" e "Mostre da rua o que você vende e como falar com você".

**Ficou de fora, como no esqueleto:** solicitações de rota e foto da fachada na ficha, que já estão no canal do Google, e a contagem de quem passa na rua, que não tem painel.

**Prova:** 496 conferências, todas passaram. São 29 novas do Ponto Físico e 6 de textos. Como todo o Inbound já tem conversão própria, as conferências da ficha geral da Etapa 4 passaram a usar o canal Ligação, do Outbound.

**O que não está provado**
- Nenhuma conta de WhatsApp ou ficha do Google foi vista. Os caminhos vêm da ajuda.
- A ajuda não diz se o QR Code leva a mensagem pronta do link curto.
- O tamanho de 8 cm x 8 cm vale para o adesivo do WhatsApp. Nenhuma fonte diz de que distância o QR Code lê.
- Da regra de placa, só a de São Paulo foi lida, e não se conferiu o que cada cidade permite escrever nela.
- A foto e o teste com uma pessoa são propostas minhas, sem fonte. Servem para achar defeito, não para medir.
- Nada foi testado com dono de empresa nem com mentor.

**Estado do lote:** a seu pedido, o lote fecha aqui, com o Inbound completo. Outbound, Branding, Indicação e Base seguem com a tela anterior.

#### 6.26. O Canal Indicação de Clientes

Aplicado em 11/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o primeiro canal do pilar Indicação e Parcerias, que você decidiu aprofundar antes de subir o módulo para o app. Você o aceitou pelas fotos em 11/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- O canal não tem painel de ferramenta. Os números vêm do CRM, ou são marcados como estimados.
- **Texto presente, na ajuda do WhatsApp Business em português, lida em 11/11:**
  - **Link de conversa (faq 5913398998672934):** leva uma mensagem pronta, que aparece no campo de texto de quem abre o link.
  - **Link curto (502291734918768 e 888878128766436):** tem uma mensagem padrão, que a pessoa pode mudar antes de enviar.
  - **Respostas rápidas (1791149784551042):** salvam um texto pronto, enviado com o atalho "/".
  - **Etiquetas (3398508707096369):** marcam conversas. Em algumas contas, elas viraram listas.
- **Regra lida, em 11/11:**
  - **Política de Mensagens do WhatsApp Business, seção 1:** a empresa só pode chamar quem deu o número a ela e aceitou receber mensagem. A seção vale para o app e para a API.
  - **LGPD, arts. 6º, 7º, 9º, 10 e 18:** quem trata o dado de alguém que não o entregou precisa de base legal, finalidade, transparência e dado estritamente necessário, e precisa atender aos direitos do titular.
  - **Guia de Legítimo Interesse da ANPD:** a fonte do dado, inclusive o compartilhado por terceiro, pesa na análise.
- A tela avisa que a leitura não é parecer jurídico.
- **Aprendizados do CRM em operação, como regra e sem número:**
  - contato que chega sem a origem registrada fica sem origem no CRM, e a indicação some da conta;
  - a origem vale pelo que o contato disse, e não pelo palpite de quem atende.
- Nenhuma conta foi vista, e o canal fica sem Exemplo Real.

**O achado:** pedir o número do amigo e chamar vai contra a política do WhatsApp. O texto pronto que o cliente encaminha resolve: quem chama é o próprio amigo.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Como você pede indicação hoje? | **Mando um texto pronto para o cliente encaminhar** / Peço de boca, sem texto / Peço o número do amigo, e eu mesmo chamo / Não peço, mas recebo indicação / Não peço e não recebo / Não sei | Todos |
| 2 | Pegue os cinco últimos clientes que receberam o serviço sem reclamação. Em quantos você pediu indicação? | **Nos cinco** / Em alguns / Em nenhum / Não sei | Quem pede |
| 3 | Abra o texto pronto. O que ele tem? | **O que a empresa faz e o link ou o número do WhatsApp da empresa** / Só o nome da empresa / Como falar, sem dizer o que a empresa faz / Não sei | Quem manda texto |
| 4 | Quantas Indicações Chegaram nos Três Últimos Meses Completos? | Número, medido ou estimado / Não sei | Quem recebe indicação |
| 5 | Pegue as três últimas indicações. Quem indicou recebeu o seu obrigado? | As três / Alguma / Nenhuma / Não sei quem indicou / Não sei | Quem recebe indicação, com alguma indicação |

- **Dois pontos decidem o "de pé":**
  - o texto pronto, com o que a empresa faz e como falar com ela;
  - o pedido a todo cliente satisfeito.
- **Por onde começar:** o texto vem primeiro, porque sem ele o pedido não chega ao amigo.
- **Em parte:**
  - quando um dos dois falha;
  - quando o pedido é de boca ou pelo número do amigo;
  - quando a indicação chega sem pedido, como na seção 4.3.
- **Falta:** "Não peço e não recebo" ("não usa"). **Não sei:** leva a conferir e voltar.
- **Só informam:** as indicações dos três meses, mostradas como "cerca de X por mês", e o obrigado a quem indicou, que vira ajuste em paralelo.
- **Entregável:** o validado, "O pedido de indicação feito a todo cliente satisfeito, com um texto pronto para encaminhar".
- **Para o atendimento, como pergunta:**
  - Pedido feito e nenhuma indicação: "O que o texto pede, e em que momento ele chega?"
  - Indicação sem pedido: "Quem são os clientes que mais indicam?"
  - "Não sei quem indicou": "Como a empresa fica sabendo quem indicou cada contato?"

**Saiu da tela**
- A pergunta simples "Como você faz isto hoje?" e as três respostas do molde antigo.
- A medida "Pedidos de Indicação Feitos no Último Mês". A conferência dos cinco últimos clientes entrou no lugar.
- O retorno "X em cada 10" deste canal.
- As dicas "Peça a indicação logo depois de uma boa entrega" e "Avise quem indicou sobre o resultado". Entraram as quatro dicas novas.

**Etapa 4, Conversão**
- **O teste:** o dono encaminha o texto pronto a alguém de fora, e essa pessoa fala com a empresa como indicada. Sem texto pronto, a pessoa manda mensagem dizendo que foi indicada por um cliente.
- **Respostas:** **Uma pessoa respondeu e ficou sabendo quem indicou** / Uma pessoa respondeu, mas ninguém soube quem indicou / Só veio resposta automática, ou ninguém respondeu / Não abriu, ou foi para outro número / Não testei.
- **De pé:** o teste aprovado. O tempo de resposta é opcional.

**Etapa 5, só no caminho da Indicação de Clientes e para quem tem CRM**
- Entra o campo "Desses, Quantos Entraram no CRM com a Origem Indicação?". Só vale o contato com a origem e o nome de quem indicou.
- Com menos contatos no CRM do que indicações por mês, a pergunta vai para o atendimento. Na persona fica assim: "Chegaram cerca de 10 indicações por mês, e 4 entraram no CRM com a origem Indicação. Onde ficaram as outras 6?"

**Tela final:** o dono lê "Seu pedido de indicação" e "Peça indicação a todo cliente satisfeito, com um texto pronto". Os ajustes em paralelo seguem esta ordem: o conserto do teste, o obrigado a quem indicou e o ponto em falta. São no máximo dois.

**Prova:** 526 conferências, todas passaram.
- São 26 novas da Indicação e 4 de textos que saíram.
- A conferência da conversão geral do pilar passou para o Programa de Indicação.
- A contagem de "Todos os canais" passou a 23 canais com medida própria e 12 com retorno.

**O que não está provado**
- A ajuda não trata de encaminhar o link. Encaminhar é uso comum do WhatsApp, sem página que confirme.
- Não está provado que o amigo complete o nome em "Vim por indicação de".
- O filtro de etiquetas por data não foi confirmado.
- "O link curto tem uma mensagem só, que vale para todo mundo" é leitura minha da ajuda.
- Os cinco últimos clientes e "sem reclamação" como sinal de satisfeito são escolhas minhas.
- A LGPD não diz que o indicado deve procurar a empresa. É leitura minha dos artigos, com o guia da ANPD.
- O obrigado a quem indicou não tem fonte oficial. Ele já estava nas dicas validadas do pilar.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.27. O Canal Programa de Indicação

Aplicado em 11/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o segundo canal do pilar Indicação e Parcerias, e você o aceitou pelas fotos em 11/11/2026 ("Ok, aceito").

**Fontes e tipo de prova**
- O canal não tem painel de ferramenta. O número vem do CRM, ou é marcado como estimado.
- **Regra lida, em 11/11:**
  - **Lei 5.768/1971, art. 1º:** sorteio, vale-brinde, concurso ou operação parecida, como propaganda, depende de autorização prévia do Ministério da Fazenda.
  - **Lei 5.768/1971, art. 12:** sem autorização, a multa vai até 100% do valor dos prêmios, e a empresa pode ficar até 2 anos proibida de fazer promoção.
  - **Decreto 70.951/1972:** regulamenta a lei.
  - **Página da Secretaria de Prêmios e Apostas, do Ministério da Fazenda:**
    - a FAQ 11 dá o prazo do pedido, em geral de 40 a 120 dias antes do início;
    - a FAQ 59 diz que benefício dado a todos que cumprem uma condição clara e definida antes, sem sorte, competição nem estoque limitado, "em regra" não depende de autorização.
  - **Código de Defesa do Consumidor, arts. 30, 31, 35 e 37:** a oferta precisa obriga, a informação precisa ser clara, e omitir dado essencial é publicidade enganosa.
  - **Lei 8.981/1995, art. 63:** o prêmio em bens de sorteio tem imposto de renda retido na fonte.
- A tela avisa que a leitura não é parecer jurídico.
- **Aprendizados do CRM em operação, como regra e sem número:**
  - sem o nome de quem indicou registrado, o prêmio não tem a quem ser entregue;
  - a origem vale pelo que o contato disse.

**O achado:** o programa com sorteio precisa de autorização do Ministério da Fazenda. O prêmio certo para todo indicado que comprar, em regra, não precisa.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Quem indica ganha o quê? | **Um prêmio certo, com a regra por escrito** / Um prêmio certo, combinado só de boca / Concorre a um sorteio / Ganha um agrado quando eu lembro, sem regra / Não tenho programa / Não sei | Todos |
| 2a | Abra a regra escrita. O que ela diz? | **O que se ganha, a condição para ganhar e o prazo de entrega** / Falta a condição ou o prazo / Não sei | Regra escrita |
| 2b | O sorteio tem a autorização do Ministério da Fazenda? | **Sim, tem a autorização** / Não tem / Não sei | Sorteio |
| 3 | Quem já ficou sabendo do programa? | **Todos os clientes da base** / Só quem comprou depois que o programa começou / Só quem pergunta, ou quem vê no balcão e nas redes / Não sei | Prêmio combinado ou sorteio |
| 4 | Pegue os três últimos prêmios devidos. Foram entregues no prazo? | **Os três, no prazo** / **Ainda não houve prêmio devido** / Algum atrasou ou não foi entregue / Não sei | Prêmio combinado ou sorteio |
| 5 | Quantas Indicações Chegaram pelo Programa nos Três Últimos Meses Completos? | Número, medido ou estimado / Não sei | Quem tem programa, inclusive o agrado |

- **Três pontos decidem o "de pé":**
  - a regra escrita completa, ou o sorteio autorizado;
  - a regra mandada a toda a base;
  - os prêmios entregues no prazo.
- **Em parte:**
  - algum dos três pontos falha;
  - o prêmio é só de boca;
  - ou é o agrado sem regra, como na seção 4.3.
- **Sorteio sem autorização:** a tela traz a regra da lei e o passo "Pare o sorteio e troque por um prêmio certo para todo indicado que comprar, ou peça a autorização antes".
- **Não tenho programa:** "Este Canal Pode Esperar", porque o programa vem depois do pedido a todo cliente satisfeito. A seção 4.3 dizia "falta", e você aprovou a troca.
- **Só informam:** as indicações pelo programa, mostradas como "cerca de X por mês".
- **Entregável novo, aprovado por você:** "A regra do programa por escrito, mandada a toda a base, com todo prêmio entregue no prazo."
- **Por Que Importa:** "Com a regra escrita, quem indica sabe o que ganha e quando. Pelo Código de Defesa do Consumidor, a empresa precisa cumprir o que a regra diz."
- **Para o atendimento, como pergunta:**
  - Regra a toda a base e nenhuma indicação: "O prêmio interessa a quem já é cliente?"
  - Prêmio atrasado: "O que atrasou a entrega dos prêmios?"
  - Agrado sem regra: "Quanto a empresa pode dar por indicação que vira venda?"

**Saiu da tela**
- A pergunta simples, as três respostas do molde antigo e a medida "Indicações Recebidas pelo Programa no Último Mês".
- A frase sem fonte de que a indicação "vira hábito".
- As dicas antigas, entre elas "Entregue o prêmio rápido".

**Etapa 4, Conversão**
- O teste do indicado, com as mesmas respostas da Indicação de Clientes: "Peça a alguém de fora que mande mensagem à empresa dizendo que foi indicado por um cliente, pelo programa."
- **Por Que Importa:** "Sem saber quem indicou, a empresa não consegue entregar o prêmio que a regra promete."
- **De pé:** o teste aprovado. O tempo de resposta é opcional.

**Etapa 5:** sem campo de origem no CRM, como na Oferta de Entrada. Quem chega pelo programa tem a origem Indicação. O programa é uma marca a mais no contato, com o nome de quem indicou.

**Tela final:** o dono lê "Seu programa de indicação" e "Escreva a regra do programa e mande a toda a base". Os ajustes em paralelo seguem esta ordem: o conserto do teste, a entrega do prêmio atrasado e o ponto em falta. São no máximo dois. O prêmio atrasado não se repete quando já é o passo da semana.

**Prova:** 552 conferências, todas passaram.
- São 21 novas do Programa e 5 de textos que saíram.
- As conferências da conversão geral do pilar e do canal com a tela anterior passaram para Parceiros de Negócio.
- A contagem de "Todos os canais" passou a 22 canais com medida própria.

**O que não está provado**
- A FAQ 59 diz "em regra", e a SPA não tem orientação específica sobre "indique e ganhe".
- A Portaria SEAE/ME 7.638/2022 não abriu, e não está provado que seja a vigente.
- Não está confirmado se o prêmio em dinheiro dado a todos que indicam é programa de fidelidade ou promoção. Por isso a tela não pergunta o tipo de prêmio.
- O prêmio a quem indica ser oferta do Código de Defesa do Consumidor é leitura minha.
- "Toda a base" é declaração do dono. Os três últimos prêmios são escolha minha.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.28. A Trilha Própria do GEO

**O pedido:** em 11/11/2026, no meio do lote de Indicação e Parcerias, você pediu um foco muito grande no GEO, por ser um conhecimento que quase ninguém tem. Você escolheu fazer nesta sessão e, entre os formatos propostos, a "trilha própria".

**A aprovação:** aplicada em 11/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela, e aceita pelas fotos no mesmo dia ("Ok, aceito"). Ela substitui a Etapa 3 da seção 6.22. A Etapa 4 continua a mesma.

**Fontes e tipo de prova (texto presente, lido em 11/11)**
- **Google:**
  - o guia de otimização para IA, de 15/05/2026: a base é o SEO, e não é preciso llms.txt, marcação especial nem texto picado para IA;
  - a página "Recursos de IA e o seu site": página no índice, robô liberado e conteúdo importante em texto;
  - o relatório de IA generativa do Search Console, com impressões das Visões Gerais e do Modo IA juntas, aberto a todos desde 31/08/2026;
  - o controle de IA generativa do Search Console;
  - o canal Assistente de IA do Analytics;
  - o Google-Extended, que não tira o site da Pesquisa.
- **OpenAI:** OAI-SearchBot para a busca e GPTBot para o treino. A FAQ dos publishers e a da busca deram erro e foram lidas por trechos da busca.
- **Microsoft:** o AI Performance do Bing Webmaster Tools, em prévia, e o Bing Places, que importa o Perfil do Google, pelo blog oficial.
- **Perplexity:** PerplexityBot e Perplexity-User. A página de rótulos de fonte tinha instruções dirigidas a agentes de IA, e o agente não seguiu.
- **Anthropic:** Claude-SearchBot, Claude-User e ClaudeBot.
- **Apple:** Applebot e Applebot-Extended, e o Apple Business, antes Business Connect.
- **Aprendizados do CRM em operação, como regra e sem número:**
  - a origem vale pelo que o contato disse, e quem lê a resposta da IA e liga direto não deixa rastro no site;
  - o bloqueador de anúncio, que já estava na Etapa 4.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Abra o seu site/robots.txt. O arquivo bloqueia algum robô de busca das IAs? | **Não bloqueia nenhum, ou o arquivo não existe** / Bloqueia algum deles / Não tenho site / Não sei | Todos |
| 2 | No Search Console, em Configurações, o site está incluído nos recursos de IA generativa da Pesquisa? | **Incluído** / Excluído / Não tenho o Search Console / Não sei | Quem tem site |
| 3 | Abra a página do seu serviço principal. O serviço, a cidade e o jeito de pedir estão escritos em texto? | **Sim, em texto** / Parte só em imagem ou vídeo / Não tenho página para o serviço / Não sei | Quem tem site |
| 4 | A empresa está no Perfil da Empresa no Google e no Bing Places? | **Nos dois** / Só no Google / Só no Bing / Em nenhum / Não sei | Quem tem site |
| 5 | Compare a ficha no Google com o site. Nome, telefone, endereço e horário são iguais? | Tudo igual / Há diferença em algum / Não sei | Quem está no Google |
| 6 | E os robôs de treino: Google-Extended, GPTBot, ClaudeBot e Applebot-Extended? | Liberados / Bloqueados, por decisão da empresa / Não sei | Quem tem site |
| 7 | Quantas Visitas o Canal Assistente de IA Teve nos Três Últimos Meses Completos? | Número / Não sei | Quem tem site |
| 8 | O relatório de IA generativa do Search Console mostra impressões do site nos três últimos meses completos? | Mostra impressões / Mostra zero / O relatório não aparece para o site / Não sei | Quem tem o Search Console |
| 9 | No Bing Webmaster Tools, o relatório AI Performance mostra citações do site no Copilot? | Mostra citações / Mostra zero / Não uso o Bing Webmaster Tools / Não sei | Quem tem site |
| 10 | Pergunte ao ChatGPT e ao Gemini pelo seu serviço na sua cidade. A empresa apareceu? | As mesmas da seção 6.22 | Quem tem site |

- **Quatro pontos decidem o "de pé", todos com fonte oficial:** robôs de busca liberados, site incluído nos recursos de IA, serviço principal em texto e empresa no Google e no Bing.
- **Por onde começar:** segue essa ordem.
- **Sem o Search Console:** o ponto 2 fica "não sei", com a tarefa de adicionar o site, como no SEO. **Sem site:** o canal pode esperar.
- **A ficha igual ao site deixou de decidir e virou ajuste**, porque nenhuma fonte oficial diz que a igualdade decide a citação.
- **As perguntas 6 a 10 informam:** os robôs de treino, com a leitura "isso não tira a empresa das respostas de busca", as visitas, as impressões, as citações e o teste de perguntar a uma IA.
- **Para o atendimento:**
  - robô de busca bloqueado: "Quem decidiu bloquear, e por quê?";
  - site excluído dos recursos de IA: "Quem excluiu, e por quê?";
  - IA com informação errada: "O que a IA disse de errado, e onde essa informação está publicada?"
- **Entregável novo:** "O site aberto aos robôs de busca das IAs e incluído nos recursos de IA do Google, com o serviço principal escrito em texto e a empresa no Google e no Bing."

**As duas folhas de conhecimento, abertas pelo "?"**
- **Onde Cada IA Busca:** um bloco por assistente (Google, ChatGPT, Copilot, Perplexity, Claude, Siri e Apple), com o robô de busca, o robô de treino, o cadastro e a medição de cada um.
- **O Que Não Precisa:** sete mitos sem fonte oficial:
  - o llms.txt;
  - a marcação especial para IA;
  - a marcação de perguntas frequentes, que o Google deixou de mostrar em 2026;
  - o texto picado;
  - as menções compradas;
  - nome, endereço e telefone iguais em todo diretório;
  - pagar para aparecer.

**Saiu da tela**
- "Informação clara, igual em todos os lugares e confirmada por outras fontes aumenta a chance de aparecer", que não tem fonte.
- "O Gemini usa as informações públicas do Google Maps". O levantamento de 11/11 não achou de novo essa página. No lugar entrou "O guia do Google para IA indica o Perfil da Empresa para negócio local".
- O Claude como exemplo do canal Assistente de IA, que a ajuda de 11/11 não mostra.
- O apoio antigo dos robôs, sem o Googlebot e o Applebot, e a leitura de dois pontos.

**Etapa 5:** o campo da origem GEO continua. O Onde Conferir ganhou "Quem lê a resposta da IA e liga direto não deixa rastro no site. Pergunte a todo contato novo como conheceu a empresa."

**Tela final:** continua "Sua empresa nas respostas de IA". Os ajustes em paralelo seguem esta ordem: o conserto da página, o ponto em falta e a ficha igual ao site. São no máximo dois.

**Prova:** 562 conferências, todas passaram. A seção antiga do GEO foi trocada inteira pela da trilha, e entraram 5 conferências de textos que saíram.

**O que não está provado**
- O nome em português do controle e do relatório de IA no Search Console, porque a ajuda foi lida em inglês.
- Que o Copilot use o Bing Places, ou que o Gemini use o Perfil, para recomendar uma empresa. As fontes só indicam os cadastros.
- De onde o ChatGPT tira os dados de empresas locais. A OpenAI diz só "provedores terceiros".
- Que o serviço em texto faça a IA citar a empresa. O Google pede o conteúdo em texto e não garante citação.
- "Tente selecionar a frase com o dedo" é um teste meu, sem fonte.
- Nada foi testado com dono de empresa nem com mentor.

#### 6.29. O Canal Parceiros de Negócio

Aplicado em 11/11/2026 com o seu "Sim, aplicar" sobre o esqueleto em tabela. É o terceiro canal do pilar Indicação e Parcerias. Você o aceitou em 11/11/2026 ("Ok, aceito") pelas fotos da Etapa 3, da troca de lista, da Etapa 4 e da Etapa 5, no fechamento do lote.

**Fontes e tipo de prova (regra lida, em 11/11)**
- **Código Civil, arts. 722 a 729 (corretagem):** a comissão é devida quando se obtém o resultado combinado. Sem valor ajustado, ela é arbitrada pelos usos do lugar. Só a exclusividade precisa estar por escrito.
- **LGPD, arts. 5º, XVI, 7º, 9º, V, e 18, VII:** trocar lista de clientes entre empresas é uso compartilhado. Pede base legal, e o cliente tem direito a saber para quê e com quem.
- **Política do WhatsApp:** a empresa só pode chamar quem deu o número a ela e aceitou receber mensagem.
- **Lei 4.886/1965, art. 1º:** quem indica de vez em quando não é representante.
- **Lei 7.450/1985, art. 53:** prevê retenção sobre comissão entre empresas. A vigência não foi confirmada, por isso a tela só manda conferir com o contador.

**Etapa 3, Canal**

| # | Pergunta | Respostas | Aparece para |
|---|---|---|---|
| 1 | Como os seus parceiros indicam você hoje? | **Tenho acordo com cada parceiro, com o jeito de indicar combinado** / Tenho parceiros que indicam, sem combinado / Não tenho parceiros / Não sei | Todos |
| 2 | Você tem a lista dos seus parceiros, com o nome de quem indica em cada um? | **Tenho por escrito** / Sei de cabeça / Não sei | Quem tem parceiros |
| 3 | Pegue o acordo com o parceiro que mais indica. O que ficou combinado? | **Como indicar, o que conta como indicação e, se houver comissão, o valor** / Só que um indica o outro, sem detalhe / Não sei | Quem tem acordo |
| 4 | Você e algum parceiro trocam listas de contatos de clientes? | **Não trocamos** / Trocamos / Não sei | Quem tem parceiros |
| 5 | Quantos Parceiros Indicaram Alguém nos Três Últimos Meses Completos? | Número, medido ou estimado / Não sei | Quem tem parceiros |
| 6 | Quantas Indicações de Parceiros Chegaram Nesses Meses? | Número, medido ou estimado / Não sei | Quem tem parceiros |

- **Três pontos decidem o "de pé":** não trocar lista de clientes, a lista de parceiros por escrito e o acordo com o jeito de indicar.
- **Por onde começar:** segue essa ordem.
- **Em parte:** algum ponto falha, ou "parceiros que indicam, sem combinado", como na seção 4.3.
- **Falta:** "Não tenho parceiros". **Só informam:** os números.
- **Para o atendimento:** "Os parceiros sabem o que você faz e como indicar?" e "Quem pediu a troca de lista, e o que é feito com ela?".
- **Entregável:** "Uma lista de parceiros e um acordo de como um indica o outro, sem troca de lista de clientes."
- **Saíram:** a frase sem fonte "vale mais do que dez abordagens frias", as dicas antigas e o molde simples.

**Etapa 4:** o teste do indicado por um parceiro, com as respostas da Indicação de Clientes e os consertos falando de parceiro.

**Etapa 5:** o campo "Desses, Quantos Entraram no CRM com a Origem Parceiro?". O cruzamento vai para o atendimento. Na persona: "Chegaram cerca de 2 indicações de parceiros por mês, e nenhuma entrou no CRM com a origem Parceiro. Onde ficaram as outras 2?"

**Tela final:** o dono lê "Seus parceiros" e "Combine com cada parceiro como um indica o outro".

**Prova:** 587 conferências, todas passaram.
- São 21 novas de Parceiros e 4 de textos que saíram.
- A conversão geral do pilar e o canal com a tela anterior passaram para Revendas.
- A contagem de "Todos os canais" passou a 21 canais com medida própria.

**O que não está provado**
- Se o acordo com comissão é corretagem.
- A vigência de hoje do imposto retido.
- A base legal de uma troca de lista, que a LGPD não responde em abstrato.
- Se a empresa responde pelo parceiro, que é ponto aberto.
- Nada foi testado com dono de empresa nem com mentor.

**Estado do lote, em 11/11/2026:** a seu pedido, o lote fecha aqui para subir o módulo para o app.
- **Revendas e Representantes:** o levantamento oficial está feito e guardado na nota do lote, sem esqueleto.
- **Marketplaces:** não começou.
- **Os dois:** seguem com a tela simples da seção 4.3.

---

### 7. Acréscimos Meus Que Ainda Passam pela Sua Validação

Entraram no exemplo para a tela funcionar por inteiro. Você valida cada um quando a tela aparecer na homologação.

1. As frases descritas das conversões de Outbound, Branding e Indicação.
2. O aviso "Para seguir, marque de onde vem cada número: medido ou estimado".
3. A Etapa 2 da Receita Nova sem o "Não sei" genérico, porque a primeira frase já é "Não sei de onde vêm".
4. As opções "fora do CRM" das Etapas 6, 7 e 8, que valem "em parte".
5. A saída do aviso automático de "mais da metade" na origem dos clientes.
6. A varredura de registro: onde o texto mandava anotar contato, cliente ou origem, passou a mandar registrar. O CRM é cobrado como prova na Etapa 2, ao lado do levantamento, e nas Etapas 5 a 8.
7. A leitura da ficha no Google respeita a marca do número: medido ou estimado.
8. O ponto "mais da metade não chega a ficar pronta" usa o mesmo arredondamento do número mostrado na tela.
9. Na máscara dos números, dinheiro aceita duas casas depois da vírgula, e os outros campos aceitam uma.
10. O nome do pilar entra como "pelo Inbound", sem "seu", para o mesmo padrão servir a "por Indicação e Parcerias".
11. Os textos de leitura da ficha do Google: quantos pontos estão em dia, o que falta, a leitura da procura e o ponto para o atendimento.
12. Na ficha do Google, o percentual só é pedido a quem informou o número.
13. Os textos dos testes e as frases de por onde começar da Etapa 4, além das perguntas para o atendimento nos outros casos.
14. O mapeamento das respostas dos testes: "Ninguém atendeu" e "Precisei procurar" valem "em parte"; "O número não funciona" e "Levou ao lugar errado" valem "falta".
15. Na Tela 5: os caminhos de onde conferir, as frases de por onde começar, e "Entrou, mas falta origem" e "Não entrou" valendo "em parte".
16. Na Tela 5, a frase "Os contatos não ficam registrados" no lugar de "Os contatos chegam e se perdem".
17. Na Tela 6: os caminhos de onde conferir, as frases de leitura de cada resposta e as de por onde começar, e "A maioria", "Poucos ou nenhum" e "Não consigo ver essa lista" valendo "em parte".
18. Na Tela 6, as novas frases "Você volta a falar com alguns, e os outros ficam sem próximo passo" e "Hoje, quem não compra na primeira conversa fica sem retorno".
19. No Google Ads, a frase dos lances ficou "Quando os lances usam conversões, o Google procura mais gente que faz o que você conta como principal". A ajuda do Google diz que a ação principal só entra nos lances quando eles usam conversões.
20. No Google Ads, as perguntas de termos para o atendimento ficaram assim: "Alguns dos dez termos com mais cliques não têm a ver com o que você vende. Quanto da verba foi para eles?" e "A maioria dos dez termos... Para quais buscas o anúncio está aparecendo, e por quê?". No esqueleto estava "Parte dos cliques veio de buscas...".
21. No Google Ads, as leituras de quem nunca anunciou e de quem não sabe se o anúncio rodou, e o aviso para mais conversões do que cliques ("Isso pode acontecer quando a mesma pessoa conta mais de uma vez").
22. No Google Ads, os textos do teste da página para cada resposta, inclusive "Não tenho essa página", e as perguntas da Tela 3 e da Tela 4 indo juntas para o atendimento.
23. No Anúncio Meta, as leituras de cada resposta dos testes de conversa e de formulário, e os passos de por onde começar: "Troque no anúncio o WhatsApp pelo número que a empresa atende" e "Combine quem baixa os cadastros da Central de Leads todo dia".
24. No Anúncio Meta, "Sem saber para onde o anúncio leva" vale "não sei". Para quem nunca anunciou, "Ainda não sei" vale falta.
25. No Anúncio Meta, a pergunta do engajamento para o atendimento: "Quantos contatos o anúncio trouxe no último mês?".
26. A saída da frase "O canal tem rotina, mas o resultado ainda não é medido". Ela só servia ao molde antigo do anúncio, e o motivo do canal em parte passou a ser sempre a leitura do próprio canal.
27. No SEO, o passo para as buscas muda conforme a página. Com a página do serviço principal, o passo é "Ponha no título da página do serviço principal o nome do serviço e da cidade, e responda nela ao que o cliente pergunta". Sem a página, continua "Crie uma página para o seu serviço principal".
28. No SEO, as leituras de quem não sabe se tem o Search Console e de quem tem site sem ele, as perguntas para o atendimento de cada resposta e os textos próprios do teste da página, que não falam de anúncio.
29. No SEO, a frase do atendimento mudou para "Nas consultas que o Google mostra, nenhuma é sem o nome da empresa". É mais exata, porque o Google deixa algumas consultas de fora.
30. No GEO, as leituras de cada resposta, inclusive as do teste de perguntar a uma IA, e o que falta e o passo de quem não tem ficha: "Crie a ficha da empresa no Google, com as mesmas informações do site".
31. No GEO, a frase do mentor passou a ser "Decidir o que liberar primeiro e tratar o GEO como segundo passo, depois da presença básica". A anterior falava em saber se o canal foi testado.
32. No GEO, o texto de quem não tem site: "Sem site, o GEO não é o seu próximo passo. O Gemini usa as informações públicas do Google Maps, então a ficha no Google vem antes".
33. Nas Avaliações, com "Nunca recebi", as perguntas de resposta, nota, total e cinco mais recentes não aparecem, e o ponto da resposta conta como em dia.
34. Nas Avaliações, as leituras de cada resposta, o passo "Confira com a equipe se o link está chegando a todo cliente atendido" e o que aparece em O Que Você Já Tem: "Um pedido de avaliação aos clientes, ainda incompleto".
35. Nas Avaliações, a pergunta da Etapa 4 passou a ser "Por qual botão da ficha o cliente mais chega até você?", e sem ficha a etapa diz "Sem a ficha, ainda não há porta para testar", sem pergunta.
36. As respostas da porta da ficha ficaram em um lugar só, usado pelo Google Meu Negócio e pelas Avaliações. A tela do Google Meu Negócio não mudou.
37. Na Oferta, quem marca "Não sei" na primeira pergunta não vê as outras, e a Etapa 4 diz "Confira primeiro se a empresa tem uma oferta de entrada".
38. Na Oferta, a pergunta de quem comprou só aparece quando alguém aceitou, e o que aparece em O Que Você Já Tem é "Uma oferta de entrada, ainda incompleta".
39. Na Oferta, as leituras de cada resposta, os passos do teste do pedido e os textos da Etapa 4, entre eles "Pelo Código de Defesa do Consumidor, a oferta precisa obriga a empresa a cumprir o que diz".
40. No Ponto Físico, quem não tem placa ou tem a entrada fora da rua não vê as outras perguntas, e a Etapa 4 diz "Sem fachada, ainda não há o que testar".
41. No Ponto Físico, sem contato à vista, o segundo teste não aparece e a Etapa 4 fica em falta.
42. No Ponto Físico, as leituras de cada resposta, os passos dos dois testes, as perguntas para o atendimento e "Uma fachada, ainda incompleta" em O Que Você Já Tem. A leitura ficou "Dos três pontos da fachada", no padrão dos outros canais.
43. A frase geral do início passou a ser "A medida de cada canal traz o período na própria pergunta". A anterior dizia que toda medida era do último mês, o que deixou de ser verdade com as janelas de três meses.
44. Na Indicação de Clientes, o apoio da primeira pergunta: "Quem dá prêmio ou desconto a quem indica responde no canal Programa de Indicação."
45. Na Indicação de Clientes, o Onde Conferir do texto ensina a montar o link de conversa com "Vim por indicação de" e avisa que o link curto tem uma mensagem só, que vale para todo mundo.
46. Na Indicação de Clientes, a pergunta do obrigado some quando nenhuma indicação chegou, e quem não pede e não recebe indicação não vê as outras perguntas.
47. Na Indicação de Clientes, as leituras de cada resposta, os passos de cada falta, "Indicações que chegam sem pedido" em O Que Você Já Tem e a frase da decisão: "Decidir como pedir a todo cliente satisfeito e como a empresa fica sabendo quem indicou".
48. No Programa de Indicação, o apoio da primeira pergunta: "Por exemplo: desconto no próximo serviço para quem indicar alguém que comprar."
49. No Programa de Indicação, o Onde Conferir do sorteio traz o imposto de renda na fonte sobre prêmio em bens, pela Lei 8.981/1995, e a saída de trocar o sorteio por um prêmio certo.
50. No Programa de Indicação, as leituras de cada resposta, os passos de cada falta, "Um agrado a quem indica, ainda sem regra" em O Que Você Já Tem e a frase da decisão: "Decidir o prêmio que cabe no caixa e quem cuida de entregar cada um no prazo".
51. Na trilha do GEO, as leituras de cada resposta das dez perguntas e os passos de cada ponto em falta, entre eles "Cadastre a empresa no Bing Places. Ele importa os dados do Perfil no Google".
52. Na trilha do GEO, quem não está no Google não vê a comparação entre a ficha e o site, e quem não tem o Search Console não vê a pergunta do relatório de IA.
53. Na trilha do GEO, o teste do texto na folha de Onde Conferir: "Tente selecionar a frase com o dedo: se não seleciona, é imagem".
54. Na trilha do GEO, a pergunta para o atendimento do site excluído dos recursos de IA, e "Um site aberto aos robôs de busca das IAs, incluído nos recursos de IA do Google, com a empresa no Google e no Bing" em O Que Você Já Tem.
55. Em Parceiros, o apoio da primeira pergunta: "Quem vende o seu serviço por comissão, com frequência, responde no canal Revendas e Representantes."
56. Em Parceiros, o aviso de números trocados ("mais parceiros indicando do que indicações") e as leituras de cada resposta.
57. Em Parceiros, "Parceiros que indicam, ainda sem combinado" em O Que Você Já Tem e a frase da decisão: "Decidir com quais parceiros combinar primeiro e o que cada um ganha ao indicar".

---

### 8. Estado do Exemplo e das Provas

| Item | Onde está | Situação |
|---|---|---|
| Exemplo clicável | `docs/Aceleracao-365-Exemplo-Maturidade-Geracao-de-Leads-2026-11-05.html` | Refeito com a base nova e com o racional de medição e de registro |
| Cópia antes da base nova | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Base-Nova-2026-11-06.html` | Guardada, sem alteração |
| Cópia antes do racional de medição | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-Racional-do-Mes-2026-11-06.html` | Guardada, sem alteração |
| Cópia antes da ficha do Google | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Ficha-do-Google-2026-11-06.html` | Guardada, sem alteração |
| Cópia antes da Etapa 4 | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Etapa-4-2026-11-06.html` | Guardada, sem alteração |
| Cópia antes do Google Ads | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-Google-Ads-2026-11-07.html` | Guardada, sem alteração |
| Cópia antes do Anúncio Meta | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-Anuncio-Meta-2026-11-07.html` | Guardada, sem alteração |
| Cópia antes do SEO | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-SEO-2026-11-07.html` | Guardada, sem alteração |
| Cópia antes do GEO | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-GEO-2026-11-08.html` | Guardada, sem alteração |
| Cópia antes das Avaliações | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-das-Avaliacoes-2026-11-08.html` | Guardada, sem alteração |
| Cópia antes da Oferta de Entrada | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Oferta-de-Entrada-2026-11-08.html` | Guardada, sem alteração |
| Cópia antes do Ponto Físico | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-Ponto-Fisico-2026-11-08.html` | Guardada, sem alteração |
| Cópia antes da Indicação de Clientes | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Indicacao-de-Clientes-2026-11-11.html` | Guardada, sem alteração |
| Cópia antes do Programa de Indicação | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-do-Programa-de-Indicacao-2026-11-11.html` | Guardada, sem alteração |
| Cópia antes da trilha do GEO | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-da-Trilha-do-GEO-2026-11-11.html` | Guardada, sem alteração |
| Cópia antes de Parceiros | `docs/Aceleracao-365-Exemplo-Maturidade-Copia-Antes-de-Parceiros-2026-11-11.html` | Guardada, sem alteração |
| Prova do exemplo atual | `docs/Aceleracao-365-Prova-do-Racional-de-Medicao-Roteiro-2026-11-06.js` e `docs/Aceleracao-365-Prova-do-Racional-de-Medicao-Saida-2026-11-06.txt` | 587 conferências executadas, todas passaram |
| Prova da base nova | `docs/Aceleracao-365-Prova-da-Base-Nova-Roteiro-2026-11-06.js` e a saída dela | Vale só para a versão anterior do exemplo |
| Homologação tela a tela | No chat | Em andamento. Recomeçou pela Tela 1, depois do racional de medição e de registro |

Tipo de prova: comportamento executado. O roteiro carrega o código do exemplo, abre cada tela com respostas definidas e confere o texto que a tela mostra.

---

### 9. O Que Este Registro Não É

- Não é validação de mentor. As frases e as medidas foram validadas por você, em bloco, e podem ser ajustadas na homologação tela a tela.
- Não é o aplicativo. Nada do exemplo foi para a plataforma real.
- Não muda o que ficou em aberto no documento de fechamento: o uso do diagnóstico em papel, o método escrito dos mentores e o que a plataforma guarda.
