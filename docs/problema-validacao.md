# Problema e validação

**Solução:** Achados e Perdidos UCSal
**Equipe e turma:** ADS matutina (terças-feiras, 07:00-09:50)
**Integrantes:** Cauã de Oliveira Lopes · Ryan Abade Oliveira · Pedro Luiz de Barros Pereira · Arivaldo Teixeira Moraes Neto

---

## Anexo A — Ficha do problema

**Formulação:** Para *estudantes, professores, colaboradores e visitantes da UCSal (Campus Pituaçu) que perdem objetos no campus*, que enfrentam *a dificuldade de saber à distância se o pertence foi encontrado* durante *a rotina diária nas salas e espaços do campus*, a consequência é *objetos que permanecem armazenados por até um ano sem resgate e deslocamentos presenciais desnecessários até a sala B304 apenas para consultar se o item está lá*. Hoje, esse público tenta resolver a situação por meio de *ir presencialmente ao setor de Achados e Perdidos, onde o atendimento é exclusivamente presencial e o registro dos objetos é manual*.

| Campo | Preenchimento |
|-------|---------------|
| **Público** | Beneficiários diretos: estudantes de graduação e pós-graduação, professores e visitantes da UCSal que perdem pertences no Campus Pituaçu (estimativa de 140 a 200 atendimentos diretos por semestre, com base na média de 7 a 10 itens recebidos por semana em 20 semanas letivas). Beneficiários indiretos: funcionário responsável pelo setor de Achados e Perdidos, recepção/portaria e demais frequentadores do campus (~3.000 pessoas). |
| **Situação** | Quando alguém perde um objeto (garrafas, fones de ouvido, carregadores, óculos, casacos, celulares ou documentos) nas dependências do campus e precisa saber se ele foi entregue ao setor de Achados e Perdidos, localizado na sala de apoio B304 (3º andar). |
| **Problema** | Não existe canal remoto de consulta: a pessoa só descobre se o objeto foi encontrado indo presencialmente ao setor. Por sua vez, o funcionário cataloga cada item manualmente com fita crepe (data e local) e o armazena por categoria em caixas e prateleiras, sem apoio de sistema digital. |
| **Impacto** | Itens comuns ficam acumulados por quase um ano antes de seguirem para doação por falta de procura; alunos perdem tempo com deslocamentos desnecessários (inclusive pessoas com dificuldade de locomoção); e o setor sofre sobrecarga com consultas presenciais repetitivas e controle manual. |
| **Alternativa atual** | Deslocamento presencial até a sala B304; busca visual em caixas/prateleiras por categoria; registro manual com fita crepe e preenchimento de ficha física na retirada (nome, matrícula, curso, RG, CPF e data). Documentos e carteiras ficam 2 a 3 dias no setor e depois seguem para a recepção principal e segurança. |
| **Hipótese crítica** | (1) Um catálogo web público com busca e status reduz deslocamentos desnecessários e aumenta a recuperação de objetos. (2) A catalogação assistida por IA a partir de uma foto agiliza o registro feito pelo funcionário sem exigir digitação extensa. (3) Ocultar detalhes de itens sensíveis e manter a entrega presencial preserva a privacidade (LGPD) e evita reivindicações falsas. |
| **Evidência** | Entrevista estruturada com o funcionário do setor de Achados e Perdidos da UCSal e experimento prático com protótipo inicial (chatbot) realizado com estudantes no Projeto de Extensão *"Inteligência Artificial para Inclusão e Cidadania"* (2026.2, Grupo AF), detalhados no Anexo B. |
| **Recorte** | Catálogo web público sem login (filtros, busca inteligente com sinônimos e status em tempo real), sinalização de interesse pelo aluno, controle de pedidos concorrentes e catalogação assistida por foto com IA (com fallback). A confirmação de propriedade e a entrega física continuam presenciais na sala B304. |

---

## Anexo B — Registro de validação

Cada linha registra uma entrevista, observação, teste ou fonte relevante, sem identificação pessoal.

| Data e perfil | Hipótese | Evidência observada | Decisão |
|---------------|----------|---------------------|---------|
| **1. 10/2026** — funcionário do setor de Achados e Perdidos da UCSal (sala B304, Campus Pituaçu, ~11 anos de atuação). Fonte: entrevista do Projeto de Extensão *"Inteligência Artificial para Inclusão e Cidadania"* (2026.2, Grupo AF). | O setor não possui sistema digital e a falta de comunicação remota faz com que objetos fiquem parados sem procura. | O setor recebe de 7 a 10 itens por semana, catalogados à mão com fita crepe (data e local) e separados em caixas por categoria. Não há telefone ou WhatsApp para consulta devido à equipe reduzida. Enquanto celulares são procurados rapidamente, garrafas, fones, casacos e acessórios chegam a ficar armazenados por cerca de 1 ano antes de irem para doação. Documentos/carteiras ficam 2 a 3 dias e seguem para a recepção/segurança. | **Manter** o problema, a entrega presencial com conferência física e o tratamento diferenciado para itens sensíveis (celular, carteira e documentos). |
| **2. 30/10 a 13/11/2026** — 15 sessões de uso e questionário de avaliação com estudantes de graduação (experimento do protótipo conversacional Typebot + Groq no Projeto de Extensão). | Um chatbot conversacional seria suficiente e intuitivo para o estudante consultar se seu objeto foi encontrado. | Das 15 interações registradas, 40% buscaram itens perdidos e 33,3% consultaram localização/horário, porém várias sessões foram abandonadas antes do preenchimento completo. No questionário (13/11/2026), ambos os respondentes confirmaram já ter tido dificuldade para localizar objetos/setor, mas avaliaram a facilidade de navegação do chatbot como *"muito difícil"* e *"regular"*, apontando atendimento apenas parcial e pedindo melhor organização visual. | **Alterar** a abordagem de chatbot para um **catálogo web visual** direto (sem necessidade de conversa guiada), mantendo a IA aplicada à busca semântica e à catalogação automática por foto. |

### Síntese dos aprendizados

- **Problema validado na operação real:** o gargalo principal não é a guarda física dos objetos na sala B304, mas a barreira de comunicação entre o setor e a comunidade acadêmica, que gera acúmulo prolongado de pertences e deslocamentos desnecessários.
- **Pivô fundamentado em teste com usuários:** a experiência anterior com chatbot mostrou atrito de navegação e abandono no meio do fluxo conversacional. A migração para um catálogo web visual com filtros e status imediatos elimina etapas desnecessárias para o aluno.
- **Segurança e privacidade desde o desenho:** em alinhamento com a rotina real do setor e com os princípios de necessidade e segurança da LGPD, itens sensíveis (celulares, carteiras e documentos) não expõem foto nem descrição detalhada na consulta pública, e a validação final de propriedade permanece humana e presencial.
- **Limitação declarada:** a validação atual baseia-se na entrevista com o funcionário do setor e nos dados do experimento anterior com estudantes no projeto de extensão. A validação de usabilidade específica desta interface web do MVP com colegas e com o funcionário do setor está planejada para ocorrer antes da mostra de 01/12/2026.

### Mudanças realizadas no problema ou na solução

- **Migração de chatbot para sistema web de catálogo:** substituímos o fluxo conversacional por uma listagem web filtrável com busca inteligente por sinônimos e ciclo de vida explícito (`Disponível` → `Em análise` → `Devolvido`), atendendo tanto à usabilidade dos alunos quanto ao requisito de fluxo ponta a ponta do POOALAB.
- **Catalogação assistida por foto com IA (e fallback):** incorporamos o envio de foto pelo responsável para sugestão automática de categoria, título, cor, marca e características de conferência via Gemini, reduzindo o trabalho manual da fita crepe sem retirar a revisão humana antes de salvar.
- **Proteção de itens sensíveis e pedidos concorrentes:** implementamos ocultação automática de detalhes para celular, carteira e documentos na visão pública e suporte a múltiplos pedidos simultâneos pelo mesmo item para conferência presencial no balcão.
