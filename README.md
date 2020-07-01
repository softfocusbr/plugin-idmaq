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
<idmaq-plugin token="" />
```

### Parâmetros
- Ao inserir a tag idmaq-plugin, alguns parâmetros podem ser passados, sendo o parâmetro `token` obrigatório.
- `token`: chave de acesso à aplicação de cadastro de maquinário do IDMAQ [**OBRIGATÓRIO**];
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
- Após um maquinário ser cadastrado com sucesso, o mesmo irá retornar um pincode, que é a identificação da máquina. O mesmo poderá ser acessado logo após o fechar o popup, através do comando `IdmaqPlugin.getIdmaqPinCode()`.
