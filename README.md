# Style Generator

Criado com o intuito de prover uma forma diferente de estilizar componentes em React. O principal objetivo do pacote é permitir que o desenvovedor possa programar sua interface web sem que para isso seja necesário sair do bom e velho Javascript.

# Instalação

```
npm install style-generator
```

# Documentação

O pacote utiliza a função create para fazer o gereneciamento dos estilos que serão aplicados a um determinado componente. Para que isso ocorra deve-se primeiramente passar na chamada do componente por meio de props(utilizando Camel Case) os estilos CSS desejados. Logo após, no aquivo do componente é chamada a função create do objeto StyleGenerator, que receberá como parâmetro as props do componente e retornará assim um objeto que deverá ser inserido na propriedade style da tag alvo.

# Exemplos
