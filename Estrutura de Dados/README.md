# Estruturas de Dados Simplesmente Explicadas

Este documento contém o resumo de cada estrutura de dados abordada no vídeo, incluindo seu nome, uma breve explicação textual e exemplos práticos.

---

## 1. Arrays (Matrizes / Vetores)
* **Texto:** É uma coleção ordenada de itens de tamanho fixo onde cada item fica em uma posição numerada, permitindo que você acesse qualquer valor instantaneamente ($O(1)$). No entanto, sua principal limitação é a rigidez: alterar o tamanho ou inserir um elemento no meio do Array é muito custoso, pois exige realocar um novo bloco de memória ou deslocar todos os outros elementos.
* **Exemplo:** Os assentos numerados em um cinema. Se você procura a cadeira 47, vai direto para lá sem checar as outras. Outros exemplos são os pixels de uma imagem ou os frames de uma transmissão de vídeo.

## 2. Linked Lists (Listas Encadeadas)
* **Texto:** Criada para resolver a falta de flexibilidade dos Arrays. Consiste numa corrente de "nós" (nodes) espalhados na memória. Cada nó guarda seu valor e um ponteiro apontando exatamente para o próximo. Inserir ou remover é instantâneo (apenas mudando os ponteiros), mas a leitura é lenta, pois você precisa percorrer a corrente do início até achar a informação.
* **Exemplo:** Uma caça ao tesouro, onde cada pista simplesmente diz onde está escondida a próxima pista.

## 3. Stacks (Pilhas)
* **Texto:** Uma estrutura de dados estritamente guiada pela lógica "o último a entrar é o primeiro a sair" (LIFO - Last In, First Out). Você só pode adicionar (*Push*) ou remover (*Pop*) elementos no topo da pilha, o que torna as operações super rápidas. Você não pode retirar nada do meio ou do fundo.
* **Exemplo:** Uma pilha de pratos (você pega e põe sempre o do topo). Aplica-se no botão "Voltar" do navegador ou na função de Desfazer (Ctrl+Z) de editores de texto.

## 4. Queues (Filas)
* **Texto:** O exato oposto das pilhas. Usa a lógica de "o primeiro a entrar é o primeiro a sair" (FIFO - First In, First Out). Elementos são adicionados sempre no final (*Enqueue*) e removidos sempre da frente (*Dequeue*).
* **Exemplo:** Uma fila física em uma cafeteria (quem chegou primeiro será servido primeiro) ou a fila de documentos esperando para serem impressos em uma impressora compartilhada.

## 5. Deques (Filas de Duas Pontas)
* **Texto:** Uma estrutura mais dinâmica, sendo uma "fila de ponta dupla". Ela permite que você adicione e remova itens instantaneamente tanto pela parte da frente quanto pela parte de trás. Pode se comportar como uma Fila ou como uma Pilha, a depender da sua necessidade.
* **Exemplo:** Um trem onde os passageiros podem acessar e sair de forma simultânea por qualquer lado. Também usada no histórico do navegador (permitindo voltar e avançar) e em processamento de janelas deslizantes (*sliding windows*).

## 6. Hashmaps (Tabelas Hash)
* **Texto:** Estrutura que armazena dados em pares de "chave" e "valor". Quando você insere algo, a chave passa por uma função matemática (*função hash*) que a converte em um número, indicando um endereço exato na memória. O acesso é incrivelmente rápido ($O(1)$) porque, independente de ter 10 ou 10 milhões de dados, encontrar um registro é sempre instantâneo.
* **Exemplo:** Buscar pela sua "Mãe" na sua lista de contatos do celular; a chave é a palavra e o valor é o número de telefone que aparece na hora, sem precisar vasculhar todos os contatos.

## 7. Hash Sets (Conjuntos Hash)
* **Texto:** Basicamente um Hashmap focado exclusivamente nas "chaves", descartando os valores. Ele serve inteiramente para responder de forma imediata a uma única pergunta: "Este item já existe nessa coleção?". Como regra, cada item dentro dele aparece exatamente apenas uma vez, não possuindo duplicatas.
* **Exemplo:** A lista de convidados checada pelo segurança de uma boate (ele só quer saber se seu nome está ali e mais nada).

## 8. Trees (Árvores)
* **Texto:** Ao invés de uma lista plana, é uma estrutura que representa hierarquias. Possui uma "raiz" principal no topo, que se ramifica de forma direcional em diversos "nós" e termina em "folhas" na base. É focada nas relações de parentesco (pai e filho).
* **Exemplo:** O explorador de arquivos do seu computador (uma raiz dividida em pastas, e depois arquivos) ou as tags HTML organizadas dentro de uma página web.

## 9. Binary Search Trees / BST (Árvores de Busca Binária)
* **Texto:** Aplica uma regra rígida às árvores normais: em todo nó, o elemento à esquerda deve ser sempre menor e o à direita deve ser maior. Isso faz com que cada passo dado na busca elimine metade de todas as outras possibilidades, acelerando incrivelmente a procura de informações.
* **Exemplo:** O clássico jogo de tentar adivinhar um número entre 1 e 1000. Se a pessoa chutar 500 e a resposta for "muito alto", ela instantaneamente corta fora todas as possibilidades de 500 para cima.

## 10. Heap
* **Texto:** Uma estrutura baseada em árvore que foca em dar acesso imediato apenas ao "elemento mais importante". Ela se reorganiza de forma silenciosa e automática sempre que um novo dado é adicionado, certificando-se de manter o item de prioridade mais alta fixo lá no topo da lista.
* **Exemplo:** A sala de emergência de um hospital (se alguém com um ataque do coração chega, pula na frente do paciente que chegou primeiro apenas com dor de cabeça). Outro exemplo é um aplicativo de GPS que fica recalculando rapidamente as rotas com melhor prioridade perante o trânsito.

## 11. Graphs (Grafos)
* **Texto:** Esqueça a ordem limpa e estrita das outras ferramentas. Grafos são modelagens visualmente caóticas de conexões baseadas apenas em pontos (chamados "nós" ou "vértices") e as linhas que os conectam (chamadas de "arestas"). Se há conectividade, você está lidando com um grafo.
* **Exemplo:** O Facebook (você é um nó, e todas as suas amizades ou páginas curtidas são arestas de conexões) e o Google Maps calculando rotas baseadas na conexão entre diversas cidades.

## 12. Tries (Árvores de Prefixos)
* **Texto:** Uma árvore inteligente construída com a intenção de agilizar buscas parciais de caracteres. Cada nível de ramificação representa a letra de uma palavra. Conforme as letras são consultadas, a estrutura afunila todos os caminhos até revelar exatamente apenas as palavras que possuem aquele prefixo.
* **Exemplo:** A função de autocompletar da busca do Google (você começa a digitar "App", ele já entra no ramo que possui "Apple" e "App Store") ou o corretor ortográfico do teclado.

## 13. Disjoint Sets / Union Find (Conjuntos Disjuntos)
* **Texto:** Uma estrutura feita especificamente para monitorar agrupamentos e rastrear quem está na mesma rede, mesmo de forma indireta. Eles funcionam identificando os líderes de cada grupo; checar se dois pontos compartilham do mesmo líder revela imediatamente suas conexões.
* **Exemplo:** Checar em uma festa de cem convidados se "Peter" tem alguma conexão com o "Bob", verificando as correlações com os amigos do meio.

## 14. Bloom Filters (Filtros de Bloom)
* **Texto:** Trata-se de uma estrutura minúscula, extremamente rápida e de baixíssimo custo de memória, mas que às vezes "mente". Ela funciona como um porteiro veloz que diz um firme "Não" (100% garantido de que um item não está na base) ou um "Sim" (o item "provavelmente" está lá, gerando um possível falso positivo). Ela nunca gerará um falso negativo.
* **Exemplo:** Quando você cria uma conta em um sistema e ele verifica em um banco de dados de bilhões de registros, usando só alguns megabytes, se a sua tentativa de nova senha já foi vazada em brechas de dados.

## 15. LRU Cache (Least Recently Used)
* **Texto:** É a estrutura mestre das decisões sobre "o que o computador deve esquecer" num limite de memória. Combina as lógicas da Lista Encadeada e do Hashmap. Ele afunila os acessos, mantendo na memória sempre as coisas que você tem usado ativamente e deletando silenciosamente os últimos elementos que não foram abertos recentemente para salvar espaço.
* **Exemplo:** A memória Cache da própria CPU ou de um navegador de internet que esquece atividades isoladas antigas.

---
*Referência do vídeo:* [Every Data Structure Simply Explained in 25 Minutes!](http://www.youtube.com/watch?v=vVL6NFzr0Rg)
