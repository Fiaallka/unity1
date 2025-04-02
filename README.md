# unity1
Физика прыгающих шаров с одинаковой массой

В данной симуляции я продемонстрировала влияние упругости материалов и начальных условий на движение шаров с одинаковой массой. 
Я создала платформу Plane, и сверху 30 сфер с одинаковой массой 1 кг.
Чтобы с объектом можно было работать, нужно сделать его "физическим" с помощью Rigidbody. 
Но если так сделать, то шар просто упадет на платформу, чтобы они отпрыгивали, необходимо создать Create -> New Physics Material, назовем его Bouncy ball - он будет определять поведение мяча при столкновениях. 
Теперь нужно задать необходимые настройки:

1. Dynamic Friction (Динамическое трение)
   Значение: 0.6
Определяет трение, когда объект уже движется по поверхности.
Для мяча:
Среднее значение (0.6) даёт небольшое сопротивление качению.

2. Static Friction (Статическое трение)
   Значение: 0.6
Он показывает трение, которое нужно преодолеть, чтобы сдвинуть объект с места.

Пример:
Если мяч лежит на наклонной плоскости, 0.6 не даст ему сразу скатиться.

3. Bounciness (Упругость)
   Значение: 1 (максимум)
Определяет, насколько высоко объект отскочит после удара.

0 = Мяч не отскакивает (как пластилин).
1 = Идеальный отскок (без потерь энергии)
Я поставила значение 0.8, чем больше будет число, тем выше сферы будут отскакивать.

4. Friction Combine (Комбинация трения)
   Значение: Minimum
Он решает, как рассчитывается трение при столкновении двух объектов.

5. Bounce Combine (Комбинация упругости)
   Значение: Maximum
   Аналогично Friction Combine, но для упругости.

Симуляция наглядно показывает, что при одинаковой массе поведение шаров зависит только от упругости материалов.
