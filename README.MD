# TableFinder

### Класс полностью написанный с помощью ChatGPT 3.5.

[Статья на Хабре.](https://habr.com/ru/articles/738038/)

_Слово автору:_

Этот класс содержит метод для поиска диапазона таблицы на листе Excel.

`FindTableRange(rng As Range) As Range` - Находит диапазон таблицы в заданном диапазоне Range.

Конечный пользователь может использовать этот класс следующим образом:

1. Создайте новый модуль в Excel VBA и скопируйте код класса в него.
1. В вашей книге Excel создайте таблицу.
1. В модуле VBA создайте новую переменную типа Range и назовите ее "tableRange".
1. Напишите следующий код:

```VB
Set tableRange = TableFinder.FindTableRange(Range("A1:F10"))
```

Здесь `"A1:F10"` - это диапазон, в котором вы ищете таблицу. Это может быть любой диапазон на листе Excel, который вы хотите проверить на наличие таблицы.

Вы можете использовать переменную `tableRange` для выполнения различных операций с таблицей, например, для копирования ее содержимого в другой лист Excel или для выполнения вычислений на ее основе.
Пример использования класса:

```VB
Sub TestFindTableRange()
    Dim tableRange As Range
    Set tableRange = TableFinder.FindTableRange(Range("A1:F10"))
    If Not tableRange Is Nothing Then
        MsgBox "Таблица найдена в диапазоне " & tableRange.Address
    Else
        MsgBox "Таблица не найдена"
    End If
End Sub
```

Этот пример ищет таблицу в диапазоне "A1:F10" и выводит сообщение, если таблица найдена или не найдена.
