# Cadastro de novo usuário

### Necessidades

* Precisamos cadastrar um usuário com email e senha além de algumas informações pessoais.


### Atributos

Nome, cpf, email, senha, data criação, data de atualização.

### Restrições

*   Nome não pode ser nulo e só pode letras
*   Cpf não pode ser nulo e deve estar no formato correto
*   O instante não pode ser nulo e não pode ser no futuro
*   O email precisa ter o formato do email e não pode se nulo
*   A senha não pode ser branca ou nula
*   A senha precisa ter no mínimo 6 caracteres
*   A senha deve ser guardada usando algum algoritmo de hash da sua escolha.

### Desafio extra

* Faça testes unitários para cobrir todo o código criado

### Resultado esperado

*  O usuário precisa estar criado no sistema
*  O cliente que fez a requisição precisa saber que o usuário foi criado. Apenas um retorno com status 200 está suficente.
*  Em caso de falha de validação status 400


### **Informações de suporte geral**

1.  Se a resposta para o ponto 1 foi sim, recomendo de novo esse material aqui sobre [arquitetura x design](https://youtu.be/HIIKgnIo7SA). Também acho que vai ser legal você olhar a [minha implementação logo de cara](https://youtu.be/1sXFbr19byA), apenas para ter uma ideia de design que estou propondo.

2.  [Controllers 100% coesos](https://youtu.be/NNKG2TFctfo) para lembrar você a nossa ideia de ter controllers que utilizam todos os atributos.

3.  Ainda sobre as dicas, será que você recebeu a senha do usuário como String no construtor? Se sim, como que o ponto do código que chama aquele construtor sabe que aquela String precisa ser encodada ou não encodada? Você encodou a senha dentro do construtor? E se o outro ponto de código tiver encodado a senha também, vai rolar uma dupla encodada? Como você pode fazer para deixar uma dica ou aumentar a restrição em tempo de compilação?
