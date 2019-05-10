def dec_to_roman(input):
    input=5
    if not isinstance(input, type(1)):
        print  ("inserir numeros inteiros")
    if not 0 < input < 4000:
        print ("O numero deve estar entre 1 e 3999")

    ints = (1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1)
    nums = ('M', 'CM', 'D', 'CD','C', 'XC','L','XL','X','IX','V','IV','I')
    result = []

    for i in range(len(ints)):
        count = int(input / ints[i])
        result.append(nums[i] * count)
        input -= ints[i] * count
    return (''.join(result))

print (dec_to_roman(5))
