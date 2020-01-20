# Style Generator

Criado com o intuito de prover uma forma diferente de estilizar componentes em React. O principal objetivo do pacote é permitir que o desenvovedor possa programar sua interface web sem que para isso seja necesário sair do bom e velho Javascript.

# Instalação

```
npm install style-generator
```

# Documentação

O pacote utiliza a função create para fazer o gerenciamento dos estilos que serão aplicados a um determinado componente. Para que isso ocorra deve-se primeiramente passar na chamada do componente por meio de props(utilizando Camel Case) os estilos CSS desejados. Logo após, no aquivo do componente é chamada a função create do objeto StyleGenerator, que receberá como parâmetro as props do componente e retornará assim um objeto que deverá ser inserido na propriedade style da tag alvo.

# Exemplos

MeuComponentePai.js

```JSX
import React from 'react';
import MeuComponentFilho from './meu-componente-filho.js'

class MeuComponentePai extends React.Component{

  render(){

    return(
      <MeuComponenteFilho border="1px solid #eaeaea"/>
    )
    
  }
  
}

export default MeuComponentePai;
```

MeuComponenteFilho.js

```JSX
import React from 'react';
import StyleGenerator from 'style-generator';

class MeuComponenteFilho extends React.Component{

  render(){

    return(
      <div style={StyleGenerator.create(this.props)}/>
    )
    
  }
  
}

export default MeuComponenteFilho;
```



