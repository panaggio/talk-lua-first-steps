!SLIDE transition=scrollUp center

# Primeiros passos

!SLIDE

# Hello World

    print("Hello World")

!SLIDE

# Rodando programas

    $ lua hello.lua

!SLIDE

# Abrindo o interpretador

    $ lua

!SLIDE

# _Chunk_

- Qualquer pedaço de código executável
- Sequência de _statements_

!SLIDE

# Separação de _statements_

    a = 1
    b = 2

    a = 1; b = 2
    a = 1 b = 2  -- ugh

!SLIDE

# Variáveis globais

- Não precisam ser declaradas
- Só existem se tiverem um valor não `nil`

!SLIDE

# Variáveis globais

    print(x)  --> nil -- x não existe
    x = 1             -- cria global x
    print(x)  --> 1
    x = nil           -- remove global x
    print(x)  --> nil -- x não existe mais

!SLIDE

# Palavras reservadas

    and       break     do        else      elseif
    end       false     for       function  if
    in        local     nil       not       or
    repeat    return    then      true      until
    while

!SLIDE

# Identificadores

- letras maiuscuas ou minúsculas, incluindo `ç`, `ã`, ... (dependendo do _encoding_)
- números (só não pode no início)
- _underscores_
- que não sejam palavras reservadas

!SLIDE

# Comentários

    -- comentário de uma linha

    --[[
    comentário
    multilinha
    ]]

    --[[
    comentário
    multilinha
    maroto
    --]]

!SLIDE

# `arg`

    $ lua examples/arg.lua a b c

    --[[
    arg[-1] = lua
    arg[0] = examples/arg.lua
    arg[1] = a
    arg[2] = b
    arg[3] = c
    --]]
