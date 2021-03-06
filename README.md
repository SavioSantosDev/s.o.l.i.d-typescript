# S.O.L.I.D-Typescript
Repositório para o entendimento dos 5 princípios S.O.L.I.D utilizando Typescript.

- Antes de tudo, uma recomendação, principalmente para os iniciantes, é desenvolver todo o código da forma que sabemos até eles estiver funcionando e pronto para ser utilizado. Depois disso, visto que um código nunca está pronto, podemos ir implementando boas práticas de programação.

Será utilizado um programa de carrinho de compras com funcionalidades para adicionar/remover itens, verificar se o carrinho está vazio, calcular o valor total dos itens do carrinho, checar e finalizar o pedido.

A pasta `src/legacy` contém o arquivo inicial de carrinho de compras com todas as funcionalidades acima.

## S - Single responsability principle || Princípio da responsabilidade única

As classes devem ter apenas uma responsabilidade, por exemplo, se for desenvolvido um programa para eccomerce, as responsabilidades deverão ser abstraídas em várias classes, como carrinho de compras, envio de email, envio de mensagens informativas, verificação dos produtos no carrinho... e assim por diante.

- Em legacy o carrinho tem a responsabilidade de gerenciar os ítens do carrinho, checar e confirmar o pedido. Tudo será abstraído em outras classes, novas funcionalidades foram adicionadas e o arquivo `main.ts` será utilizado para instanciar tudo.

## O - Open/Closed principle || Princípio do aberto/fechado

Todas as entidades (classes, módulos, métodos...) devem ser abertas para expansão e fechadas para a modificação.

Será adicionado a funcionalidade de cupom de descontos de uma forma que não seja necessário modificar nossas entidades para adicionar/remover descontos em nosso programa e que ao mesmo tempo seja possível expandir novas funcionalidades em nossa aplicação.

## L - Liskov substitution priciple || Princípio da substituição de Liskov

Subtipos precisam ser substituíveis por seus tipos de base
- Se meu programa espera um Animal, algo do tipo Cachorro (que herda de Animal) deve servir como qualquer outro animal.
- Se um mamífero não mama ele não deveria ser um mamífero

## I - Interface segragation principle || Princípio da segregação de interface

Os clientes não devem ser forçados a depender de interfaces, types ou classes abstratas que não utilizam. Ou seja, interfaces muito 'gordas', com muitas propriedades, forçam as classes implementa-las o que por vezes pode conter propriedades que não sejam utilizadas, neste caso, fazer uma refatoração na interface é uma boa.

## D - Dependency inversion principle || Princípio da inversão de dependência

Módulos de alto nível não devem depender de módulos de baixo nível, ambos devem depender de abstrações.

- Dependa de abstrações não de implementações
- Abstrações não devem depender de detalhes. Detalhes devem depender de abstrações
- Classes de baixo nível são classes que executam tarefas (detalhes)
- Classes de alto nível gerenciam classes de baixo nível.


## Vantagens e desvantagens de SOLID

**Vantagens**  
- Código modular
- Código reutilizável, D.R.Y (Dont't repeat yourself)
- Código testável
- Baixo acoplamento e alta coesão
- Código expandível
- Separação de conteitos
- Fácil manutenção

**Desvantagens**  
- Aumento de complexidade
- Aumento na quantidade de código digitável
- Tempo de desenvolvimento aumenta bastante

**Cuidados**  
- YAGNI: You aren't gonna neet it (Você não precisa disso)
- KISS: Keep it simple, stupid  (Matenha isto simples, estúpido);
