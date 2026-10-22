# Configuração de usuários, grupos e diretórios Linux

## Objetivo

Criar um script Bash para automatizar a criação de diretórios, grupos e usuários no Linux, definindo permissões de acesso conforme as regras da atividade.

## O que foi feito

- Criados os diretórios `/publico`, `/adm`, `/ven` e `/sec`.
- Criados os grupos `GRP_ADM`, `GRP_VEN` e `GRP_SEC`.
- Criados nove usuários, distribuídos entre os três grupos.
- Definidos os grupos responsáveis pelos diretórios departamentais.
- Configuradas as permissões de acesso com os comandos `chown` e `chmod`.

## Distribuição dos usuários

| Grupo | Usuários |
|---|---|
| GRP_ADM | carlos, maria, joao |
| GRP_VEN | debora, sebastiana, roberto |
| GRP_SEC | josefina, amanda, rogerio |

## Permissões dos diretórios

- `/publico`: permissão `777`, permitindo leitura, escrita e execução para todos.
- `/adm`: permissão `770`, com acesso total ao proprietário e ao grupo `GRP_ADM`.
- `/ven`: permissão `770`, com acesso total ao proprietário e ao grupo `GRP_VEN`.
- `/sec`: permissão `770`, com acesso total ao proprietário e ao grupo `GRP_SEC`.

O usuário `root` é o proprietário dos diretórios.

## Como executar

Execute o script em um terminal Linux com privilégios administrativos:

```bash
sudo bash iacl.sh
```

## Comandos utilizados

- `mkdir`: cria diretórios.
- `groupadd`: cria grupos.
- `useradd`: cria usuários.
- `chown`: define o proprietário e o grupo de um diretório.
- `chmod`: configura as permissões de acesso.
- `openssl passwd`: gera o hash da senha inicial dos usuários.

**Observação:** a senha inicial definida no script é `Senha123`. Execute o script em um ambiente de laboratório e verifique previamente se os usuários, grupos e diretórios já existem.
