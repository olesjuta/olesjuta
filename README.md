Ввод оценок за семестр
grades = [int(input(f"Введите оценку {i + 1}: ")) for i in range(10)]

Вычисление среднего арифметического
average_grade = sum(grades) / len(grades)

Определение наклейки
if average_grade <= 3:
    sticker = "красная наклейка (плохой результат)"
elif 3 < average_grade <= 6:
    sticker = "оранжевая наклейка (недостаточный уровень знаний)"
elif 6 < average_grade <= 8:
    sticker = "жёлтая наклейка (допустимый уровень знаний)"
else:
    sticker = "зелёная наклейка (идеальный уровень знаний)"

Вывод наклейки
print(f"Ученик получает {sticker}")

Подсчет количества каждого типа наклеек
red_count = grades.count(1) + grades.count(2) + grades.count(3)
orange_count = grades.count(4) + grades.count(5) + grades.count(6)
yellow_count = grades.count(7) + grades.count(8)
green_count = grades.count(9) + grades.count(10)

Определение приза в конце года
if red_count > orange_count and red_count > yellow_count and red_count > green_count:
    prize = "Ученик не получает никаких призов"
elif orange_count > red_count and orange_count > yellow_count and orange_count > green_count:
    prize = "Ученик получает маленький приз"
elif yellow_count > red_count and yellow_count > orange_count and yellow_count > green_count:
    prize = "Ученик получает средний приз"
else:
    prize = "Ученик получает большой приз"

Вывод приза
print(prize)
