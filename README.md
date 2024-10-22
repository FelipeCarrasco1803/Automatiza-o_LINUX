# **Script de Automação para Criação de Usuários, Grupos e Diretórios no Linux**

Este script automatiza o processo de configuração inicial de usuários, grupos e diretórios em uma máquina Linux. Ele cria os grupos de usuários, adiciona usuários a esses grupos, cria diretórios e configura permissões, preparando a máquina para uso com todos os recursos já configurados.

## **Objetivo**

O objetivo deste projeto é criar um script simples em Bash que facilite a criação e configuração de usuários e seus respectivos diretórios, sem a necessidade de realizar essas configurações manualmente toda vez que uma nova máquina virtual for iniciada. O script pode ser reutilizado em diferentes ambientes, garantindo uma configuração consistente.

## **Funcionalidades**

- Criação de grupos (admin, dev, user).
- Criação de usuários e adição aos grupos correspondentes.
- Definição de senhas para os usuários.
- Criação de diretórios padrão para os usuários.
- Configuração de permissões para os diretórios conforme o grupo de cada usuário.

## **Tecnologias Utilizadas**

- **Linux** (Ubuntu/Debian ou similar)
- **Bash Scripting**

## **Como Usar**

### 1. **Criação do Arquivo de Script**

Abra o terminal e crie um novo arquivo para o script:

```bash
nano setup_users.sh
```

Cole o conteúdo do script (disponível abaixo) e salve o arquivo pressionando **Ctrl + O** e saindo com **Ctrl + X**.

### 2. **Dar Permissão de Execução**

Após criar o arquivo, é necessário dar permissão de execução ao script. Execute o seguinte comando:

```bash
chmod +x setup_users.sh
```

### 3. **Executar o Script**

Agora você pode rodar o script para realizar todas as configurações necessárias. Execute o seguinte comando no terminal:

```bash
./setup_users.sh
```

### 4. **Personalização (Opcional)**

- Para personalizar os usuários, grupos ou permissões, basta editar o arquivo **`setup_users.sh`** antes de executá-lo.
- O script foi projetado para ser de fácil personalização, permitindo que você adicione ou remova usuários, grupos e diretórios conforme sua necessidade.

## **Estrutura do Script**

Aqui está um resumo do que o script faz:

1. **Criação de Grupos**:
   - Cria os grupos **admin**, **dev** e **user**.

2. **Criação de Usuários**:
   - Adiciona os usuários **admin_user**, **dev_user** e **regular_user** aos grupos correspondentes.
   - Define a senha padrão para todos os usuários como **senha123**.

3. **Criação de Diretórios**:
   - Cria diretórios **/home/admin_user**, **/home/dev_user** e **/home/regular_user**.

4. **Configuração de Permissões**:
   - Define permissões de diretórios:
     - **admin_user**: Permissão total **700**.
     - **dev_user**: Permissão **770** (grupo e dono com permissões totais).
     - **regular_user**: Permissão **755** (leitura e execução para todos).

## **Exemplo de Uso**

### Exemplo:

```bash
$ ./setup_users.sh
Criando grupos...
Criando usuários...
Definindo senhas...
Criando diretórios para os usuários...
Configurando permissões dos diretórios...
Infraestrutura de usuários, grupos e diretórios configurada com sucesso!
```

## **Upload no GitHub**

Caso você queira salvar este script no GitHub para fácil acesso e reutilização:

1. Crie um repositório no [GitHub](https://github.com).
2. Inicialize o repositório localmente:

   ```bash
   git init
   ```

3. Adicione o arquivo e faça o commit:

   ```bash
   git add setup_users.sh
   git commit -m "Adiciona script para criação de usuários e diretórios"
   ```

4. Conecte o repositório remoto e envie o arquivo:

   ```bash
   git remote add origin https://github.com/seu-usuario/seu-repositorio.git
   git push -u origin master
   ```

## **Licença**

Este projeto é licenciado sob a licença MIT - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## **Contribuições**

Contribuições são bem-vindas! Para contribuir, basta fazer um **fork** do repositório, criar uma branch para sua feature e enviar um pull request.

## **Notas Finais**

Este script é uma maneira rápida e prática de configurar uma máquina Linux para uso em ambientes de desenvolvimento ou produção. Ele pode ser modificado para se adaptar a diferentes configurações e ambientes.

---

### Como Salvar este README

1. **Crie o arquivo `README.md`**: No mesmo diretório onde você salvou o script, crie um novo arquivo chamado **`README.md`**.

   ```bash
   nano README.md
   ```

2. **Cole o conteúdo acima**: Após abrir o arquivo no editor, cole o conteúdo do README que forneci.

3. **Salvar o arquivo**: No editor **nano**, salve o arquivo pressionando **Ctrl + O** e depois saia com **Ctrl + X**.

Agora você tem tanto o script quanto o README prontos para serem armazenados e compartilhados no GitHub!
