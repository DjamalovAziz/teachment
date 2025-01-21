
# Магические методы и атрибуты объектов в Python

## Создание и уничтожение объекта
- `object.__new__(cls[, ...])` — Создание нового экземпляра класса.
- `object.__init__(self[, ...])` — Инициализация экземпляра класса.
- `object.__del__(self)` — Вызов при уничтожении экземпляра.

## Строковое представление и форматирование
- `object.__repr__(self)` — Официальное строковое представление объекта.
- `object.__str__(self)` — Неформальное строковое представление объекта.
- `object.__bytes__(self)` — Представление объекта в виде байтов.
- `object.__format__(self, format_spec)` — Форматирование объекта.

## Операторы сравнения
- `object.__lt__(self, other)` — Оператор меньше (`<`).
- `object.__le__(self, other)` — Оператор меньше или равно (`<=`).
- `object.__eq__(self, other)` — Оператор равенства (`==`).
- `object.__ne__(self, other)` — Оператор неравенства (`!=`).
- `object.__gt__(self, other)` — Оператор больше (`>`).
- `object.__ge__(self, other)` — Оператор больше или равно (`>=`).

## Хэширование и логическое представление
- `object.__hash__(self)` — Вычисление хэш-значения объекта.
- `object.__bool__(self)` — Логическое представление объекта.

## Работа с атрибутами
- `object.__getattr__(self, name)` — Получение атрибута, если он не найден.
- `object.__getattribute__(self, name)` — Получение атрибута.
- `object.__setattr__(self, name, value)` — Установка атрибута.
- `object.__delattr__(self, name)` — Удаление атрибута.
- `object.__dir__(self)` — Возврат списка атрибутов и методов объекта.
- `object.__get__(self, instance, owner=None)` — Получение значения атрибута.
- `object.__set__(self, instance, value)` — Установка значения атрибута.
- `object.__delete__(self, instance)` — Удаление значения атрибута.
- `object.__set_name__(self, owner, name)` — Установка имени атрибута.

## Классы и наследование
- `object.__objclass__` — Указание класса объекта.
- `object.__slots__` — Ограничение атрибутов экземпляра.
- `object.__mro_entries__(self, bases)` — Коррекция MRO (Method Resolution Order).

## Вызов и длина объекта
- `object.__call__(self[, args...])` — Вызов объекта как функции.
- `object.__len__(self)` — Возврат длины объекта.
- `object.__length_hint__(self)` — Оценка длины объекта.

## Работа с элементами
- `object.__getitem__(self, key)` — Получение элемента по ключу.
- `object.__setitem__(self, key, value)` — Установка элемента по ключу.
- `object.__delitem__(self, key)` — Удаление элемента по ключу.
- `object.__missing__(self, key)` — Обработка отсутствующего ключа.
- `object.__iter__(self)` — Возврат итератора.
- `object.__reversed__(self)` — Возврат обратного итератора.
- `object.__contains__(self, item)` — Проверка наличия элемента.

## Математические операции
- `object.__add__(self, other)` — Оператор сложения (`+`).
- `object.__sub__(self, other)` — Оператор вычитания (`-`).
- `object.__mul__(self, other)` — Оператор умножения (`*`).
- `object.__matmul__(self, other)` — Оператор матричного умножения (`@`).
- `object.__truediv__(self, other)` — Оператор деления (`/`).
- `object.__floordiv__(self, other)` — Оператор целочисленного деления (`//`).
- `object.__mod__(self, other)` — Оператор взятия остатка (`%`).
- `object.__divmod__(self, other)` — Возврат частного и остатка.
- `object.__pow__(self, other[, modulo])` — Оператор возведения в степень (`**`).
- `object.__lshift__(self, other)` — Оператор сдвига влево (`<<`).
- `object.__rshift__(self, other)` — Оператор сдвига вправо (`>>`).
- `object.__and__(self, other)` — Оператор побитового И (`&`).
- `object.__xor__(self, other)` — Оператор побитового исключающего ИЛИ (`^`).
- `object.__or__(self, other)` — Оператор побитового ИЛИ (`|`).

## Обратные математические операции
- `object.__radd__(self, other)` — Обратный оператор сложения (`+`).
- `object.__rsub__(self, other)` — Обратный оператор вычитания (`-`).
- `object.__rmul__(self, other)` — Обратный оператор умножения (`*`).
- `object.__rmatmul__(self, other)` — Обратный оператор матричного умножения (`@`).
- `object.__rtruediv__(self, other)` — Обратный оператор деления (`/`).
- `object.__rfloordiv__(self, other)` — Обратный оператор целочисленного деления (`//`).
- `object.__rmod__(self, other)` — Обратный оператор взятия остатка (`%`).
- `object.__rdivmod__(self, other)` — Обратный оператор `divmod`.
- `object.__rpow__(self, other[, modulo])` — Обратный оператор возведения в степень (`**`).
- `object.__rlshift__(self, other)` — Обратный оператор сдвига влево (`<<`).
- `object.__rrshift__(self, other)` — Обратный оператор сдвига вправо (`>>`).
- `object.__rand__(self, other)` — Обратный оператор побитового И (`&`).
- `object.__rxor__(self, other)` — Обратный оператор побитового исключающего ИЛИ (`^`).
- `object.__ror__(self, other)` — Обратный оператор побитового ИЛИ (`|`).

## Операторы присваивания
- `object.__iadd__(self, other)` — Оператор `+=`.
- `object.__isub__(self, other)` — Оператор `-=`.
- `object.__imul__(self, other)` — Оператор `*=`.
- `object.__imatmul__(self, other)` — Оператор `@=`.
- `object.__itruediv__(self, other)` — Оператор `/=`.
- `object.__ifloordiv__(self, other)` — Оператор `//=`.
- `object.__imod__(self, other)` — Оператор `%=`.
- `object.__ipow__(self, other[, modulo])` — Оператор `**=`.
- `object.__ilshift__(self, other)` — Оператор `<<=`.
- `object.__irshift__(self, other)` — Оператор `>>=`.
- `object.__iand__(self, other)` — Оператор `&=`.
- `object.__ixor__(self, other)` — Оператор `^=`.
- `object.__ior__(self, other)` — Оператор `|=`.

## Унарные операции
- `object.__neg__(self)` — Унарный оператор отрицания (`-`).
- `object.__pos__(self)` — Унарный оператор положительности (`+`).
- `object.__abs__(self)` — Возврат абсолютного значения.
- `object.__invert__(self)` — Оператор побитового отрицания (`~`).

## Преобразование типов
- `object.__complex__(self)` — Преобразование в комплексное число.
- `object.__int__(self)` — Преобразование в целое число.
- `object.__float__(self)` — Преобразование в число с плавающей точкой.
- `object.__index__(self)` — Преобразование в целое число для индексации.
- `object.__round__(self[, ndigits])` — Округление числа.
- `object.__trunc__(self)` — Усечение числа до целого.
- `object.__floor__(self)` — Округление вниз.
- `object.__ceil__(self)` — Округление вверх.

## Контекстные менеджеры
- `object.__enter__(self)` — Вход в контекст.
- `object.__exit__(self, exc_type, exc_value, traceback)` — Выход из контекста.

## Сопоставление с образцом
- `object.__match_args__` — Аргументы для сопоставления с образцом.

## Работа с буферами
- `object.__buffer__(self, flags)` — Создание буфера.
- `object.__release_buffer__(self, buffer)` — Освобождение буфера.