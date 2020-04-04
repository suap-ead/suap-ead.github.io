# Começando no projeto

Todo o restante da documentação irá considerar que você tenha criado uma pasta chamada `SEAD` e uma variável de ambiente chamada `$SEAD_HOME`, a qual contém path para o diretório padrão será em `~/devel/SEAD`. 

O código a seguir contém todos os comandos necessários para:
1. configurar a variável de ambiente `$SEAD_HOME`
2. criar diretório padrão `~/devel/SEAD`
3. baixar os repositórios
4. fazer um undeploy de todas os serviços
5. copiar os arquivos de configuração padrões
6. fazer um novo deploy de todas os serviços

```bash
. <(curl "https://raw.githubusercontent.com/suap-ead/suap-ead.github.io/master/new_install?$RANDOM")
source ~/.bashrc
cd $SEAD_HOME/bin
```

Com isso, toda vez que você abrir teu terminal a variável de ambiente `$SEAD_HOME` estará declarada.

Casos desejes um diretório diferente, baixe o arquivo `https://raw.githubusercontent.com/suap-ead/suap-ead.github.io/master/new_install?$RANDOM`, edite-o e execute-o.
