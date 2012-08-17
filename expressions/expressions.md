!SLIDE transition=scrollUp center

# Expressões

!SLIDE

# Operadores aritméticos

    sqrtdelta = math.sqrt(b^2 - 4*a*c)
    xp  = (-b + sqrtdelta) / (2*a)
    xpp = (-b - sqrtdelta) / (2*a)

!SLIDE

# Operadores relacionais

    1 > 2      --> false
    'a' < 'b'  --> true
    -- also <= and >=

    1 == 2  --> false
    1 ~= 2  --> true
    -- x ~= y --> not(x == y)

- `nil`, `boolean`, `number`, `string` são comparados por valor

!SLIDE

# Operadores relacionais

    a = { x = 1, y = 0 }
    b = { x = 1, y = 0 }
    c = a

    a == c --> true
    a ~= b --> true

- `table`, `userdata`, e `function` são comparados por referência

!SLIDE

# Operadores lógicos

    print(4 and 5)       --> 5
    print(nil and 13)    --> nil
    print(false and 13)  --> false
    print(4 or 5)        --> 4
    print(false or 5)    --> 5
    print(not nil)       --> true
    print(not not nil)   --> false

!SLIDE

# Concatenação de `string`s

    'a' .. 'b'  --> ab
    1 .. 2      --> 12
    10 .. ''    --> 10
