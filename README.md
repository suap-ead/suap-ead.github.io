# SEAD

# O que é o SEAD
O SEAD **(Ecosistema de apoio à Gestão do suap-Edu)** é um conjunto de microsserviços para apoio os gestores que oferece funções complementares à oferecidas pelo SUAP-Edu.


# Qual a necessidade de criar este projeto se já existe o SUAP

Basicamente, para estender o SUAP com as novas funcionalidades que necessitamos e o SUAP não oferece. Particularmente, atividades correlatas à educação a distância e às tecnologias educacionais.


# Objetivo deste repositório

O propósito deste repositório é servir de documentação ao **SEAD**.


# Como iniciar o desenvolvimento

Antes de iniciar, verifique sua [instalação do Docker e Docker Compose](docker).


## Diretório e variável de ambiente padrão

Todo o restante da documentação irá considerar que você tenha criado uma pasta chamada `SEAD` e uma variável de ambiente chamada `$SEAD_HOME`, a qual contém o PATH para aquela pasta `SEAD` que você criou.

O código a seguir contem todos os comandos necessários para iniciar um ambiente de desenvolvimento.

```bash
. <(curl https://raw.githubusercontent.com/SEAD-cte-zl-ifrn/bin/master/new_install)
source ~/.bashrc
cd $SEAD_HOME/bin
```

Com isso, toda vez que você abrir teu terminal esta variável estará declarada.


# Saiba mais

Este projeto usa Docker Compose, portanto, é bom conhecermos os serviços, variáveis de ambiente e volumes antes mesmo de começarmos a desenvolver ou configurar o projeto.

1.  [Services do projeto](services).
1.  [Variáveis de ambiente](envs).
1.  [Volumes](volumes).
1.  [Ports](ports).
1.  [Começando no projeto](beginning).
1.  [Instalando](install).
