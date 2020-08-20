# Idmaq Plugin

Plugin Idmaq para incorporação em sites genéricos.

## Instruções para utilização do plugin
- Importar os arquivos necessários
```html
<link rel="stylesheet" href="css/idmaq-plugin.css">
<script src="js/idmaq-plugin.js"></script>
```

- Inserir no HTML a tag idmaq-plugin. Será através dela que será criado o botão de cadastro no site do IMDAQ.
```html
<idmaq-plugin token="" modalidade=""/>
```

### Parâmetros
- Ao inserir a tag idmaq-plugin, alguns parâmetros podem ser passados, sendo o parâmetro `token` obrigatório.
- `token`: chave de acesso à aplicação de cadastro de maquinário do IDMAQ [**OBRIGATÓRIO**];
- `modalidade`: código para definir se a modalidade do plugin é para cadastro ou para consulta [**OBRIGATÓRIO**];
    - "1": Cadastro
    - "2": Consulta
- `pincode`: IDMAQ Pincode que pode ser adicionado para que, ao abrir o popup, o valor já seja atribuido e consultado [**OPCIONAL**];
- `nome-integrador`: nome do site hospedeiro [**OPCIONAL**];
- `nome-usuario-logado`: nome do usuário logado no site. [**OPCIONAL**];
- `tema`: tema do popup de cadastro de maquinário. [**OPCIONAL**];
    - cinza (default);
    - branco.
- `posicao-tooltip`: posição relativa ao botão, onde será mostrado o tooltip de informações sobre o botão IDMAQ. [**OPCIONAL**];
    - topo (default);
    - esquerda.
    - direita.
    - baixo.


### Métodos
- Após um maquinário ser cadastrado com sucesso, o mesmo irá retornar um pincode, que é a identificação da máquina. O mesmo poderá ser acessado logo após fechar o popup, através do comando `IdmaqPlugin.getIdmaqPinCode()`.
- Também é possível setar o valor do IDMAQ Pincode por meio do método `IdmaqPlugin.setIdmaPinCode()`, passando uma string por parâmetro;
    - Exemplo: `IdmaqPlugin.setIdmaPinCode('AA999A')`
