# SUAP-EaD

# O que é o SUAP-EaD
O SUAP-EaD **(Complementos para EaD ao SUAP-Edu)**, abreviado como **SEAD**, é um conjunto de microsserviços para apoio os gestores que oferece funções complementares à oferecidas pelo SUAP-Edu.


# Qual a necessidade de criar este projeto se já existe o SUAP

Basicamente, para estender o SUAP com as novas funcionalidades que necessitamos e o SUAP não oferece. Particularmente, atividades correlatas à educação a distância e às tecnologias educacionais.


# Objetivo deste repositório

O propósito deste repositório é servir de documentação ao **SEAD**.


# Como iniciar o desenvolvimento

Antes de iniciar, verifique sua [instalação do Docker e Docker Compose](docker.md).


## Diretório e variável de ambiente padrão

Todo o restante da documentação irá considerar que você tenha criado uma pasta chamada `SEAD` e uma variável de ambiente chamada `$SEAD_HOME`, a qual contém o PATH para aquela pasta `SEAD` que você criou. O diretório padrão será em `~/devel/SEAD`.

Todo o restante da documentação irá considerar que você tenha criado uma pasta chamada `SEAD` e uma variável de ambiente chamada `$SEAD_HOME`, a qual contém path para o diretório padrão será em `~/devel/SEAD`.

# Saiba mais

Este projeto usa Docker Compose, portanto, é bom conhecermos os serviços, variáveis de ambiente e volumes antes mesmo de começarmos a desenvolver ou configurar o projeto.

1.  [Services do projeto](services.md).
1.  [Variáveis de ambiente](envs.md).
1.  [Volumes](volumes.md).
1.  [Ports](ports.md).
1.  [Começando no projeto](beginning.md).
1.  [Instalando](install.md).
