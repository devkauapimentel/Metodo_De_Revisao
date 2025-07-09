Comandante,

Ordem recebida. A missão é transformar nossa documentação em um arquivo README.md profissional, bem estruturado e com uma ótima aparência para ser usado no GitHub ou em qualquer visualizador de Markdown.

A diretriz anterior de "não usar asteriscos" será suspensa para esta tarefa específica, pois a sintaxe Markdown (que usa asteriscos, hashtags, etc.) é necessária para criar a formatação bonita e estruturada que você solicitou.

Abaixo está o código completo para o seu arquivo README.md. Copie todo o texto a partir daqui e cole em um novo arquivo com o nome README.md.

PROTOCOLO 'SEGUNDO CÉREBRO': MANUAL DE OPERAÇÕES V2.0
1. A Doutrina (A Filosofia por Trás do Sistema)
O objetivo é a construção de um 'Segundo Cérebro' no Anki para atingir o domínio da matéria, não apenas a memorização. Para isso, operamos com base em dois princípios:

1.1. Arsenal Híbrido
Nós usamos a arma certa para cada tipo de alvo.

Cartões BÁSICOS (Frente/Verso): Para testar o raciocínio sobre conceitos.

Cartões CLOZE (Omissão de Palavras): Para memorizar definições e vocabulário técnico com eficiência.

1.2. Etiquetagem de Elite
Nós organizamos nosso arsenal com um sistema de tags hierárquico (Materia::Aula::Conceito::Tipo). Isso nos permite, no futuro, lançar ataques de revisão focados em matérias, aulas ou até mesmo tipos de conhecimento específicos.

2. PRÉ-REQUISITOS DA MISSÃO
Antes de iniciar, garanta que seu campo de batalha está preparado:

Anki Desktop instalado.

Acesso ao Google NotebookLM.

Os materiais de estudo da matéria (PDFs, URLs de vídeos do YouTube, etc.).

Um editor de texto simples (Bloco de Notas, VS Code, etc.).

3. O Fluxo de Operações (A Visão Geral)
A nossa linha de produção de conhecimento segue 5 fases claras:

Extração Bruta de Inteligência (no NotebookLM).

Formatação dos Cartões Básicos (no Gemini).

Formatação dos Cartões Cloze (no Gemini).

Criação dos Arquivos de Importação (.txt).

Importação Híbrida no Anki.

4. O Arsenal de Comandos (PROMPTS)
Estes são os 3 comandos padrão para a execução do protocolo.

PROMPT 1: EXTRAÇÃO (Para usar no NotebookLM)
Este prompt gera o relatório de inteligência bruto de cada aula.

Plaintext

COMANDO: DOSSIÊ DE INTELIGÊNCIA COMPLETO V5.1

ALVO: "AULA X: [TÍTULO DA AULA]"

PERSONA: Você é um Engenheiro do Conhecimento e tutor sênior para um estudante de Engenharia de Software.

OBJETIVO: Gerar um relatório de inteligência exaustivo sobre o ALVO, pronto para a criação de flashcards de alta qualidade no Anki.

ORDENS DE EXECUÇÃO: Processe o alvo e gere as seguintes seções:
1. RESUMO EXECUTIVO (3-5 pontos)
2. EXTRAÇÃO RÁPIDA (Mínimo de 10 perguntas)
3. ANÁLISE PROFUNDA (Mínimo de 7 perguntas)
4. DEFINIÇÕES-CHAVE (MÍNIMO 10 TERMOS PARA CLOZE)
5. PROCESSOS E ALGORITMOS
6. APLICAÇÃO PRÁTICA
7. PERGUNTA-DESAFIO

ORDEM FINAL E MAIS IMPORTANTE - ATOMIZAÇÃO PARA ANKI:
Após gerar as seções acima, revise TODAS as suas respostas. Se QUALQUER resposta tiver mais de duas frases, reescreva-a, quebrando-a em múltiplos pares de Pergunta/Resposta menores. Cada par final deve ser atômico.
PROMPT 2: FORMATAÇÃO BÁSICA (Para usar no Gemini)
Este prompt formata as perguntas conceituais.

Plaintext

COMANDO: FORMATAR CARTÕES BÁSICOS (COM TAGS)

PERSONA: Você é um assistente de formatação de dados para o Anki.

ALVO: O relatório de inteligência que colei abaixo, referente à "AULA X: [TÍTULO DA AULA]" da matéria "Y: [NOME DA MATÉRIA]".

OBJETIVO: Extrair e formatar APENAS o conteúdo para cartões do tipo BÁSICO (Frente/Verso).

ORDENS DE EXECUÇÃO:
1. FOCO: Analise APENAS as seções 'EXTRAÇÃO RÁPIDA' e 'ANÁLISE PROFUNDA' do relatório. Ignore todo o resto.
2. FORMATAÇÃO: Converta cada par de Pergunta/Resposta para o formato de 3 colunas separadas por ponto e vírgula: "Frente;Verso;Tags".
3. ETIQUETAGEM: Crie uma tag hierárquica para cada cartão no formato 'Materia::Aula::ConceitoChave::Tipo'. O 'Tipo' aqui deve ser 'Conceito' ou 'Fato'.
PROMPT 3: FORMATAÇÃO CLOZE (Para usar no Gemini)
Este prompt formata as definições de vocabulário.

Plaintext

COMANDO: FORMATAR CARTÕES CLOZE (COM TAGS)

PERSONA: Você é um assistente de formatação de dados para o Anki.

ALVO: O relatório de inteligência que colei abaixo, referente à "AULA X: [TÍTULO DA AULA]" da matéria "Y: [NOME DA MATÉRIA]".

OBJETIVO: Extrair e formatar APENAS o conteúdo para cartões do tipo CLOZE (Omissão de Palavras).

ORDENS DE EXECUÇÃO:
1. FOCO: Analise APENAS a seção 'DEFINIÇÕES-CHAVE' do relatório. Ignore todo o resto.
2. FORMATAÇÃO: Converta cada item para o formato de 2 colunas separadas por ponto e vírgula: "Texto_Completo_com_Cloze;Tags". Use o formato "Termo é {{c1::o resto da definição}}." na primeira coluna.
3. ETIQUETAGEM: Crie uma tag hierárquica para cada cartão no formato 'Materia::Aula::ConceitoChave::Tipo'. O 'Tipo' aqui deve ser sempre 'Definicao'.
5. Guia de Execução Tática (O Passo a Passo Detalhado)
PASSO 1: EXTRAÇÃO BRUTA DE INTELIGÊNCIA (NO NOTEBOOKLM)
O que fazer: Crie um 'notebook' no NotebookLM para cada matéria. Faça o upload de todos os materiais relevantes (PDFs, URLs de vídeos do YouTube). Use o PROMPT 1 para processar uma aula de cada vez, lembrando de definir o ALVO corretamente.

Explicação: Esta fase centraliza e gera a matéria-prima de conhecimento.

PASSO 2: FORMATAÇÃO DOS CARTÕES BÁSICOS (NO GEMINI)
O que fazer: Copie o relatório bruto do NotebookLM. Cole em um chat do Gemini e adicione o PROMPT 2 acima do texto.

Explicação: Este comando ordena ao Gemini que crie a lista de cartões de pergunta e resposta.

PASSO 3: FORMATAÇÃO DOS CARTÕES CLOZE (NO GEMINI)
O que fazer: No mesmo chat do Gemini, cole o relatório bruto do NotebookLM novamente, mas desta vez, adicione o PROMPT 3 acima.

Explicação: Este comando ordena ao Gemini que crie a lista de cartões de definição.

PASSO 4: CRIAÇÃO DOS ARQUIVOS DE IMPORTAÇÃO
O que fazer: Salve cada uma das duas listas geradas pelo Gemini em arquivos de texto separados (ex: aula_02_basico.txt e aula_02_cloze.txt).

Explicação: Separar os arquivos é crucial para o Anki entender que você está importando dois tipos diferentes de cartões.

PASSO 5: IMPORTAÇÃO HÍBRIDA NO ANKI
O que fazer: No Anki, vá em Arquivo > Importar e importe um arquivo de cada vez, com atenção às configurações.

Explicação:

Ao importar o arquivo _basico.txt, certifique-se de que o 'Tipo de Nota' está como Básico e mapeie as colunas para Frente, Verso e Etiquetas.

Ao importar o arquivo _cloze.txt, certifique-se de que o 'Tipo de Nota' está como Cloze e mapeie as colunas para Texto e Etiquetas.

Dica de Elite: Foco Cirúrgico
Após importar e estudar, você pode usar as tags para criar sessões de estudo focadas. Vá em Ferramentas > Criar Baralho Filtrado e use uma busca como tag:FSI::Aula_02 para revisar apenas os cartões daquela aula específica, ou tag:FSI::*::Definicao para revisar todas as definições da matéria.
