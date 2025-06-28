# Evolua seu terminal com Oh My Zsh + Plugins

Todos nós já conhecíamos o `bash` como nosso antigo terminal e com a chegada do `zsh`, virou nossa primeira opção nos macOS, nos dando mais liberdade de configuração no terminal.

## Oh My Zsh

Oh My Zsh é um excelente framework de código aberto e orientado pela comunidade para gerenciar sua configuração do zsh. Ele vem com milhares de funções úteis, auxiliares, plugins, temas e algumas coisas que fazem você gritar...

Primeiramente executamos o curl de instalação do `oh-my-zsh` :

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

E já podemos ver a carinha dele instalado:

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image.png)

Com a instalação dele, nosso arquivos de variáveis de ambiente `~/.zshrc`  já podemos visualizar muitas informações sobre o nosso framework(`oh-my-zsh`), como theme, plugins e configurações.

Por si só, o `oh-my-zsh` já é muito bom, porém pode ficar muito melhor, com alguns plugins que considero essenciais.

# Plugins

### Auto suggestions

É um plugin que sugere alguns dos comandos mais executados, ou seja, quando você começa a escrever aquele comando super longo que não decorou de cabeça, ele te salva dando a sugestão por já tê-lo executado anteriormente.

Para baixá-lo, é só clonar o repositório git e adicioná-lo ao caminho `/path/to/new-custom-folder/plugins/zsh-autosuggestions`  executando este comando:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### Syntax-highlighting

Este plugin facilita nossa vida validando se um comando é válido antes de executar ou não. Ou seja, baseado nos plugins que estão instalados no `oh-my-zsh` , ele pode validar a sintaxe, deixando comandos válidos em verde e inválidos em vermelho. Isso é realmente muito útil no dia-a-dia.

Para baixá-lo, é só clonar o repositório git e adicioná-lo ao caminho `/path/to/new-custom-folder/plugins/zsh-syntax-highlighting`  executando este comando:

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

Após baixar estes plugins, precisamos adicioná-los ao `oh-my-zsh` , então abrindo o nosso arquivo de configuração `~/.zshrc`  buscamos por `plugins=(git)` e vamos adicionar os dois novos plugins dessa forma:

`plugins=(git zsh-autosuggestions zsh-syntax-highlighting)` 

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%201.png)

Salvamos o arquivo, execute `source ~/.zshrc`  ou feche e reabra seu terminal que os dois plugins já estarão prontos para uso👌🏻

Podemos ver o comando em verde por estar correto e a sugestão do último comando executado.

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%202.png)

O `oh-my-zsh`  já vem com diversos plugins, porém não estão habilitados, você pode visualizar todos neste [link](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) e ler o readme no qual desejar, que terá como ativá-lo nas configurações do terminal e como usá-lo.

## Sugestões de Plugins

- vscode
- sublime
- docker
- python
- zsh-interactive-cd

# Temas

Por padrão o tema defino do `oh-my-zsh` é o `Robby Russell` , podemos ver isso no `~/.zshrc` 

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%203.png)

Porém, há diversos temas que podem ser encontrados aqui neste [link](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) e seguir o passo a passo da configuração.

## Powerlevel 10k

Trago agora a cereja do bolo, o melhor tema que testei para este terminal e que com certeza dá uma cara muito mais moderna e facilita na visualização das coisas.

Ele tem alguns steps para instalar então vou descrevê-los adiante:

Primeiro ele necessita de algumas fontes específicas, por utilizar alguns caracteres especiais que não tem nas padrões do mac, então é necessário realizar o download e instalação

**Download neste link:**

[https://github.com/romkatv/powerlevel10k/issues/2217#issuecomment-1494200707](https://github.com/romkatv/powerlevel10k/issues/2217#issuecomment-1494200707)

**Baixe as 4 fontes**

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%204.png)

Após o download, clique encima de cada fonte para realizar a instalação:

![install-fonts.gif](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/install-fonts.gif)

Feito a instalação das fontes vamos clonar o repositório do `powerlevel10k` :

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"
```

Agora precisamos alterar o tema nas configs do `oh-my-zsh` , entrando no arquivo `~/.zshrc` , buscamos por `ZSH_THEME` e alteramos o valor para `"powerlevel10k/powerlevel10k"`  e salvamos.

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%205.png)

Após isso, fechamos o terminal e iniciará o wizard de configuração do powerlevel10k, mas mesmo com a instalação das fontes podemos ver que o ícone ainda não está exibindo no terminal

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%206.png)

Isso acontece porque a fonte que está configurada no terminal não é a que baixamos, precisamos alterar:

1. No teminal digite `command` + `,`  irá abrir as configurações do terminal
2. Clique em `Perfis`  ao lado de `Geral` 
3. Clique em `Alterar...` 

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%207.png)

1. Selecione as novas fontes instaladas

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%208.png)

1. Feche e reabra o terminal que provavelmente já esteja visualizando o diamante conforme pede no wizard

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%209.png)

1. Só confirmar as informações e estilizar o terminal como mais te agradar

![image.png](Evolua%20seu%20terminal%20com%20Oh%20My%20Zsh%20+%20Plugins%2022056106348f8075baa6dc82533a0969/image%2010.png)
