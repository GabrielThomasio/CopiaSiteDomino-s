Trabalho G1 – Front-End: Clone da tela de login da Domino's

Nome: Gabriel Thomasio Bordignon RA: 1139694 Disciplina: Front-End — Prof. Matheus Henrique Barquette Site de referência: https://www.dominos.com.br/login

Sobre o projeto

Esse projeto reproduz a tela de login do site da Domino's Pizza, incluindo o fluxo de escolha entre "Login com senha" e "Login com código". Como é uma página estática (sem JavaScript), cada uma dessas opções foi feita como uma página HTML separada, simulando a navegação real do site:

index.html — tela inicial, com o header completo do site e o cartão de escolha de login
login-senha.html — tela de login com e-mail e senha (formulário acessível)
login-codigo.html — tela de escolha entre receber o código por e-mail ou celular
style.css — todo o estilo visual das três páginas

A estrutura foi toda construída olhando o resultado visual do site (não usei Ctrl+U nem "Inspecionar > Copiar HTML" em nenhum momento), tentando reproduzir proporções, cores e organização o mais próximo possível do original.

Checklist da Parte 1
1.1 Estrutura HTML semântica e acessível ✅

Usei header pra área de navegação do topo (logo, menu, botão de acompanhar pedidos e ícones de usuário/carrinho), nav para o menu de links dentro dele, e main pra envolver o conteúdo principal de cada página — já que cada uma delas é uma tela própria e independente. footer foi usado no final das páginas pra seção de identificação do projeto.

Optei por div só nos casos sem significado semântico próprio (o agrupamento dos ícones do header, a barra de localização), e por article/section não foram necessários aqui, já que essa tela específica de login não tem repetição de conteúdo (tipo cards de produto) nem múltiplos blocos temáticos — o enunciado deixa claro que as tags são usadas "conforme a estrutura da página".

Todas as imagens têm alt descritivo, explicando o que cada uma representa (logo, ícones de login social, ícone de localização, etc.).

O formulário de e-mail e senha (login-senha.html) usa label associado a cada input através dos atributos for/id, e os campos usam os type corretos (email e password) para melhor usabilidade e validação nativa do navegador.

1.2 Fidelidade visual à referência escolhida ✅

Mantive a mesma paleta de cores do site (azul e vermelho da marca), a mesma organização geral (header fixo no topo, cartão de login centralizado) e a mesma disposição dos elementos (título, subtítulo, botões, divisor "Faça login com", ícones sociais).

Diferença assumida: a Domino's usa uma fonte proprietária própria da marca; como não tenho acesso a ela, usei a fonte padrão do sistema (Arial/Helvetica) como substituta, mantendo pesos (negrito) e tamanhos semelhantes aos do original.

(Espaço reservado para os prints lado a lado do site original x meu resultado — adicionar aqui antes da entrega.)

1.3 CSS: seletores, box model e variáveis ✅

Usei variáveis CSS (:root) para centralizar as cores da marca (--azul-dominos, --vermelho-dominos, etc.), facilitando manter consistência visual em todas as páginas.

Usei pelo menos três tipos diferentes de seletores:

Seletor de classe: .botao, .tela-de-login
Seletor descendente: #header-principal nav a (aplica só nos links que estão dentro do nav do header, sem afetar outros links da página)
Seletor de pseudo-classe: .botao-vermelho:hover, que muda a cor de fundo do botão quando o mouse passa por cima

Também usei ::before/::after para desenhar as linhas do divisor "Faça login com" sem precisar de elementos extras no HTML.

1.4 Responsividade: Flexbox, Grid e mobile first ✅

O CSS foi escrito pensando primeiro em telas pequenas (mobile first): o header e os elementos do cartão de login já funcionam empilhados, sem depender de nenhuma media query. Usei Flexbox para alinhar o header, os botões, os ícones sociais e centralizar o cartão de login.

Adicionei uma media query com min-width: 768px que ajusta o header para não quebrar linha em telas maiores (tablets e desktop).

1.5 Personalização e originalidade ✅

Adicionei um rodapé (.rodape-pessoal) no final das páginas, com meu nome e matrícula, identificando esse projeto como um trabalho acadêmico — esse elemento não existe no site original da Domino's.

Como visualizar o projeto

Basta abrir o arquivo index.html em qualquer navegador. A navegação entre as telas funciona pelos próprios botões da página (não precisa de servidor local).
