# A TAPADINHA — Manual Editorial e de Publicação Automática

**Versão:** 1.0 · 23/11/2026  
**Projeto:** Semanário digital independente sobre o Atlético Clube de Portugal  
**Repositório:** `thegamingdoctor85/a-tapadinha` · ramo `main`  
**Site:** https://a-tapadinha.netlify.app/  
**Referência visual aprovada:** https://a-tapadinha.netlify.app/edicoes/2026-11-09.html

> **Objetivo principal:** produzir e publicar, todas as semanas, uma revista investigada, envolvente, visualmente rica e factual, com intervenção humana apenas em caso de bloqueio real. Este manual é a referência permanente das automatizações de domingo (pesquisa) e segunda-feira (edição, controlo de qualidade e publicação).

## 1. Princípios editoriais

- **Leitores:** adeptos, familiares, leitores de jornal local e pessoas sem conhecimentos técnicos de futebol ou medicina. A revista deve ser compreensível e agradável para os pais do editor.
- **Tom:** jornalismo local e desportivo, caloroso, vivo, imaginativo, claro, com pequenas histórias e humor moderado. Títulos cativantes e artigos desenvolvidos; nunca um mero boletim de resultados.
- **Rigor:** nenhum resultado, citação, entrevista, lesão, fotografia, vídeo, estatística ou acontecimento pode ser inventado. Distinguir facto verificado, análise editorial e expectativa futura.
- **Autonomia:** procurar, verificar, redigir, diagramar e publicar sem pedir aprovações rotineiras. Na dúvida factual, investigar mais; se não for possível confirmar, omitir a afirmação ou assinalar claramente a incerteza.
- **Originalidade:** não repetir temas, mitos, personalidades e crónicas de semanas anteriores sem novidade factual ou ângulo realmente diferente.
- **Privacidade:** conteúdo inteiramente público. Nunca divulgar informação médica ou interna não publicada legitimamente.

## 2. Janela temporal e calendário

- A edição de cada **segunda-feira** cobre a **segunda a domingo anteriores**, com datas explícitas em `dd/mm/aaaa`.
- **Domingo, 20:00 — Pesquisa:** compilar dossier verificável; guardar em `pesquisa/YYYY-MM-DD.md`, em que `YYYY-MM-DD` é a **data da segunda-feira da edição**.
- **Segunda-feira, 07:00 — Edição:** ler dossier, atualizar o que mudou até à publicação, redigir, paginar, verificar e publicar.
- **Controlo de qualidade:** obrigatório **antes** de qualquer alteração pública; está integrado na tarefa de segunda-feira, sem necessidade de uma terceira automatização.
- Se o dossier não existir, estiver incompleto ou desatualizado, **efetuar pesquisa de contingência na segunda-feira**, em vez de produzir texto baseado em suposições.
- As tarefas agendadas têm de possuir acesso efetivo à pesquisa web e ao GitHub. O agendamento e a leitura deste manual não garantem, por si só, permissões ou publicação.

## 3. Hierarquia de fontes e método de pesquisa

Pesquisar de forma suficientemente ampla para captar tanto os resultados como a vida quotidiana do clube:

1. **Fontes oficiais:** Atlético CP, FPF, Liga 3, Taça de Portugal, páginas e comunicados dos adversários, competições, bilheteiras e calendário oficial.
2. **Jornalismo:** imprensa nacional, regional e local; reportagens, entrevistas a treinador, jogadores, direção e outras figuras do clube; confirmar atribuições e datas.
3. **Comunidade:** publicações públicas de Facebook, Instagram, YouTube, podcasts, associações de adeptos e fóruns; distinguir opinião e testemunho de notícia factual.
4. **Arquivo:** história oficial do clube, Hemeroteca Municipal de Lisboa, Biblioteca Nacional, imprensa de época, arquivos municipais e outros acervos fiáveis.
5. **Medicina desportiva:** revisões sistemáticas, consensos, orientações clínicas e estudos credíveis, interpretados com contexto e limitações.

**Em cada facto significativo**, guardar a data do acontecimento, data da publicação, fonte/URL direta e grau de confirmação. Cruzar informação sensível ou disputada em mais de uma fonte independente quando possível. Não confundir notícia publicada esta semana com acontecimento antigo. Não citar uma entrevista como se tivesse sido lida quando apenas foi confirmada a sua existência. Não inventar citações.

### Pesquisa desportiva mínima

- Atlético CP: jogo(s) da semana, resultado, competição, local, incidências e protagonistas **publicamente verificados**; análise contextual, forma recente e próximo adversário.
- **Liga 3 — Séries A e B:** jornada, classificação, jogos relevantes, números e tendências, apenas com dados confirmados e data de referência.
- **Taça de Portugal:** jogos e percurso do Atlético, sorteio, adversários e calendário, quando aplicável.
- **Clube alargado:** equipa B, direção, SAD, modalidades, iniciativas, adeptos, vida de Alcântara e da Tapadinha, sempre que exista matéria confirmável.
- **Vozes e multimédia:** entrevistas, declarações, vídeos, resumos, podcasts e material de bastidores oficialmente disponibilizado.

Se não houver notícias relevantes num tópico, não fabricar enchimento: desenvolver investigação histórica, contexto tático ou uma boa história documentada.

## 4. Dossier de pesquisa de domingo

**Ficheiro:** `pesquisa/YYYY-MM-DD.md` (data da edição, segunda-feira seguinte).

Estrutura recomendada:

1. **Identificação:** semana coberta, data/hora da recolha e limitações relevantes.
2. **Factos essenciais:** jogos, resultados, classificação, agenda e eventos, cada um com URL direta e data.
3. **Histórias potenciais:** notícias, entrevistas, comunidade, equipa B, direção/SAD e pontos de vista contrastantes.
4. **À Lupa:** lance, dinâmica de jogo ou situação tática suficientemente sustentada por vídeo, relato ou dados.
5. **História e figuras:** episódio de arquivo e personalidade concreta para duas rubricas distintas, com fontes primárias ou credíveis.
6. **Medicina:** um tema científico pertinente, links para estudos, conclusão possível e principais cautelas.
7. **Multimédia:** fotografia/vídeo, URL direta, autoria/créditos, correspondência ao evento, permissão ou forma legítima de ligação/incorporação.
8. **Novidade:** comparação com `EDITORIAL_TEMAS.md` e temas a evitar.
9. **Pendências:** factos a rever na segunda-feira; não tratá-los como confirmados.

Gravar o ficheiro no GitHub e **confirmar o commit**. A tarefa de domingo **não edita** `index.html` nem os HTML públicos das edições.

## 5. Estrutura editorial permanente da revista

A edição deve ter desenvolvimento jornalístico real, com a profundidade adequada à semana, mantendo as rubricas fundamentais:

- **Capa e editorial:** história principal, imagem forte real ou elemento de arquivo claramente identificado, manchete e contextualização.
- **A semana do Atlético:** crónica principal do(s) jogo(s), protagonistas, contexto, dados e ambiente, sem frases feitas.
- **À Lupa:** leitura de um lance ou momento tático, explicada de modo simples e sustentada por factos/vídeo.
- **Liga 3, Séries A e B:** resultados e classificação com referência temporal, estatísticas e consequências desportivas.
- **Taça de Portugal / Próximos desafios:** quando pertinente, com adversários e datas confirmadas.
- **Dentro e à volta do clube:** equipa B, SAD, direção, iniciativas, adeptos e redes sociais, conforme exista matéria verificável.
- **ARQUIVO DA TAPADINHA — História do Clube:** **obrigatório em todas as edições**. Um episódio, ano, conquista, local, objeto, fotografia, rivalidade ou recorte **concreto**, contextualizado e documentado. Nunca apenas um parágrafo sentimental genérico.
- **FIGURAS DA TAPADINHA — Personalidades:** **obrigatório em todas as edições**. Retrato biográfico individual de alguém comprovadamente ligado ao clube, com nome, datas, contribuição e fontes. Não confundir com o jogador em destaque no jogo da semana. Alternar gerações e papéis.
- **MEMÓRIA DA BANCADA:** rubrica própria, diferente de Arquivo e Figuras; cultura de bairro, tradições e experiência dos adeptos, com histórias concretas.
- **O que mudou no futebol?:** regras, equipamentos, tecnologia, organização ou hábitos, numa explicação curiosa e acessível.
- **SAÚDE EM FOCO:** artigo de medicina desportiva útil e compreensível, baseado em evidência atual e sem identificação de casos clínicos não públicos.
- **MITOS E VERDADES:** preferencialmente 2 a 4 afirmações **novas**, diferentes das edições anteriores, explicadas com evidência específica.
- **Curiosidades / fun facts e multimédia:** integrados de forma natural, sem ocupar espaço em detrimento do conteúdo.

Não impor uma contagem artificial de páginas, mas **não reduzir uma edição completa a poucos parágrafos lineares**. A qualidade da edição aprovada de 09/11/2026 é a referência de ambição editorial e design.

## 6. Originalidade e registo editorial

Antes de escolher histórias, **ler** `EDITORIAL_TEMAS.md` e consultar os HTML já publicados em `edicoes/`. Após uma publicação validada, **atualizar** o registo com:

- data, manchete e ângulo da edição;
- temas de saúde e cada mito/verdade;
- assunto de Arquivo, personalidade de Figuras e episódio de Memória da Bancada;
- entrevistas, vídeo, histórias relevantes, fontes e links;
- indicação explícita de um eventual **seguimento** de assunto anterior e o que mudou.

**Assuntos recentes a não reciclar sem novidade real:** ausência de dor como critério de aptidão; aquecimento e risco zero; Nordic hamstring/isquiotibiais; AINE preventivos; cãibras/magnésio; oito horas de sono; relatos genéricos da fundação e do estádio. O histórico completo e mais atualizado está no ficheiro `EDITORIAL_TEMAS.md`, que prevalece sobre esta lista exemplificativa.

## 7. Medicina desportiva e proteção de dados

- Preferir temas pertinentes para a medicina do futebol (prevenção, recuperação, sono, concussão, hidratação, carga, nutrição, comunicação em equipa), **sem partir de informação clínica privada sobre atletas**.
- Explicar o significado e a dimensão dos resultados científicos e mencionar incertezas e limitações; não transformar associações em causalidade nem recomendações gerais em aconselhamento individual.
- Incluir links discretos para as fontes científicas no artigo ou no seu final, não uma bibliografia pesada.
- Não divulgar diagnósticos, lesões, resultados de exames, tratamentos, prognósticos, disponibilidade competitiva, conversas internas, conflitos ou dados identificáveis **não tornados públicos por vias legítimas**.
- Sobre um atleta identificado, utilizar apenas informação clínica **publicada legitimamente** por fonte oficial e com atribuição.
- É permitido descrever genericamente o trabalho de um departamento médico, de forma humana, anónima e sem revelar dados sensíveis.
- Se a fronteira entre público e privado não for clara, **não publicar a informação**.

## 8. Fotografia, vídeo e direitos

- Priorizar **imagens reais, recentes e verificadas** do clube, jogos, estádio, protagonistas e arquivo histórico. Identificar claramente imagens de arquivo e a respetiva data quando conhecida.
- Antes de incorporar uma imagem, verificar que corresponde ao evento ou pessoa, que o `src` abre e que existem direitos ou autorização adequados de utilização. Uma fotografia encontrada na web **não está automaticamente autorizada** a ser republicada.
- Quando não houver permissão, utilizar **ligação direta à galeria oficial**, imagem autorizada alternativa, emblema autorizado ou recurso gráfico original. Nunca simular fotografias documentais de acontecimentos reais.
- Para YouTube, confirmar **ID, URL, equipas e data**. Incorporar responsivamente por `youtube-nocookie.com/embed/ID` **apenas quando a incorporação estiver permitida**; incluir título, `loading="lazy"`, opção para abrir na origem e fallback.
- Para Canal 11, Instagram, Facebook ou outros sem incorporação legítima, usar cartão visual e **link direto** para a página/vídeo correto, nunca uma falsa reprodução.
- Não copiar ou hospedar transmissões protegidas, contornar autenticação, licenças ou paywalls.
- Se não existir vídeo autêntico verificável, omitir o bloco. Nunca deixar um player ou imagem vazios.

## 9. Design, HTML e experiência de leitura

**Modelo visual obrigatório:** `edicoes/2026-11-09.html` (09/11/2026). **Consultar o código real** antes de desenhar a edição nova e recuperar a sua linguagem visual, não apenas a descrição textual.

- Revista digital vertical, fluida, pensada para telemóveis e tablets (referência editorial 10:16), mas responsiva em desktop.
- Identidade Atlético CP: azul/celeste, amarelo e vermelho, emblema em evidência, capa forte, tipografia expressiva e paginação/navegação por capítulos.
- Fotografia, quadros de resultados, tabelas, cartões, citações, estatísticas e ritmo visual equilibrados; manter uma boa relação entre texto, imagem e espaço em branco.
- Evitar colunas esmagadas, caixas desalinhadas, textos demasiado pequenos, elementos sobrepostos e grandes blocos vazios quando imagens falham.
- `alt` em imagens, links funcionais, elementos de navegação acessíveis e boa legibilidade/contraste.
- Recursos externos só quando confiáveis e permitidos; preferir caminhos relativos para recursos locais.
- **Não substituir um webzine rico por HTML minúsculo ou um texto simples** por conveniência de execução.

## 10. Repositório e publicação — regras de segurança

Estrutura pretendida (sem eliminar outros ficheiros existentes):

```text
a-tapadinha/
├── MANUAL_EDITORIAL.md          ← este ficheiro, na raiz
├── EDITORIAL_TEMAS.md           ← histórico de temas
├── index.html                   ← capa, destaque atual e arquivo
├── pesquisa/
│   └── YYYY-MM-DD.md            ← dossier da edição da segunda-feira
└── edicoes/
    ├── 2026-11-09.html          ← modelo visual aprovado
    ├── 2026-11-16.html
    ├── 2026-11-23.html
    └── YYYY-MM-DD.html           ← nova edição
```

Procedimento de publicação:

1. Ler a versão atual dos ficheiros relevantes no GitHub, sobretudo `index.html` e o histórico de edições. **Nunca sobrescrever cegamente** a página inicial.
2. Construir e rever uma **edição completa** antes de enviar o novo HTML público.
3. Verificar que o caminho `edicoes/YYYY-MM-DD.html` não pertence a uma edição anterior; **não substituir nem eliminar edições antigas**.
4. Confirmar qualidade editorial, multimédia e técnica segundo a lista da secção 11. Se falhar, **não publicar uma edição inferior**.
5. Criar o HTML no ramo `main`; confirmar o commit.
6. Atualizar `index.html` **preservando todos os links de arquivo**, o desenho existente e a navegação; acrescentar a edição em destaque sem apagar anteriores. Ler o SHA/conteúdo atual antes de editar.
7. Atualizar `EDITORIAL_TEMAS.md` e confirmar o respetivo commit.
8. A integração GitHub → Netlify deverá desencadear o deploy automaticamente; verificar **separadamente** a URL pública da edição e a página inicial.
9. Só declarar **«publicado no Netlify»** se a página pública carregar e corresponder à edição criada. Um commit no GitHub não prova que o deploy esteja concluído.
10. Se a publicação ou verificação falhar, não criar outro site/repositório nem alterar DNS; comunicar o estado preciso e preservar a última edição válida.

**Destino:** https://a-tapadinha.netlify.app/  
**Edições:** `https://a-tapadinha.netlify.app/edicoes/YYYY-MM-DD.html`.

## 11. Lista de controlo obrigatório antes de publicar

### Editorial

- [ ] Semana e datas corretamente identificadas.
- [ ] Resultados, classificações, calendários e protagonistas confirmados, com fontes.
- [ ] Artigos desenvolvidos, informativos e agradáveis para leitores não especialistas.
- [ ] Arquivo e Figuras incluem duas peças substanciais, novas e documentadas.
- [ ] Memória da Bancada é uma rubrica autónoma.
- [ ] Saúde em Foco é rigorosa, acessível e não divulga informação privada.
- [ ] Mitos e Verdades são novos e sustentados; histórico consultado.
- [ ] Sem citações inventadas, conteúdos duplicados ou notícias antigas apresentadas como novas.

### Imagem e experiência

- [ ] Template de 09/11 efetivamente consultado e respeitado.
- [ ] Capa, emblema, identidade cromática, paginação e conteúdo visual com qualidade equivalente.
- [ ] Fotografias/vídeos autênticos, relevantes, autorizados ou ligados legitimamente à origem.
- [ ] URLs de imagem, vídeo e links verificados; sem players ou espaços vazios.
- [ ] Legibilidade e navegação verificadas em ecrã pequeno, na medida em que as ferramentas disponíveis o permitam.
- [ ] Sem erros grosseiros de HTML, problemas de codificação ou secções cortadas.

### Publicação

- [ ] HTML novo completo e caminho correto.
- [ ] Edições antigas e links de arquivo preservados.
- [ ] Commits GitHub confirmados.
- [ ] `EDITORIAL_TEMAS.md` atualizado.
- [ ] Acesso público no Netlify verificado antes de anunciar sucesso.

**Regra de bloqueio:** se uma verificação essencial falhar (privacidade, factos nucleares, direitos de utilização, conteúdo incompleto, integridade do arquivo ou ausência de confirmação de publicação), interromper a etapa afetada e comunicar o bloqueio. Não substituir uma edição válida por um rascunho inferior.

## 12. Relatório final e tratamento de falhas

A mensagem ao utilizador deve ser curta e útil, contendo:

- edição e semana coberta;
- 3–5 destaques editoriais;
- ligação pública direta **apenas se verificada**;
- estado separado de **dossier**, **commit GitHub**, **índice/arquivo** e **deploy Netlify**;
- problema concreto e ação necessária, apenas se houver falha.

Quando não for possível concluir, entregar um resumo substantivo do material apurado e indicar o que ficou por verificar, sem inventar resultados nem afirmar que ficheiros foram criados. O relatório técnico de falhas é dirigido ao utilizador, **não aparece como texto dentro da revista**.

## 13. Instruções curtas para as automatizações

**Automatização A — domingo, 20:00 (Europe/Lisbon):**

> Consulta `MANUAL_EDITORIAL.md` no ramo `main` de `thegamingdoctor85/a-tapadinha`, executa integralmente a secção de pesquisa semanal e guarda `pesquisa/YYYY-MM-DD.md`, com data da segunda-feira seguinte. Confirma o commit. Não alteres `index.html` nem as edições públicas. Se uma fonte falhar, regista a lacuna em vez de inventar.

**Automatização B — segunda-feira, 07:00 (Europe/Lisbon):**

> Consulta `MANUAL_EDITORIAL.md`, `EDITORIAL_TEMAS.md`, `edicoes/2026-11-09.html`, `index.html` e o dossier `pesquisa/YYYY-MM-DD.md` do repositório `thegamingdoctor85/a-tapadinha`. Faz pesquisa complementar se necessário. Produz a revista da semana anterior, executa a lista de controlo e só então publica no GitHub, atualiza o índice preservando o arquivo e verifica o deploy no Netlify. Se a edição falhar os critérios essenciais, não publiques uma versão reduzida. Comunica o estado real.

---

**Nota operacional:** Este manual estabelece regras e caminhos. Para haver autonomia real, ambas as automatizações devem estar criadas/ativas e possuir acesso às ferramentas GitHub, pesquisa e publicação. O ficheiro sozinho não inicia tarefas nem concede permissões. O Netlify publica automaticamente alterações no ramo ligado quando a integração está funcional, mas a verificação do deploy continua obrigatória.


## 18. Rubrica fixa: «O Atlético na Imprensa» (adenda 25/11/2026)

O semanário deve procurar de forma sistemática notícias sobre o Atlético na imprensa nacional e regional, com particular atenção a **entrevistas individuais e coletivas, perfis de jogadores, treinadores e dirigentes, grandes reportagens, histórias sobre modalidades, clube/SAD, adversários e cobertura fotográfica**. Pesquisar por nome completo do clube, sigla, Tapadinha, nomes das pessoas e próximo adversário. Fontes prioritárias a verificar: Record, A Bola, O Jogo, RTP/Lusa, Renascença, Diário de Notícias, Jornal de Notícias, Público, Observador, SIC, TVI/CNN e imprensa regional. Não ficar apenas nas fontes oficiais nem em manchetes de domingo.

A rubrica **«O Atlético na Imprensa»** terá, sempre que existam notícias novas relevantes, 1–4 recortes em destaque, com design de revista ilustrada, síntese original (80–200 palavras por notícia), referência explícita a **jornal, autor e data**, link direto para a publicação legítima ou edição/página impressa e foto utilizável com crédito quando os direitos o permitirem. NÃO reproduzir extensamente o texto original, páginas integrais, fotos comerciais sem autorização ou conteúdo premium. O link para o artigo original e um bloco gráfico em HTML/CSS são alternativas quando não houver licença para a fotografia original. Evitar repetir a crónica de jogo como se fosse novidade; explicar o que a nova entrevista revelou.

**Pista obrigatória para a edição de 30/11/2026:** ler antes de tudo `pesquisa/2026-11-30-pistas-imprensa.md`. Inclui a página 23 do **Record de 25/11/2026**, artigo de **Francisco Guerra** sobre **Janico**, com título «Fresneda do Atlético faz mira ao Sporting». O utilizador forneceu fotografia da página. Produzir resumo próprio dessa entrevista, destacando a passagem de Janico de protagonista do golo contra o Casa Pia a figura de jornal nacional, a comparação com Fresneda, a tranquilidade perante Alvalade e o foco no Lusitano de Évora. Incluir uma fotografia verdadeira de Janico licenciada ou com autorização identificada; se indisponível, usar um cartão editorial próprio com link direto e crédito ao Record, sem substituir por fotografia de outro atleta. O recorte fornecido não é licença implícita de republicação em site aberto.

**Checklist antes de publicar:** a pesquisa consultou a imprensa nacional? há alguma entrevista ou destaque realmente novo? as datas e nomes são rigorosos? as fotografias são legítimas e legíveis em telemóvel? há link legítimo, resumo original e distinção em relação às edições anteriores? Foi preservada toda a riqueza da capa, rubricas históricas, Figuras, Mitos, multimédia e arquivo?
