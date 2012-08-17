!SLIDE transition=scrollUp center

# Funções

!SLIDE

# Nome, parâmetros e corpo

    function fact(n)
      if n == 0 then
        return 1
      else
        return n * fact(n - 1)
      end
    end
    -- name: fact
    -- body: the list of statements
    -- parameters: n (locals on body)

!SLIDE

# Chamadas

    function f(a, b) return a or b end

    f(3)        -- a=3, b=nil
    f(3, 4)     -- a=3, b=4
    f(3, 4, 5)  -- a=3, b=4   (5 is discarded)

!SLIDE

# Argumentos múltiplos

    function sum(...)
      local s = 0
      for i,v in ipairs(arg) do
        s = s + v
      end
      return s
    end
