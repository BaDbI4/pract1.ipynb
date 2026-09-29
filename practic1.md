Практическое занятие №1
1. Знакомство с языком
№1.1 Вывод числа 42 с помощью 10 различных вариантов
```
#q = 42

#w = "42"

#e = 42.000

#r = "101010b"

#t = "сорок_два"

#y = "fourty_two"

#u = "052"

#i = "2A"

#o = "XLII"

#p = "0x2A"
```

#2.1 НЕВЕРНЫЙ СИНТАКСИС
#2.2 НЕЛЬЗЯ ПРИСВОИТЬ К ЛИТЕРАЛУ
#2.3 ИМЯ НЕ ОПРЕДЕЛЕНО
#2.4 НЕЗАВЕРШЕННЫЙ СТРОКОВЫЙ ЛИТЕРАЛ
#2.5 НЕПОДДЕРЖИВАЕМЫЙ ТИП ОПЕРАЦИИ ДЛЯ...
#2.6 ОЖИДАЛСЯ БЛОК С ОТСТУПОМ
#2.7 ОТСТУП НЕ СООТВЕСТВУЕТ  НИКАКОМУ УРОВНЮ ОТСТУПА
#2.8 МАТЕМАТИЧЕСКАЯ ДОМЕННАЯ ОШИБКА
#2.9 МАТЕМАТИЧЕСАЯ ОШИБКА ДИАПАЗОНОВ



# 3.1
#a = 1
#s = a + a
#d = s + s
#f = d + d
#g = f + d


# 3.2
#a = 1
#s = a + a
#d = s + s
#f = d + d
#g = f + f


# 3.3
#a = 1
#b = a + a
#c = b + b
#d = c + c
#e = a - d 
#f = d - (e)

Исходный код

#def naive_mul(x, y):

#   r = 1;

#    for i in range(0, y - 1)

#    x = x + r;

#    end

#ИСПРАВЛЕНЫЙ
#import random

#def kodone_mul(x, y):
#   result = 0
#   for i in range(y):
#       result = result + x;
#   return result
#print (x)
#t = 10
#for o in range(t):
#    g = random.randint(0, 100)
#    h = random.randint(0, 100)
#    my_result = kodone_mul(g, h)
#    correct_result = g * h
#    if my_result == correct_result:
#        print ("uspeh")
#        print (g)
#        print (h)
#    else:
#        print ("neuspeh")

#def rus_cre_mul(x, y):
#    result = 0
#    while x > 0:
#        if x % 2 != 0:
#            result += y
#        x //= 2
#        y *= 2
#    return result
#print (rus_cre_mul)
