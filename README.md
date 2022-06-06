# Fácil Consulta - [👩‍⚕Cadastro]

##### *Recomenda-se para uma maior compreensão, visualizar esse arquivo em algum visualizador de arquivos markdown. Extenções do Visual Studio Code como a Markdown Preview Github Styling (Link no final do arquivo) permitem isso.

## Sistema de Cadastro (front-end)

O projeto refere-se à um Sistema de Cadastro para profisionais da saúde que desejam oferece seus serviços para eventuais consultas.

## Status do Projeto
  
  Em construção 🚧
  

### Pontos importantes (dúvidas/problemas/obsevações)

- Bootstrap Vue, aparentemente não tem suporte oficial para a versão 3.0 do Vue js. 
- Por algum motivo o Vue não está reconhecendo o Vuex, mesmo colocando o modúlo para ser utilizado globalmente (com .use no mount da aplicação). O erro retornado é que  $store não foi declarada.
- O design do projeto ainda não foi todo concluído
- Melhorar a documentação ao final do projeto 
- Vale a pena restruturar com o Nuxt?
- Passar dados por referência, usar injeção de dependência pra criar, emitir um evento, qual caminho seguir pra tornar um componente, que possue um input, reutilizável?     

## Reflexão

Depois de quase 15 dias, não tão produtivos devido a rotina atual e também à problemas técnicos, tive a percepção que ficar 1 ano sem utilizar o Vue me trouxe vários desafios e dificuldades que eu não imaginei ter até determinado ponto do desenvolvimento do projeto. Ficou claro pra mim que devo me aprofundar mais no entendimento do vuex em conjunto de uma componentização mais limpa e versátil. Além disso, alguns pontos que me levaram a algumas soluções bem diferentes, seja na própria estruturação do projeto, seja em microproblemas como "Qual plugin utilizar para a criação de máscaras de input? E pra validação, será que esse é melhor? ele não parece bem documentado, muito confuso", a partir disso eu posso concluir que devo práticar não só mais o Vue, React, Angular, etc, mas também padrões de desenvolvimento, e apesar do projeto está longe de estar completo e eu não ter completado o objetivo, foi muito importante para mim perceber as falhas que devo corrigir para novas oportunidades.


## Como rodar o projeto 

```
npm install
```

##### Para rodar o projeto, utilize o comando a seguir na pasta raíz do projeto, e em seguida abrar no seu navegador o endereço correspondente que irá ser indicado pelo Nuxt.
```
npm run dev
```

### Extenções

[Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles) 

### Autor

@Ezequias Kluyvert de Oliveira Lemos
