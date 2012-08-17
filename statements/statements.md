!SLIDE transition=scrollUp center

# _Statements_

!SLIDE

# _Assignment_

    x = 1
    a, b = 1, 2

    x, y = y, x
    h.x, h.y = h.y, h.x

!SLIDE

# _Assignment_

    a, b, c = 0, 1
    print(a,b,c)           --> 0   1   nil
    a, b = a+1, b+1, b+2   -- value of b+2 is ignored
    print(a,b)             --> 1   2
    a, b, c = 0
    print(a,b,c)           --> 0   nil   nil

!SLIDE

# Variáveis locais e blocos

    j = 10         -- global variable
    local i = 1    -- local variable

!SLIDE

# Variáveis locais e blocos

    x = 10
    local i = 1        -- local to the chunk

    while i <= x do
      local x = i*2    -- local to the while body
      print(x)         --> 2, 4, 6, 8, ...
      i = i + 1
    end

    if i > 20 then
      local x          -- local to the "then" body
      x = 20
    else
      print(x)         --> 10  (the global one)
    end

    print(x)           --> 10  (the global one)

!SLIDE

# Variáveis locais e blocos

    do
      local a2 = 2*a
      local d = sqrt(b^2 - 4*a*c)
      x1 = (-b + d)/a2
      x2 = (-b - d)/a2
    end          -- scope of `a2' and `d' ends here
    print(x1, x2)

!SLIDE center

# Estruturas de controle

!SLIDE

# `if then else`

    if a < 0 then a = 0 end

    if a < b then return a else return b end

    if x > max then
      y = x
      z = x + 1
    end

    if x > 0 then
      x = x - 1
    elseif x < 0 then
      x = x + 1
    else
      return
    end

!SLIDE

# `while`

    x = { 1, 2, 3 }
    local i = 1
    while x[i] do
      print(x[i])
      i = i + 1
    end

!SLIDE

# `repeat`

    -- print the first non-empty line
    repeat
      line = os.read()
    until line ~= ""
    print(line)

!SLIDE

# `for` numérico

    for x = from, to, step do
      something
    end

!SLIDE

# `for` genérico

    for x in iterator do
      something
    end

    -- print all values of array `a`
    for i,v in ipairs(a) do print(v) end

    -- print all keys of table `t`
    for k in pairs(t) do print(k) end

!SLIDE

# `break` e `return`

    -- search for `v` in array `a`
    local i = 1
    while a[i] do
      if a[i] == v then break end
      i = i + 1
    end

    function fact (n)
      if n == 0 then
    return 1 else
        return n * fact(n - 1)
      end
    end
