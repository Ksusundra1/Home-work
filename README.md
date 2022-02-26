# Home-work
Home work GB 250222
# Задание 1
duration = int(input())
if 0 < duration <= 60:
    print(duration, 'сек')
elif 60 < duration <= 3600:
    print(duration // 60, 'мин', duration % 60, 'сек')
elif 3600 < duration <= 86400:
    print(duration // 3600, 'ч', (duration // 60) % 60, 'мин', duration % 60, 'сек')
elif duration > 86400:
    print(duration // 86400, 'дн', duration // 3600, 'ч', (duration // 60) % 60, 'мин', duration % 60, 'сек')

# Задание 2
def sum_num(value):
    res = 0
    while value != 0:
        res += value % 10
        value //= 10
    return res

sp = [i**3 for i in range(1, 1001, 2)]
sp7 = []
sp17 = []

for i in range(len(sp)):
    if sum_num(sp[i]) % 7 == 0:
        sp7.append(sp[i])
    if (sum_num(sp[i]) + 17) % 7 == 0:
        sp17.append(sp[i] + 17)

print(sp)
print(sp7)
print(sp17)
# Задание 3
for i in range(1, 101):
    if i % 10 == 1 and i != 11:
        print(i, 'процент')
    elif 5 <= i <= 20:
        print(i, 'процентов')
    elif 2 <= i % 10 <= 4:
        print(i, 'процента')
    elif i % 10 == 0:
        print(i, 'процентов')
    else:
        print(i, 'процентов')
