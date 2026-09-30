## Практическое занятие №1
# 1. Знакомство с языком
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

№1.4

```
a = 10
while a > 0:
    a -= 0.1
```

№1.5
** - возведение числа в степень. Слишком больше число для возможности его обработки


# 2. Сообщения об ошибках

2.1 НЕВЕРНЫЙ СИНТАКСИС

2.2 НЕЛЬЗЯ ПРИСВОИТЬ К ЛИТЕРАЛУ

2.3 ИМЯ НЕ ОПРЕДЕЛЕНО

2.4 НЕЗАВЕРШЕННЫЙ СТРОКОВЫЙ ЛИТЕРАЛ

2.5 НЕПОДДЕРЖИВАЕМЫЙ ТИП ОПЕРАЦИИ ДЛЯ...

2.6 ОЖИДАЛСЯ БЛОК С ОТСТУПОМ

2.7 ОТСТУП НЕ СООТВЕСТВУЕТ  НИКАКОМУ УРОВНЮ ОТСТУПА

2.8 МАТЕМАТИЧЕСКАЯ ДОМЕННАЯ ОШИБКА

2.9 МАТЕМАТИЧЕСАЯ ОШИБКА ДИАПАЗОНОВ

# 3. Арифметика
3.1 Умножение на 12. Используйте 4 сложения.
```
a = 1
s = a + a
d = s + s
f = d + d
g = f + d
print(g)
```
3.2 Умножение на 16. Используйте 4 сложения.
```
a = 1
s = a + a
d = s + s
f = d + d
g = f + f
print (g)
```
3.3 Умножение на 15. Используйте 3 сложения и 2 вычитания.
```
a = 1
b = a + a
c = b + b
d = c + c
e = a - d 
f = d - (e)
print (f)
```
3.4 Решение задачи с неправильным кодом
```
x = 10
y = 15
r = 0
while x > 0:
    if x % 2 != 0:
        r += y
    x = x // 2
    y = y * 2
print (r)
```
3.5


3.6


3.7
```
import random
def mul_bits(x, y, bits):
    x &= (2 ** bits - 1)
    y &= (2 ** bits - 1)
    return x * y
def mul16(x, y):
    mask = 0xFF
    x_hi = (x >> 8) & mask
    x_lo = x & mask
    y_hi = (y >> 8) & mask
    y_lo = y & mask
    p1 = mul_bits(x_hi, y_hi, 8)
    p2 = mul_bits(x_hi, y_lo, 8)
    p3 = mul_bits(x_lo, y_hi, 8)
    p4 = mul_bits(x_lo, y_lo, 8)
    return (p1 << 16) + ((p2 + p3) << 8) + p4
print("Запуск тестирования функции")

test_cases = [
    (0, 0), (0, 65535), (65535, 0), (65535, 65535),
    (255, 255), (256, 256), (1, 65535), (32768, 2)
]
for a, b in test_cases:
    assert mul16(a, b) == a * b, f"Ошибка на граничных значениях: {a} * {b}"
for _ in range(10000):
    a = random.randint(0, 65535)
    b = random.randint(0, 65535)
    assert mul16(a, b) == a * b, f"Ошибка: {a} * {b} != {mul16(a, b)}"
print (a)
print (b)
print("Тест пройден")
```
## Домашняя работа
№4
```
s = "Привет, информатика!"
n = len(s)
print("Символов:", n)
print ("объем:", n * 8, "бит =", (n * 8) / 8, "байт")
```
 

№5
```
import math
p = 0.25
x = math.log2(1 / p)
print ("Частная энтропия при p = ", p, "равна", x, "бит")
```
 

№6 
```
import math
def entropy(probs):
    h = 0.0
    for p in probs:
        if p > 0:
            h -= p * math.log2(p)
    return h
print(f"2 символа: {entropy([0.5, 0.5])} бит")
print(f"4 символа: {entropy([0.25, 0.25, 0.25, 0.25])} бит")
 ```
№7
```
import math
def b_entropy(p):
    if p == 0 or p == 1:
        return 0.0
    return -(p * math.log2(p) + (1 - p) * math.log2(1 - p))
for p in [0.5, 0.9, 1.0]:
    print(f"H({p}) = {round(b_entropy(p), 3)} бит")
```
 
№8
```
dano = [12, -1, 45, 0, 78, -5, 33]
result = [x for x in dano if x > 0]
print("Было:", dano)
print("Стало:", result)
 ```

№9
```
balls = [56, 12, 89, 34, 5]
print("По возрастанию:", sorted(balls))
print("По убыванию:", sorted(balls, reverse=True))
 ```

№10
```
dano1 = ["иванов", "петров", "сидоров"]
dano2 = ["кузнецов", "смирнов"]
combined = dano1 + dano2
formalized = [name.capitalize() for name in combined]

print(formalized)
 ```
№11
```
properties = [
    "объективность",
    "достоверность",
    "полнота",
    "точность",
    "актуальность",
    "полезность",
    "своевременность",
    "понятность",
    "краткость",
]
for i, prop in enumerate(properties, start=1):
    print(i, prop)
 ```

№13
```
def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result
massiv = [5, 1, 8, 3, 7, 2, 9, 4]
seredina = len(massiv) // 2
left = sorted(massiv[:seredina])
right = sorted(massiv[seredina:])
print("Левая:", left)
print("Правая:", right)
print("Слияние:", merge(left, right))
 ```

№14
```
tasks = [f"T{i}" for i in range(1, 11)]
nodes = {
    "Узел-A": [],
    "Узел-B": [],
    "Узел-C": [],
}
node_names = list(nodes.keys())
for i, task in enumerate(tasks):
    node = node_names[i % 3]
    nodes[node].append(task)
for name, task_list in nodes.items():
    print(name, ":", task_list)
```
