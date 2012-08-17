!SLIDE transition=scrollUp center

# Tipos e valores

!SLIDE

# Tipagem

- Dinâmica
- Forte
- Coerção automática de tipos

!SLIDE

# Coerção automática

    > = 2 + '2'
    4
    > = '2' + '2'
    4
    > = '2' .. '2'
    22
    > = '2' .. 2
    22
    > = 'a' + 1
    stdin:1: attempt to perform arithmetic on a string value

!SLIDE

# Tipos

- nil
- `boolean`
- `number`
- `string`
- `table`
- `function`
- `userdata`
- `thread`

!SLIDE

# `boolean`

    > = true         --> true
    > = false        --> false
    > = not not nil  --> false
    > = not not 55   --> true
    > = not not ''   --> true
    > = not not 0    --> true

!SLIDE

# `number`

    4     0.4     4.57e-3     0.3e12     5e+20

- Só suporta ponto flutuante
- Dizem que não precisam de mais nada

!SLIDE

# `string`

    a = 'single quoted string are valid'
    b = "double quoted string are valid too"

    c = [[
    multiline strings
    are also valid
    ]]

!SLIDE

# `string`

    a = "\200\129\246"

    > x = 'a string'
    > y = string.gsub(x, 'a', 'another')
    > -- in fact, another string

!SLIDE

# `table`

    x = {}
    print(x)  --> table: 0x10b314d40

!SLIDE

# `table`

    x = {7, 8, 9}
    print(x[1])  --> 7
    print(x[2])  --> 8
    print(x[3])  --> 9

!SLIDE

# `table`

    x = {}
    x[-2] = 4; x[-1] = 5; x[0] = 6; x[1] = 7; x[2] = 8
    print(x[-2], x[-1], x[0], x[1], x[2])
    --> 4       5       6       7       8

!SLIDE

# `table`

    x = { field1 = 'value1', field2 = 'value2' }
    print(x['field1'])  --> value1
    print(x.field2)     --> value2

!SLIDE

# `table`

    > x = {}

    print(x[10])
    --> nil

    > x[nil] = 'oops'
    --> stdin:1: table index is nil

    > print(x[nil])
    --> nil

!SLIDE

# `table`

    x = { 7, 8, 9, field1 = 'value1', field2 = 'value2'}
    print(x[1])         -->  7
    print(x['field1'])  --> value1

!SLIDE

# `table`

    x = { 7, 8, 9 }
    x = { [1] = 7, [2] = 8, [3] = 9 }

!SLIDE

# `table`

    x = { field1 = 'value1', field2 = 'value2' }
    x.field1 = nil
    print(x.field1)  --> nil

!SLIDE

# `function`

    function fact(n)
      if n == 0 then
        return 1
      else
        return n * fact(n - 1)
      end
    end

!SLIDE

# `type`

    print(type(nil))            --> nil
    print(type(true))           --> boolean
    print(type(10.4*3))         --> number
    print(type("Hello world"))  --> string
    print(type({}))             --> table

    print(type(print))          --> function
    print(type(type))           --> function
    print(type(type(X)))        --> string
