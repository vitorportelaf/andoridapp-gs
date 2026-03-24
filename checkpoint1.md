Descrição do projeto

Este projeto tem como objetivo demonstrar a navegação entre telas em um aplicativo Android utilizando Jetpack Compose. O foco está na configuração das rotas e na forma como os dados são passados entre diferentes telas.

Ao longo do projeto, são abordados conceitos como parâmetros obrigatórios, parâmetros opcionais e envio de múltiplos dados na navegação. As telas foram estruturadas para receber e utilizar essas informações, permitindo entender como a navegação pode ser dinâmica e adaptável.

O projeto prioriza a parte funcional da navegação, servindo como um exemplo prático para compreender a comunicação entre telas dentro de uma aplicação.

------------------------------------

Objetivo da prova

O objetivo da prova é analisar os 4 últimos commits (tirando o "Criação do README") realizados no projeto e descrever as mudanças aplicadas na navegação entre telas, demonstrando entendimento sobre como os parâmetros são utilizados e como influenciam o funcionamento da aplicação.

------------------------------------

Commit 1 — Passagem de parâmetros obrigatórios na tela de Perfil

Neste commit foi implementada a utilização de parâmetro obrigatório na navegação. Antes, a rota era apenas "perfil" e passou a ser "perfil/{nome}", exigindo que um valor seja informado no momento da navegação.

A navegação foi ajustada para enviar, por exemplo: navController.navigate("perfil/Fulano de Tal")

A principal ideia é que a tela passa a depender de um dado para funcionar corretamente.

------------------------------------

Commit 2 — Passagem de parâmetros opcionais na tela de Pedidos

Neste commit foi implementado um parâmetro opcional na navegação utilizando query parameter. A rota passou a ser: "pedidos?cliente={cliente}"

Foi definido um valor padrão "Cliente Genérico", permitindo navegar de duas formas:
- Enviando valor:
	navController.navigate("pedidos?cliente=Vitor")
- Sem enviar valor:
	navController.navigate("pedidos"), retornando o valor padrão.

A principal ideia é permitir que a tela funcione mesmo sem receber dados.

------------------------------------

Commit 3 — Inserindo valor ao parâmetro opcional na tela de Pedidos

Neste commit foi implementado o envio de um valor dinâmico no parâmetro opcional.

A navegação passou a ser feita, por exemplo: navController.navigate("pedidos?cliente=Vitor")

Com isso, a tela passa a exibir o valor enviado de "Vitor", ao invés de usar apenas o valor padrão.

A principal ideia é utilizar o parâmetro opcional para personalizar a tela.

------------------------------------

Commit 4 — Passagem de múltiplos parâmetros

Neste commit foi implementado o envio de múltiplos parâmetros na navegação.

A rota passou a ser: "perfil/{nome}/{idade}"

A navegação foi ajustada para enviar os valores juntos, por exemplo: navController.navigate("perfil/Fulano de Tal/27")

A principal ideia é permitir o envio de mais de uma informação ao mesmo tempo entre telas.